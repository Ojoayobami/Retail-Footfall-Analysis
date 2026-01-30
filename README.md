# 📌 PROJECT TITLE 
👣 Retail Footfall Analysis

# 📌 INTRODUCTION 

This project analyzes retail **footfall and average daily sales** to understand how customer traffic translates into sales performance and operational outcomes.

Using sales transaction data, daily footfall was **estimated at store level** and analyzed across stores, regions, and sales channels. The analysis focuses on identifying high-traffic and low-traffic periods, evaluating the relationship between footfall and revenue, and highlighting areas where conversion efficiency can be improved.

The objectives of this analysis are to:

- Estimate **daily footfall per store** using sales transaction data  
- Calculate **average daily sales** by store, region, and sales channel  
- Identify **high-traffic and low-traffic days** across the week  
- Analyze the **impact of footfall on sales performance** and revenue generation  
- Compare stores with **high footfall versus high sales** to assess conversion efficiency  
- Provide **actionable business and operational recommendations** based on insights

# 📂 DATA CLEANING & PREPARATION

All datasets (sales transactions and store/channel dimension tables) were imported into **Power BI** for cleaning and transformation.  
Several steps were carried out to ensure the data was accurate, consistent, and ready for **footfall estimation and performance analysis**.

---

### 🧹 Data Cleaning Overview

| Step | Description | Action Taken |
|------|-------------|--------------|
| Data Merging | Combined datasets | Merged all sales and store/channel datasets into a single fact table |
| Removed Duplicates | Eliminated duplicate records | Removed duplicate transactions across all stores |
| Checked for Blanks | Ensured data completeness | Checked key fields (order date, store, channel, quantity, amount) for missing values |
| Data Type Validation | Ensured correct formats | Converted `order_datetime` to Date/Time and `order_date` to Date |
| Standardized Columns | Corrected naming inconsistencies | Standardized store names, channel names, and region codes for consistency |
| Footfall Calculation Prep | Prepared data for footfall estimation | Ensured sales transactions had valid quantities to estimate daily footfall |

These steps ensured that the dataset was **clean, consistent, and ready for modeling, analysis, and dashboard visualization**.

## ⚙️ CALCULATED FIELDS & MEASURES

To enable advanced **footfall and sales analysis**, several calculated tables, columns, and measures were created in **Power BI**.

---

### 📅 Calculated Table

A dedicated **Date Table** was created to support time intelligence analysis.

**Table Name:** `DateTable`  

**Calculated Columns Created:**
- **Year** – Extracted year from order date  
- **Month** – Month name  
- **MonthNumber** – Numeric month value (1–12)  
- **Day of Week** – Day name (Monday–Sunday)  
- **Day Number** – Numeric day value (1–31)  

This table was linked to the sales table using `order_date` to support **daily, weekly, and monthly analysis**.

---

### 📊 Calculated Measures

| Measure Name | Description |
|--------------|-------------|
| **Active Sales Days** | Number of days with at least one transaction per store |
| **Average Daily Footfall** | Average number of customers visiting each store per day |
| **Average Daily Orders** | Average number of transactions per store per day |
| **Average Daily Sales** | Average revenue generated per store per day |
| **Average Selling Price** | Average price per item sold |
| **Average Spend per Head** | Average revenue per customer |
| **Average Units per Order** | Average number of items per transaction |
| **Footfall** | Estimated daily customer count per store (based on transactions) |
| **Max Daily Sales** | Highest revenue generated in a single day |
| **Max Footfall** | Highest number of customers in a single day |
| **Min Daily Sales** | Lowest revenue generated in a single day |
| **Min Footfall** | Lowest number of customers in a single day |
| **Total Orders** | Total number of transactions per store or period |

These calculated measures **enabled comprehensive footfall and sales performance analysis**, including weekly and monthly trends, peak and low traffic evaluation, channel comparisons, and store-level performance insights.

---

## 🔧 DATA TRANSFORMATION TOOLS USED

