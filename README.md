# Taller-2
##PUNTO 1
Este código separa los dígitos de un número entero ingresado por el usuario y los muestra de manera individual.

Primero, se pide al usuario que ingrese un número entero usando la función “input()”. Luego, se crea una lista vacía llamada “digitos” que almacenará los dígitos separados del número.

A continuación, se usa un bucle “while” para dividir el número por 10 y almacenar el resto en una variable llamada “digito”. Luego, se agrega el dígito a la lista “digitos” y se actualiza el valor de “numero” dividiéndolo por 10. Este proceso se repite hasta que “numero” sea menor o igual a cero.

Después de obtener todos los dígitos, se utiliza la función “reverse()” para invertir el orden de los dígitos en la lista. Finalmente, se muestra cada dígito de la lista, uno por uno, usando un bucle “for” y la función “print()”.
##PUNTO 2
Este código le pide al usuario que ingrese un número y lo almacena en la variable numero. Luego, se define una función llamada partes que toma un argumento a. Dentro de la función, el número ingresado por el usuario se convierte en un entero y se almacena en la variable a, mientras que la parte decimal del número se almacena en la variable b. Finalmente, la función imprime un mensaje que muestra la parte entera del número y la parte decimal.

Por último, se llama a la función partes con el argumento numero, que es el número que el usuario ingresó anteriormente. De esta manera, la función se ejecuta y muestra la parte entera y la parte decimal del número ingresado por el usuario.
##PUNTO 3
Este código pide al usuario que ingrese dos números enteros. Luego, define una función llamada "espejo" que toma dos argumentos "n" y "m", que son los números ingresados por el usuario.

Dentro de la función, se asigna el valor de "numero1" a la variable "k". Se inicializa una cadena vacía llamada "espejo". Luego, se realiza un bucle "while" que se ejecuta mientras "k" sea mayor que cero. En cada iteración del bucle, se obtiene el último dígito de "k" usando el operador módulo (%), y se agrega a la cadena "espejo". Luego, se divide "k" por 10 usando el operador de división entera (//) para eliminar el último dígito de "k".

Después del bucle, se compara la cadena "espejo" con el número ingresado por el usuario "numero2", convirtiendo "numero2" en una cadena usando la función "str()". Si "espejo" es igual a "numero2", se imprime un mensaje que indica que los dos números son "números espejo" entre sí. De lo contrario, se imprime un mensaje que indica que los dos números no son "números espejo" entre sí.

Finalmente, se llama a la función "espejo" pasando los argumentos "numero1" y "numero2" que se recopilaron al principio del programa.
##PUNTO 4
Este código es un ejemplo de cómo se puede aproximar el valor del coseno de un número utilizando la serie de Maclaurin. En la primera línea se importa la función matemática de Python, que se utiliza para calcular el factorial de un número.

Luego, se le pide al usuario que ingrese el valor del coseno que desea aproximar y el error porcentual que necesita de aproximación.

El siguiente paso es definir la operación que se va a hacer globalmente, que es el cálculo de la serie de Maclaurin para el coseno. Se utiliza un ciclo while que se ejecuta hasta que se cumple la condición de que el valor de la serie es mayor que el valor real del coseno menos el error porcentual.

Dentro del ciclo, se calcula el término de la serie actual utilizando la fórmula de Maclaurin. Luego se suma al valor de la serie global y se incrementa el valor de n, que es el número de términos que se han sumado.

Finalmente se calcula el error porcentual de la aproximación y se imprime el valor de la serie, el error y el número de términos sumados.
##PUNTO 5
Este código es un programa que calcula el MCM (mínimo común múltiplo) y el MCD (máximo común divisor) de una lista de números. Primero, el programa solicita al usuario que ingrese una lista de números separados por espacio, y los convierte a una lista de enteros. Luego, el programa utiliza un algoritmo que descompone cada número en sus factores primos y almacena estos factores en listas separadas. Después, el programa utiliza un conjunto de diccionarios para determinar los factores comunes de cada número de la lista. Finalmente, el programa calcula el MCM y el MCD utilizando los factores comunes. Si el usuario ingresa "mcm", el programa devuelve el MCM de los números, y si el usuario ingresa "mcd", el programa devuelve el MCD de los números. El código utiliza principalmente ciclos for y condicionales if para realizar los cálculos necesarios.

##PUNTO 6
solicita al usuario que ingrese una lista de elementos separados por espacios. Luego, convierte cada elemento en un string y los almacena en la lista elementos_x.

Después, el código busca elementos repetidos en la lista elementos_x, utilizando la función count() para contar cuántas veces aparece un elemento en la lista. Si un elemento aparece más de una vez, se agrega a la lista repetidos y se elimina de la lista elementos_x utilizando la función remove().

Finalmente, si no hay elementos repetidos en la lista elementos_x, se imprime "En esta lista no existen elementos repetidos". En caso contrario, los elementos repetidos se almacenan en la lista repetidos pero no se imprimen en este código.
##PUNTO 7
Este programa tomará una cadena de caracteres del usuario, la dividirá en palabras y almacenará cada palabra en una lista llamada palabra. Luego, definirá una función llamada contadorvocales que toma la lista de palabras como argumento.

La función contadorvocales busca las vocales en cada palabra de la lista y cuenta todas las apariciones de vocales. Si el recuento de vocales en una palabra es mayor o igual a 2, la función imprimirá esa palabra.

En resumen, el programa imprimirá todas las palabras de la lista que contengan al menos dos vocales.

##PUNTO 8
Este código permite al usuario ingresar dos listas de números separados por espacio en la línea de comandos. Luego, se comprueba cuál de las dos listas es más larga. Si la segunda lista es más larga, se intercambian las listas.

Después, se crea una lista vacía llamada 'descuadre'. A continuación, se realiza un bucle 'for' para iterar a través de todos los elementos de la lista más larga (ahora 'lista_a'). Si un elemento de 'lista_a' no está presente en 'lista_b', se agrega a la lista 'descuadre'.

Finalmente, el código imprime las listas 'lista_a', 'lista_b' y 'descuadre'. 'lista_a' y 'lista_b' son las listas originales ingresadas por el usuario, mientras que 'descuadre' es una lista de elementos que están presentes en 'lista_a' pero no en 'lista_b'.


##PUNTO 10
Este programa en Python se encarga de verificar si una matriz es mágica, es decir, si la suma de los elementos de cada fila, cada columna y cada diagonal principal es igual.

Primero, se crea una matriz vacía, y se pide al usuario que ingrese los elementos de la primera fila separados por espacios, los cuales se convierten en enteros y se agregan a la matriz. Luego, se pide al usuario que ingrese los elementos de las filas restantes, y se agregan a la matriz hasta que se hayan ingresado todas las filas.

Después, se definen varias funciones para invertir la matriz, sumar los elementos de cada fila y diagonal principal, y obtener la matriz traspuesta. Estas funciones se utilizan para verificar si la matriz es mágica. Si todas las sumas son iguales, la matriz es mágica y se imprime un mensaje indicando esto.

El programa también utiliza la función limpiar para borrar las listas que se usan para almacenar las sumas de las filas y las diagonales principales, de manera que se puedan usar para almacenar las sumas de las filas y diagonales principales de la matriz traspuesta y la matriz invertida.
