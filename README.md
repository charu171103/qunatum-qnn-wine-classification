# Quantum Neural Network for Wine Dataset 🧠🍷

This project demonstrates a **Quantum Neural Network (QNN)** for classifying the **Wine dataset**, combining classical preprocessing with quantum circuit layers using **PennyLane** and **PyTorch**.

---

## Overview

A **Quantum Neural Network (QNN)** is a hybrid model that integrates classical neural networks with quantum computing principles. It leverages quantum circuits to encode data and perform computations that exploit quantum phenomena such as superposition and entanglement, aiming for enhanced learning capabilities.

This notebook implements a QNN to classify wine types based on their chemical properties, using:

- Classical preprocessing to scale and encode data
- Quantum data embedding via angle encoding
- Parameterized quantum layers (`StronglyEntanglingLayers`)
- Measurement of quantum observables as outputs
- Classical postprocessing for final classification

---

## Structure of the QNN

### 1. Classical Preprocessing Layer
- Maps input features to the number of qubits using a linear transformation.
- Prepares the classical data for quantum embedding.

### 2. Quantum Circuit Layer
- **Data Encoding**: Uses angle embedding to map classical inputs into quantum states.
- **Parameterized Layers**: Applies trainable quantum gates (`RX`, `RY`, `RZ`) arranged in strongly entangling layers to create complex quantum feature maps.
- **Entanglement**: Uses entangling gates (e.g., CNOT) to correlate qubits.
- **Measurement**: Observes qubits in the Pauli-Z basis to extract expectation values.

### 3. Classical Postprocessing Layer
- Maps quantum measurements to output classes using a linear layer.

---

## Technologies Used

- [PennyLane](https://pennylane.ai/) — for quantum circuit definition and automatic differentiation  
- [PyTorch](https://pytorch.org/) — for classical neural network components and optimization  
- [Scikit-learn](https://scikit-learn.org/) — for dataset preprocessing and evaluation metrics  
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/) — for visualization

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/charu171103/qml-qnn-wine-classification.git
   cd qml-qnn-wine-classification
