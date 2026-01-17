# Minesweeper-AI
Minesweeper AI using propositional logic. CS50 AI project.




# Minesweeper-AI

AI agent that plays Minesweeper using propositional logic and knowledge-based inference. Built with Python and Pygame. CS50 AI project.

<img width="584" height="393" alt="image" src="https://github.com/user-attachments/assets/33996aa9-19e3-4d68-9156-cf52d93bda34" />


## About

This project was developed as part of the [CS50's Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/) course. The AI uses knowledge-based reasoning to deduce which cells are safe and which contain mines, making logical inferences from revealed numbers on the board.

## How It Works

The AI represents knowledge using logical sentences of the form:

```
{A, B, C, D} = 2
```

This means: "Out of cells A, B, C, and D, exactly 2 are mines."

### Inference Rules

The AI applies three key inference strategies:

1. **Safe Cell Detection:** If `{A, B, C} = 0`, all cells are safe
2. **Mine Detection:** If `{A, B, C} = 3`, all cells are mines
3. **Subset Inference:** If `{A, B, C} = 1` and `{A, B, C, D, E} = 2`, then `{D, E} = 1`

By continuously applying these rules, the AI can often determine safe moves without guessing.

## Features

- Knowledge-based AI that makes logical deductions
- Visual interface showing the game board
- AI Move button to let the AI play
- Flags mines automatically when identified
- Falls back to random moves only when no safe move can be determined

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/JawadAlnatah/Minesweeper-AI.git
   cd Minesweeper-AI
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the game:
   ```bash
   python runner.py
   ```

## Requirements

- Python 3.x
- Pygame


## How to Play

1. **Click** on a cell to reveal it
2. **Right-click** to flag a cell as a mine
3. **AI Move** button lets the AI make a move
4. Reveal all safe cells without hitting a mine to win!

## What I Learned

- Knowledge representation and propositional logic
- Knowledge-based agents and inference
- Set operations for logical reasoning
- Building interactive applications with Pygame
- Python object-oriented programming

## Acknowledgments

This project is part of CS50's Introduction to Artificial Intelligence with Python course by Harvard University.
