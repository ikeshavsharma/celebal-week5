# CEI Week 5 – Apache Spark Data Processing Using PySpark

## Project Overview

This project was completed as part of the Celebal Technologies Excellence Internship (CEI) Week 5 Assignment. The objective was to understand Apache Spark fundamentals and perform data cleaning, transformation, filtering, and aggregation using PySpark DataFrames.

---

## Dataset Used

The project uses the Superstore Dataset.

The original dataset contained very few data quality issues. To properly demonstrate Spark DataFrame cleaning operations, I created a modified version of the dataset by intentionally introducing:

* Null values in the Sales column
* Duplicate records

This helped simulate real-world data quality problems and allowed all required cleaning operations to be performed and validated.

Modified Dataset:

* Superstore_Modified.csv

---

## Data Cleaning Performed

### Null Value Handling

Missing values were identified and replaced using Spark DataFrame operations. This ensured that aggregation and analysis could be performed without data quality issues.

### Duplicate Removal

Duplicate records were detected and removed using the dropDuplicates() function to improve data consistency.

### Data Type Conversion

Several columns were converted into appropriate numeric data types:

* Sales → Double
* Quantity → Integer
* Discount → Double

This made mathematical calculations and aggregations possible.

---

## Data Analysis Performed

### Category-wise Sales Analysis

Sales were grouped by product category to understand which category generated the highest revenue.

### Region-wise Sales Analysis

Regional sales were analyzed to compare business performance across different regions.

### Profit Analysis

Profit values were analyzed to identify profitable and loss-making transactions.

### Customer Analysis

Top customers were identified based on total sales contribution.

### Product Analysis

Top-performing products were identified using sales-based aggregation.

---

## Filtering Operations

The following filtering operations were performed:

* High-value orders (Sales > 1000)
* Technology category products
* Loss-making transactions (Profit < 0)

These filters helped analyze specific business scenarios.

---

## Additional Transformation

A new column named Profit_Status was created:

* Profit → If Profit > 0
* Loss → If Profit ≤ 0

This simplified profitability analysis.

---

## Data Processing Pipeline

Load Data
→ Schema Validation
→ Null Value Detection
→ Duplicate Detection
→ Missing Value Handling
→ Duplicate Removal
→ Data Type Conversion
→ Filtering Operations
→ Aggregation & Analysis
→ Profit_Status Creation
→ Business Insights

---

## Key Findings

* Technology products generated the highest sales among all categories.
* The West region contributed the highest overall sales.
* Several products generated negative profit despite having good sales.
* A small number of customers contributed significantly to total revenue.
* Data cleaning improved the reliability of analytical results.

---

## Conclusion

This project provided hands-on experience with Apache Spark and PySpark DataFrames. By introducing null values and duplicate records into the dataset, real-world data cleaning scenarios were simulated. The project demonstrated how Spark can be used to clean, transform, filter, and analyze large datasets efficiently while generating meaningful business insights.
