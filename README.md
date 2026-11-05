# Physics-Informed Neural Networks for Stiff Guitar String Vibrations

<img src="assets/ams_group_tui.png" alt="AMS Group – TU Ilmenau" width="100">

> **[WS26/27] Research Seminar / Forschungsseminar (MT und MIW)**  
> Institut für Medientechnik · AMS Group · Technische Universität Ilmenau

| | |
|---|---|
| **Supervisor** | Renato Fera P. · [![LinkedIn](https://img.shields.io/badge/LinkedIn-renato--profeta-0a66c2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/renato-profeta/) |
| **Fachgebietsleiter** | Prof. Dr.-Ing. Gerald Schuller |
| **Repository** | [github.com/TUIlmenauAMS/fs-ws2627-pinn-guitar](https://github.com/TUIlmenauAMS/fs-ws2627-pinn-guitar) |

---

## Context

Guitar strings exhibit dispersive, high-frequency vibration behaviour due to bending stiffness, making accurate physical modelling challenging. Classical numerical methods such as Finite-Difference Time-Domain (FDTD) are well-established for this task but suffer from numerical dispersion at high frequencies. Physics-Informed Neural Networks (PINNs) have recently emerged as a promising alternative, embedding the governing PDE directly into the neural network loss function.

## Objective

Review the state of the art on PINNs for acoustic and electric guitar string modelling, and compare FDTD and PINN simulations of a single plucked stiff string against an analytical modal reference solution.

---

## Tasks

1. **Literature review** — survey physical modelling of stiff strings, foundational PINN methods, and recent applications of PINNs in musical acoustics.
2. **Analytical reference** — derive and implement the analytical modal solution for a plucked stiff string.
3. **FDTD simulation** — implement an FDTD simulation for the same stiff string model and initial conditions.
4. **PINN implementation** — implement a PINN for the same problem, incorporating the stiff string PDE along with initial and boundary conditions into the loss function, following [[1]](#references).
5. **Comparison** — select appropriate metrics, compare all three approaches quantitatively, and discuss accuracy, computational cost, and suitability for sound synthesis.

---

## Notebooks

| # | Title | Description | Links |
|---|-------|-------------|-------|
| 00 | **Project Overview** | The stiff guitar string problem, project structure, course deadlines, and an overview of the tutorial notebook series. | [![Read](https://img.shields.io/badge/Read-HTML-a78bfa?style=flat)](https://TUIlmenauAMS.github.io/fs-ws2627-pinn-guitar/notebooks/NB00_project_overview.html) |
| 01 | **PDE Basics** | What is a PDE? Boundary and initial conditions, the 1D heat equation as a worked example, and how to read and visualise PDE solutions in Python. | [![GitHub](https://img.shields.io/badge/GitHub-notebook-34d399?style=flat&logo=github&logoColor=white)](https://github.com/TUIlmenauAMS/fs-ws2627-pinn-guitar/blob/main/notebooks/NB01_pde_basics.ipynb) [![Colab](https://img.shields.io/badge/Colab-open-fb923c?style=flat&logo=googlecolab&logoColor=white)](https://colab.research.google.com/github/TUIlmenauAMS/fs-ws2627-pinn-guitar/blob/main/notebooks/NB01_pde_basics.ipynb) [![nbview](https://img.shields.io/badge/nbview-render-2dd4bf?style=flat)](https://nbview.org/github/TUIlmenauAMS/fs-ws2627-pinn-guitar/blob/main/notebooks/NB01_pde_basics.ipynb) |

---

## Quick Start

This project uses [uv](https://docs.astral.sh/uv/) for dependency management.

**Install uv:**

```bash
# Linux / WSL
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
winget install --id=astral-sh.uv -e
```

**Clone and set up the environment:**

```bash
git clone https://github.com/TUIlmenauAMS/fs-ws2627-pinn-guitar
cd fs-ws2627-pinn-guitar
uv sync        # creates .venv and installs all dependencies
```

Then open the repository in VS Code and select the `.venv` interpreter as the Jupyter kernel.

---

## References

[1] Luan, X., Okada, K., Tabata, R., & Scavone, G. (2026). *Towards Physics-Informed Neural Networks for Stiff Guitar String Vibrations.* https://arxiv.org/abs/2609.21795

[2] Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). *Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations.* Journal of Computational Physics, 378, 686–707.

[3] Bilbao, S. (2009). *Numerical Sound Synthesis: Finite Difference Schemes and Simulation in Musical Acoustics.* Wiley.

[4] Välimäki, V., Pakarinen, J., Erkut, C., & Karjalainen, M. (2006). *Discrete-time modelling of musical instruments.* Reports on Progress in Physics, 69(1), 1–78.

[5] Luan, X., & Scavone, G. (2025). *Physics-Informed Deep Learning for Nonlinear Friction Model of Bow-String Interaction.* DAFx 2025. https://arxiv.org/abs/2505.18950

---

<sub>Institut für Medientechnik · AMS Group · Technische Universität Ilmenau</sub>
