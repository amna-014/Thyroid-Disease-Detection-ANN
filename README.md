# Thyroid Disease Detection using Artificial Neural Networks

> **A Machine Learning approach for the early diagnosis of Hypothyroidism and Hyperthyroidism.**

[![Language](https://img.shields.io/badge/Language-MATLAB-orange)]()
[![Algorithm](https://img.shields.io/badge/Algorithm-Backpropagation-blue)]()
[![Accuracy](https://img.shields.io/badge/Accuracy-100%25-brightgreen)]()

## Project Abstract
Thyroid disorders are prevalent endocrine conditions that are often undiagnosed due to subtle symptoms. This project implements an **Artificial Neural Network (ANN)** to automate the diagnosis process based on clinical indicators.

Using **MATLAB's Neural Network Toolbox**, a Multi-Layer Perceptron (MLP) was trained to classify patient data as either "Normal" or "Thyroid Positive" with high precision.

## Network Architecture
The model utilizes a **Feedforward Backpropagation** architecture with the following topology:

| Layer | Neurons | Activation Function | Description |
| :--- | :---: | :--- | :--- |
| **Input** | 11 | - | Features including TSH levels, Age, Gender, and Medication history. |
| **Hidden** | 10 | **Logsig** (Sigmoid) | Extracts non-linear patterns from clinical data. |
| **Output** | 1 | **Logsig** (Sigmoid) | Binary Classification (0 = Normal, 1 = Disease). |

![Network Diagram](https://github.com/amna-014/Thyroid-Disease-Detection-ANN/blob/main/ann%20diagram.jpg?raw=true)

## Methodology & Training
* **Algorithm:** Scaled Conjugate Gradient (`trainscg`).
* **Loss Function:** Cross-Entropy (penalizes large classification errors).
* **Data Split:** 70% Training, 15% Validation, 15% Testing.
* **Preprocessing:** Binary encoding was applied to categorical variables (Gender, Pregnant, Sick, etc.).

## Performance Metrics
The model achieved **100% classification accuracy** on the test subset, demonstrating effective convergence.

### 1. Confusion Matrix
The matrix shows zero false positives and zero false negatives across all datasets.
![Confusion Matrix](https://github.com/amna-014/Thyroid-Disease-Detection-ANN/blob/main/confusion%20matrix.jpg?raw=true)

### 2. Receiver Operating Characteristic (ROC)
The Area Under the Curve (AUC) is **1.0**, indicating perfect discrimination between the two classes.
![ROC Curve](https://github.com/amna-014/Thyroid-Disease-Detection-ANN/blob/main/roc%20curve.jpg?raw=true)

### 3. Error Analysis
* **Best Validation Performance:** 0.008543 at Epoch 25.
* **Error Histogram:** Errors are tightly clustered around zero, confirming consistent prediction accuracy.

## Repository Contents
* **📄 Project Report:** Detailed documentation of the ANN design and literature review.
* **💻 MATLAB Script (`.m`):** Auto-generated code for training and testing the network.
* **📊 Dataset:** Preprocessed clinical data sample (Excel/CSV).

## Limitations & Future Scope
* **Sample Size:** This project served as a feasibility study with a limited dataset (10 clinical records).
* **Future Work:** The model architecture is ready to be scaled to larger datasets (e.g., the full UCI Machine Learning Repository dataset) to validate robustness on unseen data.

---
*© 2026 Biomedical Engineering Project.*
