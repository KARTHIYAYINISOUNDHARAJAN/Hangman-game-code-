# Hangman-game-code
import random

HANGMAN_PICS = [
    '''
      +---+
          |
          |
          |
         ===''', '''
      +---+
      O   |
          |
          |
         ===''', '''
      +---+
      O   |
      |   |
          |
         ===''', '''
      +---+
      O   |
     /|   |
          |
         ===''', '''
      +---+
      O   |
     /|\\  |
          |
         ===''', '''
      +---+
      O   |
     /|\\  |
     /    |
         ===''', '''
      +---+
      O   |
     /|\\  |
     / \\  |
         ==='''
]

# Word list
words = ['apple', 'banana', 'grapes', 'orange', 'mango', 'cherry']
word = random.choice(words)

# Initialize game state
guessed_word = ['_'] * len(word)
wrong_guesses = 0
max_attempts = len(HANGMAN_PICS) - 1
guessed_letters = []

print("🎮 Welcome to Hangman with ASCII Art!")

# Game loop
while wrong_guesses < max_attempts and '_' in guessed_word:
    print(HANGMAN_PICS[wrong_guesses])
    print("\nWord:", ' '.join(guessed_word))
    print(f"Wrong guesses left: {max_attempts - wrong_guesses}")
    guess = input("Guess a letter: ").lower()

    if not guess.isalpha() or len(guess) != 1:
        print("❌ Please enter a single letter.")
        continue

    if guess in guessed_letters:
        print("⚠️ You've already guessed that letter.")
        continue

    guessed_letters.append(guess)

    if guess in word:
        print("✅ Correct!")
        for i in range(len(word)):
            if word[i] == guess:
                guessed_word[i] = guess
    else:
        print("❌ Wrong!")
        wrong_guesses += 1

# Game over
if '_' not in guessed_word:
    print("\n🎉 You won! The word was:", word)
else:
    print(HANGMAN_PICS[wrong_guesses])
    print("\n💀 You lost! The word was:", word)e-
