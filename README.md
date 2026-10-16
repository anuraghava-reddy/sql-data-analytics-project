# 📊 SQL Sales Analytics Project

End-to-end exploratory and advanced data analysis of a retail sales dataset using **SQL Server**. The project turns raw sales, customer, and product data into business answers: who the best customers are, which products drive revenue, how sales trend over time, and where performance is slipping.

I built this as part of my move into data analytics, after ~7 years in construction and engineering management. I spent those years planning resources and tracking site performance across multiple projects. This project is where I practise the same kind of thinking with SQL.

---

## 🎯 Business Questions Answered

- How is revenue trending month over month and year over year?
- Which products and categories contribute most to total sales?
- Who are the top customers, and how can customers be segmented (VIP / Regular / New)?
- Which products are performing above or below their average?
- What does the running total of sales look like over time?

---

## 🗂️ Dataset & Data Model

The data follows a **star schema** in a `gold` layer:

| Table | Type | Description |
|---|---|---|
| `gold.fact_sales` | Fact | Order-level sales transactions (order date, quantity, price, sales amount) |
| `gold.dim_customers` | Dimension | Customer details (name, country, gender, birthdate) |
| `gold.dim_products` | Dimension | Product details (category, subcategory, cost, product line) |

---

## 🔍 Analysis Workflow

**Part 1: Exploratory Data Analysis (EDA)**

1. **Database exploration**: tables, columns, and structure
2. **Dimensions exploration**: unique countries, categories, and products
3. **Date exploration**: data range, first and last orders, customer ages
4. **Measures exploration**: total sales, quantity, orders, and customers
5. **Magnitude analysis**: comparing measures across dimensions
6. **Ranking analysis**: top and bottom performers

**Part 2: Advanced Analytics**

7. **Change over time**: monthly and yearly trends
8. **Cumulative analysis**: running totals and moving averages
9. **Performance analysis**: current vs. average and vs. previous year
10. **Data segmentation**: grouping customers and products into segments
11. **Part-to-whole**: each category's share of total sales
12. **Customer report**: a reusable view of customer KPIs
13. **Product report**: a reusable view of product KPIs

---

## 🛠️ SQL Techniques Used

- Aggregations with `GROUP BY` and `HAVING`
- Joins across fact and dimension tables
- Window functions: `RANK()`, `ROW_NUMBER()`, `LAG()`, `SUM() OVER()`, `AVG() OVER()`
- CTEs for readable, step-by-step logic
- `CASE WHEN` for segmentation and business rules
- Date functions: `DATETRUNC()`, `DATEDIFF()`, `YEAR()`, `MONTH()`
- Views for reusable reporting layers

---

## 💡 Key Insights

> _Fill these in from your own query results. Concrete numbers make the project stand out._

- 📈 _e.g. Sales peaked in [month/year], driven by [category]._
- 🚲 _e.g. [Category] accounts for ~XX% of total revenue._
- 👥 _e.g. VIP customers make up XX% of customers but XX% of sales._
- ⚠️ _e.g. [Product] has been below its average sales for X consecutive years._

---

## 📁 Repository Structure

```
sql-data-analytics-project/
├── datasets/          # Source CSV files
├── scripts/           # SQL scripts, numbered by analysis step
│   ├── 00_init_database.sql
│   ├── 01_database_exploration.sql
│   ├── ...
│   └── 13_report_products.sql
└── README.md
```

---

## ▶️ How to Run

1. Install **SQL Server** (Express is fine) and **SSMS** or Azure Data Studio.
2. Run `scripts/00_init_database.sql` to create the database and load the data.
3. Run the remaining scripts in order, or open any script on its own to explore a single analysis.

---

## 🙏 Acknowledgements

This project is based on the SQL Data Analytics course by [Data With Baraa](https://www.youtube.com/@DataWithBaraa). The original materials are licensed under the MIT License. My additions include the business questions, my own insights, and extended queries.

---

## 👋 About Me

Hi there! I'm **Anuraghava Reddy A**. I'm a former Senior Manager with ~7 years of experience in civil engineering and construction management, where I led resource planning and operations across multiple projects. I'm now moving into **data analytics and data engineering**, building hands-on projects that turn raw data into clear business decisions.

- 💼 LinkedIn: www.linkedin.com/in/anuraghava-reddy-anugula-023605159
- 🐙 GitHub: anuraghava-reddy
- 📧 Email: aanuraghavareddy123@gmail.com

⭐ If you found this project useful, feel free to star the repo!

