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

## Results & Observations

- `MarkDown` columns had significant missing values → filled with `0`
- Outliers detected and clipped using IQR method across all numeric columns
- `Date` column decomposed into `Year`, `Month`, `Day`, `Week`
- Store `Type` encoded: `A → 0`, `B → 1`, `C → 2`
- No duplicate rows found in the training set
