#CodeAlpha Task
🕹️ Hangman Game with ASCII Art — Python Project

🎯 Project Overview

This is a console-based Hangman game developed in Python.
Players try to guess a hidden word one letter at a time. If they guess wrong, a stick figure is gradually drawn using ASCII art. The game ends when the player guesses the full word or the hangman is completely drawn.


---

📌 Features

✅ Random word selection from a word list

✅ Displays hangman figure step-by-step

✅ Shows number of wrong attempts left

✅ Prevents duplicate letter guessing

✅ Easy to read, beginner-friendly code

✅ Clean command-line interface (CLI)



---

🖼️ Example Output

🎮 Welcome to Hangman with ASCII Art!

  +---+
      |
      |
      |
     ===

Word: _ _ _ _ _
Wrong guesses left: 6
Guess a letter: a
✅ Correct!

  +---+
  O   |
 /|\  |
 / \  |
     ===

💀 You lost! The word was: mango


---

🔧 How It Works

1. A word is randomly picked from a list.


2. The player is shown underscores representing the letters.


3. For each guess:

If correct → it reveals the letter.

If wrong → it draws part of the hangman.



4. The game continues until:

🎉 All letters are guessed → You win

💀 Max wrong guesses → You lose





---

🗃️ File Structure

hangman_game.py   ← main Python file with full logic


---

🧠 Concepts Used

random.choice() to pick a word

Lists and strings for word tracking

ASCII art for visual game stages

input() and loops for game interaction

Basic validation and logic control



---

▶️ How to Run

1. Make sure you have Python installed (python --version)


2. Save the code as hangman_game.py


3. Run using:



python hangman_game.py


---

💡 Want to Improve?

Add categories (Fruits, Countries, Movies)

Let user enter their own word

Add score or timer

GUI version using Tkinter or PyQt



---

📜 License

This project is open source and free to use for learning purposes. 🎓
