# Reto-4

#### Acontinuación veremos los las respuestas a los problemas planteados en el reto 4, usando notebook de python, adicional a esto, se adjunto un archivo ipynb con todo el comando para ejecutar en VS Studio Code y probar los comandos.

###### 1. Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.

```
n = int(input("Ingrese un numero entero"))
if n >= 97 and n <= 122:
    print("El numero " + str(n) + " pertenece a una vocal minuscula del codigo ASCII ")
else:
    print("El numero " + str(n) + " no pertenece a una vocal minuscula del codigo ASCII "  "ingresar un numero valido")
```

###### 2. Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.

```
a = input("Ingresa una cadena de longitud 1: ")
if len(a) == 1 and a.isdigit():
    n = int(a)
    if n % 2 == 0:
        print("El dígito " + str(n) + " es par")
    else:
        print("El dígito " + str(n) + " no es par")
else:
    print("Error. Debes ingresar exactamente un dígito") 
```

###### 3. Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

```
c = input("Ingresa un carácter: ")
if len(c) == 1 and c.isdigit():
    m = int(c)
    if -9 <= m <= 9:
        print("El carácter " + str(m) + " es de un solo dígito.")
else:
    print("Error. El carácter no es un dígito o no es de un solo dígito.")
```

###### 4. Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no. 
###### - Positivo: "El número x es positivo
###### - Negativo: "El número x es negativo"
###### - Cero (0): "El número x es el neutro para la suma"

```
x : float
x = float(input("Ingrese un numero entero: "))
if x > 0:
  print("El numero "+str(x)+" es positivo")
elif x < 0:
  print("El numero "+str(x)+" es negativo")
else:
  print("El numero "+str(x)+" es neutro")
```

###### 5. Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.

```
def c(x_punto, y_punto, centro_x, centro_y, radio):
    c_centro = ((x_punto - centro_x)**2 + (y_punto - centro_y)**2)**0.5
    if c_centro < radio:
        return True
    else:
        return False
try:
    x = float(input("Ingrese la coordenada x del punto: "))
    y = float(input("Ingrese la coordenada y del punto: "))
    centro_x = float(input("Ingrese la coordenada x del centro del círculo: "))
    centro_y = float(input("Ingrese la coordenada y del centro del círculo: "))
    radio = float(input("Ingrese el radio del círculo: "))
    if c(x, y, centro_x, centro_y, radio):
        print(f"El punto ({x}, {y}) está en el interior del círculo.")
    else:
        print(f"El punto ({x}, {y}) no está en el interior del círculo.")
except ValueError:
    print("Ingrese coordenadas válidas (números).")
```

###### 6. Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

```
def t (a, b, c):
    if a <= 0 or b <= 0 or c <= 0:
        return False
    if a + b > c and a + c > b and b + c > a:
        return True
    else:
        return False
try:
    l1 = float(input("Digite la longitud del primer lado: "))
    l2 = float(input("Digite la longitud del segundo lado: "))
    l3 = float(input("Digite la longitud del tercer lado: "))
    if es_triangulo(l1, l2, l3):
        print("Con estas longitudes se puede construir un triángulo.")
    else:
        print("Con estas longitudes no se puede construir un triángulo.")
except ValueError:
    print("Digite solo números positivos.")
```
