# AI-Powered Stratified Clinical Trial Simulation and Stroke Risk Modeling

This project simulates a randomized clinical trial (RCT) using real-world stroke prediction data. It applies statistical planning principles (SAP simulation), performs stratified randomization, builds SDTM/ADaM-like datasets, runs QC checks, and visualizes outcomes using Python.

---

## 🎯 Goal

To emulate a clinical trial analysis pipeline with:
- Eligibility criteria (Inclusion/Exclusion)
- Stratified randomization
- Endpoint definition
- CDISC-like output (SDTM, ADaM)
- Quality control and statistical reporting

---

## 👥 Intended Audience

- Clinical Biostatisticians
- Contract Research Organizations (CROs)
- Regulatory Science Analysts
- Health Data Scientists & AI/ML Engineers
- Pharma/MedTech Hiring Managers

---

## 📊 Strategy & Pipeline

1. Load dataset from Google Drive (Kaggle stroke dataset)
2. Apply inclusion: Age >= 18, BMI not null
3. Define covariates: age, hypertension, heart disease, smoking status
4. Simulate stratified randomization (gender × hypertension)
5. Define endpoints: primary (stroke), secondary (age group)
6. Create SDTM-like (DM, VS, MH) and ADaM-style datasets
7. QC checks: missing, outliers, duplicates
8. Visualize risk score and outcomes
9. Export CSVs and Markdown SAP

---

## ❓ Problem Statement

How can data scientists simulate trial-quality randomized cohorts using public health data, while producing audit-ready statistical outputs without SAS?

---

## 📂 Dataset

- **Name**: Stroke Prediction Dataset
- **Source**: [Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- **Fields**: Age, gender, BMI, hypertension, heart disease, avg_glucose_level, stroke
- **Size**: ~5,000 samples

---

## 🤖 Machine Learning Prediction & Outcomes

**Risk Score Formula**:
```
risk_score = (0.02 * age) + 1 * hypertension + 1.5 * heart_disease + 0.01 * avg_glucose_level
```

**Groups**: Treatment vs Control  
**Balance**: Stratified 50/50 split across gender × hypertension strata  
**Visual Insights**: Boxplots and countplots of outcome distributions

---

## 📁 Exported Outputs

- `adam_dm.csv` → Analysis-ready dataset
- `qc_log.csv` → QC findings (missing/outliers/duplicates)
- `analysis_plan.md` → Simulated SAP

---

## 🧠 AGI Enhancement Potential

This workflow mimics what an AGI system could automate:
- Cohort definition
- Randomization logic
- Regulatory-style data derivation
- QC + SAP generation
- Dashboard-ready outputs for trial feasibility evaluation

---

## 🛠 Tools Used

- Python
- Pandas
- Scikit-learn
- Seaborn
- Matplotlib
- Google Colab

---

## 📚 References

- CDISC ADaM/SDTM Guidelines
- GCP ICH E9 Statistical Principles
- Kaggle Stroke Dataset (2022)

---

> Developed by Ronald Kalani  
> [LinkedIn](https://www.linkedin.com/in/ronald-kalani-1a465533/) | [GitHub](https://github.com/ronaldkalani)

