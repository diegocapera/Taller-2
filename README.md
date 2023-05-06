# Taller-2
**PUNTO 1**
Desarrollar un programa que ingrese un número entero n y separe todos los digitos que componen el número.
```Python
numero = int(input("Ingresa un número entero: "))
digitos = []

while numero > 0:
    digito = numero % 10
    digitos.append(digito)
    numero = numero // 10

digitos.reverse()

print("Los dígitos separados son: ")
for digito in digitos:
    print(digito)
```

Este código separa los dígitos de un número entero ingresado por el usuario y los muestra de manera individual.

Primero, se pide al usuario que ingrese un número entero usando la función “input()”. Luego, se crea una lista vacía llamada “digitos” que almacenará los dígitos separados del número.

A continuación, se usa un bucle “while” para dividir el número por 10 y almacenar el resto en una variable llamada “digito”. Luego, se agrega el dígito a la lista “digitos” y se actualiza el valor de “numero” dividiéndolo por 10. Este proceso se repite hasta que “numero” sea menor o igual a cero.

Después de obtener todos los dígitos, se utiliza la función “reverse()” para invertir el orden de los dígitos en la lista. Finalmente, se muestra cada dígito de la lista, uno por uno, usando un bucle “for” y la función “print()”.

**PUNTO 2**
Desarrollar un programa que ingrese un número flotante n y separe su parte entera de la parte decimal, y luego entrege los digitos tanto de la parte entera como de la decimal.
```Python
##Entrada un numero flotante
#Salida un numero entero y un valor decimal
numero = float(input("Por favor ingrese un numero:  "))
def partes(a): #Se define la funcion
  a = int(numero) #El numero ingresado por el usuarios
  b = numero - a #La operacion que se hace para separar la parte entera de la decimal
  print(f"La parte entera del numero es {a} y la parte decimal es {b}")
partes(numero) #Se imprime por medio de la variable "partes"
```

Este código le pide al usuario que ingrese un número y lo almacena en la variable numero. Luego, se define una función llamada partes que toma un argumento a. Dentro de la función, el número ingresado por el usuario se convierte en un entero y se almacena en la variable a, mientras que la parte decimal del número se almacena en la variable b. Finalmente, la función imprime un mensaje que muestra la parte entera del número y la parte decimal.

Por último, se llama a la función partes con el argumento numero, que es el número que el usuario ingresó anteriormente. De esta manera, la función se ejecuta y muestra la parte entera y la parte decimal del número ingresado por el usuario.

**PUNTO 3**
Desarrollar un programa que permita ingresar dos números enteros y determinar si se tratan de números espejos.
```Python
#Numeros espejo
numero1 = int(input("Por favor ingrese un numero:   "))
numero2 = int(input("Por favor ingrese un numero:   "))
def espejo(n,m):  
  k = numero1
  espejo = ""
  while(k>0):
    dig = k%10
    sig = k//10
    x = str(dig)
    espejo+=x
    k = sig
  if(espejo == str(numero2)):
    print(f"El numero {numero1} y el numero {numero2} son numeros espejo entre sí")
  else:
    print(f"El numero {numero1} y el numero {numero2} no son numeros espejo entre sí")
espejo(numero1,numero2)
```

Este código pide al usuario que ingrese dos números enteros. Luego, define una función llamada "espejo" que toma dos argumentos "n" y "m", que son los números ingresados por el usuario.

