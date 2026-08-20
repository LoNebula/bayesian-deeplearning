<p align="center">
  <img src="assets/hero.svg" alt="🧠 Bayesian Deep Learning & Function Approximation Hero Banner" width="100%" />
</p>

<h1 align="center">🧠 Bayesian Deep Learning & Function Approximation</h1>

<p align="center">
  <strong>Uncertainty-Aware Deep Neural Networks & Variational Inference on Complex Manifolds.</strong>
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-code-architecture">Code Architecture</a> •
  <a href="#-system-flow">System Flow</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-license">License</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-2.0+-ee4c2c?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" /> <img src="https://img.shields.io/badge/Python-3.10+-3776ab?style=for-the-badge&logo=python&logoColor=white" alt="Python" /> <img src="https://img.shields.io/badge/Jupyter-Lab-f37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter" /> <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License" />
</p>

---

## 📌 Overview

A deep learning framework focusing on Bayesian neural networks and uncertainty-aware function approximation. By incorporating Monte Carlo Dropout and Variational Inference layers into PyTorch architectures, the model separates aleatoric (data noise) from epistemic (model ignorance) uncertainty, preventing overconfident predictions on out-of-distribution manifolds.

---

## ✨ Features (Key Outcomes & Capabilities)

| Icon | Feature | Outcome & Real Proof |
| :---: | :--- | :--- |
| 📉 | **Deep Manifold Approximation** | Approximates complex non-linear continuous functions with deep neural architectures |
| 🛡️ | **Epistemic Uncertainty** | Measures model uncertainty via MC Dropout stochastic forward sampling |
| 📊 | **Out-of-Distribution Detection** | High variance warning triggers on unobserved input spaces |
| 🐳 | **Jupyter & Docker Stack** | Self-contained GPU environment for reproducible benchmarking |

---

## 🔬 Code Architecture & Implementation

### 🔬 Code Implementation (`src/`)
- **PyTorch BNN Architecture**: Linear layers with active test-time dropout (`p=0.2`) to sample posterior weight trajectories.
- **Monte Carlo Sampling**: Executes $T=100$ stochastic forward passes per test point to compute empirical predictive mean $\hat{\mu}$ and variance $\hat{\sigma}^2$.
- **Function Approximation**: Tested on synthetic non-linear benchmarks (multimodal sinusoid, Rastrigin) and high-dimensional manifolds.

---

## 📊 System Flow

```mermaid
graph TD
  X[🔢 Input x] --> BNN[🧠 PyTorch Neural Network with MC Dropout]
  BNN -->|T Stochastic Passes| Samples[📊 [y_1, y_2, ..., y_T]]
  Samples --> Mean[🎯 Predictive Mean μ]
  Samples --> Var[🛡️ Epistemic Uncertainty ±2σ]

  classDef primary fill:#a855f7,stroke:#9333ea,stroke-width:2px,color:#fff;
  classDef accent fill:#ec4899,stroke:#db2777,stroke-width:2px,color:#fff;
  class BNN primary;
  class Samples,Mean,Var accent;
```

---

## 📁 Project Structure

```bash
bayesian-deeplearning/
├── 📁 assets/                 # High-resolution SVG banners
├── 📁 data/                   # Synthetic benchmark manifolds
├── 📁 src/                    # PyTorch BNN models & training scripts
├── 📄 jupyter-docker.zip      # Docker Compose configuration
└── 📄 README.md               # Documentation
```

---

## 🚀 Quick Start

```bash
# 1. Clone repository
git clone https://github.com/LoNebula/bayesian-deeplearning.git
cd bayesian-deeplearning

# 2. Run training script
python src/train.py
```

---

<p align="center">
  Released under the <a href="LICENSE">MIT License</a>. Crafted with precision by <a href="https://github.com/LoNebula">LoNebula</a>
</p>
