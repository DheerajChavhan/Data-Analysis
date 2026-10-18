# 🛍️ Customer Shopping Behavior Analysis

A comprehensive end-to-end data analysis project that explores customer purchasing patterns, segmentation, revenue drivers, and discount effectiveness using **Python**, **SQL (PostgreSQL)**, and **Power BI**.

---

## 📁 Project Structure

```
Data Analysis/
│
└── Customer_Shopping_Behaviour/
    ├── customer_shopping_behavior.csv             # Raw dataset (3,900 records)
    ├── Customer_Shopping_Behavior_Analysis.ipynb  # Python EDA & data cleaning notebook
    ├── customer.sql                               # SQL queries for business questions
    ├── customer_behavior.pbix                     # Power BI dashboard
    ├── customer_behavior.pdf                      # Power BI dashboard (PDF export)
    ├── Customer Shopping Behavior Analysis.pdf    # Full analysis report
    ├── Customer-Shopping-Behavior-Analysis.pptx   # Presentation deck
    └── Business Problem Document.pdf              # Problem statement
```

---

## 📊 Dataset Overview

- **Source:** `customer_shopping_behavior.csv`
- **Records:** 3,900 customer transactions
- **Features:** 18 columns

| Column | Type | Description |
|---|---|---|
| Customer ID | int | Unique customer identifier |
| Age | int | Customer age (18–70) |
| Gender | str | Male / Female |
| Item Purchased | str | Product name (25 unique items) |
| Category | str | Clothing, Footwear, Outerwear, Accessories |
| Purchase Amount (USD) | int | Transaction value ($20–$100) |
| Location | str | US state (50 states) |
| Size | str | XS, S, M, L |
| Color | str | 25 color variants |
| Season | str | Spring, Summer, Fall, Winter |
| Review Rating | float | Rating (2.5–5.0); 37 missing values imputed |
| Subscription Status | str | Yes / No |
| Shipping Type | str | Standard, Express, Free Shipping, etc. |
| Discount Applied | str | Yes / No |
| Promo Code Used | str | Yes / No |
| Previous Purchases | int | Count of prior orders (1–50) |
| Payment Method | str | PayPal, Credit Card, Cash, Venmo, etc. |
| Frequency of Purchases | str | Weekly, Fortnightly, Monthly, etc. |

---

## 🔧 Data Cleaning (Python / Pandas)

Performed in `Customer_Shopping_Behaviour/Customer_Shopping_Behavior_Analysis.ipynb`:

- ✅ Checked for null values — only **37 missing** in `Review Rating`
- ✅ Imputed missing ratings using **category-wise mean** (group-level imputation)
- ✅ Standardized column names to **snake_case**
- ✅ Renamed `purchase_amount_(usd)` → `purchase_amount`
- ✅ Created an **`age_group`** feature using quartile-based binning:
  - `Young_Adult` | `Adult` | `Middle-Aged` | `Senior`

---

## 🗃️ SQL Analysis

All queries are in `Customer_Shopping_Behaviour/customer.sql` — targeting PostgreSQL.

| # | Business Question |
|---|---|
| Q1 | Total revenue by gender |
| Q2 | Discount users who still spent above average |
| Q3 | Top 5 products by average review rating |
| Q4 | Average purchase amount: Standard vs. Express shipping |
| Q5 | Subscriber vs. non-subscriber spend comparison |
| Q6 | Top 5 products with highest discount application rate |
| Q7 | Customer segmentation: New / Returning / Loyal |
| Q8 | Top 3 products per category (using window functions) |
| Q9 | Repeat buyers (> 5 purchases) and subscription likelihood |
| Q10 | Revenue contribution by age group |

---

## 📈 Dashboards & Reports

| File | Description |
|---|---|
| `customer_behavior.pbix` | Interactive Power BI dashboard |
| `customer_behavior.pdf` | PDF export of the Power BI dashboard |
| `Customer Shopping Behavior Analysis.pdf` | Detailed analysis report |
| `Customer-Shopping-Behavior-Analysis.pptx` | Stakeholder presentation |
| `Business Problem Document.pdf` | Problem statement & objectives |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** (Pandas) | Data cleaning & EDA |
| **Jupyter Notebook** | Interactive analysis environment |
| **PostgreSQL / SQL** | Business question querying |
| **Power BI** | Interactive dashboards & visualization |

---

## 🚀 Getting Started

### Python Notebook
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install pandas jupyter
   ```
3. Open the notebook:
   ```bash
   jupyter notebook "Customer_Shopping_Behaviour/Customer_Shopping_Behavior_Analysis.ipynb"
   ```

### SQL Queries
1. Load `customer_shopping_behavior.csv` into a PostgreSQL table named `customer`
2. Run queries from `customer.sql` in your preferred SQL client (e.g., pgAdmin, DBeaver)

### Power BI Dashboard
1. Open `customer_behavior.pbix` in **Power BI Desktop**
2. Update the data source path to point to the local CSV file if needed

---

## 👤 Author

**Dheeraj Chavhan**  
[GitHub: DheerajChavhan/Data-Analysis](https://github.com/DheerajChavhan/Data-Analysis)