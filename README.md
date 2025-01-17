echo "# Nee" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/neelang24/Nee.git
git push -u origin main# Nee
Numberss
import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")
    
    # Generate a random number between 1 and 100
    number_to_guess = random.randint(1, 100)
    attempts = 0
    max_attempts = 10  # Limit the number of attempts
    
    while attempts < max_attempts:
        try:
            # Get the player's guess
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            # Check the guess
            if guess < number_to_guess:
                print("Too low! Try again.")
            elif guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number in {attempts} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")
    
    if attempts == max_attempts and guess != number_to_guess:
        print(f"Sorry, you've used all {max_attempts} attempts. The number was {number_to_guess}.")
    print("Thanks for playing!")

# Run the game
number_guessing_game()
