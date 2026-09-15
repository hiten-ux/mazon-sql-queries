# Amazon-sql-queries
# 🛒 Olist E-Commerce SQL Analysis

SQL solutions to 14 real-world business questions on the Olist Brazilian E-Commerce dataset (framed here as an "Amazon Brazil" case study). This project covers seller performance, revenue trends, payment behavior, customer value, and delivery metrics — the kind of questions logistics, finance, CRM, and growth teams actually ask.

## 📊 About This Project

I worked through 14 business scenarios end-to-end — starting from the stakeholder's question ("why does this matter"), translating it into a SQL query, and writing production-style logic using **views** and **window functions** instead of quick one-off queries. This was built as part of my Data Analytics + Gen AI coursework, applied to a public e-commerce dataset.

## 🗂️ Dataset

📦 **Full dataset (MySQL dump):** the Kaggle link is in [`Analysis/Raw File`](Analysis/Raw%20File)

Based on the public Olist Brazilian E-Commerce dataset, structured into a MySQL schema with the following tables:

- `customers`
- `orders`
- `order_items`
- `order_payments`
- `order_reviews`
- `products`
- `sellers`
- `product_category_name_translation`

Download the dataset from the link in `Analysis/Raw File` and import it into MySQL before running the queries in `Analysis/Cleaned Data`.

## ❓ Questions Answered

| # | Question |
|---|----------|
| 1️⃣ | Total orders fulfilled by each seller state |
| 2️⃣ | Cumulative revenue per product category over time |
| 3️⃣ | Most used payment method and average order value per payment type |
| 4️⃣ | Customer who has spent the most across all orders |
| 5️⃣ | Average review score per product category |
| 6️⃣ | Total orders placed by each customer, broken down by state |
| 7️⃣ | Sellers who registered but never fulfilled an order |
| 8️⃣ | Top 5 product categories by total revenue |
| 9️⃣ | Median delivery time (in days) between order placement and delivery |
| 🔟 | Products that have never been ordered |
| 1️⃣1️⃣ | Sellers who fulfilled more orders than the platform average |
| 1️⃣2️⃣ | States with the highest average review score for delivered orders |
| 1️⃣3️⃣ | Customers who placed orders but never left a review |
| 1️⃣4️⃣ | Month with the highest number of orders placed |

## 🛠️ What I Used

- ✅ **`CREATE VIEW`** — to break each question into a clean, readable base query before ranking or filtering
- ✅ **Window functions** — `RANK()`, `SUM() OVER()`, `ROW_NUMBER()`, `AVG() OVER()` — for rankings, running totals, and median calculation
- ✅ **`NOT EXISTS`** — for "no matching record" checks (dormant sellers, unordered products, unreviewed customers)

## ⚠️ Notes

- Written for **MySQL 8.0+** (window function support required)
- Views persist after creation — run `DROP VIEW IF EXISTS <name>;` before re-running the script, or use `CREATE OR REPLACE VIEW`

## 📁 Files

- `Analysis/Cleaned Data` — all 14 queries with supporting views
- `Analysis/Raw File` — link to the full dataset on Kaggle

## 👤 Author
Hiten Solanki BCom student | Data Analytics + Gen AI learner | Building toward a Business Analyst role 🔗 github.com/hiten-ux

**Hiten Solanki**
BCom student | Data Analytics + Gen AI learner | Building toward a Business Analyst role
🔗 [github.com/hiten-ux](https://github.com/hiten-ux)
