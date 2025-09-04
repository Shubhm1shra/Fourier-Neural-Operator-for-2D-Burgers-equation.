# Fourier-Neural-Operator-for-2D-Burgers-equation.

This repository demonstrates how to solve the **2D Burgers’ equation** using the **Fourier Neural Operator (FNO)**.  
It provides a simple, end-to-end pipeline for:

- Generating synthetic training data by numerically solving the PDE,  
- Training an FNO model to learn the operator mapping from initial condition → solution at a later time,  
- Evaluating and visualizing predictions.

---

## 🌀 Background

The **2D vector Burgers’ equation** is a canonical nonlinear PDE in fluid dynamics:

$$
\frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x} + v\frac{\partial u}{\partial y} = \nu(\frac{\partial^{2} u}{\partial x^{2}} + \frac{\partial^{2} u}{\partial y^2})
$$
$$
\frac{\partial v}{\partial t} + u\frac{\partial v}{\partial x} + v\frac{\partial v}{\partial y} = \nu(\frac{\partial^{2} v}{\partial x^{2}} + \frac{\partial^{2} v}{\partial y^2})
$$

$$
u_t + u u_x + v u_y = \nu \Delta u, \quad
v_t + u v_x + v v_y = \nu \Delta v
$$

It is widely used as a simplified model to test numerical solvers and machine learning approaches for PDEs.

**Fourier Neural Operators (FNOs)** (Li et al., 2020) learn mappings between function spaces using global convolutions in the Fourier domain, making them highly effective for PDE solution operators.

---

## 📂 Repository Structure
```
├── burgers_fno.ipynb # Main training & evaluation jupiter script
├── artifacts/ # Saved model weights & plots
├── LICENCE # MIT Licence for the project
└── README.md # Project description (this file)
```

---

## 🚀 Getting Started
### 1. Clone the repo
```bash
