<div align="center">

<img width="725" height="470" alt="image" src="https://github.com/user-attachments/assets/1ead23f5-0de9-4f8a-a61b-e1a2acd2b468" />


# Grocery Store Sales Analytics | 2024–2026


###  Data Sources → Extraction → Cleaning → Storage → Visualization → Graph DB  → Graph Query 

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-KPI%20Measures-5E5E5E?style=for-the-badge)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Relationships-2F855A?style=for-the-badge)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?style=for-the-badge)
![Neo4j](https://img.shields.io/badge/Neo4j-Graph%20DB-008CC1?style=for-the-badge)
![Cypher](https://img.shields.io/badge/Cypher-Query%20Language-2F855A?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)



> A complete end-to-end analyst portfolio project built across three industry-standard BI platforms and a graph database layer.
> Python (Data Extraction) → Raw Data → Cleaning → Modeling → Power BI · Tableau · Looker Studio → Neo4j → Cypher

</div>

---
## Live Demos


| Platform | Link |
|---|---|
| Power BI | See `/Dashboard` folder (`.pbix` file) |
| Tableau Public | [Grocery Store Sales Analytics](https://public.tableau.com/app/profile/ajit.jha/viz/GroceryStoreSalesAnalytics/Dashboard1) |
| Looker Studio | [Live Report](https://datastudio.google.com/s/uQV31od0ALk)|
| GitHub Repo | [Grocery Store Sales Analytics](https://github.com/Ajitjha3095/grocery-store-sales-analytics) |




A portfolio-ready end-to-end analytics project demonstrating **Python, Pandas, Jupyter Notebook, Power BI, Looker, Tableau, Neo4j, and Cypher**.

## 📑 Table of Contents
- [Project Overview](#-project-overview)
- [Business Objective](#business-objective)
- [Dataset](#dataset)
- [Technology Stack](#-technology-stack)
- [Project Workflow](#-project-workflow)
- [Data Preparation](#-data-preparation)
- [BI Dashboards](#-bi-dashboards)
- [Neo4j Graph Database](#-neo4j-graph-database)
- [Graph Model](#-graph-model)
- [Key Business Questions](#-key-business-questions)
- [Key Skills](#-key-skills)
- [Project Structure](#-project-structure)
- [How to Run](#how-to-run)
- [Author](#author)
- [License](#license)
## 📊 Project Overview
This project analyzes grocery-store transactions from **2024–2026** and demonstrates a complete analytics lifecycle:

```text
Raw Data
   ↓
Python + Pandas
   ↓
Cleaning & Validation
   ↓
4 Clean CSV Files
   ↓
Power BI / Looker / Tableau
   ↓
Business Insights

Clean CSV Files
   ↓
Neo4j
   ↓
Graph Modeling
   ↓
Cypher
   ↓
Relationship & Recommendation Analysis
```




##  Business Objective

Grocery stores generate large volumes of transactional data. However, raw sales data alone does not provide meaningful business insights.

This project analyzes grocery store sales data to answer important business questions such as:

- Which product categories generate the most revenue?
- Which products are the top performers?
- Which cities generate the highest sales?
- How do sales change over time?
- Which payment methods are most commonly used?
- Which customer membership groups generate the most profit?
- How can customer and product relationships be analyzed using a graph database?

---


##  Dataset

| File | Purpose | Records |
|---|---|---:|
| `customers.csv` | Customer master data | 400 |
| `products.csv` | Product master data | 96 |
| `sales.csv` | Transaction data | 3,000 |
| `stores.csv` | Store master data | 8 |

### Customer
`Customer_ID`, `Customer_Name`, `City`, `Age_Group`, `Member_Type`

### Product
`Product_ID`, `Product_Name`, `Category`, `Unit_Price`, `Unit_Cost`

### Sales
`Order_ID`, `Order_Date`, `Customer_ID`, `Product_ID`, `Store_ID`, `Quantity`, `Unit_Price`, `Unit_Cost`, `Discount_Percent`, `Gross_Sales`, `Discount_Amount`, `Revenue`, `Profit`, `Payment_Method`

### Store
`Store_ID`, `Store_Name`, `City`, `Store_Type`

## 🧰 Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing |
| Pandas | Cleaning and transformation |
| Jupyter Notebook | Data preparation |
| Power BI | Executive dashboard |
| Looker | BI analysis |
| Tableau | BI dashboard |
| Neo4j | Graph database |
| Cypher | Graph analytics |
| GitHub | Documentation and portfolio |

## 🔄 Project Workflow

### 1. Data preparation
The original dataset was cleaned and validated in Jupyter Notebook using Pandas.

Activities included:
- Missing-value checks
- Duplicate checks
- Data-type validation
- Date validation
- ID validation
- Revenue/profit validation

### 2. Data separation
The cleaned dataset was organized into four CSV files:

```text
customers.csv
products.csv
sales.csv
stores.csv
```

### 3. Visualization
The same business domain was analyzed in:
- Power BI
- Looker
- Tableau

### 4. Graph analytics
The clean data was then modeled in Neo4j for relationship-based analysis.

## 📈 BI Dashboards

### Power BI
One-page executive dashboard with:
- Total Revenue
- Total Profit
- Total Orders
- Total Customers
- Profit Margin
- Monthly Revenue Trend
- Revenue by Category
- Payment Method Distribution
- Top 10 Products
- Revenue by City
- Profit by Member Type

Filters:
- Year
- Category
- City

### Looker
Analysis includes:
- Revenue
- Profit
- Profit Margin
- Product and category performance
- Customer analysis
- Store/city analysis

### Tableau
A Tableau dashboard was created using the same cleaned analytical data to demonstrate cross-platform BI capability.

## 🕸️ Neo4j Graph Database

Neo4j adds relationship-based analysis that is different from traditional dashboard aggregation.

Examples:
- Which customers bought a product?
- Which customers bought the same product?
- Which products are connected through common customers?
- What products could be recommended to a customer?

## 🧩 Graph Model

Recommended professional model:

```text
                 ┌─────────────┐
                 │   Customer  │
                 └──────┬──────┘
                        │
                    PURCHASED
                        │
                        ▼
                 ┌─────────────┐
                 │    Sales    │
                 └──────┬──────┘
                    ┌───┴───┐
                 CONTAINS  MADE_AT
                    │         │
                    ▼         ▼
              ┌─────────┐ ┌─────────┐
              │ Product │ │  Store  │
              └─────────┘ └─────────┘
```

Nodes:
```text
(:Customer)
(:Sales)
(:Product)
(:Store)
```

Relationships:
```text
(:Customer)-[:PURCHASED]->(:Sales)
(:Sales)-[:CONTAINS]->(:Product)
(:Sales)-[:MADE_AT]->(:Store)
```


## 🔎 Key Business Questions

### Sales
- What is total revenue?
- What is total profit?
- What is profit margin?
- How does revenue change by year?

### Products
- Which products generate the most revenue?
- Which products sell the most units?
- Which categories are most profitable?

### Customers
- Which customers generate the most revenue?
- Which member type is most valuable?
- Which cities generate the most customer revenue?

### Stores
- Which stores generate the most revenue?
- Which stores generate the most profit?
- Which cities perform best?

### Graph Analytics
- Which customers bought a specific product?
- Which customers bought the same products?
- Which products are connected through common customers?
- What products could be recommended to a customer?

## 🧠 Key Skills

**Data:** Data cleaning, validation, transformation, KPI analysis

**Python:** Pandas, Jupyter Notebook, CSV processing

**BI:** Power BI, Looker, Tableau, dashboard design, business storytelling

**Graph:** Neo4j, Cypher, nodes, relationships, graph traversal, aggregation, recommendation logic

## 📁 Project Structure

```text
grocery-store-sales-analytics/
│
├── data/
│   ├── customers.csv
│   ├── products.csv
│   ├── sales.csv
│   └── stores.csv
│
├── notebooks/
│   └── data_cleaning.ipynb
│
├── Dashboard/
│   └── grocery_sales_dashboard.pbix
│   └── looker_dashboard_notes.md
│   └── grocery_sales_dashboard.twb
│
├── neo4j/
│   └── neo4j_interview_queries.txt

├── screenshots/
│   ├── powerbi-dashboard.png
│   ├── looker-dashboard.png
│   ├── tableau-dashboard.png
│   └── neo4j-graph.png
│
└── README.md
```


## How to Run

### Option 1: Clone the Repository

```bash
git clone https://github.com/Ajitjha3095/grocery-store-sales-analytics.git
cd grocery-store-sales-analytics
```

Then open the required dashboard file from the `Dashboard/` folder:

- **Power BI:** Open the `.pbix` file using Power BI Desktop.
- **Tableau:** Open the `.twbx` file using Tableau Desktop or Tableau Public.
- **Python:** Run scripts from the `python/` folder.

```bash
python python/<script_name>.py
```

### Option 2: Download ZIP File

1. Open the repository:  
   [grocery-store-sales-analytics](https://github.com/Ajitjha3095/grocery-store-sales-analytics)

2. Click **Code** → **Download ZIP**.

3. Extract the downloaded ZIP file.

4. Open the project folder.

5. Open the dashboard file from the `Dashboard/` folder:

   - Open `.pbix` files in **Power BI Desktop**.
   - Open `.twbx` files in **Tableau Desktop** or **Tableau Public**.
   - Run Python scripts from the `python/` folder.

```bash
python python/<script_name>.py
```

> Use the dashboard filters and slicers to analyze sales by year, region, beverage category, product, and sales performance.

## Author

**Ajit Jha**  
*Data Analytics & Data Engineering Portfolio Project* 

⭐ Project

If you find the analytical approach useful, feel free to explore the repository and dashboards.

- **GitHub:** [Ajitjha3095](https://github.com/Ajitjha3095)
- **LinkedIn:** [Ajit Jha](https://www.linkedin.com/in/ajitjha01/)
