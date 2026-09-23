# E-Commerce Sales & Customer Analytics

An end-to-end exploratory data analysis and customer analytics project performed on an e-commerce transactional dataset using Python.

The project transforms raw transactional data into business insights by examining sales, profitability, product performance, customer behavior, discount impact, customer concentration, and RFM-based customer segments.

---

## 📌 Project Overview

The objective of this project is to understand the key factors influencing sales and profitability and to identify different types of customers based on their purchasing behavior.

The analysis follows a structured approach:

**Raw Data → Data Preprocessing → Feature Engineering → Exploratory Data Analysis → Business Analysis → Customer Segmentation → Business Insights**

The project combines transaction-level analysis with customer-level analysis to understand not only **what is happening in the business**, but also **which products and customers are contributing to it**.

---

## 🎯 Business Problem

The analysis focuses on understanding:

- Which product categories and sub-categories drive sales and profit?
- Which products generate high sales but weak or negative profitability?
- How do different customer segments contribute to sales and profit?
- How are individual customers performing in terms of sales, profit, and order frequency?
- How concentrated are sales across the customer base?
- Which customers are most valuable based on Recency, Frequency and Monetary value?
- How does discounting relate to profitability?
- Which customer segments represent retention, growth, or reactivation opportunities?

---

## ❓ Key Business Questions

### Product Performance

1. Which categories generate the highest sales and profit?
2. Which categories have the strongest profit margins?
3. Which sub-categories are the major contributors to overall profit?
4. Which sub-categories are generating losses?
5. Why are some high-sales products not necessarily highly profitable?

### Customer Analysis

6. Which customer segments generate the highest sales and profit?
7. Does high order frequency always indicate high customer value?
8. Why do some customers with high Average Order Value generate losses?

### Customer Concentration

9. Is the company's sales concentrated among a small group of customers?
10. What proportion of customers is required to generate approximately 80% of total sales?

### RFM Analysis

11. Which customers are recent, frequent, and high-value?
12. Which previously valuable customers are becoming inactive?
13. Which customers have potential for future growth?
14. Which customers have low current engagement and value?

### Profitability & Discount


15. Which customer segments generate the highest total profit?
16. Does the most valuable customer segment also generate the highest total profit?

---

# 🧹 Data Preprocessing

The raw dataset was prepared before performing exploratory analysis.

### Data Quality Checks

The preprocessing stage included:

- Dataset inspection
- Missing-value analysis
- Duplicate-value analysis
- Category validation
- Data type conversion
- Date validation
- Numeric value validation
- Validation of Sales, Quantity and Discount values

### Feature Engineering

Additional business-oriented features were created to support analysis:

| Feature | Purpose |
|---|---|
| Year | Time-based analysis |
| Month | Monthly analysis |
| Quarter | Quarterly analysis |
| Shipping Days | Shipping duration analysis |
| Profit Margin | Measures profitability relative to sales |
| Discount Rate | Converts discount into percentage form |

### Profit Margin Formula

**Profit Margin (%) = Profit / Sales × 100**

### Discount Rate

**Discount Rate (%) = Discount × 100**

---

# 📊 Exploratory Data Analysis

The EDA examines the distribution and relationships between important numerical variables.

### Variables Analysed

- Sales
- Profit
- Quantity
- Discount

### Distribution Analysis

Histograms and boxplots were used to identify:

- Distribution patterns
- Skewness
- Potential outliers
- High-value transactions
- Loss-making transactions

### Correlation Analysis

A correlation matrix was used to examine relationships between Sales, Profit, Quantity and Discount.

Key observations include:

- Sales and Profit show a moderate positive relationship.
- Discount has a weak negative relationship with Profit.
- Quantity shows relatively weak linear relationships with Sales and Profit.

---

# 📦 Product Performance Analysis

Product performance was analysed at both **category** and **sub-category** levels.

### Category-Level Analysis

Sales, Profit and Profit Margin were compared across product categories.

Key observations:

- Technology leads in both Sales and Profit.
- Furniture generates substantial Sales but comparatively low Profit.
- Office Supplies generates lower Sales than Furniture but stronger profitability.
- Profit Margin provides a more meaningful comparison of profitability efficiency than Sales alone.

### Sub-Category Analysis

The analysis identifies products that contribute strongly to profitability as well as products that negatively affect overall profit.

Key observations:

- Phones and Chairs are major Sales contributors.
- Copiers and Paper show strong profit generation relative to their Sales.
- Labels, Paper, Envelopes and Copiers are important profit contributors.
- Tables, Bookcases and Supplies negatively affect profitability.
- Tables represent a significant area requiring further investigation.

---

# 👥 Customer Analysis

Customer performance was analysed using:

- Total Sales
- Total Profit
- Number of Orders
- Average Order Value (AOV)

### Average Order Value

**AOV = Total Sales / Number of Orders**

AOV was used to understand whether customers typically place relatively small or large orders.

An important observation from the analysis is that:

> High Average Order Value does not necessarily guarantee profitability.

Some customers generate high-value orders while still producing losses, suggesting that pricing, discounting or cost-related factors may influence profitability.

---

# 📈 Customer Concentration — Pareto Analysis

Pareto analysis was performed to understand how Sales are distributed across customers.

