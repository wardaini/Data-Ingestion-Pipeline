# Data Ingestion Pipeline – Transaction Log Cleaning

This project is a Python-based data ingestion pipeline for cleaning and analyzing e-commerce transaction logs. Built entirely with Python built-in functions (no pandas or numpy), it processes raw JSON data, filters out anomalies, normalizes text, and generates business insights.

## 📌 Project Overview
- **Objective**: Clean raw transaction data (remove negative/null prices, empty product names, standardize categories) and compute:
  - Unique customers (using `set`)
  - Total revenue per category (using `dict`)
- **Data Source**: `transaction_log.json` (100 transactions)
- **Constraints**: Only built-in Python data structures (list, set, dict) and control flow (loops, if-else, functions).

## 🗂️ Data Structure
Each transaction is a dictionary with the following keys:
- `transaction_id`: Unique transaction ID
- `timestamp`: ISO 8601 timestamp
- `customer_id`: Customer ID
- `product_category`: Product category (with inconsistent formatting)
- `item_name`: Product name
- `price`: Price (may be negative or null)
- `payment_method`: Payment method

## 🔧 Core Functions
All functions are defined in a dedicated code cell:
- `load_data_from_file()`: Reads JSON file.
- `clean_data()`: Filters invalid records and normalizes `product_category` to lowercase + strip.
- `get_unique_customers()`: Returns a set of unique `customer_id`.
- `aggregate_revenue_per_category()`: Calculates total revenue (sum of `price`) per category.

## 🚀 How to Run
1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Upload `transaction_log.json` to the Colab runtime (using the file browser).
3. Run all cells (Runtime → Run all).
4. View the cleaned data stats and revenue report.

## 📊 Results (from 100 transactions)
- **Raw data**: 100 records
- **Cleaned data**: 92 records (8 invalid records removed)
- **Unique customers**: 36
- **Revenue per category**:
  - elektronik: 3,150,000
  - makanan: 6,100,000
  - fashion: 5,650,000
  - home appliances: 7,250,000
  - alat tulis: 3,500,000
  - (empty category): 600,000

## 🛠️ Technologies
- Python 3 (built-in modules: `json`, `urllib` – if reading from URL)
- Google Colab / Jupyter Notebook
- Git & GitHub

## 📬 Contact
Created by wardaini – feel free to reach out!
