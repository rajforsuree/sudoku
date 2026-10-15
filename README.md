# Sudoku

A clean, modern Sudoku game that runs entirely in the browser. It is a **single, dependency-free HTML file** — no build step, no framework, no server, no internet needed. Open `sudoku.html` and play.

## Features

- **Four difficulty levels** — Easy, Medium, Hard and Expert.
- **Guaranteed-unique puzzles** — every board is generated fresh by a backtracking generator that verifies the solution is unique, so no puzzle is ever ambiguous or guess-based.
- **Notes / pencil marks** — mark candidates in a cell; correct placements auto-clear the matching notes in the row, column and box.
- **Smart highlighting** — selecting a cell highlights its row, column and 3×3 box, plus every cell holding the same number.
- **Mistake feedback** — wrong entries turn red and the cell shakes; duplicates are flagged.
- **Timer, mistakes and hint counters**, with **best-time tracking** saved per difficulty.
- **Undo, erase and hint** — full move history, one tap to fix a cell, one tap to reveal a correct value.
- **Pause** — stops the clock and blurs the board.
- **Progress bar** — shows how much of the grid is complete.
- **Confetti win screen** — with your time, mistakes, hints and a "new best time" badge.
- **Light and dark themes** — remembers your choice.
- **Keyboard support** — play without the mouse.
- **Responsive** — looks right on phones, tablets and desktops.

## How to play

Fill the 9×9 grid so that every row, every column and every 3×3 box contains the digits 1–9 exactly once.

### Keyboard shortcuts

| Key | Action |
| --- | --- |
| `1`–`9` | Place a number |
| `←` `↑` `→` `↓` | Move the selection |
| `Backspace` / `Delete` / `0` | Erase the selected cell |
| `N` | Toggle notes mode |
| `H` | Reveal a hint |
| `U` | Undo |
| `P` / `Space` | Pause / resume |

## Running it

No setup required:

```
# just open the file in a browser
sudoku.html
```

Or serve it locally:

```
python3 -m http.server
# then visit http://localhost:8000/sudoku.html
```

## Tech

Plain HTML, CSS and JavaScript in one file. The puzzle engine is a randomized backtracking generator with a solution counter for uniqueness checking; the UI is hand-written DOM code with no external libraries or fonts.

## License

Released for personal and educational use.
