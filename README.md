# calculadora-python
# Calculadora Básica en Python

def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b == 0:
        return "Error: No se puede dividir entre 0"
    return a / b

def menu():
    print("Calculadora Básica")
    print("Selecciona una operación:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Salir")

def main():
    while True:
        menu()
        opcion = input("Introduce el número de la operación (1/2/3/4/5): ")

        if opcion == "5":
            print("Saliendo del programa...")
            break

        try:
            num1 = float(input("Introduce el primer número: "))
            num2 = float(input("Introduce el segundo número: "))
        except ValueError:
            print("Por favor, ingresa números válidos.")
            continue

        if opcion == "1":
            print(f"{num1} + {num2} = {sumar(num1, num2)}")
        elif opcion == "2":
            print(f"{num1} - {num2} = {restar(num1, num2)}")
        elif opcion == "3":
            print(f"{num1} * {num2} = {multiplicar(num1, num2)}")
        elif opcion == "4":
            print(f"{num1} / {num2} = {dividir(num1, num2)}")
        else:
            print("Opción no válida. Intenta de nuevo.")

if __name__ == "__main__":
    main()