Customers were:

1. Ranked by Sales
2. Sorted from highest to lowest
3. Assigned cumulative Sales
4. Converted into cumulative Sales percentages
5. Compared against cumulative customer percentages

### Key Findings

- The top 20% of customers contribute approximately **48–50% of total Sales**.
- Approximately 50% of customers contribute around **80% of total Sales**.
- The dataset does not follow the classic 20% → 80% Pareto pattern.
- Sales are moderately concentrated rather than being dominated by a very small group of customers.

This indicates that the business has a relatively broad customer base contributing to overall Sales.

---

# 🎯 RFM Customer Segmentation

RFM analysis was performed at the customer level using:

### Recency

How recently the customer made a purchase.

### Frequency

How frequently the customer placed orders.

### Monetary

How much Sales the customer generated.

RFM scores were created using quintile-based scoring and combined to classify customers into four broad segments.

---

## Customer Segments

| Segment | Customer Behaviour | Business Meaning |
|---|---|---|
| **Core Loyalists** | Recent + frequent + high-value | Highly engaged and valuable customers |
| **New & Growing** | Recent but lower frequency/value | Customers with potential to increase their value |
| **At-Risk** | Not recent but relatively valuable/frequent | Previously valuable customers showing declining engagement |
| **Hibernating / Lost** | Not recent + lower frequency/value | Low current engagement and lower customer value |

A decision-tree logic was used to assign customers to these four segments.

---

# 💰 Linking RFM with Profit & Discount

The RFM segmentation was extended by merging customer-level:

- Total Profit
- Average Discount

This allowed customer behaviour to be analysed alongside profitability.

Instead of looking only at **who buys the most**, the analysis also investigates:

**Who buys → How recently → How frequently → How much they spend → How profitable they are → What discount they receive**

This provides a more business-oriented view of customer value.

---

# 🔍 Key Business Insights

### 1. Sales ≠ Profitability

High Sales do not automatically translate into high profitability.

Furniture provides an example where substantial Sales are accompanied by comparatively low profit margins.

---

### 2. Some Product Groups Destroy Profit

While several sub-categories contribute strongly to profitability, Tables, Bookcases and Supplies negatively affect overall profit.

This creates opportunities for deeper investigation into:

- Pricing
- Discounting
- Product costs
- Regional performance
- Customer mix

---

### 3. Discounting Can Affect Profitability

Discount has a weak negative relationship with Profit in the dataset.

This suggests that higher discounting can be associated with lower profitability, although discount alone does not explain all profit variation.

---

### 4. Sales Are Moderately Concentrated

The customer base does not follow the traditional 20% → 80% Pareto relationship.

Approximately half of the customers are required to generate around 80% of Sales, indicating a relatively broad distribution of revenue across customers.

---

### 5. Customer Value Depends on More Than Order Frequency

Customers with more orders are not necessarily the most profitable.

Customer-level analysis shows differences in:

- Sales
- Profit
- Order frequency
- Average Order Value

Therefore, customer evaluation should consider profitability as well as activity.

---

### 6. At-Risk Customers Represent an Important Profit Pool

The RFM analysis identifies At-Risk customers as a particularly important group because they combine previous customer value with declining recency.

The analysis found that the At-Risk segment generated approximately **120,124 in total profit**.

This makes the segment relevant for retention and win-back analysis.

---

### 7. Core Loyalists Are Highly Valuable Per Customer

Core Loyalists combine:

- Recent purchases
- High purchase frequency
- High monetary value

They represent the strongest customer engagement profile within the RFM framework.

---

### 8. New & Growing Customers Represent Development Potential

These customers are relatively recent but have not yet reached the frequency and monetary levels of Core Loyalists.

This creates an opportunity to develop customer value through repeat purchases and cross-selling.

---

# 💡 Business Recommendations

### Product Strategy

- Investigate loss-making sub-categories such as Tables and Bookcases.
- Review pricing, discounting and cost structures for low-margin products.
- Identify products with strong profit contribution for potential growth.

### Customer Strategy

- Protect high-value Core Loyalists through retention initiatives.
- Develop New & Growing customers through repeat-purchase and cross-selling strategies.
- Prioritize high-value At-Risk customers for targeted win-back campaigns.
- Use selective, low-cost reactivation strategies for Hibernating / Lost customers.

### Pricing & Discount Strategy

- Investigate products and customer groups where high discounts coincide with weak profitability.
- Avoid evaluating discount performance using Sales alone.
- Monitor Profit Margin alongside Sales and Discount.

---

# 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**
- Exploratory Data Analysis
- Feature Engineering
- Customer Analytics
- RFM Segmentation
- Pareto Analysis

---

# 📁 Project Structure

```text
E-Commerce-Sales-and-Customer-Analytics/
│
├── data/
│   ├── E-commerce_data.csv
│   └── ecommerce_feature_engineered.csv
│
├── notebooks/
│   ├── 02_Data_Preprocessing.ipynb
│   └── 03_EDA.ipynb
│
├── images/
│   ├── category_performance.png
│   ├── sub_category_performance.png
│   ├── pareto_analysis.png
│   ├── rfm_segments.png
│   └── discount_profit.png
│
└── README.md
