# Ecommercec-AB-Testing

## Overview
This project evaluates whether a redesigned **Buy Now button** improves conversion rate, revenue per user, and contribution profit per user in an e-commerce business.

The analysis uses a simulated dataset to compare the existing design (Control) with the redesigned version (Treatment).

## Business Problem
A higher conversion rate does not always mean higher profitability. The goal is to determine whether the redesigned button improves customer conversions while delivering measurable financial benefits.

## Dataset
The dataset contains **50,000 simulated user records**, split equally between Control and Treatment groups.

Key columns:
- `variant`: Experiment group
- `device`: User's device type
- `acquisition_channel`: Traffic source
- `is_new_user`: Whether the user is new
- `converted`: Whether the user completed a purchase
- `revenue`: Revenue generated per user
- `contribution_profit`: Contribution profit per user
- `experiment_date`: Experiment date

## Methodology
- Data validation and exploratory data analysis (EDA)
- Conversion rate comparison using a two-proportion z-test
- Revenue and profit comparison using Welch's t-test
- 95% confidence intervals and effect size analysis
- Holm correction for multiple hypothesis tests
- Financial impact estimation and business recommendations

## Key Results

| Metric | Control | Treatment |
|---|---:|---:|
| Conversion Rate | 8.80% | 9.67% |
| Revenue per User | 81.52 | 86.72 |
| Contribution Profit per User | 23.27 | 24.79 |

- Conversion rate increased by **9.91% relative to Control**, and the result remained statistically significant after Holm correction.
- Revenue per user increased by **6.38%**, but the result was not statistically significant after correction.
- Contribution profit per user increased by **6.50%**, but the result was not statistically significant after correction.

## Business Recommendation
**Continue testing before a full rollout.**

The redesigned button improved conversion, but the financial benefits remain uncertain. A follow-up experiment should use contribution profit per user as the primary metric.

## Project Structure

```text
ecommerce-ab-testing/
├── data/
│   └── experiment_data.csv
├── notebooks/
│   ├── 01_data_quality_and_eda.ipynb
│   └── 02_ab_test_analysis.ipynb
├── src/
│   └── statistical_tests.py
├── reports/
│   └── business_recommendation.md
├── README.md
└── requirements.txt
```

## How to Run

1. Clone this repository.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebooks folder.
4. Run the notebooks in order, starting with data quality and EDA.

## Tools Used
Python, Pandas, NumPy, SciPy, Statsmodels, Matplotlib, Seaborn, and Jupyter Notebook.

## Limitations
This project uses **synthetic data** for learning and portfolio purposes. The results do not represent a real company's experiment or establish real-world business impact.

---

**Author:** Aditya Kumar
