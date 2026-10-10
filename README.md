# 📊 Pinnacle Meta Ads Campaign Dataset – Marketing Analytics & Performance Optimization eda

## tools : Python,numpy,pandas,matplotlib,seaborn,excel,pivot

## 📌 Project Overview

This project focuses on cleaning, transforming, and analyzing a Meta Ads campaign dataset containing:

- 10000+ rows (Ads)
- ~50 structured columns (after preprocessing)
- Embedded JSON targeting specifications
- Campaign, Ad Set, and Ad-level performance metrics

The dataset required preprocessing due to:
- Semi-structured JSON columns
- Redundant system-generated metrics
- Hourly and weekday breakdown columns
- High null-value fields
- Mixed data types

The primary objective was to prepare the dataset in Excel and perform advanced Exploratory Data Analysis (EDA) in Python to generate actionable marketing insights.

---

# 🧹 Phase 1: Excel Data Cleaning & Structuring

## 🔹 JSON Column Handling
- Extracted targeting information (age range, interests, behaviors, geo-location).
- Removed raw nested JSON columns after flattening key fields.
- Reduced structural complexity for analytical clarity.

## 🔹 Data Standardization
- Converted dates, currency, and numeric fields to appropriate formats.
- Ensured Ad ID uniqueness.
- Cleaned text-based NaN values to avoid Python parsing issues.

## 🔹 Column Reduction & Optimization
- Removed columns with 80–90% null values.
- Dropped hourly breakdown columns (recalculable in Python).
- Deleted weekday-specific columns (can be derived from date).
- Removed derivable metrics such as Ad Rank, Top 25% CPC etc.
- Focused dataset on core KPIs.

## 🔹 Feature Engineering

Created new calculated metrics:

- Engagement Rate (24hr, 7-day, overall)
- Conversion Rate (24hr, 7-day, overall)
- Monthly performance column
- Date range & time-based derived columns

---

# 📊 Excel Pivot Analysis

Performed structured pivot summaries for:

### Platform-Level Analysis
- Total Spend
- Total Conversions
- Average CPC
- Conversion Rate

### Campaign-Level Performance
- Payments
- Cost per Payment (CPLPV)
- ROI %
- CTR %

### Daily Performance Summary
- Day-wise payments
- CPC trends
- Conversion trends

---

# 🐍 Phase 2: Python-Based EDA

Libraries Used:
- Pandas
- NumPy
- Matplotlib
- Seaborn

Analysis Performed:
- KPI recalculation validation
- Null and anomaly checks
- Distribution analysis
- Platform comparison
- Campaign efficiency benchmarking
- Correlation analysis
- Outlier detection

---

# 📈 Final Insights & Optimization Decisions

## 🔹 Ad-Level Performance Decision

Out of 237 Ads:

- ✅ 24 Ads meet performance benchmarks  
  (High CTR + Low CPC + Strong Conversion Rate)

- ⏸ 183 Ads currently paused  
  (Below target benchmark performance)

- ❌ 30 Ads recommended for discontinuation  
  (Low CTR, High CPC, Poor Conversion)

### Platform Performance (Winning Platform)

Ads Recommended to Continue:

- Facebook: 6
- Instagram: 7
- Threads: 11

📌 **Threads emerged as the strongest performing platform.**

---

# 📅 Best Day to Run Ads

**Tuesday** is the highest performing day:

- 308 Payments
- Lowest CPC: ₹3.5
- Above-average conversion rate

📌 Recommendation: Increase budget allocation on Tuesdays.

---

# 🎯 Campaign-Level Insights

## 🥇 Best Performing Campaign

### "VM || Delhi NCR || Traffic"

- Lowest CPC: ₹1.16
- Highest Payments: 568
- Strong Conversion Rate: 0.77

📌 Recommended to continue & scale.

---

## ⚠ Needs Optimization

### "Web App | Conversion"

- Highest Spend: ₹181K+
- High CPC: ₹13.26
- Low Conversion Rate: 0.37

📌 Requires targeting and cost optimization.

---

## 📣 Awareness Campaign Analysis

### "VM Brand Awareness"

- 8.79% of total spend
- Very cost-efficient CTR: ₹0.08
- Poor in direct conversions

📌 Effective for reach, not for payment conversion objective.

---

## ❌ Least Performing Campaigns (Discontinue)

- "ToF Engagement"
- "Straight Outta"

Both campaigns generated:
- 0 Payments
- Consumed budget

📌 Recommended to discontinue.

