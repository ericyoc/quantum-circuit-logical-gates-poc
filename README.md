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

## Comparison Table
![](https://github.com/ericyoc/quantum-circuit-logical-gates/blob/main/restults_qc_logical_gates_compare.jpg)

# Quantum Computing Platforms

## Cirq

Cirq is an open-source framework for programming quantum computers, developed by Google. It provides a way to write quantum circuits and algorithms using Python. Cirq supports a variety of quantum hardware backends, including Google's own Xmon qubits.

### Logical Gates in Cirq

Cirq provides implementations for various logical gates, including:

- `cirq.X`: NOT gate
- `cirq.AND`: AND gate
- `cirq.XOR`: XOR gate
- `cirq.OR`: OR gate
- `cirq.NOR`: NOR gate
- `cirq.NAND`: NAND gate

These gates can be applied to qubits using the `cirq.Circuit` class.

## PyQuil

PyQuil is a Python library for quantum programming using the Quil language, developed by Rigetti Computing. It allows users to construct quantum circuits, manipulate qubits, and run programs on quantum hardware or simulators.

### Logical Gates in PyQuil

PyQuil provides functions to create logical gates, such as:

- `pyquil.gates.X`: NOT gate
- `pyquil.gates.AND`: AND gate
- `pyquil.gates.XOR`: XOR gate
- `pyquil.gates.OR`: OR gate
- `pyquil.gates.NOR`: NOR gate
- `pyquil.gates.NAND`: NAND gate

These gates can be applied to qubits using the `pyquil.quil.Program` class.

## ProjectQ

ProjectQ is an open-source software framework for quantum computing, started at ETH Zurich. It allows users to implement quantum algorithms using a high-level Python interface, which can then be executed on quantum hardware or simulators.

### Logical Gates in ProjectQ

ProjectQ provides a set of built-in operations for logical gates, including:

- `projectq.ops.X`: NOT gate
- `projectq.ops.All`: AND gate
- `projectq.ops.Xor`: XOR gate
- `projectq.ops.Or`: OR gate
- `projectq.ops.Nor`: NOR gate
- `projectq.ops.Nand`: NAND gate

These gates can be applied to qubits using the `projectq.ops.C` function for controlled gates and the `projectq.ops.Tensor` function for combining multiple gates.

Each of these platforms provides a way to construct quantum circuits using logical gates and execute them on quantum hardware or simulators, making it easier for developers to explore and build quantum algorithms.

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
