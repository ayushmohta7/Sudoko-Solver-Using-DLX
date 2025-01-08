# Sudoku Solver Using DLX

This project is an implementation of Donald Knuth's Algorithm X using the Dancing Links (DLX) technique to solve Sudoku puzzles efficiently.

## Table of Contents

- [Introduction](#introduction)
- [Algorithm Overview](#algorithm-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)
- [License](#license)

## Introduction

In this project, we tackle the challenge of solving Sudoku puzzles using Algorithm X combined with Dancing Links. This clever approach transforms the puzzle into an "exact cover" problem, allowing us to efficiently find solutions.

## Algorithm Overview

Algorithm X is a recursive, nondeterministic, depth-first, backtracking algorithm devised by Donald Knuth to solve exact cover problems. The Dancing Links technique is an efficient implementation of Algorithm X using a circular doubly linked list to represent the matrix, allowing for quick removal and restoration of rows and columns during the search process.

In the context of Sudoku, the constraints are:

1. Each row must contain digits 1-9 without repetition.
2. Each column must contain digits 1-9 without repetition.
3. Each 3x3 subgrid must contain digits 1-9 without repetition.
4. Each cell must contain exactly one digit.

These constraints are mapped to an exact cover problem, which is then solved using the DLX algorithm.

## Features

- Can be used to solve N-Queen,Kakuro and Nonogram.
- Command-line interface for input and output.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ayushmohta7/Sudoko-Solver-Using-DLX.git
   cd Sudoko-Solver-Using-DLX
   ```

2. **Compile the program:**

   Ensure you have a C++ compiler installed. Then, compile the source code:

   ```bash
   g++ -o sudoku_solver main.cpp
   ```

## Usage

1. **Prepare your Sudoku puzzle:**

   Create a text file (e.g., `puzzle.txt`) containing the Sudoku puzzle. Use zeros (`0`) to represent empty cells. For example:

   ```
   530070000
   600195000
   098000060
   800060003
   400803001
   700020006
   060000280
   000419005
   000080079
   ```

2. **Run the solver:**

   ```bash
   ./sudoku_solver puzzle.txt
   ```

   The solved puzzle will be displayed in the console.

## References

- Donald Knuth's paper on Dancing Links: [http://www.ocf.berkeley.edu/~jchu/publicportal/sudoku/0011047.pdf](http://www.ocf.berkeley.edu/~jchu/publicportal/sudoku/0011047.pdf)
- Jonathan Chu's explanation on converting Sudoku to an exact cover problem: [https://www.ocf.berkeley.edu/~jchu/publicportal/sudoku/sudoku.paper.html](https://www.ocf.berkeley.edu/~jchu/publicportal/sudoku/sudoku.paper.html)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

