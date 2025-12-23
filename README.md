# Bridging Biological Neurons and Artificial Activations  
**Feed-Forward and Spiking Neural Networks via the Leaky Integrate-and-Fire Model**

**Course:** MATH 456 – Mathematical Modeling  
**Author:** Helektra Katsoulakis  
**Institution:** University of Massachusetts Amherst  
**Date:** 17 December 2025

---

## Project Overview

Modern artificial neural networks achieve strong performance but rely on dense,
continuous computation that is energy-intensive. In contrast, biological neural
systems operate using sparse, event-driven spikes while consuming orders of
magnitude less power.

This project investigates how **biological neuron dynamics**, modeled using the
**Leaky Integrate-and-Fire (LIF) neuron**, relate to standard artificial activation
functions and how these differences manifest at the network level.

Specifically, the project:
- Analyzes LIF neuron dynamics and firing-rate behavior
- Compares biological firing-rate curves to ReLU and sigmoid activations
- Trains and evaluates a **Feed-Forward Neural Network (FFNN)** and a
  **Spiking Neural Network (SNN)** on MNIST
- Quantifies computational efficiency gains from spike-based computation

---

## Key Contributions

- **LIF Modeling:**  
  Simulated LIF neuron dynamics using a biologically grounded ODE and derived
  the rheobase current analytically.

- **Non-Dimensionalization:**  
  Reduced the LIF model to a universal, parameter-independent form showing that
  behavior is controlled by a single dimensionless input parameter.

- **Activation Function Comparison:**  
  Demonstrated that standard activations (ReLU, sigmoid) fail to simultaneously
  capture the sharp threshold and saturation present in biological neurons.

- **Network-Level Comparison:**  
  Trained matched FFNN and SNN architectures on MNIST and showed:
  - Comparable classification accuracy
  - **~76× fewer operations** in the SNN due to spike sparsity

---

## Methods

### LIF Neuron Model
The neuron membrane voltage is modeled as:
\[
C_m \frac{dV}{dt} = -g_L (V - E_L) + I_{in}
\]

Spikes occur when voltage crosses threshold, followed by reset and refractory
dynamics.

### F–I Curve Analysis
- Simulated neuron response across a range of constant input currents
- Computed firing-rate vs. input-current curves
- Identified sharp thresholding and saturation behavior

### Network Models
- **FFNN:** Dense fully connected network with ReLU activations
- **SNN:** Identical architecture using LIF neurons and surrogate-gradient training
- Dataset: MNIST digit classification

---

## Results Summary

- LIF neurons exhibit sharp rheobase thresholding and firing-rate saturation
- ReLU captures threshold but not saturation; sigmoid captures saturation but not sharp onset
- SNN achieves accuracy comparable to FFNN on MNIST
- SNN requires dramatically fewer operations due to sparse spike activity
- Results support **event-driven computation** as a path toward energy-efficient AI

Full figures, derivations, and quantitative results are provided in the paper.

---

## Project Paper

**Final Report (PDF):**  
[456_FINAL_PROJECT.pdf](456_FINAL_PROJECT-3.pdf)

> **Note:** GitHub may not render this PDF inline. Please download to view.

---

## Presentation Slides

**Final Presentation:**  
[LIF_SNN_Presentation.pdf](LIF_SNN_PresentationFINAL.pdf)
> **Note:** GitHub may not render this PDF inline. Please download to view.

---

## Repository Contents

- `456_FINAL_PROJECT.pdf` — Final written report
- `LIF_SNN_PresentationFINAL.pdf` — Presentation slides
- `*.ipynb` — Simulation, analysis, and training notebooks 

---

## Key Topics

- Leaky Integrate-and-Fire neurons
- Spiking neural networks
- Non-dimensionalization of ODEs
- Activation functions (ReLU, sigmoid)
- Neuromorphic and energy-efficient computing
- MNIST classification

---

## References

See the full reference list in the project paper for sources on LIF modeling,
spiking neural networks, surrogate-gradient training, and neuromorphic hardware.

---

