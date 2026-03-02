# 💳 Credit Card Financial Weekly Dashboard (Power BI, SQL & DAX)

## 📊 Project Overview

This project presents an end-to-end Credit Card Financial Weekly Dashboard designed to monitor and analyze key business metrics such as revenue, transaction volume, customer behavior, activation rate, and delinquency trends. The dashboard is built using Power BI with data sourced from a SQL database and processed using DAX for advanced analytics and KPI tracking.

The solution enables stakeholders and analysts to gain real-time insights into credit card operations, financial performance, and customer segmentation through interactive visualizations and data-driven reporting.

---

## 🎯 Project Objective

To develop a comprehensive and interactive credit card analytics dashboard that provides real-time insights into key performance metrics and weekly trends, enabling effective monitoring of financial performance and strategic decision-making.

---

## 🛠️ Tech Stack

* **Power BI** – Data visualization & dashboard development
* **SQL (PostgreSQL / SQL Server)** – Data storage and querying
* **DAX (Data Analysis Expressions)** – Calculated measures & KPIs
* **Excel / CSV** – Data preprocessing and import
* **Data Modeling** – Star schema and relational modeling

---

## 🗂️ Dataset Description

The dataset consists of credit card transaction and customer information, including:

* Customer demographics (age, income, gender)
* Transaction amount and count
* Annual fees
* Interest earned
* Week start date
* Card category and usage details

The data is imported into a SQL database and then connected to Power BI for further analysis and visualization.

---

## 🔄 Data Pipeline & Workflow

1. Data collection from CSV files
2. Data import into SQL database
3. Data cleaning and preprocessing
4. Data modeling in Power BI
5. DAX calculations for KPIs and metrics
6. Dashboard creation and visualization
7. Insight generation and reporting

---

## 🧮 Key DAX Calculations

Some important calculated measures used in the project:

### Revenue Calculation

```
Revenue = annual_fees + total_trans_amt + interest_earned
```

### Weekly Revenue Tracking

```
Current_week_Revenue = 
CALCULATE(
    SUM(cc_detail[Revenue]),
    FILTER(
        ALL(cc_detail),
        cc_detail[week_num] = MAX(cc_detail[week_num])
    )
)
```

### Customer Segmentation

* Age Groups (20-30, 30-40, 40-50, 50-60, 60+)
* Income Groups (Low, Medium, High)

---

## 📈 Dashboard Features

* Interactive KPI Cards (Revenue, Transactions, Interest)
* Weekly Performance Trend Analysis
* Customer Segmentation (Age, Gender, Income)
* Transaction Analysis by Card Type
* Activation Rate & Delinquency Monitoring
* Regional Performance Insights
* Dynamic Filters and Slicers for drill-down analysis

---

## 📊 Key Performance Metrics (KPIs)

* Total Revenue
* Total Transaction Amount
* Total Transaction Count
* Customer Count
* Activation Rate
* Delinquency Rate
* Interest Earned
* Week-over-Week (WoW) Revenue Change

---

## 🔍 Business Insights Generated

* Revenue growth trends across weeks
* Contribution analysis by gender and card category
* Identification of high-performing regions
* Customer behavior and spending patterns
* Activation and delinquency rate monitoring
* Transaction trends and financial performance analysis

---

## 🧱 Data Modeling

The project follows a structured data model:

* Fact Table: Credit Card Transactions
* Dimension Tables: Customer Details, Time, Card Category

Relationships were created to enable efficient filtering, aggregation, and cross-analysis within Power BI.

---

## 🚀 How to Run the Project

### Step 1: Database Setup

* Create tables in SQL database
* Import CSV dataset into SQL

### Step 2: Connect to Power BI

* Open Power BI Desktop
* Connect to SQL database
* Load transaction and customer tables

### Step 3: Data Transformation

* Clean missing values
* Create calculated columns
* Perform data modeling

### Step 4: Create DAX Measures

* Revenue
* Weekly Revenue
* Customer Segmentation
* KPI Metrics

### Step 5: Build Dashboard

* Add charts, slicers, and KPI cards
* Create interactive visuals
* Publish and share dashboard

---

## 📷 Dashboard Preview

*(Add screenshots of your Power BI dashboard here)*

---

## 💼 Resume Description

Developed an interactive Power BI dashboard using SQL and DAX to analyze credit card revenue, transaction trends, customer segmentation, and weekly performance KPIs through structured data modeling and advanced analytics. Performed SQL-based data extraction and DAX calculations to generate actionable financial insights for data-driven decision-making and business performance monitoring.

---

## 📌 Future Enhancements

* Real-time data integration using APIs
* Predictive analytics for customer spending
* Automated ETL pipeline using Python
* Deployment to Power BI Service for live reporting

