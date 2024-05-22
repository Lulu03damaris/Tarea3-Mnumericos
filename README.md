# Tarea3-Mnumericos
Ejercicios de la tarea 3 de metodos numericos. 
#Ejercicio 1
def truncate(value, digits):
    factor = 10 ** digits
    return int(value * factor) / factor

def sum_series_a():
    forward_sum = 0
    backward_sum = 0
    
    # Sumar de 1 a 10
    for i in range(1, 11):
        term = 1 / (i ** 2)
        forward_sum = truncate(forward_sum + truncate(term, 3), 3)
    
    # Sumar de 10 a 1
    for i in range(10, 0, -1):
        term = 1 / (i ** 2)
        backward_sum = truncate(backward_sum + truncate(term, 3), 3)
    
    return forward_sum, backward_sum

forward_sum, backward_sum = sum_series_a()
print(f"Suma del 1 al 10: {forward_sum}")
print(f"Suma del 10 1 1: {backward_sum}")

