# Ensemble Color Quantization via Multi-Space Clustering and Consensus Weighting

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-green.svg)](https://www.python.org/downloads/)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/AmirrezaRaei/Ensemble-Color-Quantization)

This repository contains the implementation of an unsupervised ensemble framework for color quantization. The proposed pipeline bridges the gap between computational efficiency and perceptual accuracy by clustering simultaneously across multiple distinct color spaces (RGB, CIELAB, HSV, and YUV) and applying a consensus-weighting mechanism based strictly on the HaarPSI perceptual metric. 

## 🌟 Key Features
* **Multi-Space Base Palette Generation:** Independent K-Means clustering across RGB, CIELAB, HSV, and YUV spaces to capture diverse structural and perceptual aspects of the original image.
* **Perceptual Consensus Weighting:** Dynamically evaluates base models using the Haar wavelet-based perceptual similarity index (HaarPSI) to allocate weights to geometrically proximate candidate colors.
* **Meta-Clustering:** Extracts the optimal final 16-color palette via weighted clustering in a perceptually uniform space (CIELAB).
* **High Color Fidelity:** Achieves highly competitive $\Delta E_{2000}$ scores while preserving complex structural details against traditional single-space baselines.

## 🚀 Quick Start (GitHub Codespaces)
The easiest way to explore and run the ensemble pipeline is via GitHub Codespaces. Click the **Open in GitHub Codespaces** badge above. The environment will automatically set up the Python workspace and install all necessary dependencies listed in `requirements.txt`.

Alternatively, to run the pipeline locally on your machine:
```bash
git clone [https://github.com/YourUsername/Ensemble-Color-Quantization.git](https://github.com/AmirrezaRaei/Ensemble-Color-Quantization.git)
cd Ensemble-Color-Quantization
pip install -r requirements.txt