Dentro de la función, se asigna el valor de "numero1" a la variable "k". Se inicializa una cadena vacía llamada "espejo". Luego, se realiza un bucle "while" que se ejecuta mientras "k" sea mayor que cero. En cada iteración del bucle, se obtiene el último dígito de "k" usando el operador módulo (%), y se agrega a la cadena "espejo". Luego, se divide "k" por 10 usando el operador de división entera (//) para eliminar el último dígito de "k".

Después del bucle, se compara la cadena "espejo" con el número ingresado por el usuario "numero2", convirtiendo "numero2" en una cadena usando la función "str()". Si "espejo" es igual a "numero2", se imprime un mensaje que indica que los dos números son "números espejo" entre sí. De lo contrario, se imprime un mensaje que indica que los dos números no son "números espejo" entre sí.

Finalmente, se llama a la función "espejo" pasando los argumentos "numero1" y "numero2" que se recopilaron al principio del programa.

**PUNTO 4**
Diseñar una función que permita calcular una aproximación de la función coseno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Taylor. nota: use math para traer la función coseno y mostrar la diferencia entre el valor real y la aproximación. Con cuántos valores de la serie, se tienen errores del 10%, 1%, 0.1% y 0.001%.
```Python
#Coseno MacLaurin
from math import *
val = float(input("Ingrese el valor de coseno que desea aproximar:  "))
error_x = float(input("Ingrese el error porcentual que necesita de aproximacion:  ")) #Se le pide el valor de coseno y el error porcentual al que desea saber su aproximacion
n=0
serie = 0
a = ((-1)**n)*(val**(2*n))/factorial(2*n) #Se define la operacion que se va a hacer globalmente
n+=1
(1-(error_x/100))*cos(val)
while(serie<((1-(error_x/100))*cos(val))): #Se deja claro la condicion que va a tener el ciclo para se cumplido
  a = ((-1)**n)*(val**(2*n))/factorial(2*n) #La siguiente parte es donde se denota el proceso que se va a realizar para que dicho ciclo funcione
  serie+=a
  n+=1
  error = (1-(serie/cos(val)))*100
print(serie,"",error,"",n) #Se imprime 
```

Este código es un ejemplo de cómo se puede aproximar el valor del coseno de un número utilizando la serie de Maclaurin. En la primera línea se importa la función matemática de Python, que se utiliza para calcular el factorial de un número.

Luego, se le pide al usuario que ingrese el valor del coseno que desea aproximar y el error porcentual que necesita de aproximación.

El siguiente paso es definir la operación que se va a hacer globalmente, que es el cálculo de la serie de Maclaurin para el coseno. Se utiliza un ciclo while que se ejecuta hasta que se cumple la condición de que el valor de la serie es mayor que el valor real del coseno menos el error porcentual.

Dentro del ciclo, se calcula el término de la serie actual utilizando la fórmula de Maclaurin. Luego se suma al valor de la serie global y se incrementa el valor de n, que es el número de términos que se han sumado.

Finalmente se calcula el error porcentual de la aproximación y se imprime el valor de la serie, el error y el número de términos sumados.

**PUNTO 5**
Desarrollar un programa que permita determinar el Minimo Comun Multiplo de dos numeros enteros. Abordar el problema desde la perpectiva iterativa como recursiva.
```Python
print("Este programa le calcula el mcm y el mcd de n numeros")
n = [int(x) for x in input("Por favor, ingrese los numeros separados por espacio:  ").split()]
h = str(n)
m = []
primos = []
listas = []
pot = {}
p=[]
d=[]
cont = 0
while(len(n)>0):
  factores=[]
  for i in range(1,max(n)+1):
    for j in range(1,max(n)+1):
      if i%j==0:
        cont+=1
    if cont==2:
      primos.append(i)
    cont=0
  k=max(n)
  for i in primos:
    while(k%i==0):
      if k%i==0:
        factores.append(i)
        b = k//i
        k=b
  listas.insert(0,factores)
  m.append(max(n))
  n.remove(max(n))
for i in range(len(listas)):
  for j in range(len(listas[i])):
    pot[listas[i][j]]=listas[i].count(listas[i][j])
    p.append(pot)
  pot={}
for k in range(len(p)):
  if p[k] not in d:
    d.append(p[k])
def final(di):
  xd = 1
  for z in di.keys():
    f = z**(di.get(z))
    xd*=f
  return xd
xddd= input("Que necesita consultar:    ")
#mcm
if(xddd.lower()=="mcm"):
  claves = set(d[0].keys())
  for i in d[1:]:
    claves|=set(i.keys())
  for c in claves:
     valores = [x[c] for x in d if c in x]
     pot[c] = max(valores)
  print(f"El minimo comun multiplo de {h} es {final(pot)}")
#mcd
elif(xddd.lower()=="mcd"):
  claves = set(d[0].keys())
  for i in d[1:]:
    claves&=set(i.keys())
  for c in claves:
     valores = [x[c] for x in d if c in x]
     pot[c] = min(valores)
  print(f"El maximo comun divisor de {h} es {final(pot)}")
```

Este código es un programa que calcula el MCM (mínimo común múltiplo) y el MCD (máximo común divisor) de una lista de números. Primero, el programa solicita al usuario que ingrese una lista de números separados por espacio, y los convierte a una lista de enteros. Luego, el programa utiliza un algoritmo que descompone cada número en sus factores primos y almacena estos factores en listas separadas. Después, el programa utiliza un conjunto de diccionarios para determinar los factores comunes de cada número de la lista. Finalmente, el programa calcula el MCM y el MCD utilizando los factores comunes. Si el usuario ingresa "mcm", el programa devuelve el MCM de los números, y si el usuario ingresa "mcd", el programa devuelve el MCD de los números. El código utiliza principalmente ciclos for y condicionales if para realizar los cálculos necesarios.

**PUNTO 6**
Desarrollar un programa que determine si en una lista no existen elementos repetidos.
```Python
#Repetidos
elementos_x=[str(rep) for rep in input("Ingrese cualquier elemento a la lista, separados por espacios:  ").split()]
repetidos=[]
for i in elementos_x:
  if elementos_x.count(i)>1:
    repetidos.append(i)
    elementos_x.remove(i)
if(len(repetidos)==0):
  print("En esta lista no existen elementos repetidos")
````

solicita al usuario que ingrese una lista de elementos separados por espacios. Luego, convierte cada elemento en un string y los almacena en la lista elementos_x.

Después, el código busca elementos repetidos en la lista elementos_x, utilizando la función count() para contar cuántas veces aparece un elemento en la lista. Si un elemento aparece más de una vez, se agrega a la lista repetidos y se elimina de la lista elementos_x utilizando la función remove().

Finalmente, si no hay elementos repetidos en la lista elementos_x, se imprime "En esta lista no existen elementos repetidos". En caso contrario, los elementos repetidos se almacenan en la lista repetidos pero no se imprimen en este código.

**PUNTO 7**
Desarrollar un programa que determine si en una lista se encuentra una cadena de caracteres con dos o más vocales. Si la cadena existe debe imprimirla y si no existe debe imprimir 'No existe'.
```Python
#Contador de vocales
palabra = [str(c) for c in input("Ingrese su cadena de caracteres:  ").split()]
def contadorvocales(p):
  vocales = ["a","e","i","o","u"]
  cadena = ""
  cont = 0
  for i in p:
    cadena+=i
  for j in range(len(cadena)):
    if cadena[j] in vocales:
      cont+=1
  if cont>=2:
    print(cadena)
contadorvocales(palabra)
```

Este programa tomará una cadena de caracteres del usuario, la dividirá en palabras y almacenará cada palabra en una lista llamada palabra. Luego, definirá una función llamada contadorvocales que toma la lista de palabras como argumento.

La función contadorvocales busca las vocales en cada palabra de la lista y cuenta todas las apariciones de vocales. Si el recuento de vocales en una palabra es mayor o igual a 2, la función imprimirá esa palabra.

En resumen, el programa imprimirá todas las palabras de la lista que contengan al menos dos vocales.

**PUNTO 8**
Desarrollar un programa que dadas dos listas determine que elementos tiene la primer lista que no tenga la segunda lista.
```Python
#no in
lista_a = [int(x) for x in input("Ingrese los elementos separados por espacio:  ").split()]
lista_b = [int(x) for x in input("Ingrese los elementos separados por espacio:  ").split()]
if len(lista_b)>len(lista_a):
  nv = lista_a
  lista_a = lista_b
  lista_b = nv
descuadre = []
for i in lista_a:
  if i not in lista_b:
    descuadre.append(i)
print(lista_a)
print(lista_b)
print(descuadre)
```

Este código permite al usuario ingresar dos listas de números separados por espacio en la línea de comandos. Luego, se comprueba cuál de las dos listas es más larga. Si la segunda lista es más larga, se intercambian las listas.

Después, se crea una lista vacía llamada 'descuadre'. A continuación, se realiza un bucle 'for' para iterar a través de todos los elementos de la lista más larga (ahora 'lista_a'). Si un elemento de 'lista_a' no está presente en 'lista_b', se agrega a la lista 'descuadre'.

Finalmente, el código imprime las listas 'lista_a', 'lista_b' y 'descuadre'. 'lista_a' y 'lista_b' son las listas originales ingresadas por el usuario, mientras que 'descuadre' es una lista de elementos que están presentes en 'lista_a' pero no en 'lista_b'.

**PUNTO 9**

**PUNTO 10**
Desarrollar un algoritmo que determine si una matriz es mágica. Se dice que una matriz cuadrada es mágica si la suma de cada una de sus filas, de cada una de sus columnas y de cada diagonal es igual.
```Python
#matriz magica
matriz = []
suma_de_filas = []
suma_diagonal_principal=[]
traspuesta=[]
elementos = []
reversa = []
cont = 0
fila = [int(x) for x in input("Ingrese los elementos de la fila separados por espacio:  ").split()]
columnas = len(fila)-1
matriz.append(fila)
while(columnas>0):
 fila = [int(x) for x in input("Ingrese los elementos de la fila separados por espacio:  ").split()]
 matriz.append(fila)
 columnas-=1
def invertir(m,r):
 for i in range(len(m)):
   r.append(m[i][::-1])
 return r
def sumas(m,n,x):
  for i in range(len(m)):
    n.append((sum(m[i])))
    for j in range(len(m[i])):
      if i==j:
        x.append(m[i][j])
  if ((n.count(n[0])==len(n))and(sum(x)==n[0])):
    return True
def matriztraspuesta(m,t,e):
  for i in range(len(m[0])):
    for j in range(len(m)):
      e.append(m[j][i])
    t.append(e)
    e=[]
  return t
def limpiar(sf,sdp):
  sf.clear()
  sdp.clear()
#Suma de filas y diagonal principal
d = sumas(matriz,suma_de_filas,suma_diagonal_principal)
limpiar(suma_de_filas,suma_diagonal_principal)
e = sumas(matriztraspuesta(matriz,traspuesta,elementos),suma_de_filas,suma_diagonal_principal)
limpiar(suma_de_filas,suma_diagonal_principal)
f = sumas(invertir(matriz,reversa),suma_de_filas,suma_diagonal_principal)
limpiar(suma_de_filas,suma_diagonal_principal)
if((d == True) and (e == True) and (f == True)):
  print("La matriz es magica")
 ```

Este programa en Python se encarga de verificar si una matriz es mágica, es decir, si la suma de los elementos de cada fila, cada columna y cada diagonal principal es igual.

Primero, se crea una matriz vacía, y se pide al usuario que ingrese los elementos de la primera fila separados por espacios, los cuales se convierten en enteros y se agregan a la matriz. Luego, se pide al usuario que ingrese los elementos de las filas restantes, y se agregan a la matriz hasta que se hayan ingresado todas las filas.

Después, se definen varias funciones para invertir la matriz, sumar los elementos de cada fila y diagonal principal, y obtener la matriz traspuesta. Estas funciones se utilizan para verificar si la matriz es mágica. Si todas las sumas son iguales, la matriz es mágica y se imprime un mensaje indicando esto.

El programa también utiliza la función limpiar para borrar las listas que se usan para almacenar las sumas de las filas y las diagonales principales, de manera que se puedan usar para almacenar las sumas de las filas y diagonales principales de la matriz traspuesta y la matriz invertida.
