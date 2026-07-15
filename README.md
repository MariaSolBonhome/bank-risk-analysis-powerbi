# 🏦 Credit Risk Analysis — Bank Marketing Dataset

**Tools:** Power BI · DAX · Power Query  
**Domain:** Banking · Credit Risk · Business Intelligence  
**Data:** Bank Marketing Dataset — UCI Machine Learning Repository ([Kaggle](https://www.kaggle.com/datasets/josuparrarosales/dirty-bank-dataset))  
**Period:** 2008–2010 | Portuguese bank telemarketing campaign

---

## 📌 Project Overview

This project analyzes the credit risk profile of a Portuguese bank's customer portfolio using data from a telemarketing campaign which was carried out between 2008 and 2010. The dataset contains 45K records with financial variables for each customer contacted.

The analysis was built from the perspective of a **Credit Risk Manager**, with the goal of identifying which customer profiles concentrate the highest default risk and credit exposure, enabling data-driven decisions on credit approval policies and customer segmentation.

---

## 🎯 Business Problem

Credit approval and monitoring decisions at the bank were based on general criteria, without a systematic analysis of which customer profiles concentrate higher default rates or greater credit exposure (customers with both mortgage and personal loan active simultaneously). This could result in underestimated risk exposure or missed business opportunities with low-risk segments.

---

## 📊 Dashboard

The report is structured in two pages:

### Page 1 — Credit Risk Dashboard

![Credit Risk Dashboard](dashboard_page1.png)

**KPIs:**
- Total Customers: 45K contacted in campaign
- % Default: 1.80% of customers with default history
- % Double Exposure: 9.66% of customers holding both mortgage and personal loan

**Key findings:**
- Entrepreneurs show the highest default rate (3.70%), more than double that of students (0.32%)
- Customers in default have a negative average balance (-€137), vs +€1,401 for non-default customers — a strong early warning signal
- Divorced customers represent only 11% of the portfolio but concentrate the highest default rate (2.4%)
- 9.66% of customers carry both a mortgage and a personal loan simultaneously — the highest credit exposure segment

---

### Page 2 — Statistical Analysis & Projection

![Statistical Analysis & Projection](dashboard_page2.png)

**Statistical diagnosis:**
- Mean balance (€1 374) is nearly 3x the median (€448), indicating right skew driven by a small group of high-balance customers
- The histogram reveals that most customers hold balances between €0 – €500, with a long tail of high-balance outliers (>€10,000)

**Trend & Forecast:**
- Contact volume shows a declining trend after a strong peak in May
- A 3-month forecast projects continued decrease in campaign activity

> **Note:** The dataset covers a single annual campaign cycle (12 monthly data points, no year column). This limits forecast precision; in a real-world scenario with more than one year data, the projection would be more robust with a visible confidence band.

---

### Design Principles
- Minimal color palette (blues)
- Subtitles communicate the insight directly, not just the chart description
- No decorative borders or chart junk
- Interactive Education filter (slicer) for segment-level exploration

---

## 📁 Repository Structure

```
bank-credit-risk-analysis-powerbi/
├── README.md
├── bank_dataset.csv          # Original dataset (Kaggle)
├── dashboard.pbix            # Power BI report file
├── dashboard_page1.png       # Dashboard screenshot — Page 1
└── dashboard_page2.png       # Dashboard screenshot — Page 2
```
