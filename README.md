# 🎮 Ultimate Hangman Challenge V.1.0.0

<div align="center">
  <img src="https://img.shields.io/badge/version-1.0-blue.svg" alt="Version 1.0">
  <img src="https://img.shields.io/badge/python-3.10+-green.svg" alt="Python 3.10+">
  <img src="https://img.shields.io/badge/license-MIT-yellow.svg" alt="License: MIT">
</div>

<p align="center">
  <b>A modern reimagining of the classic word-guessing game with stunning visuals, immersive sound effects, and advanced gameplay features.</b>
</p>

---

## ✨ What's New in Version 1.0.0

This latest version brings significant improvements to both code structure and player experience:

- **🏗️ Class-Based Architecture**: Complete code restructuring using object-oriented programming for better organization and maintainability
- **🌈 Custom Word Categories**: New category system with Animals, Countries, Movies, and Mixed word collections
- **🏆 Enhanced Leaderboard System**: Category-specific leaderboards with detailed statistics and filtering options
- **🔄 Duplicate Letter Handling**: Fixed to reveal all instances of a correctly guessed letter at once
- **🎨 Improved Visual Presentation**: Redesigned game state display with color-coded elements and intuitive layout
- **🎭 Animated Victory & Defeat Screens**: Celebratory animations and dramatic game-over sequences
- **🎯 More Strategic Hint System**: Revamped to reveal all instances of a chosen letter

---

## 🎯 Overview

**Ultimate Hangman Challenge 1.0** takes the classic word-guessing challenge to new heights with a modernized interface, strategic gameplay mechanics, and comprehensive progression systems. Players must decipher hidden words letter by letter before running out of attempts, with each correct guess bringing them closer to victory and each mistake bringing the hangman closer to completion.
Our revamped version combines nostalgic console gameplay with contemporary design principles, creating an engaging experience that appeals to both casual players and word game enthusiasts.

---

## 🌟 Key Features

### 📊 Advanced Gameplay Systems

- **Multi-Tiered Difficulty**: Choose between Easy mode, Hard mode, or Custom Categories
- **Progressive Level System**: Advance through increasingly challenging words
- **Strategic Scoring Mechanics**:
  - **+10 points** for each correct letter
  - **-5 points** for each incorrect guess (minimum score: 0)
  - **+50 bonus points** for guessing the complete word on first attempt
  - **+1 hint** awarded for completing each level

### 🎭 Custom Word Categories

- **Animals**: From common pets to exotic wildlife (200+ entries)
- **Countries**: Nations from around the world (190+ entries)
- **Movies**: Popular film titles across genres (175+ entries)
- **Mixed**: Diverse collection of everyday words (250+ entries)

### 🏆 Comprehensive Leaderboard

- **Category Filtering**: View high scores by specific word categories
- **Performance Metrics**: Track average scores, highest scores, and player counts
- **All-Time Hall of Fame**: View complete player history or top performers
- **Data Persistence**: Scores saved between sessions using pickle

### 🖥️ Enhanced User Interface

- **Two-Column Layout**: Efficient screen space utilization
- **Color-Coded Elements**: Visual distinction between game elements
- **Alphabet Tracking**: Clear visualization of guessed and available letters
- **Dynamic Hangman Display**: Changes color based on danger level
- **Real-Time Statistics**: Continuously updated level, score, and hint information

### 🎬 Cinematic Effects

- **Victory Celebrations**: Animated trophy, confetti effects, and congratulatory messages
- **Defeat Sequences**: Dramatic game over screen with random quotes and full hangman reveal
- **Sound Effects**: Context-sensitive audio feedback for all player actions

---

## 🛠️ Installation

### System Requirements

- Python 3.6+
- 50MB free disk space
- Terminal with color support

### Dependencies