During data preparation, cleaning, transformation, and analysis, the following tools were used:

| Tool / Platform | Purpose | Key Actions Performed |
|-----------------|---------|---------------------|
| **Power Query (Power BI)** | Data cleaning and transformation | Merged datasets, removed duplicates, checked for blanks, validated data types, standardized columns |
| **DAX (Power BI)** | Calculations and measures | Created calculated columns and measures for footfall, daily sales, average spend, units per order, max/min analysis, and active sales days |
| **Power BI** | Visualization and dashboard creation | Built interactive dashboards, KPIs, and performance charts by store, region, and channel |
| **GitHub** | Version control and documentation | Stored project files, tracked changes, and documented the analysis workflow |

These tools ensured a **clean, consistent, and analysis-ready dataset**, and supported both **quantitative and visual exploration** of footfall and sales performance.

## 🔍 EXPLORATORY DATA ANALYSIS (EDA)

EDA was conducted to **understand footfall patterns, sales distributions, and relationships** in the data before deeper analysis. The focus was on **visual exploration, time-based trends, and operational insights**.

### 📊 Areas Explored

| Analysis Area | Focus |
|---------------|--------|
| Overall Business Performance | Evaluated total daily sales, total orders, and average daily footfall trends |
| Store-Level Performance | Compared stores with high footfall vs high sales to assess conversion efficiency |
| Channel Performance | Visualized footfall, sales, and average spend per head across Dine-in, Takeaway, Delivery, Drive-thru |
| Weekly Patterns | Identified high-traffic (weekends) and low-traffic (Mondays, Fridays) days |
| Monthly & Seasonal Trends | Analyzed footfall and sales across months to detect seasonality |
| Units per Order & Spend | Examined average units per order and average spend per customer |
| Regional Distribution | Compared sales and footfall patterns across regions |
| Time-Series Trends | Visualized daily, weekly, and monthly trends in traffic and sales |

EDA helped shape **dashboard design, KPI selection, and analytical focus** for deeper footfall and sales performance analysis.

---

## 📊 STATISTICAL ANALYSIS

To complement EDA, **quantitative metrics and comparisons** were calculated to measure **footfall and sales performance** formally.

### 🔢 Methods Applied

| Method | Purpose |
|--------|---------|
| Average & Total Metrics | Calculated average daily footfall, average daily sales, total orders |
| Max/Min Analysis | Identified peak and lowest sales and footfall days |
| Ranking Analysis | Ranked stores and regions by sales and footfall |
| Conversion Analysis | Compared high-footfall stores vs high-sales stores to measure efficiency |
| Time-Based Comparison | Compared weekly, monthly, and seasonal trends |

### 📐 Metrics Evaluated

- Average Daily Sales  
- Total Orders  
- Average Daily Footfall  
- Average Units per Order  
- Average Spend per Head  
- Max/Min Footfall  
- Active Sales Days per store  
- Weekly and Monthly Trends  

This quantitative approach **measured footfall performance, tracked operational efficiency, and supported further insights**, complementing patterns observed in EDA.

---

## 📈 OVERALL PERFORMANCE

Footfall and sales performance across the business shows **clear patterns and operational benchmarks**.

| Metric | Value | Notes |
|--------|-------|-------|
| **Average Daily Sales** | ₦4.11M | Consistent daily revenue across stores |
| **Average Daily Footfall** | 684.31 customers | Typical daily traffic per store |
| **Maximum Footfall (Peak)** | 1,000 customers | Weekend peak demand |
| **Minimum Footfall** | 302 customers | Low weekday traffic |
| **Units per Order** | 3.03 | Indicates common basket size or combo purchase behavior |
| **Average Spend per Head** | ₦6,000 | Stable across all channels |
| **Total Orders** | 750,000 | Total transactions recorded |
| **Primary Sales Channel** | Dine-in | Highest footfall and sales volume |
| **Top Regions** | North-West & North-East | Highest traffic and sales performance |
| **Star Store** | Store 11 | Leading store in daily sales |

