# Challenge 2: Make the Quantum Coin Biased

**Event:** Qiskit Fall Fest 2026 (IBM Quantum)
**Venue:** Vishnu Institute of Technology, Bhimavaram
**Participant:** [Your Name] · [Roll Number]

## Problem
A Hadamard gate gives a fair quantum coin (50/50). Modify a single-qubit circuit so the probabilities of `0` and `1` are not equal.

## Approach
Placing a phase gate between two Hadamards (**H, T, H**) gives P(0) ≈ 85% and P(1) ≈ 15%. Starting with an X gate flips the bias.

| Circuit | Gates | Predicted result |
|---|---|---|
| A | H, T, H | `0` more frequent (about 85%) |
| B | X, H, T, H | `1` more frequent (about 85%) |

The notebook also includes an extra experiment with an RY(θ) gate to show different degrees of bias.

## Key idea
Gates rotate the qubit's state, which changes the amplitudes of |0⟩ and |1⟩. The measurement probabilities are the squares of those amplitudes.

## Files
- `Challenge_2_Biased_Quantum_Coin.ipynb`: the notebook with circuits, predictions, results, histograms, explanation and the challenge-question answer

## How to run
```bash
pip install qiskit qiskit-aer matplotlib pylatexenc jupyter
jupyter notebook Challenge_2_Biased_Quantum_Coin.ipynb
```

## Tools
Python, Qiskit, Qiskit Aer simulator, Matplotlib
