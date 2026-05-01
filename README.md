# FINANCIAL-PERFORMANCE-PROJECT

# 💰 Financial Performance Analysis Dashboard

> ⚠️ Disclaimer: This project uses a simulated dataset for demonstration purposes.

---

## 📌 Project Overview

This dashboard analyzes financial performance across countries and customer segments to identify key revenue drivers and profitability trends.

---

## 🎯 Business Problem

Businesses require clear visibility into:
- Revenue growth
- Profit margins
- High-performing regions and segments

---

## 📊 Dataset Description

| Column   | Description |
|----------|------------|
| Country  | Sales region |
| Segment  | Customer type |
| Revenue  | Total sales |
| Profit   | Net profit |
| Date     | Transaction date |

---

## 🧮 SQL Analysis

### Total Revenue
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

---

## 📊 DAX Measures

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

## 🛠 Tools

Power BI • SQL • DAX

---


