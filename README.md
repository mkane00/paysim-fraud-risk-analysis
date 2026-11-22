# PaySim 2.0 — Fraud Risk Analysis

## Project Overview

This project analyzes 6,362,620 simulated financial transactions to identify fraud patterns and evaluate the effectiveness of fraud screening strategies.

The analysis follows a Bronze–Silver–Gold workflow, using Python to transform transaction data into actionable business insights.

## Business Objective

Evaluate the trade-offs between fraud detection, financial risk coverage, and investigation workload.

The project compares two screening strategies to understand how financial institutions can prioritize suspicious transactions while managing operational efficiency.

## Tools & Technologies

- Python
- pandas
- Matplotlib
- JupyterLab
- Data Cleaning and Validation
- KPI Analysis and Data Visualization

## Methodology — Bronze, Silver & Gold

### Bronze — Data Exploration
- Explored 6,362,620 transactions.
- Reviewed data types and transaction categories.
- Checked for missing values and duplicate records.
- Identified the initial distribution of fraudulent transactions.

### Silver — Data Preparation
- Validated data quality.
- Created risk indicators based on transaction type and amount.
- Prepared the dataset for fraud risk analysis.

### Gold — Risk Analysis
- Calculated six fraud detection and operational KPIs.
- Compared two transaction screening strategies.
- Evaluated precision, recall, investigation workload, and financial risk coverage.
- Created four visualizations and developed business recommendations.

## Key Findings

The analysis identified 8,213 fraudulent transactions out of 6,362,620 total transactions, representing an overall fraud rate of 0.129%.

### Fraud Patterns

- TRANSFER had the highest fraud rate (0.77%).
- CASH_OUT had a fraud rate of 0.18%.
- No fraudulent transactions were recorded in the remaining transaction categories.

### Screening Strategy Comparison

| Metric | Strategy A | Strategy B |
|---|---:|---:|
| Transactions Flagged | 2,770,409 | 1,934,297 |
| Fraud Recall | 100% | 79.22% |
| Precision | 0.296% | 0.336% |
| Financial Risk Coverage | 100% | 99.39% |
| Missed Fraudulent Transactions | 0 | 1,707 |

Strategy B reduced investigation workload by **30.18%**, equivalent to 836,112 fewer flagged transactions.

However, Strategy B missed 1,707 fraudulent transactions representing approximately 73.02 million in simulated transaction value.

### Business Insight

The results highlight the trade-off between fraud detection and operational efficiency.

Strategy A provides complete detection coverage within this dataset but requires substantially more investigations.

Strategy B reduces investigation workload while maintaining high financial risk coverage, although its lower recall and very low precision indicate opportunities for improvement.

## Business Recommendations

Based on the analysis, the following actions are recommended:

1. **Improve fraud screening precision:** Explore additional transaction characteristics to reduce false positives and unnecessary investigations.
2. **Balance detection and efficiency:** Evaluate screening strategies using both fraud recall and investigation workload.
3. **Monitor financial exposure:** Track the monetary value of detected and missed fraudulent transactions.
4. **Validate screening rules:** Test alternative thresholds and strategies before operational deployment.

## Project Structure

The project is organized into three analytical stages:

- **Bronze:** Initial data exploration and quality assessment.
- **Silver:** Data preparation and risk indicator development.
- **Gold:** Fraud detection KPIs, strategy comparison, visualizations, and business recommendations.

### Jupyter Notebooks

The following notebooks document the analytical workflow:

- [Bronze — Data Exploration](notebooks/01_Bronze_Data_Exploration.ipynb)
- [Silver — Data Preparation](notebooks/02_Silver_Data_Preparation.ipynb)
- [Gold — Risk Analysis](notebooks/03_Gold_Risk_Analysis.ipynb)

## Limitations

This analysis uses the PaySim simulated financial transaction dataset. Transaction amounts do not represent confirmed financial losses.

The screening strategies were evaluated on the analyzed dataset and require additional validation before real-world implementation.

## Project Status

**PaySim 2.0 — Analysis completed.**

All three analytical stages have been completed, and the notebooks have been validated for successful execution.

