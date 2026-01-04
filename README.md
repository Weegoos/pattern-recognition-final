# Intelligent Waste Sorting Expert System (Pattern Recognition Project – Part 2)

This repository contains the technical implementation for **Pattern Recognition – Project Part 2** titled **“Intelligent Waste Sorting Expert System”** for group **WS‑PR2**.

The goal is to train and evaluate deep learning models on the **TrashNet** dataset and to answer **five publication‑style research questions (RQ1–RQ5)** using a combination of CNNs, imbalance handling, data augmentation, architecture comparison, and a simple rule‑based expert system.

---

## 1. Group and Roles

- **Student 1 – Technical Lead:** Ashim Batyr  
  - Implements the complete technical pipeline, runs all experiments, prepares metrics and tables.  
- **Student 2 – Figures & Slides:** Jorge Adrian Torres  
  - Designs figures (workflow, dataset overview, network architectures, performance plots) and prepares presentation slides.
- **Student 3 – Report:** Samuel Josino de Souza  
  - Writes the report in Overleaf, aligns narrative with research questions, experiments, figures, and tables.

This repository corresponds to the **technical backbone (Part 2)** required by the course instructions.

---

## 2. Project Overview

The project builds an **image‑based waste classification system** that assigns images into six material categories from the **TrashNet** dataset:[file:40]

- `cardboard`, `glass`, `metal`, `paper`, `plastic`, `trash`.

Core components:

- **Base learner:** transfer‑learning models (ResNet18, MobileNetV2, DenseNet121) implemented in PyTorch.[file:40]  
- **Data pipeline:** preprocessing, train/validation split, and optional augmentation.  
- **Imbalance handling:** weighted cross‑entropy for rare classes (especially `trash`).  
- **Architecture trade‑offs:** measurement of accuracy vs. model size and training time.  
- **Hybrid expert system:** a simple rule engine on top of model predictions that converts probabilities into actionable routing decisions.

All experiments are organized per **research question (RQ1–RQ5)**, and each section saves metrics to Excel/NPZ files for later use in figures and tables.

---

## 3. Environment and Requirements

### 3.1. Software Stack

The notebook is designed to run in **Google Colab** with an optional **GPU (recommended)**:[file:39]

- Python 3  
- PyTorch + torchvision  
- scikit‑learn  
- matplotlib, seaborn  
- OpenCV (for possible extensions)

Required packages are installed via:

```python
!pip install -q torch torchvision scikit-learn matplotlib seaborn opencv-python
