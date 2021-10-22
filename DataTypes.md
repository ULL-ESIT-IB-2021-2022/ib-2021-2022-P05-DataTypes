# Práctica 05. Estilo. Referencias. Expresiones. La utilidad Make

# Factor de ponderación: 5

### Objetivos
Los objetivos de esta práctica son que el alumnado:

* Sea capaz de desarrollar programas simples en C++
* Conozca los tipos básicos de datos en C++, así como los fundamentos de su representación en memoria
* Profundice en el estudio de los diferentes tipos de expresiones: aritméticas, booleanas, etc.
* Ponga en práctica las recomendaciones de la Guía de estilo de Google para C++.
* Sea capaz de automatizar el proceso de compilación utilizando la herramienta `make`


### Rúbrica de evaluacion de esta práctica
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica.
El alumnado ha de acreditar que:
* Ha realizado todos los ejercicios propuestos, así como ser capaz de
  desarrollar otros programas simples similares a los que se proponen en este documento.
* Todos los programas que ha escrito son conformes a la Guía de Estilo propuesta.
* Es capaz de escribir un fichero Makefile para automatizar el proceso de compilación de
  sus programas

### La Guía de Estilo de Google para C++
[Esta guía](https://google.github.io/styleguide/cppguide.html) es un documento de referencia para todos los
programas que se desarrollen en la asignatura, de modo que debe Ud. profundizar en su estudio.

Estudie la sección de nominación 
[Naming](https://google.github.io/styleguide/cppguide.html#Naming)
y dentro de ella estudie las reglas de nombrado de ficheros, tipos, variables y constantes.
En el futuro deberá estudiar las reglas de nombrado de otras entidades que aún no se han estudiado en la asignatura.

En la sección de formato del código
[Formatting](https://google.github.io/styleguide/cppguide.html#Formatting).
estudie los apartados
[Spaces vs Tabs](https://google.github.io/styleguide/cppguide.html#Spaces_vs._Tabs),
[Conditionals](https://google.github.io/styleguide/cppguide.html#Conditionals),
[Loops and Switch Statements](https://google.github.io/styleguide/cppguide.html#Loops_and_Switch_Statements),
[Boolean Expressions](https://google.github.io/styleguide/cppguide.html#Boolean_Expressions),
[Horizontal Whitespace](https://google.github.io/styleguide/cppguide.html#Horizontal_Whitespace) y
[Vertical Whitespace](https://google.github.io/styleguide/cppguide.html#Vertical_Whitespace).

En la sección dedicada a los 
[Comentarios](https://google.github.io/styleguide/cppguide.html#Comments)
estudie los apartados
[Comment Style](https://google.github.io/styleguide/cppguide.html#Comment_Style),
[File Comments](https://google.github.io/styleguide/cppguide.html#File_Comments),
[Variable Comments](https://google.github.io/styleguide/cppguide.html#Variable_Comments) y
[Implementation Comments](https://google.github.io/styleguide/cppguide.html#Implementation_Comments).

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

5. Escriba un programa `short_cirtuit.cc` que evidencie que los operadores lógicos and y or (`&&` y `||`) de C++ utilizan
[evaluación de circuito corto](https://stackoverflow.com/questions/5211961/how-does-c-handle-short-circuit-evaluation).
En una disyunción lógica (or) el segundo operando no se evaluará si el primero es cierto (true), puesto que el resultado 
de esa evaluación no cambiaría el resultado de la disyunción, que será cierta. (Análogamente con una conjunción, and).

6. [C++ Tutor](http://pythontutor.com/cpp.html#mode=edit) es una herramienta que a través de una interfaz web
permite "visualizar" la ejecución de programas escritos en C++ (también tiene soporte para otros lenguajes).
Experimente con la herramienta y ejecute con ella los programas que haya estudiado en clase, así como todos
los programas correspondientes a los ejercicios anteriores.
Al usar la herramienta, preste especial atención a la ejecución del programa `references.cc`

7. [make](https://en.wikipedia.org/wiki/Make_(software)) es una herramienta que permite automatizar el proceso
de desarrollo de software.
La función de make es determinar automáticamente qué ficheros o módulos de un programa necesitan ser recompilados, 
y ejecutar los comandos necesarios para realizar esa tarea.
Este primer 
[Makefile Tutorial](https://makefiletutorial.com/)
le puede servir como primera toma de contacto con la utilidad make.
Estudie a continuación las transparencias  
[Automation of the Build process: the `make` utility](https://docs.google.com/presentation/d/1W7tgsr5FtCqr5zBIY8UVF3RA4ongBOMgH6kddmf0cGQ/edit?usp=sharing) 
los fundamentos de la utilidad.
Por último, el tutorial 
[A Simple Makefile Tutorial](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/)
incluye ejemplos simples desarrollados de forma incremental que pueden ayudarle a entender el uso de `make`.
En ese tutorial se utiliza el compilador `gcc`, pero puede Ud. sustituirlo por `g++` puesto que el compilador
de C++ compila igualmente el código en C (C++ es un superconjunto de C).

Finalmente escriba un único fichero Makefile que permita compilar y generar los programas ejecutables
correspondientes a los 4 ejercicios que se proponen en este documento.

### Referencias
* [Guía de Estilo de Google para C++](https://google.github.io/styleguide/cppguide.html)
* [Stackoverflow](https://stackoverflow.com/)
* [C++ Tutor](http://pythontutor.com/cpp.html#mode=edit)
* [A Simple Makefile Tutorial](https://cs.colby.edu/maxwell/courses/tutorials/maketutor/)

