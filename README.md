# Sudoku

A full-screen, modern Sudoku game that runs entirely in the browser. It is a **single, dependency-free HTML file** — no build step, no framework, no server, no internet needed. Open `sudoku.html` and play.

Designed to fill the whole viewport: a large board, a side rail on desktop, and a thumb-friendly bottom dock on phones.

## Features

**Puzzles**
- Four difficulty levels — Easy, Medium, Hard and Expert.
- **Guaranteed-unique puzzles** — every board is generated fresh by a backtracking generator that verifies the solution is unique, so no puzzle is ever ambiguous or guess-based.

**Playing**
- **Notes / pencil marks** — mark candidates in a cell.
- **Auto notes** — fill every empty cell's candidates in one tap.
- **Auto-remove notes** — a correct placement clears that candidate from its row, column and box.
- **Undo and redo** — full move history, including bulk changes like auto notes.
- **Erase** — clear the selected cell.
- **Hint** — reveal one correct value (counted).
- **Check** — validate the board and highlight anything wrong.
- **Smart highlighting** — selecting a cell highlights its row, column and 3×3 box, plus every cell holding the same number.
- **Mistake feedback** — wrong entries turn red and the cell shakes.

**Progress and stats**
- Timer with pause (and auto-pause when you switch tabs).
- Mistake counter, optional **mistake limit** that ends the game.
- **Progress bar** across the bottom of the board.
- **Best-time tracking** per difficulty.
- **Statistics** — games played, games won, win rate, total time, current and best streak, and a per-difficulty breakdown.
- **Save & resume** — close the tab and your game is exactly where you left it.

**Feel**
- **Confetti win screen** with your time, mistakes, hints and a "new best time" badge.
- Soft sound effects with a mute toggle.
- Light and dark themes, remembered between visits.
- Fullscreen mode.
- Full keyboard support.
- Toast notifications, pop/shake animations and a responsive layout from phone to widescreen.

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
| `U` / `R` | Undo / redo |
| `C` | Check the board |
| `A` | Auto notes |
| `P` / `Space` | Pause / resume |
| `Esc` | Close any open panel |

## Running it

No setup required — just open the file in a browser:

```
sudoku.html
```

Or serve it locally:

```
python3 -m http.server
# then visit http://localhost:8000/sudoku.html
```

## Tech

Plain HTML, CSS and JavaScript in one file. The puzzle engine is a randomized backtracking generator with a solution counter for uniqueness checking. The UI is hand-written DOM code with no external libraries, fonts or images — every icon is an inline SVG. Your settings, statistics and saved game live in `localStorage`.

## License

Released for personal and educational use.
