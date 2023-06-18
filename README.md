# Nim Game

This is a Python program that implements a modified version of the game Nim. The game is played between a human and a computer player. The players take turns removing marbles from two piles: a red pile and a blue pile. The goal is to force the opponent to remove the last marble.

## Prerequisites

- Python 3.x

## Usage

To run the program, execute the following command in your terminal:

```
python nim_game.py [num_red] [num_blue] [goes_first]
```

- `num_red`: The initial number of marbles in the red pile.
- `num_blue`: The initial number of marbles in the blue pile.
- `goes_first`: Specifies who goes first. Enter "computer" or "human".

If any of the command-line arguments are missing, the program will assign random values to `num_red`, `num_blue`, and `goes_first`.

## Rules of the Game

1. The game starts with an initial number of marbles in the red and blue piles.
2. Players take turns removing one marble from either the red pile or the blue pile.
3. The player who removes the last marble from any pile wins the game.
4. The computer player uses an alpha-beta search algorithm to make its decisions.

## Program Structure

The program consists of the following functions:

- `parse_command_line()`: Parses the command line arguments to initialize the game parameters.
- `utility(state)`: Calculates the utility value of a terminal state.
- `terminal_test(state)`: Checks if a state is a terminal state (either red pile or blue pile is empty).
- `successors(state)`: Generates the possible successor states from a given state.
- `alpha_beta_decision(state)`: Performs an alpha-beta search and returns the optimal action.
- `max_value(state, alpha, beta)`: Finds the maximum utility value from the successor states.
- `min_value(state, alpha, beta)`: Finds the minimum utility value from the successor states.
- `start_game(init_red, init_blue, first_player)`: Starts the game and alternates turns between the computer and the human until the game ends.

## Example

Here's an example command to run the program:

```
python nim_game.py 5 7 computer
```

This will start a game with 5 marbles in the red pile, 7 marbles in the blue pile, and the computer goes first.

## Note

- The program uses the `random` module to assign random values to the game parameters if they are not provided through command-line arguments.
- The program assumes valid user input during the human player's turn (i.e., choosing either "red" or "blue" when prompted).
- The program uses the alpha-beta search algorithm to make optimal decisions for the computer player.

Enjoy playing Nim!
