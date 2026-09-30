# CODE-ALPHA-RULE-BASED-CHATBOT(JARVIS)
HELLO EVERYONE, I'M Avinash.D i am doing my first internship in #codealpha and my first project is creating a rule-based chatbot using python.
# What This Project Can Do

## Core Functionality

## Hangman Game – Text Explanation

This Hangman game is built using only basic Python concepts, making it perfect for beginners. Here’s how it works, step by step:

## 1. Importing the Random Module

The game starts by importing the `random` module. This allows the program to randomly select one word from a predefined list each time the game is played.

## 2. Defining the Word List

A simple list called `words` contains exactly five predefined words: "python", "hangman", "coding", "game", and "logic". No external files or APIs are needed, keeping the program self-contained and easy to understand.

## 3. Selecting the Secret Word

Using `random.choice(words)`, the program picks one word at random from the list. This becomes the secret word that the player must guess.

## 4. Initializing Game Variables

Three key variables track the game state:
- `guessed_letters`: an empty list that will store every letter the player guesses
- `incorrect_guesses`: a counter starting at 0 to track wrong guesses
- `max_incorrect`: set to 6, representing the maximum allowed wrong guesses before the game ends

## 5. Displaying the Welcome Message

The program prints a welcome message and tells the player how many letters are in the secret word using `len(secret_word)`. This gives the player a hint without revealing the word.

## 6. The Main Game Loop (While Loop)

The core of the game is a `while` loop that continues running as long as `incorrect_guesses` is less than 6. Each iteration of the loop represents one turn where the player makes a guess.

## 7. Building the Display String

Inside the loop, the program creates a `display` string by checking each letter in the secret word:
- If the letter has been guessed, it shows that letter
- If not, it shows an underscore "_" as a placeholder

This creates the familiar Hangman display like "p_t_on" or "_____" that updates after each guess.

## 8. Showing Game Status

The program displays three pieces of information to the player:
- The current word progress (with guessed letters and underscores)
- The number of incorrect guesses out of 6
- All letters that have been guessed so far

## 9. Checking for a Win

Before asking for a new guess, the program checks if there are any underscores left in the display. If there are none, it means all letters have been guessed correctly, and the player wins. The loop breaks and a congratulations message is shown.

## 10. Getting Player Input

The program uses `input()` to get the player's letter guess. The `.lower()` method ensures the guess is converted to lowercase, making the game case-insensitive.

## 11. Validating the Input (If-Else)

The program validates the input using `if-else` statements:
- Checks if the input is exactly one character using `len(guess) != 1`
- Checks if it's a letter using `isalpha()`
- Checks if the letter was already guessed by seeing if it's in `guessed_letters`

If any validation fails, an error message is shown and the loop continues to the next iteration without counting it as a guess.

## 12. Processing the Guess

If the input is valid, the guessed letter is added to the `guessed_letters` list. Then another `if-else` checks whether the letter is in the secret word:
- If yes: prints "Good guess!" and continues
- If no: prints "Wrong guess!" and increments `incorrect_guesses` by 1

## 13. Checking for Game Over

When the `while` loop ends (either by breaking on a win or reaching 6 incorrect guesses), the program checks if the player lost by testing if `incorrect_guesses >= max_incorrect`. If true, it reveals the secret word and displays a game over message.

## Key Concepts Demonstrated

- **random**: Used to select an unpredictable word from the list
- **while loop**: Keeps the game running until win or loss conditions are met
- **if-else**: Handles all decision-making (validation, correct/incorrect guesses, win/loss)
- **strings**: Used for the secret word, display building, and user input
- **lists**: Store the word choices and track guessed letters throughout the game

This simple structure creates a complete, playable game while demonstrating fundamental programming concepts in a practical, hands-on way.



