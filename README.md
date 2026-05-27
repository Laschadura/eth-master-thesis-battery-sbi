# Fast Evaluation of Battery States using Physical Simulations and Simulation-Based Statistical Inference with Normalizing Flows

Master thesis conducted at ETH Zürich in collaboration with ABB Corporate Research.

This work investigates probabilistic battery state estimation using simulation-based Bayesian inference, neural posterior estimation (NPE), and conditional normalizing flows.

The objective of the project is to estimate:

- State of Charge (SoC)
- State of Health (SoH)

from current-voltage measurements using amortized Bayesian inference trained entirely on synthetic battery simulations.

---

## Thesis Summary

Battery state estimation is inherently uncertain and often ill-posed. Different combinations of battery states and parameters can produce nearly identical voltage trajectories, especially under dynamic operating conditions.

This thesis explores simulation-based inference (SBI) as a probabilistic alternative to classical deterministic approaches.

The proposed framework combines:

- Equivalent Circuit Models (ECMs)
- A Neural Posterior Estimator (NPE) with Conditional Normalizing Flows
- Bayesian uncertainty quantification
- Sequential posterior propagation

The approach enables fast amortized inference after training offline on millions of simulated datasets while maintaining calibrated posterior uncertainty estimates.

---

## Main Contributions

- Application of neural posterior estimation (NPE) to battery SoC/SoH estimation
- Demonstration of sim-to-real generalization from synthetic ECM simulations to real ABB battery measurements
- Investigation of sequential posterior propagation across consecutive time windows (seq-NPE)
- Robustness analysis under current-profile and temperature mismatch
- Runtime comparison against SMC-ABC demonstrating >100× speedup through amortized inference

---

## Key Results

### Accurate SoC Estimation

The model achieves accurate and calibrated SoC estimation across a wide range of operating conditions.

### Sim-to-Real Generalization

Models trained exclusively on synthetic ECM simulations successfully generalize to real ABB battery measurements.

### Probabilistic Uncertainty Quantification

The framework produces calibrated posterior distributions instead of deterministic point estimates.

### Amortized Bayesian Inference

Compared to Sequential Monte Carlo Approximate Bayesian Computation (SMC-ABC), the neural posterior estimator achieves inference speedups exceeding two orders of magnitude while maintaining comparable posterior quality.

---

## Methods and Technologies

### Battery Modeling
- 2RC and 3RC Thevenin Equivalent Circuit Models
- OCV-SoC modeling
- Current-profile simulation
- Parameter uncertainty modeling

### Machine Learning
- Neural Posterior Estimation (NPE)
- Conditional Normalizing Flows
- Sequential inference
- Simulation-Based Calibration (SBC)
- Posterior Predictive Checks (PPC)

### Frameworks and Tools
- Python
- TensorFlow / Keras
- BayesFlow
- NumPy
- SciPy

---

## Thesis PDF

The full thesis can be accessed here:

[📄 Simon_Scandella_Master_Thesis.pdf](Simon_Scandella_Master_Thesis.pdf)

---

## Repository Notice

This repository contains the public thesis manuscript associated with the project.

The implementation code is not publicly available due to intellectual property restrictions related to the industrial collaboration with ABB Corporate Research.

---

## Citation

```bibtex
@mastersthesis{scandella2026battery,
  title={Fast evaluation of the status of batteries using physical simulations and simulation based statistical inference with normalizing flows},
  author={Scandella, Simon},
  school={ETH Zürich},
  year={2026}
}
```

---

## Author

Simon Scandella  
ETH Zürich — Mechanical Engineering  
Machine Learning & Energy Systems  
Zürich, Switzerland
