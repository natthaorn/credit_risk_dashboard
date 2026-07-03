# 🏦 Corporate Credit Risk Prediction (End-to-End ML Pipeline)

**👉 [View Interactive Tableau Dashboard Here](https://public.tableau.com/app/profile/natthaorn.lapprasitsuk/viz/Credit_Risk_Dashboard_17830446303050/Dashboard1?publish=yes) 👈**

## 📌 Project Overview
This project aims to build a robust Machine Learning model to predict corporate loan defaults (Probability of Default - PD). Leveraging a dataset of 50,000 corporate loans across 10 sectors (simulating conditions from 2015-2024, including rate hike cycles), the goal is to identify high-risk borrowers and provide actionable business insights to minimize Non-Performing Loans (NPL). 

Source Dataset: https://www.kaggle.com/datasets/sergionefedov/credit-risk-dataset-50k-loans-10-sectors

## 🎯 Business Value & Impact
- **Risk Mitigation:** The model achieved a **Recall of 68%**, meaning it can successfully proactively identify and flag 68% of potential defaulters before the loan is approved.
- **Interpretability:** Built using Logistic Regression, ensuring compliance with banking regulations that require models to be fully explainable (unlike black-box models).
- **Strategic Action:** Identified that loans originating with a 'CCC' credit rating and those in the Financials/Energy sectors carry the highest empirical risk of default.

## 🛠️ Tech Stack & Methodology
- **Languages/Tools:** Python (Pandas, Scikit-learn, Seaborn, Matplotlib), Power BI / Tableau (for executive dashboarding).
- **Data Cleaning:** Handled missing values and rigorously eliminated **Data Leakage** variables (e.g., `loss_given_default`, `recovery_rate`, `survival_months`) to simulate a true point-of-origination prediction.
- **Feature Engineering:** 
  - Addressed the Curse of Dimensionality by properly processing high-cardinality date features.
  - One-Hot Encoding for categorical variables.
  - Standardization (`StandardScaler`) for numerical variables to ensure uniform feature scaling.
- **Modeling:** `LogisticRegression` with `class_weight='balanced'` to handle the highly imbalanced dataset (86% Non-Default vs 13.9% Default).

## 📊 Key Results
- **ROC-AUC Score:** 0.81 (Indicating excellent discriminative ability between good and bad loans).
- **Top Default Drivers (Feature Importance):**
  1. `initial_rating_CCC`
  2. `initial_rating_B`
  3. `maturity_months`
  4. `initial_rating_BB`

## 📂 Repository Structure
- `data/`: Contains the raw datasets and exported `feature_importance.csv` for BI tools.
- `1_EDA_and_Data_Cleaning.ipynb`: Jupyter Notebook detailing the EDA, leakage handling, and data profiling.
- `2_Model_Building.ipynb`: (If applicable) Jupyter Notebook containing the ML pipeline and evaluation metrics.
- `Dashboard/`: Contains the Power BI / Tableau dashboard files highlighting executive insights.

---
*This project demonstrates a complete understanding of the credit risk lifecycle, from data operations to strategic business application.*
