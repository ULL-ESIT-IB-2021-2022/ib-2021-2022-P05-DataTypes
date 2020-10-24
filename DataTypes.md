# Práctica 05. Tipos de Datos. Referencias. La utilidad Make

### Objetivos
Los objetivos de esta práctica son que el alumnado:

* Sea capaz de desarrollar programas simples en C++
* Conozca los tipos básicos de datos en C++, así como los fundamentos de su representación en memoria
* Sea capaz de automatizar el proceso de compilación utilizando la herramienta `make`


### Rúbrica de evaluacion de esta práctica
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* El alumnado ha de acreditar que es capaz de realizar programas simples en C++ similares a los que se
  proponen en este documento.
* El alumnado ha de acreditar que ha realizado todos los ejercicios propuestos, así como ser capaz de
  desarrollar otros similares
* Ha de acreditar que es capaz de escribir un fichero Makefile para automatizar el proceso de compilación de
  sus programas

### La Guía de Estilo de Google para C++
[Esta guía](https://google.github.io/styleguide/cppguide.html) será un documento de referencia para todos los
programas que se desarrollen en la asignatura, de modo que debe Ud. comenzar a familiarizarse con ella.
Por ahora basta con que estudie la sección [Naming](https://google.github.io/styleguide/cppguide.html#Naming)
y conozca las reglas para el nombrado de ficheros ([File Names](https://google.github.io/styleguide/cppguide.html#File_Names)), 
variables ([Variable Names](https://google.github.io/styleguide/cppguide.html#Variable_Names)) y constantes
([Constant Names](https://google.github.io/styleguide/cppguide.html#Constant_Names)).

Ponga en práctica esas reglas en todos los programas que desarrolle de ahora en adelante.
De forma paulatina se irá estudiando con mayor profundidad esa guía así como poniendo en práctica en los
programas a desarrollar, las recomendaciones que allí se exponen.

### Ejercicios 
1. Escriba en C++ un programa `data_types.cc` que imprima en pantalla la cantidad de memoria que utiliza su compilador para
almacenar cada uno de los tipos básicos del lenguaje.
Investigue para ello el operador [sizeof](https://en.wikipedia.org/wiki/Sizeof).
El programa deberá imprimir en pantalla líneas como la siguiente:

```
El tipo de datos int se representa utilizando 4 bytes
```
para cada uno de los tipos de datos del lenguaje.
Haga que las líneas se muestren comenzando con los tipos que utilizan menos cantidad de memoria y finalizando
con los que ocupan mayor cantidad.

2. Escriba un programa `references.cc` que declare cuatro variables de diferentes tipos y las inicialice
utilizando los diferentes mecanismos de inicialización de variables que suministra el lenguaje.
El programa declarará asimismo otras tantas referencias a las variables anteriores e imprimirá en pantalla los valores de esas
referencias. 
¿Son iguales los valores de las referencias que los de las variables referenciadas?

3. Escriba un programa `boolean_operators.cc` que imprima en pantalla la
[tabla de verdad](https://en.wikipedia.org/wiki/Truth_table#Truth_table_for_all_binary_logical_operators)
de los operadores lógicos (and, or, not) de C++.
El programa deberá utilizar un par de variables booleanas y mostrar el resultado de operar ambas variables con
todos sus posibles valores y con cada uno de los operadores lógicos.

4. Escriba un programa `arithmetic_operators.cc` que declare e inicialice variables de tipos aritméticos e
imprima en pantalla el resultado de operar esas variables con todos los operadores que pueda utilizar con
ellas.
Utilice operadores aritméticos y de comparación.
El programa imprimirá en pantalla líneas como la siguiente:
```
El resultado de operar 7 % 3 es 1
```
Para cada uno de los operadores considerados.

Estudie en [Stackoverflow](https://stackoverflow.com/) las respuestas a la entrada 
[c++ comparing two floating point values](https://stackoverflow.com/questions/5064377/c-comparing-two-floating-point-values).
Stackoverflow es uno de los mejores foros para la resolución de dudas sobre programación.
Le sugerimos la posibilidad de abrir una cuenta en esa página, para su consulta habitual.
Revise asimismo el artículo 
[Comparing Floating Point Numbers](https://randomascii.wordpress.com/2012/02/25/comparing-floating-point-numbers-2012-edition/), 
particularmente la sección "Epsilon comparisons".

Trate de incorporar en su programa `arithmetic_operators.cc` lo que haya aprendido leyendo las referencias
anteriores.

5. [C++ Tutor](http://pythontutor.com/cpp.html#mode=edit) es una herramienta que a través de una interfaz web
permite "visualizar" la ejecución de programas escritos en C++ (también tiene soporte para otros lenguajes).
Experimente con la herramienta y ejecute con ella los programas que haya estudiado en clase, así como todos
los programas correspondientes a los ejercicios anteriores.
Al usar la herramienta, preste especial atención a la ejecución del programa `references.cc`

6. [make](https://en.wikipedia.org/wiki/Make_(software)) es una herramienta que permite automatizar el proceso
de desarrollo de software.
La función de make es determinar automáticamente qué ficheros o módulos de un programa necesitan ser recompilados, 
y ejecutar los comandos necesarios para realizar esa tarea.
Estudie en las transparencias de clase 
[Make utility](https://docs.google.com/presentation/d/167rBvVIUrPAY8-7ieHnlXJ5hSstGfUIX2myyu5drCVA/edit?usp=sharing) 
los fundamentos de la utilidad.
Estudie asimismo el tutorial [A Simple Makefile Tutorial](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/).
En ese tutorial se utiliza el compilador `gcc`, pero puede Ud. sustituirlo por `g++` puesto que el compilador
de C++ compila igualmente el código en C (C++ es un superconjunto de C).

Finalmente escriba un único fichero Makefile que permita compilar y generar los programas ejecutables
correspondientes a los 4 ejercicios que se proponen en este documento.

### Referencias
[A Simple Makefile Tutorial](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/)




