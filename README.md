# Data Science & Computational Physics Portfolio

![Python](https://img.shields.io/badge/Python-3.12%2B-blue)
![License](https://img.shields.io/badge/License-MIT-purple)
![Status](https://img.shields.io/badge/Status-Active-success)

**A collection of computational pipelines bridging theoretical astrophysics, atmospheric science, and statistical inference.**

This repository documents a series of analysis projects focused on modeling physical systems from first principles. The work utilizes robust statistical methods—including MCMC, Maximum Likelihood estimation, and Monte Carlo simulations—to extract physical parameters from noisy observational data.

---

## 📂 Project Index

| Domain | Project Title | Key Techniques |
| :--- | :--- | :--- |
| **Astrophysics** | [**Galaxy Cluster Dark Matter Analysis**](astrophysics/) | Virial Theorem, Sigma-Clipping, GMM, Cosmology |
| **Atmospheric Science** | [**Exoplanet Atmosphere Reconstruction**](atmospheric_science/) | Hydrostatic Equilibrium, Radiative Transfer, Numerical Integration |
| **Comp. Modeling** | [**Monte Carlo & Statistical Inference**](computational_modeling/) | Stochastic Simulation, Hypothesis Testing, $\chi^2$ Minimization |

---

## 🔭 Featured Projects

### 1. Galaxy Cluster Dark Matter Analysis (ACO 2670)
**[View Project Directory](astrophysics/)** | **[Read Technical Report](astrophysics/aco_2670_dark_matter_analysis_report.pdf)**

A computational pipeline designed to estimate the dynamical mass of the galaxy cluster ACO 2670. By analyzing the redshift-space distortions and projected separation of 98 member galaxies, this project isolates the cluster from the background field and applies the Virial Theorem to quantify its dark matter content.

* **Core Physics:** Virialization, Dark Matter Halo Modeling, Cosmological Redshift.
* **Key Result:** Calculated a Mass-to-Light ratio of **$291 \pm 60 M_{\odot}/L_{\odot}$**, providing kinematic evidence that >95% of the cluster's mass is non-luminous.

<p align="center">
  <img src="astrophysics/images/gmm_redshift_distribution.png" width="60%" />
</p>
<p align="center"><em>Redshift distribution analysis. The data favors a single Gaussian profile (red) over a mixture model, indicating the cluster is likely virialized and not currently undergoing a major merger.</em></p>

---

### 2. Exoplanet Atmospheric Analysis
**[View Project Directory](atmospheric_science/)**

A numerical reconstruction of the thermodynamic profile of a high-gravity ($g = 20 \, \text{m/s}^2$) exoplanet. Using telemetry from descent probes, this pipeline solves the hydrostatic equilibrium and radiative transfer equations to derive the atmosphere's stability, optical depth, and hydrological cycle.

* **Core Physics:** Thermodynamics, Fluid Dynamics, Radiative Transfer.
* **Key Result:** Identified a stable troposphere with a global precipitation rate of **$0.086 \text{ mm/hr}$**, recovering missing sensor data through physical law inversion.

<p align="center">
  <img src="atmospheric_science/images/temperature_vs_pressure.png" width="60%" />
</p>
<p align="center"><em>Reconstructed temperature profiles validating hydrostatic equilibrium across multiple probes.</em></p>

---

### 3. Monte Carlo Simulation & Statistical Inference
**[View Project Directory](computational_modeling/)**

An exploration of stochastic processes and non-linear parameter estimation. This project builds Monte Carlo simulations from scratch to verify fundamental statistical theorems (CLT) and models particle transport through absorbing media, demonstrating how random walks converge to deterministic physical laws.

* **Core Physics:** Diffusion, Particle Physics (Attenuation), Error Propagation.
* **Key Result:** Empirically verified the Beer-Lambert law via discrete particle transport and validated variance scaling laws ($1/\sqrt{N}$).

<p align="center">
  <img src="computational_modeling/images/particle_attenuation.png" width="60%" />
</p>
<p align="center"><em>Simulating radiative transfer processes via inverse transform sampling.</em></p>

---

## 🛠️ Technical Stack

The analyses in this portfolio are built using a standard scientific Python stack, emphasizing vectorization and reproducibility.

* **Language:** Python 3.12+
* **Data Structures:** `Pandas`, `NumPy`
* **Scientific Computing:** `SciPy` (Optimization, Integration, Stats), `Astropy` (Cosmology, Units)
* **Visualization:** `Matplotlib`, `Seaborn`
* **Environment:** Jupyter Notebooks

---

## 🚀 Getting Started

To reproduce the analysis for any project in this portfolio:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/JacksonFergusonDev/data-science-portfolio.git
    cd data-science-portfolio
    ```

2.  **Environment Setup:**

    **Modern (Recommended):**
    This project is managed with [uv](https://github.com/astral-sh/uv). This will automatically handle Python versioning and virtual environments.
    ```bash
    # Sync dependencies and build the environment
    uv sync
    ```

    **Legacy (pip):**
    If you do not have `uv` installed, you can use standard pip:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Launch the Lab:**
    ```bash
    # Launch Jupyter Lab within the managed environment
    uv run jupyter lab
    ```

---

### Author

**Jackson Ferguson**

*Astrophysics Undergraduate, University of Victoria*

[LinkedIn](https://www.linkedin.com/in/jackson--ferguson/) | [GitHub](https://github.com/JacksonFergusonDev)