#include <iostream>
#include <iomanip>

using namespace std;

char tablero[10][10], columna[11]={' ','0','1','2','3','4','5','6','7','8','9'};
int input, coordenada_column, coordenada_fila;

void Instrucciones(){
    cout << "INSTRUCCIONES:";
    cout << "\n\nElija 'S' u 'O' como indica a continuación para formar la palabra 'OSO'. Por cada 'OSO' que forme en su turno, ganará 1 punto.";
    }

void Solicitar_letra(){
    cout << "\n\nInserte 0 o 1.\n0: O\n1: S\n\n";
    cin >> input;
    while ((input!=1)&&(input!=0)){
        cout << "\nIngrese un número válido (0 o 1):\n\n";
        cin >> input;}
    }

void Nuevo_tablero(){
    for (int espacio=0; espacio<100; espacio++){
            tablero[0][espacio]='-';
    }
    }

void Imprimir_tablero(){
    int num=0;
    for (int letra=0; letra<11; letra++){
            cout << setw(3) << columna[letra];
    }
    cout << "\n"; 
    for (int fila=0; fila<10; fila++){
        cout << setw(3) << num++;
        for (int column=0; column<10; column++){
            cout << setw(3) << tablero[fila][column];
        }
        cout << "\n";
    }
}

void Solicitar_coordenadas(){
    cout << "\n\nIngrese las coordenadas en las que desea ingresar la letra seleccionada.\n\nColumna: ";
    cin >> coordenada_column;
    while ((coordenada_column!=0)&&(coordenada_column!=1)&&(coordenada_column!=2)&&(coordenada_column!=3)&&(coordenada_column!=4)&&(coordenada_column!=5)&&(coordenada_column!=6)&&(coordenada_column!=7)&&(coordenada_column!=8)&&(coordenada_column!=9)){
        cout << "\nIngrese un número válido (0-9): ";
        cin >> coordenada_column;}
    cout << "\nFila: ";
    cin >> coordenada_fila;
    while ((coordenada_fila!=0)&&(coordenada_fila!=1)&&(coordenada_fila!=2)&&(coordenada_fila!=3)&&(coordenada_fila!=4)&&(coordenada_fila!=5)&&(coordenada_fila!=6)&&(coordenada_fila!=7)&&(coordenada_fila!=8)&&(coordenada_fila!=9)){
        cout << "\nIngrese un número válido (0-9): ";
        cin >> coordenada_column;}
}

int main() {
    Instrucciones();
    Solicitar_letra();
    Nuevo_tablero();
    Imprimir_tablero();
    Solicitar_coordenadas();
    return 0;
}
