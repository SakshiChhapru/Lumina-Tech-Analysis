# Lumina-Tech-Analysis
 LuminaTech Sales Analysis and Business Insights

# 📊 LuminaTech Sales Analysis and Business Insights

## 📌 Overview

This project analyses transactional sales data for **LuminaTech**, a lighting business, using Python. The notebook combines two datasets into a single analytical dataset and then applies a full end to end workflow covering data cleaning, validation, exploratory data analysis, anomaly detection, hypothesis testing, and regression modelling.

The goal of this project is to understand the key drivers of sales, profit, cost, and quantity sold, while also identifying operational patterns, high performing business segments, and unusual transactions that may require further attention.

---

## 🏢 Business Problem

LuminaTech operates across multiple product groups, districts, currencies, and business areas. To support better commercial decision making, this analysis answers questions such as:

1. What patterns exist in monthly sales over time?
2. Which districts, product groups, and salespeople drive the most profit and revenue?
3. Are there unusual transactions or underperforming segments that need attention?
4. Do transaction values differ across currencies, weekdays versus weekends, or business areas?
5. What factors most strongly influence sales revenue, product cost, and quantity sold?

---

## 📂 Dataset

The notebook starts by loading **two separate CSV files** and merging them into one complete dataset for analysis.

The dataset includes variables related to:

- transaction dates  
- customers  
- districts  
- product and item groups  
- business areas  
- currencies  
- quantities sold  
- sales value  
- cost value  
- salespeople  
- order and invoice information  

---

## ⚙️ What This Notebook Does

## 🧹 1. Data Import and Combination

The notebook imports two datasets and checks whether the columns match exactly before combining them into a single dataframe for analysis.

This ensures that the final dataset is structurally consistent and suitable for downstream analysis.

---

## 🧼 2. Data Cleaning and Preparation

A substantial part of the notebook is dedicated to preparing the data properly before analysis. This includes:

- removing rows with missing critical numeric values  
- converting accounting dates into a usable datetime format  
- converting relevant fields into categorical variables  
- filling missing categorical values using the mode  
- standardising categorical text values by trimming spaces and converting to uppercase  
- validating codes against metadata and removing invalid entries  
- correcting inconsistent currency labels  
- removing duplicate records based on invoice and line number  
- converting transaction values into **AUD** using year based exchange rates  
- creating clean sales and cost measures in AUD  
- generating descriptive statistics after cleaning  

This section is important because it ensures the insights are based on reliable and standardised data.

---

## 📊 3. Exploratory Data Analysis

The notebook then explores the cleaned data to uncover major business patterns.

### Key areas analysed include:

**Monthly sales trends**  
The analysis identifies recurring seasonal behaviour in monthly sales over time.

**Profit by district**  
Profitability is examined across customer district codes to highlight the most valuable regions.

**Sales versus quantity by item group**  
This helps compare which product groups generate high revenue relative to the quantity sold.

**Profit by product group**  
The notebook identifies which product groups contribute the most to total profit.

**Top salespeople by revenue**  
The analysis highlights the individuals driving the largest share of sales.

Overall, the EDA section helps turn raw transactions into actionable commercial insights.

---

## 🚨 4. Anomaly Detection

The notebook includes a structured anomaly detection section to identify records or segments that behave unusually.

Three types of anomalies are flagged:

1. **Unusual transactions**  
   Transactions with unusually high or low sales values within their product group are identified using the IQR method.

2. **Underperforming salespeople**  
   Salespeople with unusually low total sales are detected relative to their peers.

3. **District sales drops**  
   Customer districts with unusually weak sales performance are flagged for further investigation.

This section is useful for risk monitoring, operational review, and performance management.

---

## 📉 5. Hypothesis Testing

The notebook tests several business questions statistically using independent sample t tests.

### Questions tested:

**Do average unit prices differ between AUD and USD transactions?**  
This checks whether customers transacting in different currencies experience significantly different unit pricing.

**Do average sales differ between weekdays and weekends?**  
This helps evaluate whether customer spending behaviour changes based on the day of the week.

**Do average sales differ between major business area groups?**  
This tests whether some business divisions generate significantly different transaction values than others.

These tests move the analysis beyond visual observation and provide statistical evidence for business decisions.

---

## 🤖 6. Regression Modelling and Inference

The final section uses OLS regression models to understand what influences key commercial outcomes.

### Models built in the notebook:

**What drives sales revenue?**  
A regression model is used to identify the variables that explain variation in `value_sales_aud`.

**What influences product cost?**  
A separate model examines which factors affect `value_cost_aud`.

**What influences quantity sold?**  
A third model investigates the drivers of `value_quantity`.

The notebook also engineers time based features from the accounting date, filters usable predictors, handles low cardinality categorical variables, and fits interpretable regression models.

This section adds strong business value because it helps explain not just what happened, but why it happened.

---

## 🛠 Tools & Technologies

<p align="left">
  <img src="https://skillicons.dev/icons?i=python" height="45"/>
  <img src="https://skillicons.dev/icons?i=pandas" height="45"/>
  <img src="https://skillicons.dev/icons?i=numpy" height="45"/>
  <img src="https://skillicons.dev/icons?i=matplotlib" height="45"/>
</p>

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Plotly  
- SciPy  
- Statsmodels  

---

## 💡 Project Value

This notebook is more than a technical exercise. It shows how data can be used to support real business decisions in areas such as:

- pricing consistency  
- sales performance  
- profitability analysis  
- territory and district evaluation  
- salesforce performance  
- operational monitoring  
- forecasting and commercial planning  

---

## 📁 File Structure

This repository includes:

- `LuminaTechAnalysis.ipynb` → the full analysis notebook  
- `Dataset1.csv` and `Dataset2.csv` → the source files used in the notebook

  ---
  
## 📁 Files & Access

Due to file size limitations on GitHub, the full datasets and analysis files are hosted externally.

👉 **[Access Datasets & Files on Google Drive](https://drive.google.com/drive/u/1/folders/1hqMLCQ2w4Tfs6Z0-UfvUrabWsAAerky4)**

This includes:
- Raw datasets  
- Cleaned datasets  
- Supporting analysis files  

All files used in this project can be accessed through the link above.

---

## 🧠 Conclusion

This project presents a complete business analytics workflow using LuminaTech sales data. It begins with raw transactional data, transforms it into a clean analytical dataset, explores patterns in sales and profit, identifies anomalies, validates business assumptions with hypothesis testing, and builds regression models to explain the main drivers of performance.

It showcases both technical analysis and business thinking, with a strong focus on turning data into actionable insights.