---

# 👥 Ad Set-Level Insights

## 🥇 Top Performing Ad Set

### "Women - Clubbed Audience"

- 567 Payments
- Lowest CPLPV: ₹2.30
- Strong Conversion Rate: 0.81

📌 High-performing segment – recommended to scale.

---

### "RMK - Waitlist"

- Conversion Rate: 1.05
- CPLPV: ₹18.50
- Slightly higher CPC but strong efficiency

📌 Maintain & optimize budget.

---

## ❌ Underperforming Ad Sets (Discontinue)

Ad sets with 0 payments but budget consumption:

- Dating Apps
- Entrepreneurship Insta
- Travel Insta
- Interest-Based Dinner

📌 Recommended to stop to prevent further budget leakage.

---

# 📢 Top Performing Ads

Top 5 Ads (High Spend % + High Payments):

- Monkey UGC
- Ad – 1 (5 Strangers)
- Saturday Night
- Ranveer
- Instagram Post – Latest StepOut Dinner

### 🏆 Top 3 Ads (Most Efficient)

- Monkey UGC
- Saturday Night
- Ranveer

Metrics:
- High Payments
- CPLPV below ₹1.5
- Conversion Rate ~0.70

📌 Recommended for scaling.

---

# 🛠 Tech Stack

- Microsoft Excel (Cleaning + Pivot Analysis)
- Python (Pandas, NumPy)
- Matplotlib & Seaborn
- Git & GitHub

---

# 🚀 Project Value

This project demonstrates:

- Handling of semi-structured marketing export data
- JSON-based targeting interpretation
- KPI modeling & performance benchmarking
- Campaign optimization strategy development
- Data-driven decision making for ad scaling or discontinuation

---

 ---

# 📐 KPI & Metric Formulas Used in Analysis

Below are the key formulas used to calculate performance metrics in Excel and Python.

---

## 🔹 Core Performance Metrics

### 1️⃣ Click-Through Rate (CTR)

CTR (%) = (Clicks / Impressions) × 100

---

### 2️⃣ Cost Per Click (CPC)

CPC = Total Spend / Total Clicks

---

### 3️⃣ Conversion Rate (CR)

Conversion Rate = Conversions / Clicks

OR (if calculated from impressions)

Conversion Rate = Conversions / Impressions

---

### 4️⃣ Cost Per Acquisition (CPA)

CPA = Total Spend / Total Conversions

---

### 5️⃣ Cost Per Landing Page View (CPLPV)

CPLPV = Total Spend / Landing Page Views

---

### 6️⃣ Engagement Rate

Engagement Rate = Total Engagements / Impressions

---

### 7️⃣ Return on Investment (ROI)

ROI (%) = ((Revenue – Spend) / Spend) × 100

---

## 🔹 Time-Based Metrics

### 8️⃣ Daily Performance

Daily Impressions = SUM(Impressions grouped by Date)

Daily Conversions = SUM(Conversions grouped by Date)

Daily CPC = Daily Spend / Daily Clicks

---

### 9️⃣ Monthly Performance

Monthly Spend = SUM(Spend grouped by Month)

Monthly Conversion Rate = Monthly Conversions / Monthly Clicks

---

## 🔹 Benchmark Comparison Metrics

### 10️⃣ Performance vs Group Average

Metric Ratio = Ad Metric / Group Average Metric

If:
- < 0.85 → Underperforming
- > 1.15 → Overperforming

---

### 11️⃣ Performance vs Top 25 Percentile

Metric Ratio = Ad Metric / Top 25% Benchmark

Used to identify high-performing ads relative to best performers.

---

## 🔹 Decision Threshold Logic

### Continue Criteria:
- CTR above average
- CPC below average
- Conversion Rate above benchmark

### Pause Criteria:
- CTR near average
- Moderate CPC
- Inconsistent conversions

### Discontinue Criteria:
- Conversion Rate < 0.01
- High CPA
- Zero payments despite spend

---

## 🔹 Example Excel Formula Implementations

CTR:
= (Clicks / Impressions) * 100

CPC:
= Spend / Clicks

Conversion Rate:
= Conversions / Clicks

CPA:
= Spend / Conversions

ROI:
= ((Revenue - Spend) / Spend) * 100

---

> All KPIs were validated both in Excel and re-calculated in Python (Pandas) to ensure analytical consistency.
---

> This project simulates a real-world marketing analytics workflow where campaign data is cleaned, evaluated, and optimized using structured KPI benchmarks.

