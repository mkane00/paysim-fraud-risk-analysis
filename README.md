# paysim-fraud-risk-analysis
Fraud analysts need to identify suspicious transactions efficiently while minimizing investigation workload.
# PaySim Fraud Risk Analysis Dashboard

## Project Overview

This project analyzes synthetic financial transaction data to identify fraud patterns, prioritize high-risk transactions, and validate fraud detection logic.

The workflow follows a layered analytics approach:

* **Bronze Layer** → Raw transaction ingestion
* **Silver Layer** → Data cleaning, validation, and feature engineering
* **Gold Layer** → Business-ready fraud metrics and dashboard reporting

Built using:

* Python
* Pandas
* Tableau
* Fraud Signal Engineering
* Risk Segmentation

---

## Business Problem

Fraud analysts need to identify suspicious transactions efficiently while minimizing investigation workload.

This dashboard helps answer:

* Where fraud concentrates
* Which transactions are highest risk
* Whether detection rules are effective
* How transaction amount influences fraud

---

## Dataset

**PaySim** is a synthetic mobile money transaction dataset used to simulate fraud detection scenarios.

Dataset includes:

* Transaction Type
* Transaction Amount
* Account Balance Changes
* Fraud Labels (`isFraud`)
* Balance Mismatch Signals
* Transaction Risk Indicators

---

## Key Metrics

* **Total Transactions:** 6.36M
* **Fraud Transactions:** 8,213
* **Fraud Rate:** 0.13%
* **Priority Review Queue:** 318,131

---

## Dashboard Features

* Fraud Count by Transaction Type
* Fraud Rate by Transaction Type
* Fraud Count by Amount Bucket
* Fraud Signal Distribution
* Flagged vs Non-Flagged Fraud Comparison
* Interactive Filters

---

## Fraud Logic

The **Priority Review Queue** identifies transactions matching both conditions:

```text
Large Transaction Flag = TRUE
AND
Destination Balance Mismatch = TRUE
```

This creates a focused review queue that helps fraud analysts prioritize suspicious activity.

---

## Key Findings

* Fraud is concentrated in **CASH_OUT** and **TRANSFER** transactions
* Fraud rates increase with larger transaction values
* Flagged transactions show significantly higher fraud prevalence
* Fraud signal scores cluster in mid-range groups, while high-risk scores occur less frequently
* Priority Review Queue helps isolate transactions that warrant investigation

---

## Dashboard Preview

![Dashboard Preview](final_paysim_dashboard.png)

---

## Tools Used

* Python
* Pandas
* Tableau
* Jupyter Notebook
* Data Visualization
* Fraud Analytics

---
## Repository Structure

```text
paysim-fraud-risk-analysis/
│
├── README.md
├── notebooks/
│   ├── Bronze_Layer_Data_Ingestion.ipynb
│   ├── Silver_Layer_Data_Cleaning_Features.ipynb
│   └── Gold_Layer_Fraud_Analytics.ipynb
│
├── images/
│   └── final_paysim_dashboard.png
│
├── dashboard/
│   ├── paysim_dashboard.twbx
│   └── tableau_public_link.txt
│
├── outputs/
│   ├── fraud_summary.csv
│   ├── high_risk_queue.csv
│   └── gold_reporting.csv
│
└── requirements.txt
```

## Author

**Mary Kane**
Fraud Analytics | Data Analytics | Tableau | Python | SQL

GitHub: [https://github.com/mkane00](https://github.com/mkane00)

---
## Tableau Dashboard

View the interactive dashboard on Tableau Public:
[<div class='tableauPlaceholder' id='viz1777749233256' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pa&#47;PaysimDashboard&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='PaysimDashboard&#47;Dashboard1' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Pa&#47;PaysimDashboard&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1777749233256');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='1200px';vizElement.style.maxWidth='100%';vizElement.style.minHeight='850px';vizElement.style.maxHeight=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='1200px';vizElement.style.maxWidth='100%';vizElement.style.minHeight='850px';vizElement.style.maxHeight=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.minHeight='2250px';vizElement.style.maxHeight=(divElement.offsetWidth*1.77)+'px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
](https://public.tableau.com/views/PaysimDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

[PaySim Fraud Detection Dashboard]
```
