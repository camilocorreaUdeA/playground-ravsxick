# Entrada y salida estándar de datos para aplicaciones de consola en C++

Generalmente, las aplicaciones de software están diseñadas para que puedan interactuar de forma directa con usuarios. Por ejemplo, las aplicaciones web le permiten a un usuario agregar datos en campos y luego enviar esa información al presionar un botón.
En el caso de las aplicaciones de consola desarrolladas con C++, solo hay dos tipos de interacción directa entre la aplicación y el usuario: 
<ol>
<li>Mediante mensajes que la aplicación imprime en pantalla para que el usuario los lea.</li>
<li>A través de información ingresada por el usuario a la aplicación usando el teclado de la computadora.</li>
</ol>

En esta lección veremos las funciones de uso más extendido que ofrece C++ para la impresión de información en pantalla y para capturar datos ingresados por el teclado.
Al ingreso de datos por teclado y la impresión de información en pantalla se le conoce como entrada y salida estándar respectivamente en el argot del desarrollo de aplicaciones de consola en C++.
Para poder utilizar correctamente las funciones que permiten controlar la entrada y salida estándar en C++ es necesario agregar un par de líneas de código como requisito indispensable.

## Requisitos

Para poder utilizar las funciones que controlan la entrada y salida estándar en C++ es necesario:
<ol>
<li>Incluir la librería para flujos de entrada y salida de datos en C++: <b><i>iostream</i></b></li>
<li>Incluir el espacio de nombres de la librería estándar de C++: <b><i>std</i></b></li>
</ol>

Observe a continuación la sintaxis necesaria para incluir la librería iostream y el espacio de nombres std:

```C++
#include<iostream>   //Inclusion de la libreria iostream

using namespace std;  //Inclusion del espacio de nombres std

```

## Salida estándar en C++

Para poder imprimir datos en la pantalla C++ ofrece la función `cout` junto con el operador `<<`. La función `cout` permite imprimir cadenas de texto y valores almacenados en variables.

Ejemplo:

```C++ runnable
#include <iostream>

using namespace std;

int main() {
	string curso = "Informatica";
    unsigned int version = 2;

    cout << "Bienvenidos al curso de " << curso << " " << version;
}

```

## Entrada estándar en C++

Para poder capturar datos ingresados por teclado y almacenarlos en variables C++ ofrece la función `cin` junto con el operador `>>`, y la función`getline`. La función `cin` permite capturar cualquier tipo de datos, con excepción de cadenas de texto que contengan espacios. Mientras que `getline` si permite la captura de textos con espacios.

Ejemplo (copie el código en su editor de preferencia y ejecutelo):

```C++
#include <iostream>

using namespace std;

int main() {
    string nombreCompleto1 = "";
    string nombreCompleto2 = "";

    cout << "Ingrese su nombre y apellido\n";
    cin >> nombreCompleto1;
    cout << "Ingrese de nuevo su nombre y apellido\n";
    getline(cin, nombreCompleto2);
    

    cout << "Datos ingresados con cin: " << nombreCompleto1 << "\n";
    cout << "Datos ingresados con getline: " << nombreCompleto2 << "\n";
}

```
