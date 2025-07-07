# Hemodynamics Prediction in Brain Aneurysms using PINNs

Welcome to the tutorial site for the FDP talk by Dr. Sangeeta Yadav.

## Overview

This tutorial covers:

- Brain aneurysm modeling
- Physics-informed neural networks (PINNs)
- Case studies and code demos

## [Colab Demo](https://colab.research.google.com/drive/your-colab-link)

## Slides

[Click here to view slides](slides.pdf)

# Hemodynamics Prediction in Brain Aneurysms using Physics-Informed Neural Networks (PINNs)

Welcome to this tutorial from the Faculty Development Program (FDP) held at **NIT Delhi**, presented by **Dr. Sangeeta Yadav**, Assistant Professor, University of Delhi.

This tutorial provides an accessible overview of how **Physics-Informed Neural Networks (PINNs)** can be used to simulate and predict **blood flow dynamics** in **brain aneurysms** — an application of deep learning that blends data with scientific knowledge.

---

## 📌 Objectives

By the end of this tutorial, you will understand:
- What are brain aneurysms and why predicting hemodynamics is clinically important
- The limitations of traditional CFD (Computational Fluid Dynamics)
- How Physics-Informed Neural Networks work
- How to formulate a hemodynamics prediction problem using PINNs
- How to implement a simple PINN using Python
- Extensions to patient-specific modeling

---

## 🧠 1. Introduction to Brain Aneurysms

A **brain aneurysm** is a bulge or ballooning in a blood vessel in the brain. Ruptured aneurysms can lead to **hemorrhagic stroke**, and their risk is closely related to local blood flow patterns — such as **velocity**, **pressure**, and **wall shear stress**.

---

## ⚙️ 2. Governing Equations: Navier-Stokes

Blood flow in large vessels can be modeled as **incompressible Newtonian fluid flow** governed by the **Navier-Stokes equations**:

\[
\frac{\partial \mathbf{u}}{\partial t} + (\mathbf{u} \cdot \nabla)\mathbf{u} = -\nabla p + \nu \nabla^2 \mathbf{u}
\]

\[
\nabla \cdot \mathbf{u} = 0
\]

Where:
- \(\mathbf{u}\) = velocity vector field
- \(p\) = pressure
- \(\nu\) = kinematic viscosity

---

## 🤖 3. What are Physics-Informed Neural Networks (PINNs)?

**PINNs** are neural networks trained not only on data but also to **satisfy physical laws** (PDEs) by including them in the loss function.

**Loss = Data Loss + Physics Loss + Boundary/Initial Condition Loss**

This allows the model to:
- Require less training data
- Be more physically consistent
- Generalize better to unseen scenarios

---

## 🧪 4. Problem Setup for Hemodynamics

We define:
- **Inputs**: Spatial coordinates (x, y, z), time (t)
- **Outputs**: Velocity components (u, v, w), Pressure (p)

**Loss Terms:**
- Residuals of Navier-Stokes equations
- Inlet velocity boundary condition
- No-slip condition on vessel walls
- Outlet pressure or flow constraints

---

## 💻 5. Simple PINN Implementation (Colab)

Try this basic 2D example in Google Colab:  
👉 [PINN for Blood Flow in a Tube (Colab Link)](https://colab.research.google.com/drive/YOUR_LINK_HERE)

Uses:
- `TensorFlow` / `PyTorch`
- `autograd` for computing PDE residuals
- `Adam + L-BFGS` optimizers

---

## 📊 6. Visualizing the Results

- Velocity streamlines
- Pressure contours
- Wall shear stress maps

Use `matplotlib`, `paraview`, or `plotly` for visualization.

---

## 🚀 7. Extensions & Research Ideas

- Extend to **3D patient-specific geometries** using imaging data
- Add **wall compliance** (fluid-structure interaction)
- Model **thrombosis formation** or **rupture risk**
- Combine with **uncertainty quantification** or **Bayesian PINNs**

---

## 📚 References

- Raissi et al., *Physics-Informed Neural Networks*, JCP, 2019. [arXiv:1711.10561](https://arxiv.org/abs/1711.10561)
- Murali et al., *PINNs for Blood Flow Simulation*, 2022.
- Open-source libraries: [DeepXDE](https://github.com/lululxvi/deepxde), [Modulus](https://developer.nvidia.com/modulus)

---

## 🙌 Acknowledgments

This work is part of an ongoing research effort at the University of Delhi in the area of **Scientific Machine Learning and Biomedical AI**.

For questions or collaborations, feel free to reach out:

**Dr. Sangeeta Yadav**  
Assistant Professor, Dept. of Computer Science  
University of Delhi  
📧 [sangeeta@fot.du.ac.in]  
🔗 [GitHub Link]

---

