# Team4_CLS-GIZ3_DAT2_G3
Data analysis for supply chain Grad project

# Unilever Data Analytics Report  
### Supply Chain, Sustainability & Infrastructure Impact Analysis

## 📌 Project Overview
This project presents an end-to-end *data analytics case study on Unilever, benchmarked against leading global **FMCG companies*.  
The analysis focuses on *supply chain efficiency, workforce structure, sustainability performance, and the **impact of Egypt Vision 2030 infrastructure development* on logistics cost and operational performance.

The project demonstrates practical application of:
- Data cleaning & transformation
- Power BI data modeling
- DAX-based KPI development
- Performance optimization
- Strategic business insight generation

---

## 🎯 Objectives
- Compare Unilever’s *financial and operational performance* with FMCG peers
- Identify *strengths and inefficiencies* in the supply chain (with focus on Egypt / ME)
- Analyze *workforce structure* and its role in productivity & sustainability
- Evaluate Unilever’s *sustainability alignment* (People, Planet, Waste)
- Assess how *Egypt Vision 2030 infrastructure* impacts logistics costs and lead times

---

## ❓ Key Business Questions
1. How does Unilever perform financially and operationally relative to FMCG peers?
2. Where are the key *cost drivers and bottlenecks* in Unilever’s supply chain?
3. How does workforce distribution support operational efficiency and ESG goals?
4. Are Unilever’s sustainability initiatives aligned with global best practices?
5. What logistics efficiency gains are expected from Egypt Vision 2030 infrastructure?

---

## 🗂 Data Sources
- Global FMCG peer companies list
- Top 2000 Companies Financial Dataset
- Unilever supply chain & logistics data
- Unilever workforce structure data
- Unilever sustainability performance data
- Egypt Vision 2030 (roads & logistics infrastructure)

---

## 🧹 Data Preprocessing & Transformation

### Key Cleaning & Transformation Steps
- *Production Data*
  - Unpivoted monthly columns into Month_Num and Production_Volumes
  - Enabled time-series and seasonality analysis

- *Orders Data*
  - Extracted month names from order dates
  - Converted cost and revenue fields to USD currency format

- *Production Capacity*
  - Converted SKU share values to percentage format

- *Bill of Materials*
  - Removed blank rows
  - Standardized cost fields to currency format

- *Seasonality Results*
  - Unpivoted monthly data
  - Created unique Month_Key for data modeling

- *Financial Benchmarking Data*
  - Converted textual financial values (e.g. $5.8B, $650M) into numeric format using Excel formulas

---

## 🧩 Company Categorization (Power Query – M Language)
Companies were categorized into business sectors using Power Query logic based on company names:
- Consumer Goods & FMCG
- Banking & Financial Services
- Energy & Oil
- Technology
- Retail
- Healthcare
- Industrial Manufacturing
- Telecom
- Airlines
- Media & Entertainment

This enabled accurate *peer benchmarking and sector-level comparison*.

---

## 🧠 Data Modeling
- Dimension tables with unique keys were placed on the *one-side* of relationships
- Fact tables were linked using *many-to-one and many-to-many relationships* where required
- Example:
  - Month_Num used as key in Seasonality
  - SKU used as key in Products
- Model supports integrated analysis across:
  - Production
  - Costs
  - Revenue
  - Workforce
  - Sustainability
  - Infrastructure impact

---

## 📊 Key DAX Measures
```DAX
// Total Cost
Total Cost = SUM(Sales[Cost])

// Gross Margin
Gross Margin = [Total Sales] - [Total Cost]

// Gross Margin %
Gross Margin % = DIVIDE([Gross Margin], [Total Sales], 0)

// Transport Cost % of Revenue
Transport Cost % of Revenue =
DIVIDE([Total Transport Cost], [Total Revenue], 0)

// Manufacturing Cost % of Revenue
Manufacturing Cost % of Revenue =
DIVIDE([Total Manufacturing Cost], [Total Revenue], 0)

🚚 Transportation & Logistics Insights
	•	Sea transport accounts for ~70% of shipments, reducing unit cost and carbon emissions
	•	Domestic routes (Cairo–Delta, Cairo–Alexandria) show logistics costs below 0.3% of revenue
	•	International routes operate at ~3.4% of revenue with stable lead times (~20 days)
	•	High order volumes indicate strong logistics network utilization

⸻

🌱 Sustainability Analysis
	•	Sustainability embedded across supply chain operations
	•	Reduced waste through demand-driven forecasting
	•	Optimized logistics modes support emissions reduction
	•	Workforce investments align with ESG and Unilever’s Purpose, Values & Principles

⸻

⚡ Performance Optimization
	•	Power BI Performance Analyzer used to identify bottlenecks
	•	Reduced heavy visuals and simplified DAX
	•	Ensured query folding in Power Query
	•	Achieved ~30–40% improvement in dashboard load time

⸻

📈 Strategic Insights & Recommendations
	•	Unilever shows strong sustainability positioning among FMCG peers
	•	Transport and manufacturing costs present optimization opportunities
	•	Egypt Vision 2030 infrastructure is expected to:
	•	Reduce logistics costs
	•	Improve lead times
	•	Strengthen Egypt’s role as a regional supply chain hub
	•	Recommended next steps:
	•	Scenario analysis for fuel & transport volatility
	•	Deeper integration of sustainability KPIs into executive dashboards

Tools & Technologies
	•	Power BI
	•	Power Query (M Language)
	•	DAX
	•	Microsoft Excel
	•	Data Modeling & Performance Analyzer
