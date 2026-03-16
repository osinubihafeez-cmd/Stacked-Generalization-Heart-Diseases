# Stacked Generalization for Heart Disease Prediction

### Author
**Osinubi Bamidele Hafeez**  
DataraFlow Internship Programme  
Email: osinubihafeez@gmail.com  
ORCID: [0009-0008-5274-0314](https://orcid.org/0009-0008-5274-0314)  
Supervisor: Winner Emeto (DataraFlow)

---

## Overview

This repository contains the code, results, and figures for the research project:

> **Stacked Generalization for Heart Disease Prediction: UCI Cleveland Dataset — Performance and SHAP Insights**

The project implements a **stacked ensemble** framework using four base learners (Logistic Regression, Random Forest, XGBoost, and SVM) with a Logistic Regression meta-learner. It includes hyperparameter tuning, 5-fold stratified cross-validation, statistical significance testing, and SHAP interpretability analysis on the best-performing model.

---

## How to Reproduce

### 1. Clone the repository
\`\`\`bash
git clone https://github.com/osinubihafeez-cmd/stacked-generalization-heart-diseases.git
cd stacked-generalization-heart-diseases
\`\`\`

### 2. Install dependencies
\`\`\`bash
pip install -r requirements.txt
\`\`\`


### 3. Run the notebook
\`\`\`bash
jupyter notebook notebooks/MY_FINAL_HEART_PREDICTION_ANALYSIS_CODE.ipynb
\`\`\`


---
### Dataset
Name: UCI Cleveland Heart Disease Dataset
Samples: 303
Features: 13 clinical features + binary target (0 = No disease, 1 = Disease)
Source: https://archive.ics.uci.edu/dataset/45/heart+disease

---

---

## Results Summary
| Model               | AUC-ROC | Accuracy |
|---------------------|---------|----------|
| Logistic Regression | 0.9378  | 86.81%   |
| SVM                 | 0.9325  | 84.62%   |
| Stacking Ensemble   | 0.9320  | 85.71%   |
| Random Forest       | 0.9077  | 79.12%   |
| XGBoost             | 0.8975  | 76.92%   |

---

### Key Findings 
**Hypothesis H1 :**  Stacking advantage ≥ 4 percentage points: Not supported.
The stacking ensemble achieved AUC-ROC = 0.9320, marginally below Logistic
Regression (0.9378, Δ = −0.0058). This is consistent with prior literature on the
UCI Cleveland dataset where stacking gains are negligible when analysis is confined
to tabular clinical features alone, likely due to the dataset's relatively linear
decision boundary at this sample size (N = 303).
**Hypothesis H2 :**  ECG-derived features dominate SHAP rankings: Not supported.
The top four SHAP features were all structured categorical clinical variables:
asymptomatic chest pain (cp_3, mean |SHAP| = 0.6962), reversible thalassemia
defect (thal_3 = 0.5866), male sex (sex_1 = 0.5149), and one major vessel
coloured by fluoroscopy (ca_1 = 0.4845). The proxy ECG variable restecg_2
ranked ninth (0.1897).


**Top 5 features by mean |SHAP| value (Logistic Regression):**

cp_3 – Asymptomatic chest pain (0.6962)
thal_3 – Reversible thalassemia defect (0.5866)
sex_1 – Male sex (0.5149)
ca_1 – One major vessel colored by fluoroscopy (0.4845)
slope_1 – Flat ST segment (0.3036)