```
pygame>=2.1.2
appdirs>=1.4.4
termcolor>=2.1.0
pyfiglet>=0.8.0
keyboard>=0.13.5
```

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/CodeBySherwan/Ultimate-Hangman-Challenge.git
   ```

2. **Install Required Packages**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch the Game**:
   ```bash
   python Hangman.py
   ```

---

## 🎮 How to Play

### Game Flow

1. **Start & Setup**:
   - Choose from the main menu: Start Game, View Leaderboard, Clear Leaderboard, or How to Play
   - Select difficulty level: Easy, Hard, or explore Custom Categories

2. **Core Gameplay**:
   - Guess letters one at a time or attempt to solve the complete word
   - Use strategic hints when stuck (type 'hint' when prompted)
   - Monitor your progress through the real-time interface

3. **Winning & Progression**:
   - Successfully guess the word to advance to the next level
   - Accumulate points and earn additional hints
   - Try to climb the leaderboard rankings

4. **End of Game**:
   - Game ends when you run out of attempts
   - Enter your name to record your score
   - Choose to play again or return to the main menu

### Commands

- Enter a single letter to guess
- Type a complete word to attempt full solution
- Type 'hint' to reveal a letter (if hints are available)
- Type 'stp' at any time to end the current game

---

## 💻 Code Structure

Our Hangman implementation now uses a robust class-based architecture that improves organization, maintainability, and extensibility:

```
HangmanGame
├── __init__()              # Initialize game variables and resources
├── display_game_rules()    # Show instructions and options
├── select_difficulty()     # Choose game mode
├── select_word_category()  # Select custom word category
├── play_game()             # Main game loop
├── display_game_state()    # Render UI and game elements
├── check_game_status()     # Evaluate win/loss conditions
├── update_hidden_word()    # Process letter revelations
├── get_hint()              # Provide player assistance
├── display_leaderboard()   # Show and filter high scores
└── save_score_pickle()     # Persist player achievements
```

### Key Improvements

- **Encapsulation**: Game state is properly contained within the class
- **Reduced Global Variables**: Improved data management via instance attributes
- **Enhanced Error Handling**: Robust handling of edge cases
- **Better Code Organization**: Logical grouping of related functionality
- **Improved Extensibility**: Easier to add new features and word categories

---

## 🏗️ Project Structure

```
Hangman/
├── Hangman.py           # Main game script
├── soundfiles           # sound effects files(.ogg,.wav,.mp3)
├── Animals.txt          # Animal category word list
├── Countries.txt        # Country names word list
├── Movies.txt           # Movie titles word list
├── Mixed.txt            # General vocabulary word list
├── Easywords.txt        # Easy difficulty words
├── Hardwords.txt        # Hard difficulty words
├── high_scores.pkl      # Saved leaderboard data
├── requirements.txt     # Package dependencies
└── README.md            # This documentation
```

---

## 📝 Notes for Developers

Interested in contributing or extending the game? Here are some tips:

- The class-based structure makes it easy to add new features
- Word lists follow a simple format with one word per line
- Custom categories can be added by creating additional .txt files
- Sound effects can be customized by modifying the chime theme settings
- Visual elements use termcolor and can be adjusted for different terminal environments

---

## 👥 Credits

- **Developmer**:CodeBySherwan
- **Word Lists**: Curated collections of categorized vocabulary
- **Libraries**:
  - [termcolor](https://pypi.org/project/termcolor/) - Terminal text coloring
  - [pyfiglet](https://pypi.org/project/pyfiglet/) - ASCII art generation
  - [PyGame](https://pypi.org/project/pygame/) - Python Game Development
  
  Music by Cleyton Kauffman - https://soundcloud.com/cleytonkauffman
---

## 📄 License

This project is available under the MIT License. See LICENSE file for details.

---

<div align="center">
  <p>
    <b>Challenge your vocabulary, test your luck, and climb the leaderboard in this definitive version of the classic Hangman game!</b>
  </p>
</div>
<img width="791" height="958" alt="Main-Menu" src="https://github.com/user-attachments/assets/7b190c1a-60cd-49bb-9e54-6324bf5e430f" />
![Uploading Difficulty.png…]()
<img width="751" height="676" alt="Custom-Play" src="https://github.com/user-attachments/assets/35195467-9935-4c87-9294-f5cb982ff5bc" />
<img width="890" height="777" alt="Gameplay" src="https://github.com/user-attachments/assets/39f7bcc2-8196-4500-983e-19e60e86e384" />
<img width="934" height="776" alt="Hall-Of-Fame" src="https://github.com/user-attachments/assets/8b752fe4-e65b-49a2-b287-7ac5c3496a97" />




