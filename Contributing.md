# Contributing to Harmonic Resonance Forest (HRF)

Thank you for your interest in contributing to **Harmonic Resonance Forest (HRF)**. This project is a research-driven, physics-informed machine learning framework focused on resonance-based classification, spectral learning, and robust time-series analysis.

We are participating in **GSSoC 2026**, and this document outlines the proper process for contributing to this repository.

Please read this document carefully before contributing.

---

# Table of Contents

1. Project Overview
2. Repository Structure
3. Branch Policy (Important)
4. Ways to Contribute
5. Getting Started
6. Development Setup
7. Contribution Workflow
8. Coding Guidelines
9. Documentation Guidelines
10. Research Contributions
11. Issue Guidelines
12. Pull Request Rules
13. Good First Issues (GSSoC)
14. Code of Conduct
15. Final Notes

---

# Project Overview

Harmonic Resonance Forest (HRF) is a physics-informed machine learning framework that models classification as a **resonance and wave interference problem** rather than a traditional decision boundary problem.

The project combines:

* Wave Physics
* Signal Processing
* Machine Learning
* Spectral Analysis
* Statistical Validation
* GPU Computing

The core HRF engine is located in the **HRF-Engine/** directory, while application-specific implementations and experiments are located in **HRF Codes/** and **1/** directories.

This repository is structured like a **research lab + engineering project**, and contributors are encouraged to contribute not only code, but also documentation, experiments, benchmarks, and research analysis.

---

# Repository Structure

```
.
├── .github/workflows/        # CI/CD workflows
├── 1/                        # Early prototypes, notebooks, and benchmarks
├── docs/                     # Technical documentation and monograph
├── HRF Codes/                # EEG, conference, and applied HRF implementations
├── HRF-Engine/               # Core HRF engine (main algorithm)
├── Research Paper/           # Research paper and whitepaper files
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
└── .gitignore
```

### Important Directories

| Folder         | Description                                 |
| -------------- | ------------------------------------------- |
| HRF-Engine     | Core algorithm implementations              |
| HRF Codes      | Application-specific HRF implementations    |
| docs           | Technical documentation                     |
| Research Paper | Paper and whitepaper                        |
| 1              | Experimental notebooks and early benchmarks |

---

# Branch Policy (Very Important)

This repository uses a **protected main branch** workflow to maintain research stability.

| Branch     | Purpose                                    |
| ---------- | ------------------------------------------ |
| main       | Stable research version (Protected)        |
| gssoc-2026 | Development branch for GSSoC contributions |

## Rules

* Do NOT open Pull Requests to `main`
* All contributions must be made to `gssoc-2026`
* Pull Requests to `main` will be rejected
* Maintainer will periodically merge stable contributions from `gssoc-2026` into `main`

This ensures the research codebase remains stable and reproducible.

---

# Ways to Contribute

## Code Contributions

You can contribute by:

* Improving HRF engine
* Implementing multi-class HRF
* Implementing regression HRF
* Optimizing GPU implementation (CuPy / RAPIDS)
* Adding new resonance kernels
* Improving evolutionary optimization
* Adding benchmarking scripts
* Adding dataset loaders

## Documentation Contributions

* Improve README
* Improve Wiki
* Write tutorials
* Add diagrams and visual explanations
* Add mathematical derivations
* Improve code documentation

## Research Contributions

We strongly encourage research-oriented contributions such as:

* Mathematical analysis of HRF kernel
* HRF vs SVM comparison
* HRF vs Random Forest comparison
* HRF vs XGBoost comparison
* Noise robustness experiments
* Phase invariance experiments
* Time-series benchmarking

## Testing Contributions

* Add unit tests
* Add benchmark tests
* CPU vs GPU performance comparison
* Testing on new datasets

---

# Getting Started

## Step 1 — Fork the Repository

## Step 2 — Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/Harmonic-Resonance-Forest.git
cd Harmonic-Resonance-Forest
```

## Step 3 — Switch to GSSoC Branch

```bash
git checkout gssoc-2026
```

## Step 4 — Create Feature Branch

```bash
git checkout -b feature/your-feature-name
```

---

# Development Setup

## Requirements

* Python 3.10+
* NumPy
* SciPy
* scikit-learn
* Pandas
* Matplotlib
* CuPy (GPU support)
* RAPIDS cuML (optional for GPU acceleration)

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Contribution Workflow

1. Fork the repository
2. Clone your fork
3. Checkout `gssoc-2026`
4. Create a new feature branch
5. Make your changes
6. Commit your changes
7. Push to your fork
8. Open a Pull Request to **gssoc-2026**

---

# Coding Guidelines

Please follow these coding standards:

* Follow **PEP 8** style
* Use meaningful variable and function names
* Add docstrings to all functions
* Keep code modular
* Avoid hardcoding values
* Comment important logic
* Ensure notebooks are clean and readable

### Example Function

```python
def resonance_kernel(distance, gamma, omega, phase):
    """
    Compute harmonic resonance response using damped oscillator model.
    """
    return np.exp(-gamma * distance**2) * np.cos(omega * distance + phase)
```

---

# Documentation Guidelines

Good documentation should include:

* Clear explanation
* Mathematical intuition
* Equations where necessary
* Example usage
* Diagrams if possible

Documentation can be added in:

```
docs/
README.md
notebooks/
wiki/
```

---

# Research Contributions

Research-style contributions are highly encouraged. Suggested areas:

* Mathematical theory of HRF
* Resonance kernel analysis
* Decision boundary analysis
* Spectral domain interpretation
* Phase invariance proof
* Noise robustness experiments
* Time-series benchmarking

Research contributions should include:

* Problem statement
* Method
* Experiment
* Results
* Conclusion

---

# Issue Guidelines

Before opening an issue:

* Check if the issue already exists
* Use a clear title
* Describe the problem clearly
* Include logs or screenshots if possible

### Example Issue Titles

* "Bug: HRF GPU memory overflow"
* "Feature: Add multi-class HRF"
* "Docs: Add HRF mathematical derivation"

---

# Pull Request Rules

Before submitting a Pull Request:

* Code must run without errors
* Notebook outputs should be cleared
* Documentation must be updated if necessary
* Pull Request must target **gssoc-2026**
* Pull Request must include clear description

### Pull Request Title Format

```
[Feature] Added multi-class HRF
[Fix] Fixed GPU bug
[Docs] Updated README
[Benchmark] Added EEG dataset test
```

Pull Requests that do not follow these guidelines may be closed.

---

# Good First Issues (GSSoC)

### Beginner Level

* Improve documentation
* Add comments to code
* Add example notebooks
* Add visualization plots
* Fix typos and formatting

### Intermediate Level

* Add dataset loaders
* Implement multi-class HRF
* Implement regression HRF
* Add benchmark comparisons

### Advanced Level

* GPU optimization
* New resonance kernel implementation
* Mathematical analysis of HRF
* Large dataset benchmarking

---

# Code of Conduct

All contributors are expected to be respectful, collaborative, and professional.

This project aims to build a serious open-source and research community around **physics-informed machine learning**.

---

# Final Notes

HRF is not just a coding project. Contributors are encouraged to think about:

* Physics
* Mathematics
* Signal Processing
* Machine Learning Theory

**Build not just code — build understanding.**

---

# Important Summary

| Rule                       | Requirement |
| -------------------------- | ----------- |
| Fork repository            | Required    |
| Work on branch             | gssoc-2026  |
| Pull Request to main       | Not allowed |
| Pull Request to gssoc-2026 | Required    |
| Follow coding guidelines   | Required    |
| Documentation              | Required    |

---

Thank you for contributing to Harmonic Resonance Forest.
