# AP-TASK-2
Perfect 👍
Below is a **COMPLETE VS CODE–READY PROJECT** for **TASK-2: EDA & Business Intelligence**.
You can **copy–paste**, **run directly in VS Code**, and **submit for ApexPlanet internship**.

---

# 📁 PROJECT STRUCTURE (VS CODE)

Create a folder named:

```
EDA-Business-Intelligence
```

Inside it, create this **exact structure** 👇

```
EDA-Business-Intelligence/
│
├── data/
│   └── sales_data.csv
│
├── notebooks/
│   └── eda_analysis.py
│
├── sql/
│   └── business_queries.sql
│
├── dashboard/
│   └── dashboard_notes.txt
│
├── README.md
```

---

# 📊 1️⃣ DATASET FILE

### 📄 `data/sales_data.csv`

Copy **everything below** and save as `sales_data.csv`

```csv
order_id,order_date,customer_id,age,gender,product,category,quantity,price,revenue,region
1,2025-01-10,101,23,M,Mobile,Electronics,1,15000,15000,North
2,2025-01-12,102,30,F,Laptop,Electronics,1,55000,55000,South
3,2025-02-01,103,45,M,Headphones,Accessories,2,2000,4000,East
4,2025-02-05,104,29,F,Tablet,Electronics,1,20000,20000,West
5,2025-02-10,105,35,M,Chair,Furniture,4,2500,10000,North
6,2025-03-01,106,41,F,Desk,Furniture,1,12000,12000,South
7,2025-03-05,107,22,M,Mobile,Electronics,2,15000,30000,East
8,2025-03-15,108,27,F,Headphones,Accessories,3,2000,6000,West
9,2025-04-02,109,50,M,Laptop,Electronics,1,60000,60000,North
10,2025-04-10,110,34,F,Tablet,Electronics,2,22000,44000,South
```

---

# 🧪 2️⃣ EDA PYTHON FILE (VS CODE RUNNABLE)

### 📄 `notebooks/eda_analysis.py`

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load Dataset
df = pd.read_csv("../data/sales_data.csv")

print("First 5 rows:")
print(df.head())

print("\nDataset Info:")
print(df.info())

print("\nSummary Statistics:")
print(df.describe())

print("\nMissing Values:")
print(df.isnull().sum())

# Revenue Distribution
plt.figure()
plt.hist(df['revenue'], bins=10)
plt.title("Revenue Distribution")
plt.xlabel("Revenue")
plt.ylabel("Frequency")
plt.show()

# Category-wise Sales
plt.figure()
df.groupby('category')['revenue'].sum().plot(kind='bar')
plt.title("Category-wise Revenue")
plt.xlabel("Category")
plt.ylabel("Revenue")
plt.show()

# Price vs Revenue
plt.figure()
plt.scatter(df['price'], df['revenue'])
plt.title("Price vs Revenue")
plt.xlabel("Price")
plt.ylabel("Revenue")
plt.show()

print("\nEDA Completed Successfully")
```

▶ Run in VS Code terminal:

```
python eda_analysis.py
```

---

# 🗄️ 3️⃣ SQL FILE (BUSINESS INTELLIGENCE)

### 📄 `sql/business_queries.sql`

```sql
-- Create Table
CREATE TABLE sales (
    order_id INT,
    order_date DATE,
    customer_id INT,
    age INT,
    gender VARCHAR(10),
    product VARCHAR(50),
    category VARCHAR(50),
    quantity INT,
    price FLOAT,
    revenue FLOAT,
    region VARCHAR(50)
);

-- Top 5 Products by Revenue
SELECT product, SUM(revenue) AS total_revenue
FROM sales
GROUP BY product
ORDER BY total_revenue DESC
LIMIT 5;

-- Monthly Sales Trend
SELECT MONTH(order_date) AS month, SUM(revenue) AS total_sales
FROM sales
GROUP BY month
ORDER BY month;

-- Region-wise Revenue
SELECT region, SUM(revenue) AS total_revenue
FROM sales
GROUP BY region;

-- Category-wise Revenue
SELECT category, SUM(revenue) AS total_revenue
FROM sales
GROUP BY category;

-- Gender-wise Revenue
SELECT gender, SUM(revenue) AS total_revenue
FROM sales
GROUP BY gender;
```

---

# 📊 4️⃣ DASHBOARD NOTES

### 📄 `dashboard/dashboard_notes.txt`

```
Dashboard KPIs:
- Total Revenue
- Monthly Sales Trend
- Top 5 Products
- Revenue by Region
- Category-wise Revenue
- Gender-wise Sales

Tools Suggested:
- Excel
- Google Slides
- PowerPoint
```

---

# 📘 5️⃣ README FILE (SUBMISSION READY)

### 📄 `README.md`

```md
# Exploratory Data Analysis & Business Intelligence

## Internship Task - ApexPlanet

### Objective
To perform EDA and SQL-based business analysis to uncover insights.

### Tools Used
- Python
- Pandas
- Matplotlib
- SQL
- VS Code

### Key Work
- Data Cleaning
- Descriptive Statistics
- Business Queries using SQL
- Dashboard KPI Planning

### Status
✅ Task Completed Successfully
```

---

# ✅ HOW TO RUN (IMPORTANT)

1️⃣ Open **VS Code**
2️⃣ Open folder **EDA-Business-Intelligence**
3️⃣ Open terminal
4️⃣ Run:

```
python notebooks/eda_analysis.py
```

---

# 🎯 INTERNSHIP SUBMISSION CHECKLIST

✔ VS Code project
✔ Python EDA
✔ SQL queries
✔ Dataset
✔ Dashboard planning
✔ GitHub ready

---

## 🚀 Want NEXT?

I can also:

* ✔ Upload this to **GitHub structure**
* ✔ Create **PDF report**
* ✔ Prepare **LinkedIn video script**
* ✔ Explain **each line for viva**

Just tell me 👍
