# 🛒 Retail Data Pipeline and Analytics (Python + SQL)

An end-to-end data engineering and analytics project. This project demonstrates automated data ingestion via Kaggle API, data cleaning and feature engineering in Python (Pandas), automated database load into Microsoft SQL Server using SQLAlchemy, and strategic business analysis using complex SQL queries [1-3].

---

## 📌 Project Architecture & Workflow

1. **Data Ingestion**: Programmatically download the retail orders dataset from Kaggle using the Kaggle API and extract the zip archive in Python [1, 4].
2. **Data Cleaning & Transformation (Pandas)**:
   - Handle missing and dirty values (e.g., mapping strings like `'not available'` and `'unknown'` to null values) [5].
   - Standardize column names to `snake_case` format [6, 7].
   - Parse string dates into proper `datetime` objects (`YYYY-MM-DD`) [8].
   - Perform feature engineering to derive business metrics: `discount_amount`, `sale_price`, and `profit` [7].
3. **Data Loading (ETL)**: Establish a database connection using `SQLAlchemy` and `pyodbc` to load clean, typed data into MS SQL Server [2, 9, 10].
4. **Data Analysis (SQL)**: Write analytical SQL queries incorporating Window Functions, Common Table Expressions (CTEs), and Aggregations to extract business insights [11-14].

---

## 🛠️ Tech Stack & Tools

* **Language**: Python 3.x
* **Data Processing**: Pandas, Zipfile [4, 15]
* **Database & ORM**: MS SQL Server, SQLAlchemy, PyODBC [2, 9]
* **Data Source**: Kaggle API (`orders.csv`) [1, 4]
* **Analytics**: SQL (CTEs, Window Functions, Aggregations) [12, 13]

---

## 📂 Project Structure

├── data/                      # Contains Kaggle API config & extracted datasets ├── notebooks/ │   └── retail_etl_pipeline.ipynb # Python ETL script for cleaning & DB loading ├── sql/ │   └── business_queries.sql   # SQL scripts answering business analysis questions ├── README.md                  # Project documentation └── requirements.txt           # Python dependencies

---

## 📊 Key Business Questions Solved in SQL

The project answers core retail performance questions [3, 12-14, 16]:
1. **Top 10 Revenue Generators**: Identify the top 10 highest revenue-generating products [3, 11].
2. **Regional Top Sellers**: Find the top 5 highest-selling products across each geographic region using ranking window functions [16].
3. **Month-over-Month Growth**: Compare month-by-month sales totals between 2022 and 2023 [12, 17].
4. **Category Peak Months**: Determine the highest-selling month for each product category [13, 18].
5. **YoY Profit Growth**: Identify which product subcategory achieved the highest year-over-year profit growth percentage in 2023 compared to 2022 [14].

---