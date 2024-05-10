import random

def guess_number(min_value, max_value):
    secret_number = random.randint(min_value, max_value)
    
    while True:
        guess = int(input(f"Guess the number (between {min_value} and {max_value}): "))
        
        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print("Congratulations! You guessed the number", secret_number)
            break

min_value = int(input("Enter the minimum value for the range: "))
max_value = int(input("Enter the maximum value for the range: "))

guess_number(min_value, max_value)
