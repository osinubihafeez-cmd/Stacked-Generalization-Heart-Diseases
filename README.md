# Stacked Generalization for Heart Disease Prediction
# UCI Cleveland Dataset — Performance and SHAP Insights

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



## Results Summary
| Model               | AUC-ROC | Accuracy |
|---------------------|---------|----------|
| Logistic Regression | 0.9378  | 86.81%   |
| SVM                 | 0.9325  | 84.62%   |
| Stacking Ensemble   | 0.9320  | 85.71%   |
| Random Forest       | 0.9077  | 79.12%   |
| XGBoost             | 0.8975  | 76.92%   |

