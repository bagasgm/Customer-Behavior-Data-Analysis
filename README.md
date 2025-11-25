# Customer Behavior Data Analysis

## 📊 Overview

This project analyzes customer shopping behavior using transactional data to uncover patterns in purchases, demographics, and shopping preferences. The goal is to provide actionable insights that can drive strategic business decisions, improve customer engagement, and optimize marketing strategies.

## 📁 Dataset

- **Source**: Customer shopping behavior dataset
- **Records**: 3,900 transactions
- **Features**: 18 columns including:
  - Customer demographics (Age, Gender, Location)
  - Purchase details (Item, Category, Amount, Season, Size, Color)
  - Behavioral data (Discount Usage, Previous Purchases, Review Ratings, Subscription Status)
  - Shopping preferences (Shipping Type, Payment Method, Purchase Frequency)
- **Missing Data**: 37 missing values in Review Rating

## 🛠️ Tools & Technologies

- **Python** (Pandas, SQLAlchemy) - Data cleaning and preprocessing
- **PostgreSQL** - Data storage and analysis
- **Power BI** - Data visualization and dashboard creation
- **Gamma AI** - Presentation creation

## 📋 Project Steps

### 1. Data Loading & Exploration

- Loaded dataset using Pandas in Jupyter Notebook
- Performed initial exploration with **df.info()** and **df.describe()**
- Identified data types and missing values

### 2. Data Cleaning & Preprocessing

- Handled 37 missing values in Review Rating using category-wise median imputation
- Standardized column names to snake_case for consistency
- Created new features:
  - **age_group** - Binned customers into Young Adult, Adult, Middle-Aged, Senior
  - **purchase_frequency_days** - Converted purchase frequency to numerical days
- Removed redundant **promo_code_used** column (identical to **discount_applied**)

### 3. Database Integration

- Connected to PostgreSQL using SQLAlchemy
- Loaded cleaned data into **customer** table in **customer_behavior** database

### 4. SQL Analysis

Performed comprehensive analysis answering 10 key business questions:

- Revenue distribution by gender
- High-value discount customers
- Top-rated products
- Shipping type comparisons
- Subscription behavior analysis
- Discount dependency by product
- Customer segmentation (New, Returning, Loyal)
- Top products per category
- Repeat buyer subscription patterns
- Revenue contribution by age group

### 5. Visualization & Reporting

- Built interactive Power BI dashboard with key metrics
- Created comprehensive documentation
- Developed presentation using Gamma

## 📈 Dashboard

![Dashboard Preview](https://github.com/user-attachments/assets/2d3f2828-9130-41fd-9f62-158a657ba121)
The Power BI dashboard provides:

- Key metrics: Customer count, average rating, purchase amount
- Subscription and gender distribution
- Revenue analysis by category and age group
- Interactive filters for category, shipping type, and more

## 🔍 Key Findings

- **Male customers** generate significantly higher revenue than female customers
- **Express shipping** users spend more on average than standard shipping users
- **Non-subscribers** contribute more total revenue despite similar average spend
- **Young Adults** are the highest revenue-generating age group
- **Loyal customers** (3116) significantly outnumber new customers (83)
- Top products vary by category, with Blouse and Jewelry being most popular

## 💡 Business Recommendations

- **Boost Subscriptions** - Offer exclusive benefits to increase subscriber base
- **Loyalty Programs** - Implement rewards to retain returning customers
- **Discount Strategy** - Balance discount usage with profit margins
- **Product Positioning** - Highlight top-rated and best-selling items in marketing
- **Targeted Campaigns** - Focus on high-revenue demographics and shipping preferences

## 🚀 How to Run This Project

### Prerequisites

- Python 3.8+
- Power BI Desktop
- Jupyter Notebook

### Installation Steps

1. **Clone the repository**

```bash
git clone https://github.com/bagasgm/Customer-Behavior-Data-Analysis.git
cd customer-trends-data-analysis-SQL-Python-PowerBI
```

2. **Open customer_shopping_behavior_analysis.ipynb notebook**

```bash
jupyter notebook customer_shopping_behavior_analysis.ipynb
```

3. **Load the data from Python notebook into MySQL/PostgreSQL/MS SQL Server**

- Create a Database in SQL
- Run Python code to load data into SQL database
- open **customer_behavior_sql_queries.sql**

4. **Connect the SQL Database to Power BI**

- Open **customer_behavior_dashboard.pbix**
- Create interactive dashboard in Power BI

## 📬 Contact

For any questions or collaboration opportunities, feel free to reach out.
