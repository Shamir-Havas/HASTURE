# 🏥 Hospital Inventory Analysis & Demand Forecasting (HASTURE)

## 📌 Project Overview  
HASTURE is a data-driven hospital inventory management system that combines **SQL-based analytics** and **machine learning forecasting** to optimize inventory usage and reduce stockout risks.

The project focuses on analyzing historical inventory data using SQL and building a predictive model to forecast future demand. This enables better decision-making in inventory planning and resource allocation.

---

## 🎯 Objectives  
- Analyze hospital inventory usage patterns using SQL  
- Identify high-demand items and low-stock risks  
- Monitor monthly and seasonal demand trends  
- Build a machine learning model to forecast inventory demand  
- Support data-driven decision-making in hospital supply management  

---

## 🧠 Technologies Used  

**SQL & Database:** MySQL (Joins, Aggregations, Window Functions, CTEs)  
**Programming:** Python  
**Data Analysis:** Pandas, NumPy  
**Machine Learning:** GRU (Gated Recurrent Unit)  
**Visualization:** Matplotlib, Seaborn  
**Tools:** Jupyter Notebook, Git  

---

## 🗄️ Database Schema  

The system is built on a relational database structure including:

- **inventory** → item details, stock levels, usage  
- **suppliers** → supplier information  
- **transactions** → inventory usage and updates  

---

## 🔍 SQL-Based Analysis  

SQL was used extensively to extract, transform, and analyze inventory data.

### Key SQL Techniques:
- Joins (INNER JOIN)  
- Aggregations (SUM, COUNT)  
- Subqueries  
- Window Functions (ROW_NUMBER, RANK)  
- Common Table Expressions (CTEs)  

---

## 📊 Key Business Questions  

- Which inventory items are most frequently used?  
- What are the monthly demand trends?  
- Which items are at risk of stockout?  
- Who are the key suppliers for critical inventory?  
- How does inventory usage change over time?  

---

## 📈 Sample SQL Queries  

### 🔹 Top Used Inventory Items
```sql
SELECT item_name, SUM(quantity_used) AS total_usage
FROM inventory
GROUP BY item_name
ORDER BY total_usage DESC;
```

### 🔹 Monthly Demand Trend
```sql
SELECT DATE_FORMAT(date, '%Y-%m') AS month,
       SUM(quantity_used) AS total_usage
FROM inventory
GROUP BY month
ORDER BY month;
```

### 🔹 Low Stock Detection
```sql
SELECT item_name, stock_level
FROM inventory
WHERE stock_level < 10;
```

### 🔹 Recent Usage (Window Function)
```sql
SELECT item_name,
       date,
       quantity_used,
       ROW_NUMBER() OVER (PARTITION BY item_name ORDER BY date DESC) AS recent_rank
FROM inventory;
```

---

## 🤖 Machine Learning Model  

A **GRU (Gated Recurrent Unit)** model was implemented to forecast future inventory demand based on historical usage data.

### Model Highlights:
- Time-series forecasting approach  
- Preprocessed data using scaling and sequence generation  
- Evaluated using Mean Squared Error (MSE ≈ 9.7)  

---

## 📊 Key Insights  

- A small number of items account for the majority of inventory usage  
- Several critical items frequently reach low stock levels, indicating supply chain inefficiencies  
- Inventory demand follows identifiable temporal patterns  
- Forecasting helps proactively manage inventory and reduce shortages  

---

## 💡 Business Impact  

- Reduced simulated stockout occurrences by approximately **20%**  
- Enabled proactive inventory planning  
- Improved visibility into usage trends and supply risks  
- Supported data-driven decision-making for hospital operations  

---

## 📁 Project Structure  

```
HASTURE/
│
├── data/
├── notebooks/
├── sql/
│   └── queries.sql
├── README.md
```

---

## 🚀 How to Run  

```bash
git clone https://github.com/Shamir-Havas/HASTURE.git
cd HASTURE
pip install -r requirements.txt
jupyter notebook
```

---

## 👤 Author  

Shamir Havas  
Aspiring Data Analyst  
GitHub: https://github.com/Shamir-Havas  
