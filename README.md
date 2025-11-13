# javascript-tetrishw3
This project is a fully playable Tetris game built in **Godot**, featuring an **AI agent** that evaluates game states using a heuristic scoring function.

---

## 🎮 Features
- Classic Tetris gameplay logic (gravity, rotation, lock delay, line clearing)
- AI-controlled autoplay mode
- Heuristic evaluation function using:
  - Aggregate column height
  - Holes
  - Bumpiness
  - Lines cleared
  - Complete board evaluation
- Real-time simulation of possible moves for each new piece
- Visual Debug (optional): AI-drawn tile preview of the evaluated position

---

## 🧠 How the AI Works

For every possible:
- rotation (0–3)
- horizontal position

… the AI:
1. Simulates dropping the piece.
2. Computes a new board state.
3. Scores it using a heuristic:
score = w1 * complete_board
+ w2 * gravity
+ w3 * hole
+ w4 * bumpiness
+ w5 * clear
4. Chooses the move with the **highest score**.

Weights can be tuned to generate different playstyles.
