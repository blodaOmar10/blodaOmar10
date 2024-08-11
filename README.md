import random

def jugar_adivinanza():
    print("¡Bienvenido al juego de adivinanza!")
    numero_secreto = random.randint(1, 100)
    intentos = 0
    adivinado = False

    while not adivinado:
        try:
            guess = int(input("Adivina el número (entre 1 y 100): "))
            if 1 <= guess <= 100:
                intentos += 1
                if guess < numero_secreto:
                    print("El número es mayor.")
                elif guess > numero_secreto:
                    print("El número es menor.")
                else:
                    adivinado = True
                    print(f"¡Felicidades! Has adivinado el número en {intentos} intentos.")
            else:
                print("Por favor, introduce un número entre 1 y 100.")
        except ValueError:
            print("Entrada no válida. Introduce un número entero.")

if _name_ == "_main_":
    jugar_adivinanza()
