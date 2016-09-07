//proyecto_1
//Desarrollar un programa en C que permita leer de un archivo de texto una agenda telefónica, cada elemento de la agenda tiene un //nombre  y un número telefónico de 10 dígitos, ambos está separados por una "," , además de leer el archivo, el programa debe //permitir crear, borrar, mostrar y guardar datos en el mismo archivo. Tema 1, Programación Avanzada 
#include <stdio.h>
#include <stdlib.h>

int main(){

    int Opc;
    FILE *f;// este es el archivo
    char cadena;
    
    printf("Qu%c es lo que deseas hacer?\n",130);
 	printf("----------Men%c----------\n",163);
	printf("1. Leer y mostrar agenda telefonica\n");
	printf("2. Crear un nuevo registro\n");
	printf("3. Mostra un registro\n");
	scanf("%d", &Opc);
	switch(Opc)
	{
		case 1:
			f=fopen("agenda.txt","r");
			printf("La agenda telefonica es\n\n");
			while (feof(f) == 0)
		{
			cadena =fgetc(f);
			printf("%c", cadena);
		}
			break;
		case 2:
			
			break;
		case 3:
			
			break;
	
		defalut:
			printf("Opcion no valida\n");
			break;
	}
	fclose(f);
	getchar();
}
