import random

def guess_the_number():
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    guessed_correctly = False

    print("Welcome to the Guess the Number game!")
    print("I have generated a random number between 1 and 100. Try to guess it!")

    # Loop until the user guesses the number correctly
    while not guessed_correctly:
        try:
            # Get the user's guess
            user_guess = int(input("Enter your guess: "))
            attempts += 1

            # Compare the guess with the generated number
            if user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                guessed_correctly = True
                print(f"Congratulations! You've guessed the number correctly in {attempts} attempts.")

        except ValueError:
            print("Invalid input! Please enter a valid number.")

# Run the game
guess_the_number()

