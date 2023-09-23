```
# Listas (se conocen como conecciones)
# datos mutables y inmutables

def suma(a,b):
    return a+b

def resta(a,b):
    return a-b

def multiplicacion(a,b):
    return a*b

def division(a,b):
    return a/b

operaciones=[suma,resta,multiplicacion,division]
print(operaciones[0](1,2))
print(operaciones[1](1,2))
print(operaciones[2](1,2))
print(operaciones[3](1,2))
for operacion in operaciones:
    print(operacion(1,2)) 
lista=[1,2,3,4,5,True,1.2,'hola',[1,2,3]]
```

```
# funcion pura = tiene argumentos, no producen efectos secundarios, retorna siempre el mismo valor con la misma entrada
# ejemplo funcion pura = Math.sqrt(49)-> 7

## funcion impura = no tiene argumentos, puede retornar valores distintos, 
# ejemplo funcion impura= Math.random() -> 0.05
#                         Math.random() -> 3 
""" 
while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion >= '5':
        print("¡Hasta luego!")
        break

    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))

    if opcion == '1':
        print("Resultado:", num1 + num2)
    elif opcion == '2':
        print("Resultado:", num1 - num2)
    elif opcion == '3':
        print("Resultado:", num1 * num2)
    elif opcion == '4':        
        if num2 != 0:
            print("Resultado: ", num1 / num2)
        else:
            print("No se puede dividir entre cero")
    else:
        print("¡Gracias por usar Mi Calculadora!") """
 
""" class MiCalculadora:
    def _init_(self):
        pass

    def suma(self, a, b):
        return a + b

    def resta(self, a, b):
        return a - b

    def multiplicacion(self, a, b):
        return a * b

    def division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "No se puede dividir entre cero"

calculadora = MiCalculadora()

while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))

    if opcion == '1':
        print("Resultado:", calculadora.suma(num1, num2))
    elif opcion == '2':
        print("Resultado:", calculadora.resta(num1, num2))
    elif opcion == '3':
        print("Resultado:", calculadora.multiplicacion(num1, num2))
    elif opcion == '4':        
        if num2 != 0:
            print("Resultado:", calculadora.division(num1, num2))
        else:
            print("No se puede dividir entre cero") """

""" def suma(a, b):
    return a + b

def resta(a, b):
    return a - b

def multiplicacion(a, b):
    return a * b

def division(a, b):
    return a / b

def mi_calculadora(opcion, num1, num2):
    if opcion == '1':
        return suma(num1, num2)
    elif opcion == '2':
        return resta(num1, num2)
    elif opcion == '3':
        return multiplicacion(num1, num2)
    elif opcion == '4' and num2 != 0:
        return division(num1, num2)
    else:
        return "Opción no válida"

while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")

    opcion = input("Selecciona una opción: ")

    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
        resultado = mi_calculadora(opcion, num1, num2)
        print("Resultado:", resultado) """


n:str=10
print(f'n str esta en la direccion: {id(n)}')
n:int='hola'
print(f'n str esta en la direccion: {id(n)}')
hola=10
print(f'n str esta en la direccion: {id(hola)}')
cadena='hola'
print(f'n str esta en la direccion: {id(cadena)}')
```

```
# TIPOS DE DATOS
numero: int =10
numero= 'dos'
print(numero)
```
*Operadores logicos*

```
True
False
if 5 > 4:
    print(True)
print(5>7)
 
received: bool = False
not received
```

```
nombre: str = 'hugo'
print(nombre)
print(type(nombre))
nombre.capitalize()
nombre.upper()
```

```
num: int = 10
pi: float = 3.14
es_alumno: bool = True
name: str = 'Hugo'
print(f'{num}--{pi}--{es_alumno}--{name.upper()}')
```

*Operadores Aritmeticos*
```
print(5+4)
print(5-4)
print(5*4)
print(5/4)
print(5//4) # division entera
print(5%4) # modulo o residuo
print(5**4) # x a la y
```

```
# main(entry point=punto de entrada)
# un lenguaje 
""" import libreria.suma as lib
import libreria.resta as lib
from libreria import suma,resta """
# import libreria as lib

if __name__ == "__main__":
    print(lib.suma(7,8))
    print(lib.resta(8,5))
```

```
# funcion decorador se utiliza para modificar el comportamiento de otra funcion

from dataclasses import dataclass

@dataclass #decorators
class User:
    id: str
    name: str
    age: int

    def show_data(self):
        return f"ID: {self.id}\nNOMBRE: {self.name}\nAÑO: {self.age}"

if __name__ == "__main__":
    usuario1 = User("1","leonardo",25)
    usuario2 = User("2","sebastian",25)
    usuario3 = User("3","gonzalez",25)
    usuario4 = User("4","rodriguez",25)
    usuarios = [usuario1,usuario2,usuario3,usuario4]
    for usuario in usuarios:
        print(usuario.show_data())
```

```
import streamlit as st
st.sidebar.title("CALCULADORA ICI")

def pedir_valores():
    name = st.text_input("NOMBRE: ")
    n1 = st.number_input("NUMERO 1")
    n2 = st.number_input("NUMERO 2")

    if st.button("SUMAR"):
        st.success(f"HOLA {name}")
        st.write(f"{n1} + {n2} = {n1+n2}")
    elif st.button("RESTAR"):
        st.success(f"HOLA {name}")
        st.write(f"{n1} - {n2} = {n1-n2}")
    

opcion = st.sidebar.selectbox("opciones:",[
    "SUMA","RESTA","MULTIPLICACION","DIVISION","ACERCA DE"
])

match opcion:
    case "SUMA":
        st.write("ESTA ES LA SUMA DE...")
        pedir_valores()
    case "RESTA":
        st.write("ESTA ES LA RESTA DE...")
        pedir_valores()
    case "MULTIPLICACION":
        st.write("ESTA ES LA MULTIPLICACION DE...")
    case "DIVISION":
        st.write("ESTA ES LA DIVISION DE...")
    case "ACERCA DE":
        st.write("DERECHOS RESERVADOS")
        st.write("UCOL-FIME-ICI")
```

```
def resta(a:int,b:int) ->int:
    return a-b
if __name__ == "__main__":
    print(resta(8,5))
```

```
# hins(pistas): se le conoce asi a a asignacion en este caso es el entero


def suma1(a: int ,b: int)->int: #salida entera
    return a + b

def suma2(a:float,b:float)->float:
    return a+b
def suma(a:int|float,b:int|float)->int|float:
    return a+b

if __name__ == "__main__": # equivalente de un entry point en python
    print(suma1(5,6))
    print(suma2(4.5,4.5))
    print(suma(5,5.5))
```
