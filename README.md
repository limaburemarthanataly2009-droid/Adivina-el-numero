import random


def jugar():

    numero_secreto = random.randint(1, 100)
    intentos = 0

    print("\nSe ha generado un número entre 1 y 100")

    while True:

        try:
            numero = int(input("Ingresa tu número: "))
            intentos += 1

            if numero == numero_secreto:
                print(f"\n¡Ganaste!")
                print(f"Intentos realizados: {intentos}")
                break

            elif numero < numero_secreto:
                print("El número secreto es mayor.")

            else:
                print("El número secreto es menor.")

        except ValueError:
            print("Debes ingresar un número válido.")


def menu():

    while True:

        print("\n========================")
        print(" ADIVINA EL NÚMERO ")
        print("========================")
        print("1. Jugar")
        print("2. Salir")

        opcion = input("Seleccione una opción: ")

        if opcion == "1":
            jugar()

        elif opcion == "2":
            print("Gracias por jugar.")
            break

        else:
            print("Opción inválida.")


menu()
