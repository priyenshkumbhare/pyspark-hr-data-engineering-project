# HR Data Cleaning & Analysis using PySpark

## Project Overview

This project demonstrates end-to-end data cleaning, transformation, and
analysis of an HR dataset using PySpark.

The raw dataset contained: - Duplicate employee records - Missing salary
values - Negative salary entries - Inconsistent department names - Mixed
date formats - Unclean email formatting

The objective was to transform the raw dataset into a production-ready
structured dataset and generate meaningful business insights.

------------------------------------------------------------------------

## Tech Stack

-   Python
-   PySpark
-   Spark SQL
-   Jupyter Notebook

------------------------------------------------------------------------

## Data Cleaning Steps

### 1. Duplicate Removal

Removed duplicate employee records using `employee_id` as primary key.

### 2. Salary Cleaning & Validation

-   Replaced empty strings with NULL
-   Removed commas from salary values
-   Cast salary column to numeric type
-   Identified negative salary values
-   Created `salary_flag` column for audit tracking
-   Imputed missing/invalid salaries using department median

### 3. Department Standardization

Standardized inconsistent department values: - hr → Human Resources -
sales → Sales - it → Information Technology - finance → Finance

### 4. Date Standardization

Converted joining dates into consistent format: YYYY-MM-DD

### 5. Email Cleaning

-   Trimmed extra spaces
-   Converted all emails to lowercase

------------------------------------------------------------------------

## Business Insights

### Total Salary Expense

Total payroll cost: 3,771,350

### Employee Distribution

| Department | Employee Count |
|------------|----------------|
| Finance    | 19             |
| IT         | 16             |
| HR         | 14             |
| Sales      | 13             |

### Average Salary by Department

| Department | Avg Salary |
|------------|------------|
| Sales      | 72,166     |
| Finance    | 65,903     |
| HR         | 59,646     |
| IT         | 46,622     |

### Hiring Trend Analysis

-   Steady hiring activity across 2019--2021
-   Moderate hiring peaks during mid-year months
-   No abnormal spikes detected
-   Slight slowdown observed in early 2021

------------------------------------------------------------------------

## Final Dataset Columns

-   employee_id
-   name
-   department
-   salary
-   joining_date
-   email
-   salary_flag

------------------------------------------------------------------------

## Key Learnings

-   Handling missing and invalid data in PySpark
-   Data validation and audit tracking
-   Group-based imputation strategy
-   Aggregation and business metric generation
-   Transforming raw data into decision-ready insights

------------------------------------------------------------------------

## Future Improvements

-   Add visualizations
-   Build interactive dashboard
-   Implement automated data quality checks
-   Integrate into ETL pipeline
