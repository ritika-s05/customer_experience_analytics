# customer_experience_analytics
Bank cx analytics

# Bank Customer Experience Analytics

An end-to-end CX analytics pipeline analyzing 10,000 bank customers —
covering KPI reporting, customer segmentation, and churn prediction.
Built to mirror real-world analytics workflows in financial services CX teams.

---

## Business Questions Answered
1. What is the overall health of the customer base — churn, complaints, satisfaction?
2. Which regions have the highest churn and complaint rates?
3. Does satisfaction score actually predict churn?
4. Which customers are at highest risk of leaving?
5. What features most strongly drive a customer to churn?

---

## Key Findings
- **Churn rate: 20.4%** — 1 in 5 customers is leaving
- **Complaint = churn**: Customers who complained churned at 99.5% vs 0.1% for non-complainers
- **Satisfaction score is flat** — churn rate is ~20% across all scores 1–5, proving it alone is not a reliable CX metric
- **Germany churn rate: 32.4%** — exactly 2x France and Spain despite identical satisfaction scores
- **57% of customers fall in High Risk or Critical segments** — majority of base needs retention intervention
- **Critical segment holds highest avg balance ($79,953)** — most valuable customers are most likely to leave
- **Random Forest AUC: 0.859** — model correctly identifies churn risk from behavioral and demographic features

---

## Project Structure
```
customer_experience_analytics/
│
├── data/
│   ├── raw/                  ← original dataset (gitignored)
│   └── processed/            ← cleaned data
│
├── notebooks/
│   ├── 01_eda_and_kpis       ← KPI dashboard, regional analysis, complaint impact
│   ├── 02_segmentation       ← CX risk scoring, 4-tier segmentation
│   └── 03_churn_model        ← Logistic Regression + Random Forest, feature importance
│
├── outputs/
│   ├── charts/               ← all saved visualizations
│   └── cx_dashboard.xlsx     ← Excel dashboard with 5 analysis tabs
│
└── requirements.txt
```

---

## Tech Stack
Python · Pandas · Scikit-learn · Matplotlib · Seaborn · Excel (openpyxl)

---

## Data Source
Kaggle — Bank Customer Churn Dataset (10,000 records, 18 features)
https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn
