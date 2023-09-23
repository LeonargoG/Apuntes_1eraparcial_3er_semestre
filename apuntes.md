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
