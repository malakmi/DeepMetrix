# Walmart Sales Forecasting — EDA & Preprocessing

> Graduation Project | Exploratory Data Analysis & Data Preprocessing Pipeline

---

## Team

| Name | LinkedIn |
|------|----------|
| Youssef Moussa | [theyoussefmoussa](https://www.linkedin.com/in/theyoussefmoussa) |
| Malak Abdallah | [malak-abdallah](https://www.linkedin.com/in/malak-abdallah/) |
| Zyad Ashraf | [zyad-ashraff](https://www.linkedin.com/in/zyad-ashraff/) |
| Hamza Ahmed | [hamzaahmedamin](https://www.linkedin.com/in/hamzaahmedamin/) |
| Rahma Essam | [rahma-essam](https://www.linkedin.com/in/rahma-essam/) |
| Sara Mostafa | [sara--mostafa](https://www.linkedin.com/in/sara--mostafa/) |

## Project Structure

```
📦 Graduation Project
├── data/
│   ├── train.csv
│   ├── test.csv
│   ├── stores.csv
│   └── features.csv
├── notebooks/
│   └── clean_notebook.ipynb
├── src/
├── tests/
├── main.py
├── requirements.txt
├── .gitignore
└── README.md
Project Description

This notebook covers the Exploratory Data Analysis (EDA) and Data Preprocessing pipeline for predicting weekly sales across Walmart stores. The project focuses on transforming raw, unclean data into a structured and analysis-ready dataset that can support accurate forecasting models.

From a business perspective, accurate sales forecasting helps retail companies optimize inventory management, reduce stock shortages and overstock, and improve promotional strategies — ultimately increasing revenue and efficiency.

The workflow begins with data integration, where multiple datasets (train, stores, and features) are merged using common keys such as Store and Date, resulting in a unified dataset that combines sales data, store information, and external economic factors.
## How to Run

1. Clone the repo and navigate to the project folder
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn
```
3. Open the notebook:
```bash
jupyter notebook notebooks/eda_preprocessing.ipynb
```
4. Update `DATA_DIR` in the **Constants & Config** cell to match your local path

---
EDA Questions & Analysis

As part of the analysis phase, a set of analytical questions (15+) were defined and answered using visualizations and statistical insights, such as:

Which stores generate the highest weekly sales?
What is the impact of holidays on sales performance?
Which store type (A/B/C) performs best?
How do promotions (MarkDowns) affect sales?
What are the monthly and yearly sales trends?
Which departments are consistently high-performing?
Is there a correlation between economic factors (CPI, unemployment) and sales?
How does temperature or fuel price influence sales behavior?

These questions guided the EDA process and helped uncover meaningful patterns and business insights.

📊 Exploratory Data Analysis (EDA)

The EDA phase explores:

Data distributions and skewness
Sales trends over time (seasonality & patterns)
Impact of holidays on sales
Relationship between promotions (MarkDowns) and sales
Correlation between economic indicators and sales
🧹 Data Preprocessing Pipeline
Handling Missing Values:
MarkDown1–5 columns contained significant missing values and were filled with 0 under the assumption of no active promotion.
Outlier Treatment:
Extreme values were detected using the IQR method and clipped to reduce their impact on model performance.
Feature Engineering:
The Date column was decomposed into:
Year
Month
Week
Day
Encoding Categorical Variables:
Store types were converted into numerical values:
A → 0
B → 1
C → 2
Data Validation:
No duplicate rows were found
Data types were checked and corrected
📊 Key Observations
Sales exhibit strong seasonal patterns, especially during holidays
Larger stores (Type A) tend to generate higher sales
Promotional markdowns significantly influence sales spikes
Economic indicators show relatively weak correlation with weekly sales
🤖 Next Step

The cleaned dataset will be used for:

Machine Learning models (Linear Regression, Random Forest, XGBoost)
Time Series models (ARIMA, Prophet)
Evaluation using RMSE and MAE

## Results & Observations

- `MarkDown` columns had significant missing values → filled with `0`
- Outliers detected and clipped using IQR method across all numeric columns
- `Date` column decomposed into `Year`, `Month`, `Day`, `Week`
- Store `Type` encoded: `A → 0`, `B → 1`, `C → 2`
- No duplicate rows found in the training set
