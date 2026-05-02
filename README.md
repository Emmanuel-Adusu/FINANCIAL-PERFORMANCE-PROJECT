# 💰 Financial Performance Analysis Dashboard

> ⚠️ Disclaimer: This project uses a simulated dataset for demonstration purposes.

---

## 📌 Project Overview

This project analyzes financial performance across multiple regions and customer segments to identify revenue drivers, profitability trends, and opportunities for business growth.

The dashboard enables stakeholders to make data-driven decisions by providing visibility into key financial metrics.

---

## 🎯 Business Problem

Organizations need clear insights into:

- Which regions generate the most revenue?
- Which customer segments are most profitable?
- How stable is profit over time?

Without this visibility, decision-making becomes reactive rather than strategic.

---

## 📊 Dataset Description

| Column   | Description |
|----------|------------|
| Country  | Sales region |
| Segment  | Customer segment |
| Revenue  | Total sales value |
| Profit   | Net profit |
| Date     | Transaction date |

---

## 🧠 Data Preparation

Data was cleaned and validated to ensure:
- No missing values in key financial fields
- Consistent date formatting
- Accurate aggregation levels for reporting

---

## 🧮 SQL Analysis (Exploratory Phase)

SQL was used to explore and validate the dataset before building the dashboard.

---

### 📌 Total Revenue

```sql
SELECT SUM(Revenue) AS total_revenue
FROM finance;
````

### Profit Margin
```sql
SELECT 
    SUM(Profit) / SUM(Revenue) AS profit_margin
FROM finance;
````

### Revenue by Country
```sql
SELECT Country, SUM(Revenue) AS revenue
FROM finance
GROUP BY Country
ORDER BY revenue DESC;
````

### 📌 Revenue by Segment
```sql
SELECT 
    Segment,
    SUM(Revenue) AS revenue
FROM finance
GROUP BY Segment
ORDER BY revenue DESC;
````

---

## 📊 DAX Measures (Power BI Layer)

DAX was used to create dynamic KPIs for interactive analysis.

### Total Revenue
```DAX
Total Revenue = SUM('Finance'[Revenue])
````

### Total Profit
```DAX
Total Profit = SUM('Finance'[Profit])
````

### Profit Margin
```DAX
Profit Margin = DIVIDE([Total Profit], [Total Revenue])
````

---

## 📊 Dashboard Features

The Power BI dashboard includes:
KPI Cards (Revenue, Profit, Profit Margin)
Bar Charts (Revenue by Country & Segment)
Trend Analysis (Time-based performance)
Interactive filtering across dimensions

---

## 📸 Dashboard Preview


---

## 🔍 Key Insights
- France and Canada are top-performing markets
- Government segment contributes the highest revenue
- Profit shows periodic fluctuations

---

## 💡 Business Recommendations
- Focus expansion on high-performing regions
- Improve cost control to stabilize profit
- Target high-value customer segments

---

## 🛠 Tools & Technologies
- Power BI (Visualization & Dashboarding)
- SQL (Data exploration & validation)
- DAX (KPI calculations)

---

## 📌 Project Outcome

This project demonstrates how financial data can be transformed into actionable insights to support strategic decision-making.


