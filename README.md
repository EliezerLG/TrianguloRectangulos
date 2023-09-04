#
## Aplicación para realizar Triangulos rectangulos
```
* * * * *  
* * * * 
* * * 
* * 
*

        *
      * *
    * * *
  * * * *
* * * * *

* * * * * 
  * * * * 
    * * * 
      * * 
        *

* * * * * 
  * * * * 
    * * * 
      * * 
        *


```
--------
-------
##
## En Pseudocogido:
```
Algoritmo TriangulosRectangulo
    Definir continuar como Caracter
	Definir opcion, altura como Entero
    continuar = 's'
	
    Mientras continuar = 's' Hacer
        
        Escribir "Ingrese la altura del triangulo:"
        Leer altura
        
        Escribir "Elija una opcion para imprimir el triangulo:"
        Escribir "1. hacia arriba a la derecha"
        Escribir "2. hacia arriba a la izquierda"
        Escribir "3. hacia abajo a la derecha"
        Escribir "4. hacia abajo a la izquierda"
        Leer opcion
        
        Segun opcion Hacer
            Caso 1:
                Escribir "Ejecutando la opcion 1. hacia arriba a la derecha"
				Para i <- 1 Hasta altura Hacer
					Para j <- 0 Hasta altura - i Hacer
						Escribir sin saltar "  "; 
					FinPara
					Para k <- 1 Hasta  i Hacer
						Escribir sin saltar " *"; 
					FinPara
					Escribir" "; 
				FinPara
            Caso 2:
                Escribir "Ejecutando la opcion 2. hacia arriba a la izquierda"
                Para i <- 1 Hasta altura Hacer
                    Para j <- 1 Hasta i Hacer
                        Escribir sin saltar "* ";
                    FinPara
                    Escribir " ";
                FinPara
				
            Caso 3:
                Escribir "Ejecutando la opcion 3. hacia abajo a la derecha"
                Para i <- 1 Hasta altura Hacer
                    Para j <- 0 Hasta i - 1 Hacer
                        Escribir sin saltar"  ";
                    FinPara
                    Para k <- i Hasta altura Hacer
                        Escribir sin saltar "* ";
                    FinPara
                    Escribir " ";
                FinPara
				
            Caso 4:
                Escribir "Ejecutando la opcion 4. hacia abajo a la izquierda"
                Para i <- altura Hasta 1 Con Paso -1 Hacer
                    Para j <- 1 Hasta i Hacer
                        Escribir sin saltar"* ";
                    FinPara
                    Escribir " ";
                FinPara
				
            De Otro Modo:
                Escribir "Opcion no valida"
				
        FinSegun
		
		Escribir "Desea ingresar una nueva opcion?"
		Leer continuar
		Limpiar Pantalla
    FinMientras
	
    Escribir "Gracias por utilizar el programa"
FinAlgoritmo

```
##
## En C++:
```
//Imprimir triangulos rectangulo de cuatro maneras
#include <iostream>
using namespace std;
int main () {
     char continuar;
    do {
        int opcion;
        int altura;
        cout << "Ingrese la altura del triangulo: "<<endl;
        cin >> altura;
        cout << "Elija una opcion para imprir el triangulo "<<endl;
        cout << "1. hacia arriba a la derecha "<<endl;
        cout << "2. hacia arriba a la izquierda"<<endl;
        cout << "3. hacia abajo a la derecha "<<endl;
        cout << "4. hacia abajo a la izquierda "<<endl;
        cin >> opcion;
        if (opcion == 1) { 
        cout << "Ejecutando la opcion " "1. hacia arriba a la derecha"<<endl;
            for (int i = 1; i <= altura; i++) {
            for (int j = 1; j <= altura - i; j++) {
                cout << "  ";
            }
            for (int k = 1; k <= i; k++) {
                cout << "* ";
            }
            cout << endl;
        }
        }else if (opcion == 2){
            cout << "Ejecutando la opcion " "2. hacia arriba a la izquierda"<<endl;
            for (int i = 1; i <= altura; i++) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
        }else if (opcion == 3){
            cout << "Ejecutando la opcion " "3. hacia abajo a la derecha"<<endl;
            for (int i = 1; i <= altura; i++) {
            for (int j = 1; j < i; j++) {
                cout << "   ";
            }
            for (int k = i; k <= altura; k++) {
                cout << " * ";
            }
            cout << endl;
        }
        }else if (opcion == 4){
            cout << "Ejecutando la opcion " "4. hacia abajo a la izquierda"<<endl;
            for (int i = altura; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
        }else {
            cout <<"opcion no valida"<<endl;
        }
        cout <<"Desea ingresar una nueva opcion? (S/N)"<<endl;
        cin >> continuar;
        }while (continuar == 'S'|| continuar == 's');

    cout << "Gracias por utilizar el programa"<<endl;
    return 0;
}
```
##
## En Python:
```
while True:
    opcion = input("Elija una opción para imprimir el triángulo:\n"
                   "1. Triángulo hacia arriba a la derecha\n"
                   "2. Triángulo hacia abajo a la izquierda\n"
                   "3. Triángulo hacia abajo a la derecha\n"
                   "4. Triángulo hacia arriba a la izquierda\n"
                   "5. Salir\n")
                   
                   

    if opcion == '1':
        altura = int(input("Ingrese la altura del triángulo: hacia arriba a la derecha\n"))
        for i in range(1, altura + 1):
            espacios = " " * (altura - i)
            asteriscos = "* " * i
            linea = espacios + asteriscos
            print(linea.rjust(altura * 2))
    elif opcion == '2':
        altura = int(input("Ingrese la altura del triángulo: hacia abajo a la izquierda\n"))
        for i in range(0, altura + 1):
            print("* " * (altura - i + 1))
    elif opcion == '3':
        altura = int(input("Ingrese la altura del triángulo: hacia abajo a la derecha\n"))
        for i in range(altura, 0, + i):
            asteriscos = "* " * 1
            linea = asteriscos.rjust(altura * i)
            print(linea)
    elif opcion == '4':
        altura = int(input("Ingrese la altura del triángulo: hacia arriba a la izquierda\n"))
        for i in range(1, altura + 1):
            print("* " * i)
    elif opcion == '5':
        break
    else:
        print("Opción no válida. Por favor, elija una opción válida.")

print("Gracias por utilizar el programa")

```