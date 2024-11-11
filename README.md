# Sudoku Solver

A React-based Sudoku Solver application that allows users to input values, check progress, solve the puzzle, or reset the board.

## Project Structure

The main files and components in this project include:

- **App.js**: The core of the Sudoku Solver, containing the main logic and functions.
- **App.css**: Styles for the application.
- **public/index.html**: The main HTML file.

## Features

- **Input Sudoku values**: Users can input numbers 1-9 in the cells.
- **Check Solution**: A button to verify if the current entries are on the right path or complete.
- **Solve Puzzle**: A solver function that fills in the board with the correct solution.
- **Reset Board**: Resets the grid to the initial state.

## Installation

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Start the project with `npm start`.

## Usage

1. Input values in empty cells.
2. Use the "Check" button to verify your progress.
3. Click "Solve" to auto-complete the puzzle.
4. Use "Reset" to start over with the initial configuration.

## Algorithm

This application uses a **backtracking algorithm** to solve the Sudoku puzzle, implemented in the `solver` function within `App.js`.

### Algorithm Explanation

1. **Recursive Cell Filling**:
   - The algorithm fills each cell by trying numbers 1 through 9.
   - It checks if placing a number in a cell is valid (i.e., doesn’t repeat in its row, column, or 3x3 box).

2. **Validation Functions**:
   - **checkRow**: Confirms the number isn’t repeated in the row.
   - **checkCol**: Confirms the number isn’t repeated in the column.
   - **checkBox**: Confirms the number isn’t repeated in the 3x3 box.

3. **Backtracking Process**:
   - If a valid number is found, it is placed in the cell, and the function proceeds to the next cell.
   - If a cell has no valid number, the function backtracks to the previous cell and tries a different number.
   - The process continues until the board is completely and correctly filled.

4. **Final Check**:
   - Once completed, the board is validated to ensure it adheres to Sudoku rules.

### Key Functions in `App.js`

- **getDeepCopy**: Creates a deep copy of the board to avoid mutating the original array.
- **onInputChange**: Handles user input for each cell.
- **compareSudokus**: Checks if the current board matches the solved board.
- **solver**: Implements the backtracking algorithm to solve the puzzle.
- **resetSudoku**: Resets the board to its initial configuration.

## Future Enhancements

Possible improvements for this Sudoku Solver:
- **Hints**: Suggest a valid move for users.
- **Live Validation**: Show warnings for incorrect entries as users type.
- **Game Mode**: Add a timer and scoring system for a challenge.

## License

This project is open-source and available under the MIT License.
