### Quantum Tic-Tac-Toe Rules and Step-by-Step Instructions

Quantum Tic-Tac-Toe is an adaptation of the classic Tic-Tac-Toe game designed to introduce concepts from quantum mechanics such as superposition, entanglement, and measurement collapse. In this game, instead of simply placing an X or O in a square, players place quantum "spooky" markers that can exist in multiple squares simultaneously. The game progresses with these quantum markers until a cyclic loop is detected, forcing a collapse to a classical state. The winner is determined based on the final state of the board after all quantum states have collapsed.

## Complete steps from 1-5 
https://github.com/Roua91/Quantum-Computing-for-Quantum-Curious/blob/main/Labs/tic_tac_toe/Quantum_tic_tac_toe.py
### Step-by-Step Instructions

#### **Step 1: Define the Game Board**
In Quantum Tic-Tac-Toe, the game board is a 3x3 grid, just like in classical Tic-Tac-Toe. However, in this version, each square of the grid is represented by a quantum bit (qubit) in a quantum circuit.

- **Objective**: Create a quantum circuit with 9 qubits, each representing a square on the board.
- **Instructions**:
  1. Import the necessary libraries from Qiskit.
  2. Define a quantum circuit with 9 qubits. These qubits correspond to the 9 squares on the board.



#### **Step 2: Initialize the Board with Quantum Superposition**
Each qubit starts in a quantum superposition, meaning it can represent both X and O simultaneously. This is achieved using the Hadamard gate.

- **Objective**: Place each qubit into a superposition state to represent the possibility of occupying multiple states at once.
- **Instructions**:
  1. Use a loop to apply the Hadamard gate to each of the 9 qubits. This will put each square into a superposition of states.


#### **Step 3: Player Moves**
In Quantum Tic-Tac-Toe, players do not place a single marker but rather create quantum entanglements between squares. Each player places quantum markers on two different squares, and these markers are entangled using a controlled-X (CX) gate.

- **Objective**: Simulate a player's move by entangling two qubits and then maintaining them in superposition.
- **Instructions**:
  1. Define a function to handle a player’s move. The function should take the quantum circuit, the indices of two squares, and the player as input.
  2. Use the controlled-X (CX) gate to entangle the two qubits corresponding to the chosen squares.
  3. Apply Hadamard gates to maintain the qubits in a superposition state.
  4. Measure the qubits to simulate a partial collapse (for visualization purposes).



#### **Step 4: Game Loop**
The game alternates between Player X and Player O, who take turns placing their quantum markers on the board. Each player inputs their chosen squares, and the moves are processed by the `player_move` function.

- **Objective**: Execute a series of moves where both players place quantum markers on the board.
- **Instructions**:
  1. Create a loop to allow Player X and Player O to take turns making moves.
  2. Use a helper function to validate the user input and ensure that two different squares are chosen.
  3. Call the `player_move` function to apply the move to the quantum circuit.



#### **Step 5: Collapse the Quantum State**
Once the players have taken their turns, the quantum state of the board collapses to a classical state. This collapse occurs when a cyclic loop is detected or when the game reaches the end of the prescribed moves.

- **Objective**: Collapse the quantum state of all qubits to determine the final board configuration.
- **Instructions**:
  1. Measure all the qubits to collapse the quantum states.
  2. Use Qiskit’s Aer simulator to run the quantum circuit and retrieve the results.
  3. Display the final probabilities for each possible board configuration using a histogram.


