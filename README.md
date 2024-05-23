# pythonpro
This Python code is a number guessing game 🎲.
 It generates a random number between 1 and 100 🔢 and prompts the user to guess it, providing feedback if the guess is too low 📉 or too high 📈. The game keeps track of the number of attempts and congratulates the user when they guess correctly 🎉.
 After a successful guess, the user is asked if they want to play again 🔄,resetting the game if they do


********CODE*****************


 import random

# Generate a random number between 1 and 100
number = random.randint(1, 100)

# Initialize a variable to keep track of the number of attempts
attempts = 0

# Main game loop
while True:
  # Prompt the user to input their guess
  guess = int(input("Enter your guess: "))

  # Increment the number of attempts
  attempts += 1

  # Compare the guess to the generated number
  if guess < number:
    print("Too low!")
  elif guess > number:
    print("Too high!")
  else:
    print(f"Congratulations! You guessed the number in {attempts} attempts.")
    break

# Play again?
response = input("Do you want to play again? (y/n): ")
if response.lower() == "y":
  # Reset the variables and start over
  number = random.randint(1, 100)
  attempts = 0
else:
  print("Thanks for playing!")
