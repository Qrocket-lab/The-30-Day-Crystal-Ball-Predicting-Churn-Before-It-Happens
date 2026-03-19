# Oxygen Leak Mission: Telco Churn Intelligence

Pillar: Life Support (Operations and Finance)  
Status: Analysis and Modeling Complete  
Power BI Dashboard: In Development

## Mission Objective
This project is built to plug revenue leaks before they become visible in monthly reporting.  
Using 7,043 customer records with a 26.5% churn rate, the model assigns churn probability and converts those probabilities into operational risk tiers that a retention team can act on immediately.

## Business Impact
- Revenue leak prevention: churn risk is surfaced early enough to intervene before cancellation.
- Operational efficiency: outreach can be targeted to the highest-value risk pool instead of broad, low-yield campaigns.
- Focus on the top 10% at-risk customers: in this dataset, that is about 704 customers (0.10 x 7,043), a practical daily work queue for a retention team.
- Better campaign economics: threshold optimization reduces wasted offers on low-probability churners while preserving recall on true churn cases.

## Technical Scope
- Data ingestion and preprocessing pipeline for 7,043 telecom customers.
- Numeric correction of `Total Charges` with null remediation logic tied to early-tenure customers.
- Class imbalance handling using `compute_class_weight` for the 26.5% churn minority class.
- Model comparison with Gradient Boosting selected as best performer.
- Feature importance analysis, with contract type and tenure highlighted as core churn drivers.
- Probability-based risk segmentation into five intervention tiers.
- Precision-Recall threshold optimization to tune retention action policy beyond default 0.50.
- Deployment-ready scoring function for new customer cohorts.

## Workflow Map
1. Step 1-2: Data ingestion and preprocessing.
2. Step 4: Class imbalance treatment.
3. Step 5-6: Gradient Boosting training and feature importance.
4. Step 7: Risk segmentation (Critical, High, Elevated, Moderate, Low equivalent tiering).
5. Step 8: Precision-Recall threshold optimization.

## Repository Structure
```
.
|-- main_telco.ipynb
|-- Dataset/
|   `-- telco.csv
`-- README.md
```

## Run Instructions
1. Install dependencies: pandas, numpy, scikit-learn, matplotlib, seaborn.
2. Open and run all cells in `main_telco.ipynb`.
3. Review generated artifacts:
   - `oxygen_leak_eda.png`
   - `oxygen_leak_feature_importance.png`
   - `oxygen_leak_risk_segments.png`
   - `oxygen_leak_precision_recall.png`
   - `oxygen_leak_mission_summary.png`

## Current Delivery Status
- Modeling and risk logic are complete.
- Dashboard layer is pending.
- Power BI Dashboard is In Development.
