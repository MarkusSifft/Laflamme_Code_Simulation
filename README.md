# Laflamme Code with Braunstein Improvement

## Overview

This repository contains a Jupyter Notebook demonstrating a quantum error correction simulation using the Laflamme code with Braunstein's improvement. The notebook focuses on simulating the evolution of a logical qubit using the stochastic master equation, showcasing how quantum error correction protects the quantum state over time.

## Contents

### Key Sections of the Notebook

1. **Defining Quantum Gates and Operators for Error Correction**:
   - Spin operators (Pauli matrices) for each qubit in a 5-qubit system are defined. These operators are essential for constructing the Hamiltonian and applying gates to model quantum operations.

2. **Initializing the System State and Hamiltonian**:
   - Initial state setup and the system Hamiltonian definition. The logical qubit is initialized in the excited state.

3. **Measurement Strengths and Operators**:
   - Specifies damping and measurement strengths, along with the necessary collapse operators to model environmental effects.

4. **Encoding and Decoding Functions**:
   - Functions to encode and decode the logical qubit state are defined using the Braunstein formulation of the Laflamme code.

5. **Error Correction Procedure**:
   - Defines possible single-qubit errors and constructs a correction table based on syndrome measurements, which maps errors to appropriate correction operations.

6. **System Evolution Simulation**:
   - Using `mesolve` and the stochastic master equation, the notebook simulates the time evolution of the system state and applies error correction at regular intervals.

7. **Visualization**:
   - The notebook includes a plotting function to visualize the evolution of the qubit states and the fidelity of the error-corrected logical qubit over time.

8. **Full Simulation**:
   - The notebook runs a complete cycle of encoding, error correction, and decoding across multiple time steps. It then compares the fidelity of the error-corrected qubit with that of an uncorrected qubit, demonstrating the effectiveness of the Laflamme code.

### Results Summary

During each cycle of encoding and decoding, the fidelity decreases as expected because the encoded state is distant from the initial state in Hilbert space. However, after decoding and applying corrections to the ancilla and main qubit, the fidelity returns to approximately its maximum value. By contrast, the fidelity of the uncorrected qubit decays significantly over time.

## How to Run the Notebook

1. **Prerequisites**:
   - Python with `qutip`, `numpy`, `matplotlib`, and `itertools`.

2. **Running the Notebook**:
   - Open the notebook in Jupyter, execute each cell in sequence, and follow the outputs. The code will display graphs showing the fidelity of the error-corrected and uncorrected qubits over time.

## Purpose

This notebook serves as an educational demonstration of quantum error correction principles. It provides a practical simulation of how error correction can preserve quantum information despite noise and errors.
