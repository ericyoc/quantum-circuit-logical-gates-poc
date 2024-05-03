# Quantum Circuit Logical Gates

This Python code demonstrates the implementation of various logical gates using quantum circuits. The code utilizes three popular quantum computing libraries: Cirq, PyQuil, and ProjectQ. The logical gates implemented in this code include NOT, AND, XOR, OR, NOR, and NAND.


# Motivating Article
S. A. Metwalli and R. Van Meter, "Testing and Debugging Quantum Circuits," in IEEE Transactions on Quantum Engineering, vol. 5, pp. 1-15, 2024, Art no. 2500415, doi: 10.1109/TQE.2024.3374879.

https://ieeexplore.ieee.org/abstract/document/10463159

## Logical Gates

### NOT Gate
The NOT gate, also known as the inverter, flips the state of a single qubit. If the input qubit is in the state |0⟩, the NOT gate transforms it to |1⟩, and vice versa. The NOT gate is implemented using the Pauli X gate, which is a single-qubit gate that applies a rotation of π radians around the X-axis of the Bloch sphere.

### AND Gate
The AND gate performs a logical AND operation on two or more qubits. The output qubit is in the state |1⟩ only if all the input qubits are in the state |1⟩. The AND gate is implemented using the Toffoli gate (CCNOT), which is a three-qubit gate that applies a controlled-controlled-NOT operation. The Toffoli gate flips the state of the target qubit if both control qubits are in the state |1⟩.

### XOR Gate
The XOR gate (exclusive OR) performs a logical XOR operation on two qubits. The output qubit is in the state |1⟩ if exactly one of the input qubits is in the state |1⟩. The XOR gate is implemented using the CNOT gate (controlled-NOT), which is a two-qubit gate that applies a NOT operation to the target qubit if the control qubit is in the state |1⟩.

### OR Gate
The OR gate performs a logical OR operation on two or more qubits. The output qubit is in the state |1⟩ if at least one of the input qubits is in the state |1⟩. The OR gate is implemented by combining the Pauli X gate and the Toffoli gate. The input qubits are first inverted using the Pauli X gate, then the Toffoli gate is applied, and finally, the output qubit is inverted again using the Pauli X gate.

### NOR Gate
The NOR gate performs a logical NOR operation on two or more qubits. The output qubit is in the state |1⟩ only if all the input qubits are in the state |0⟩. The NOR gate is implemented by combining the Pauli X gate and the Toffoli gate. The input qubits are inverted using the Pauli X gate, then the Toffoli gate is applied, and the output qubit remains unchanged.

### NAND Gate
The NAND gate performs a logical NAND operation on two or more qubits. The output qubit is in the state |0⟩ only if all the input qubits are in the state |1⟩. The NAND gate is implemented by applying the Toffoli gate followed by the Pauli X gate on the output qubit.

## Quantum Gates Used

The quantum gates used in the construction of the logical gates are:

- Pauli X gate: A single-qubit gate that applies a rotation of π radians around the X-axis of the Bloch sphere, effectively flipping the state of the qubit.
- CNOT gate (controlled-NOT): A two-qubit gate that applies a NOT operation to the target qubit if the control qubit is in the state |1⟩.
- Toffoli gate (CCNOT): A three-qubit gate that applies a controlled-controlled-NOT operation, flipping the state of the target qubit if both control qubits are in the state |1⟩.

## Usage

To run the code and see the quantum circuits for each logical gate using different libraries, simply execute the Python script. The code will generate and print the circuit diagrams for each gate using Cirq, PyQuil, and ProjectQ. Additionally, a table comparing the gates and their implementations across the libraries will be displayed.

Make sure to have the required libraries installed before running the code.

## Dependencies

- Python 3.x
- Cirq
- PyQuil
- ProjectQ
- Tabulate

You can install the dependencies using pip:

```
pip install cirq pyquil projectq tabulate
```

Feel free to explore and experiment with the code to gain a better understanding of how logical gates are implemented using quantum circuits!

Disclaimer This repository is intended for educational and research purposes.
