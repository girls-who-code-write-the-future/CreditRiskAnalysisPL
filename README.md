# 📈 Credit Risk Analysis in Polish Regions (2020–2023)

This project estimates the relative credit risk for Poland's 16 voivodeships using socio-economic data from 2020 to 2023. The goal was to create a synthetic index and visualize regional disparities in credit risk over time.

## 🌍 Project Overview

This analysis aims to:

- Normalize and compare key economic indicators.
- Build a synthetic **Credit Risk Index**.
- Visualize changes over time (2020 → 2023).
- Identify the most influential variables contributing to regional risk.

## 📊 Data Sources

The project uses cleaned datasets (CSV format) from the [Główny Urząd Statystyczny (GUS)](https://stat.gov.pl):

- **Disposable income per capita**
- **Unemployment rate**
- **Working age population share (%)**
- **Population density (per km²)**
- **Median age**

Each dataset includes yearly values (2020–2023) for all 16 Polish voivodeships.

## 🧬 Methodology

### 1. Data Preparation

- Region names standardized across datasets.
- All numerical values converted to consistent format.
- Missing or invalid entries removed.
- Cleaned datasets uploaded to **Google BigQuery** and joined using **SQL**.

### 2. Index Creation (2023)

The **Credit Risk Index** is computed as the average of normalized values:

- *Unemployment rate* (higher → higher risk)
- *Income per capita* (lower → higher risk)
- *Working age population share* (lower → higher risk)

All values are normalized to a [0, 1] scale using Min-Max normalization.

### 3. Change Analysis

- Difference in Credit Risk Index between 2020 and 2023.
- Highlighted **top 3 increases** and **top 3 improvements**.

### 4. Correlation Analysis

- Pearson correlation between each indicator and the final index.
- Strongest negative correlation observed: **Working age population share (∼ -0.75)**.

## 🌐 Visualizations

- 🗺️ **Choropleth map**: Credit Risk Index by voivodeship (2023).
- 📊 **Bar chart**: Voivodeships with the largest changes in risk.
- 🧮 **Correlation bar plot**: Gradient highlights variable impact.

## 📆 Key Findings

- **Lubelskie** and **Zachodniopomorskie** showed the largest increase in risk.
- **Mazowieckie** and **Warmińsko-Mazurskie** showed slight improvements.
- **Working age population share** is the strongest driver of credit risk variation.

## 🚀 How to Run

1. Clone this repository.
2. Open the `.ipynb` file in Jupyter Notebook or [Google Colab](https://colab.research.google.com/).
3. Run all cells in order to reproduce the analysis.

Created by **Olga Skóra**  
🎓 Junior Data Analyst | [LinkedIn](https://www.linkedin.com/in/olga-sk%C3%B3ra/)  
📅 2025 Portfolio Project
