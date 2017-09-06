# Tic Tac Toe with Alpha Beta MiniMax Search Algorithm with GUI
An interactive 4X4 Tic-Tac-Toe game with GUI for a person to play against the computer. The game consists of a 4X4 grid. To win, a player must place 4 of his/her symbols on 4 squares that line up vertically, horizontally or diagonally (45 or 135 degrees.)

### Prerequisite
Python 3.6 and knowledge of Tkintrer python package for GUI.

### Overview

This code demonstrates the use of Alpha Beta Pruning for Game playing. Since, Tic Tac Toe has a depth of 9 , I have used a heuristic function that evaluates the Board State after searching for 10 seconds. The heuristic function calculates the expected score of winning for the PC given the board state.

The hueristic function used is as follows

Eval(s) = 6X <sub>3</sub> + 3X <sub>2</sub> (s) + X <sub>1</sub> (s) − (6O <sub>3</sub> + 3O <sub>2</sub> (s) + O <sub>1</sub> (s))

where s is the current state, X <sub>n</sub> is the number of rows, columns, or diagonals with exactly n X's and no O’s. Similarly, O <sub>n</sub> is the number of rows, columns, or diagonals with just n O’s. To compute the above evaluation function, you should consider every row and every column but only the middle 45 degree diagonal (with 4 squares) and the middle 135 degree diagonal (with 4 squares).

There are three types of terminal nodes:
* player X wins
* player O wins
* draw -- 4×4 grid is filled up and neither player has 4 symbols lined up. Assign a utility value of +1000, -1000 and 0 to the three types of terminal nodes

Each time the ALPHA-BETA SEARCH function is called to return the best action, output the following information (statistics) on the screen

* whether cutoff occurred
* maximum depth reached
* total number of nodes generated (including root node)
* number of times pruning occurred within the MAX-VALUE function
* number of times pruning occurred within the MIN-VALUE function
