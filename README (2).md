# Clinical Healthcare Analytics: Early Cardio-Metabolic Disease Risk Prediction (UN SDG 3)
**Author:** Naveen Kakarla | **Email:** kakarlanaveen19@gmail.com  
**Masterclass:** BharatCares AI & Data Analytics Final Project  
**Mentors:** Himanshu Souda & Kartik Hooda  

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3+-orange.svg)](https://scikit-learn.org/)
[![UN SDG](https://img.shields.io/badge/UN%20SDG-Goal%203%20Good%20Health-emerald.svg)](https://sdgs.un.org/goals/goal3)

---

## 📌 Project Overview
Early detection of chronic cardiovascular and metabolic diseases is critical for preventative medical care. This project implements a complete, end-to-end Machine Learning pipeline to predict patient cardio-metabolic risk based on non-invasive vitals (Blood Pressure, Glucose, Cholesterol, BMI, and Lifestyle habits).

## 🚀 Key Highlights
- **Exploratory Data Analysis (EDA):** Complete biomarker distributions, box plots, and correlation heatmaps.
- **Class Balancing & Standardization:** Scaled continuous clinical vitals using `StandardScaler`.
- **Ensemble ML Comparison:** Evaluated Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting.
- **Winning Performance:** **91.47% Accuracy**, **91.04% Recall**, and **0.9612 ROC-AUC**.

## 📊 Evaluation Summary
| Classifier | Accuracy | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|
| **Gradient Boosting** | **91.5%** | **91.0%** | **90.4%** | **0.961** |
| Random Forest | 89.9% | 88.1% | 88.1% | 0.949 |
| Logistic Regression | 84.0% | 86.6% | 84.7% | 0.912 |

## 📁 Repository Structure
```
├── clinical_cardio_risk_data.csv     # Clean clinical patient dataset
├── clinical_disease_prediction.ipynb  # Executable Jupyter Notebook
├── Project_Report.md                 # Formal Masterclass Project Report
└── README.md                         # Repository Documentation
```

## 🏃 Quick Start Guide
```bash
# 1. Clone repository
git clone https://github.com/your-/cardio-health-risk-ml.git
cd cardio-health-risk-ml

# 2. Install requirements
pip install pandas numpy scikit-learn matplotlib seaborn

# 3. Launch Jupyter
jupyter notebook clinical_disease_prediction.ipynb
```
