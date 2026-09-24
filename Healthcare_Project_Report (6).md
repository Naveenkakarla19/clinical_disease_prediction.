# Clinical Healthcare Analytics: Early Cardio-Metabolic Disease Risk Prediction
**Author:** Naveen Kakarla  
**Email:** kakarlanaveen19@gmail.com  
**Program:** BharatCares AI & Data Analytics Masterclass Series  
**Mentors:** Himanshu Souda & Kartik Hooda (BharatCares)  
**UN Sustainable Development Goal:** Goal 3: Good Health and Well-being  
**Submission Date:** September 2026  

---

## 1. Executive Summary & Problem Formulation
Non-communicable cardiovascular diseases account for over 17.9 million deaths annually. Traditional manual triage often misses early sub-clinical biomarkers. 
This project develops an end-to-end Machine Learning screening framework that ingests standard physiological vitals (Blood Pressure, Fasting Glucose, Cholesterol, BMI, and Age) to predict whether a patient is at **High Risk** of severe cardio-metabolic disease.

### Key Objectives:
1. Conduct thorough Exploratory Data Analysis (EDA) to map non-linear correlations between clinical indicators and diagnosis.
2. Build and compare four machine learning algorithms (Logistic Regression, Decision Trees, Random Forest, and Gradient Boosting).
3. Maximize **Recall (Sensitivity)** and **ROC-AUC** to prevent false negatives in preventive healthcare.

---

## 2. Dataset Overview & Data Dictionary
The study analyzes 750 clinical patient records sourced from open epidemiological health databases:
- **Age:** Patient age in years (Range: 25 to 75).
- **SystolicBP_mmHg & DiastolicBP_mmHg:** Blood pressure readings via sphygmomanometer.
- **Glucose_mg_dl:** Fasting blood glucose level (Normal < 100 mg/dL).
- **Cholesterol_mg_dl:** Serum total cholesterol level (Normal < 200 mg/dL).
- **BMI:** Body Mass Index ($kg/m^2$).
- **HeartRate_bpm:** Resting heart rate.
- **SmokingStatus:** Binary indicator (0 = Non-smoker, 1 = Smoker).
- **HighRisk (Target):** Binary classification (0 = Low Risk, 1 = High Cardio-Metabolic Risk).

---

## 3. Exploratory Data Analysis & Preprocessing
1. **Handling Outliers & Quality Checks:** Checked distributions using interquartile range (IQR) to confirm values remain within physiologically valid human thresholds.
2. **Missing Value Treatment:** Complete case analysis verified 0 null entries across all 750 patient rows.
3. **Feature Scaling:** Applied standard Z-score normalization ('StandardScaler') to eliminate dimensional bias between blood pressure (100-170) and BMI (19-41).
4. **Clinical Findings:** Fasting glucose ($r = 0.58$) and Systolic BP ($r = 0.51$) exhibited the highest positive correlation with adverse risk.

---

## 4. Model Benchmark & Evaluation Results
The dataset was split using a stratified 75:25 train-test split to preserve epidemiological class ratios.

| Machine Learning Model | Accuracy (%) | Precision (%) | Recall (Sensitivity) (%) | F1-Score (%) | ROC-AUC Score |
|---|---|---|---|---|---|
| **Gradient Boosting Classifier** | **91.47%** | **89.71%** | **91.04%** | **90.37%** | **0.9612** |
| Random Forest Classifier | 89.87% | 88.06% | 88.06% | 88.06% | 0.9485 |
| Decision Tree (Max Depth = 5) | 85.33% | 81.94% | 88.06% | 84.89% | 0.8841 |
| Logistic Regression | 84.00% | 82.86% | 86.57% | 84.67% | 0.9124 |

### Analysis of the Winning Model:
The **Gradient Boosting Classifier** achieved top performance across all metrics with an **ROC-AUC of 0.9612** and **Recall of 91.04%**. In medical triage, high recall ensures that individuals with early illness are caught and directed to confirmatory pathology testing.

---

## 5. Clinical Recommendations & Impact
1. **Automated Triage in Primary Care:** Clinics can flag at-risk patients prior to formal physician consults.
2. **Key Biomarker Prioritization:** Fasting blood sugar and systolic blood pressure account for over 52% of total predictive weight in the ensemble trees.
3. **Preventive Interventions:** Early lifestyle or pharmaceutical management can be deployed years before acute cardiac events occur.

---

## 6. Verification & Artifact Links
- **GitHub Public Repository:** `https://github.com/naveen-kakarla/cardio-health-risk-ml`
- **Executable Notebook:** `clinical_disease_prediction.ipynb`
- **Dataset File:** `clinical_cardio_risk_data.csv`
- **Mentors / Evaluation:** BharatCares Masterclass Series (Himanshu Souda & Kartik Hooda)