This high-level overview **provides a clear picture of footfall, sales, and customer behavior**, and sets the stage for deeper analysis at the **store, channel, and regional level**, helping management make informed decisions on staffing, promotions, and operational planning.

## 💡 INSIGHTS & RECOMMENDATIONS

This section summarizes key observations from the footfall analysis and provides actionable recommendations for business and operational improvements.

---

### 📊 Core Performance KPIs

| Metric | Value | Notes |
|--------|-------|-------|
| **Average Daily Sales** | ₦4.11M | Average sales across all stores per day |
| **Average Daily Footfall** | 684.31 customers | Typical daily traffic per store |
| **Maximum Footfall (Peak)** | 1,000 customers | Highest daily traffic observed |
| **Minimum Footfall** | 302 customers | Lowest daily traffic observed |
| **Units per Order** | 3.03 | Average items per transaction; indicates strong combo/bucket culture |
| **Average Spend per Head** | ₦6,000 | Stable across Dine-in, Takeaway, Drive-thru |

---

### 🛍️ Channel Performance Analysis

| Channel | Key Observations |
|---------|-----------------|
| **Dine-In** | Highest traffic and total quantity sold; likely used by families/groups; generates highest daily sales |
| **Drive-Thru** | Highest average spend per customer (₦6,003) |
| **Takeaway** | Average spend per customer ₦6,002 |
| **Delivery** | Lowest average spend per customer ₦5,998; average selling price consistent (~₦1,980) across all channels |

---

### 📅 Weekly Activity Insights

- **Weekend Peaks:** Saturday (₦4.99M, 834 customers) and Sunday (₦4.94M, 832 customers) dominate traffic and revenue.  
- **Weekday Lows:** Monday and Friday consistently record lower sales and footfall.  

---

### 🏬 Store & Sales Performance

- **Star Store:** KFC Store 11 leads in daily sales (₦69,847.31).  
- **High Footfall ≠ Highest Sales:** Store 51 has higher footfall but lower sales than Store 59, suggesting better conversion efficiency or higher average transaction value at Store 59.  

---

### 🌍 Regional Performance

| Region | Average Daily Sales | Notes |
|--------|-------------------|-------|
| Northwest | ₦686.13K | Slightly leads in sales and total orders |
| Northeast | Similar to Northwest | High-volume region |
| South-South | Similar to Northeast | Balanced sales |
| North Central | Lowest | Gap minimal; consistent national pricing and behavior |

---

### 📈 Monthly Performance & Seasonality

- **Peak Month:** December — 249,315 items sold, 887 daily footfall, 82,500 orders.  
- **Lowest Month:** January — 124,589 items sold, 41,250 orders.  
- **Trend:** Steady increase in footfall drives proportional growth in orders and quantity sold throughout the year.  

---

### 🎯 Recommendations

#### 1️⃣ Balance Weekly Traffic
- **Mid-Week Promotions:** Introduce offers like “Tuesday Family Platter” for Dine-in to boost traffic during slower days.  
- **Corporate & Office Outreach:** Launch Corporate Lunch Specials in Northwest and Northeast to drive Monday–Thursday footfall.  

#### 2️⃣ Scale for Seasonality
- Use quieter Q1 (Jan–Mar) for **staff training, process improvement, and store optimization**.  
- Begin gradual hiring in Q3 to prepare for high-demand months.  

#### 3️⃣ Maximize Average Spend
- Introduce **delivery-exclusive bundles** slightly above ₦5,998 to increase revenue without reducing demand.  
- Focus on **smart upselling** rather than price increases across all channels.  

#### 4️⃣ Optimize Regional Strengths
- Northwest and Northeast are growth engines — optimize **store layout and dine-in efficiency** for faster service and higher throughput.

## MAINDASHBOARD

The Power BI dashboard provides **interactive visualizations** to explore footfall patterns, daily sales, units per order, and average spend per customer across stores, channels, and regions. It enables management to **monitor performance, identify trends, and make data-driven operational decisions**.


