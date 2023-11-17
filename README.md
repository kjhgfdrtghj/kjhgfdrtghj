import random

def get_secret_number():
    return random.randint(1, 100)

def start_game():
    print("Adivina el número secreto!")
    number = get_secret_number()
    tries = 0
    guess = None

    while guess != number:
        guess = int(input("Ingresa tu guess: "))
        tries += 1

        if guess == number:
            print(f"Felicidades! Adivinaste el número secreto {number} en {tries} intentos!")
        elif guess > number:
            print("El número secreto es menor. Intenta de nuevo.")
        else:
            print("El número secreto es mayor. Intenta de nuevo.")

    print("Juego terminado.")

if __name__ == "__main__":
    start_game()
