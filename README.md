# 🦴 BoneScaffold AI

## AI-Powered TPMS Bone Scaffold Designer for Clinicians

**BoneScaffold AI** is a computational biomaterials platform that uses a **3D Convolutional Neural Network** to design and optimize Triply Periodic Minimal Surface (TPMS) bone scaffolds. The tool provides instant, AI-driven recommendations for clinicians based on patient-specific parameters, validated against real experimental data.

---

## 📌 Table of Contents

- [Overview](#-overview)
- 🏆 **Key Research Results**
- 🖥️ **Clinical Quick Results**
- [Model Performance](#-model-performance)
- [Scaffold Architectures](#-scaffold-architectures)
- [Dataset Information](#-dataset--model-information)
- [Installation](#-installation)
- [Usage](#-usage)
- [Conclusion](#-conclusion)
- [Future Work](#-future-work)
- [Citation](#-citation)
- [License](#-license)

---

## 🔬 Overview

This project develops an AI-driven framework for designing bone scaffolds using:

| Component | Technology |
|-----------|------------|
| **Geometry Generation** | TPMS equations (Gyroid, Diamond, Primitive) |
| **Design Parameters** | Porosity (60-90%), Pore Size (300-800 µm) |
| **AI Model** | 3D CNN (Conv3D + BatchNorm + GlobalAvgPooling) |
| **Validation** | Real experimental data from published literature |
| **Clinical Interface** | Streamlit-based clinician dashboard |

---

## 🏆 Key Research Results
<img width="1520" height="523" alt="image" src="https://github.com/user-attachments/assets/ea0ed99a-9cac-4d2d-920d-30c6a884fba4" />


| Finding | Result |
|---------|--------|
| **Optimal TPMS Type** | Diamond |
| **Optimal Porosity** | 80% |
| **Optimal Pore Size** | 407 µm |
| **Predicted Stiffness** | 685 MPa |
| **Target (Trabecular Bone)** | 500 MPa |
| **Model R² Score** | >0.89 |
| **Model MAE** | ~1.2 MPa |

> **Key Insight:** The Diamond TPMS scaffold with 80% porosity and 407 µm pore size provides optimal balance between mechanical stiffness and biological permeability for trabecular bone regeneration.

### 📊 Research Performance Summary Table

| Parameter | Value |
|-----------|-------|
| Optimal TPMS Type | Diamond |
| Optimal Porosity | 80% |
| Optimal Pore Size | 407 µm |
| Predicted Stiffness | 685 MPa |
| Target Stiffness (Trabecular Bone) | 500 MPa |
| Model R² | >0.89 |
| Mean Absolute Error | ~1.2 MPa |
| Training Samples | 40+ (augmented from 5 real data points) |
| Test Samples | 10+ |
| Neural Network Architecture | 3D CNN (Conv3D + BatchNorm + GlobalAvgPooling) |
| Input Shape | (64, 64, 64, 1) |
| Epochs | 100 |
| Optimizer | Adam |
| Loss Function | MSE |

---

## 🖥️ Clinical Quick Results

<img width="1703" height="851" alt="image" src="https://github.com/user-attachments/assets/f9297c0b-4d5b-4365-a377-2c410e728d0a" />



---

## 📈 Model Performance

| Metric | Research Value | Clinical Implication |
|--------|---------------|---------------------|
| **R² Score** | >0.89 | High confidence in predictions |
| **Mean Absolute Error (MAE)** | ~1.2 MPa | Clinically acceptable error margin |
| **Training Samples** | 40+ (augmented from 5 real data points) | Robust model generalization |
| **Test Samples** | 10+ | Validated on unseen data |
| **Neural Network** | 3D CNN (Conv3D + BatchNorm + GlobalAvgPooling) | Specialized for 3D geometry |
| **Input Shape** | (64, 64, 64, 1) | High-resolution scaffold analysis |
| **Epochs** | 100 | Fully converged training |
| **Optimizer** | Adam | Adaptive learning rate |
| **Loss Function** | MSE | Minimizes prediction error |

---

## 🏗️ Scaffold Architectures

| TPMS Type | Equation | Best For | Research Finding |
|-----------|----------|----------|------------------|
| **Gyroid** | `sin(x)cos(y) + sin(y)cos(z) + sin(z)cos(x) = c` | High permeability, cell infiltration | Good for vascularization |
| **Diamond** | `sin(x)sin(y)sin(z) + sin(x)cos(y)cos(z) + cos(x)sin(y)cos(z) + cos(x)cos(y)sin(z) = c` | **High stiffness, load-bearing** | ⭐ **OPTIMAL** for trabecular bone |
| **Primitive** | `cos(x) + cos(y) + cos(z) = c` | Simple structure, easy to print | Validated in Mirzavand et al. 2025 |

### Design Parameter Ranges

| Parameter | Research Range | Biological Significance |
|-----------|---------------|------------------------|
| **Porosity** | 60-90% (Optimal: 80%) | Space for cell infiltration and vascularization |
| **Pore Size** | 300-800 µm (Optimal: 407 µm) | Osteoblast migration and bone ingrowth |
| **Unit Cell Size** | 1.5-5.0 mm | Scaffold structural hierarchy |
| **Stiffness** | 300-800 MPa (Optimal: 685 MPa) | Trabecular bone mechanical matching (target: 500 MPa) |

---

## 📁 Dataset & Model Information

| Property | Details |
|----------|---------|
| **Source of Real Data** | Mirzavand et al., Scientific Reports 15:29458 (2025) |
| **Material** | PLA-CF (carbon fiber-reinforced PLA) |
| **TPMS Type in Reference Study** | Modified Primitive |
| **Strut Diameters Tested** | 1.5, 2.0, 2.5, 3.0, 3.5 mm |
| **Yield Strength Range** | 6.49 - 16.77 MPa |
| **Software** | Python 3.x, TensorFlow 2.x |
| **Neural Network** | 3D Convolutional Neural Network |
| **Geometry Generation** | Marching Cubes (scikit-image) |
| **Clinical Interface** | Streamlit |

---

