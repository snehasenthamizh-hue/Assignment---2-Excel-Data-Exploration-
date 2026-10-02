Excel Data Cleaning and Transformation – Product Dataset

 📌 Project Overview

This project demonstrates the process of **data cleaning and preparation using Microsoft Excel**.

The dataset contains product information such as Product ID, Product Name, Brand Name, Quantity, Category, and Price.

The main objective of this project is to clean and transform the dataset so that it is more consistent, structured, and ready for further data analysis.

🎯 Problem Statement

Real-world datasets often contain:

* Missing values
* Inconsistent text formatting
* Typographical errors
* Duplicate records
* Poorly structured columns
* Inconsistent data formats

In this project, Excel was used to identify and resolve these data-quality issues and prepare the dataset for analysis.

 📊 Dataset Information

**Dataset:** Product Dataset
Columns

| Column       | Description                       |
| ------------ | --------------------------------- |
| Product ID   | Unique identifier for the product |
| Product Name | Name of the product               |
| Brand Name   | Brand associated with the product |
| Quantity     | Available quantity                |
| Category     | Product category                  |
| Price        | Product price                     |


 🧹 Data Cleaning and Transformation

1. Handling Missing Values

 Missing Values in Price

The dataset contained **3 missing values in the Price column**.

Two approaches were considered:

1. Replace missing prices with `0`.
2. Calculate the median price and use it for missing values.

The median price was calculated using:
=MEDIAN(D2:D35)
The calculated median was:
130

Therefore, the median can be used as an alternative approach for imputing missing price values.

 Missing Categories

There were **4 missing Category values**.

Instead of assigning categories randomly, each missing product was compared with similar products that already had categories in the dataset.

| Product         | Assigned Category |
| --------------- | ----------------- |
| Backpack        | Accessories       |
| Sneakers        | Fashion           |
| Coffee Maker    | Kitchen           |
| Fitness Tracker | Electronics       |

This approach uses the existing dataset as a reference for category imputation.

2. Correcting Inconsistent Data
Product Name Formatting

The Product Name column contained inconsistent text formatting.

A new column named:

NEW PRODUCT NAME

was created.

The Excel `PROPER` function was used to standardize product names.

Example:
=PROPER(A2)

This converts text into a consistent capitalization format.

Category Typo

A typo was identified in the Category column:
Electroni → Electronics

The Excel **Find and Replace (Ctrl + H)** feature was used to correct the typo.

Other product names such as Laptop, Smartphone, and Sneakers were also standardized using the Find and Replace method where required.

3. Removing Duplicate Records

The dataset was checked for duplicate rows using the complete row information.

Result

**No duplicate rows were found.**

Therefore, no records needed to be removed.


4. Splitting and Merging Data
Product ID Transformation

The Product ID column was split using the **Text to Columns → Delimited** option.

The required information was separated into:

* Manufacturing Date
* Country Code

Unnecessary parts were removed.

After splitting, the required columns were combined where necessary using the **CONCATENATE** function.
Creating Product Brand

The Brand Name and Product Name columns were merged into a new column named:

Product Brand

This creates a combined product description containing both the brand and product name.

Example:
Brand Name + Product Name

5. Number Formatting

 Price

The Price column was formatted as **Currency**.

Steps followed:

Home → Number → Currency ($)**

This makes the price values easier to read and interpret.
Manufacturing Date

The required format was:
DD-MM-YYYY

However, the dataset only provides the **day and month** and does not contain the year.

Therefore, the Manufacturing Date could not be correctly displayed in the requested `DD-MM-YYYY` format without introducing a year that is not present in the source data.

6. Conditional Formatting

Price Data Bars

Conditional Formatting was applied to the Price column using **Data Bars**.

Steps:

Select Price Column → Home → Conditional Formatting → Data Bars**

This provides a visual comparison of product prices.

Higher prices have longer bars, while lower prices have shorter bars.

Highlight Electronics Category

A conditional formatting rule was created for the Category column to highlight cells where:

text
Category = Electronics

Steps:

Select Category Column → Home → Conditional Formatting → Highlight Cells Rules**

The formatting was then customized using a font style and cell fill color.

📈 Key Data Cleaning Results

| Data Quality Issue           | Result                              |
| ---------------------------- | ----------------------------------- |
| Missing Price Values         | 3                                   |
| Median Price                 | 130                                 |
| Missing Category Values      | 4                                   |
| Category Imputation          | Completed using similar products    |
| Category Typo                | Electroni → Electronics             |
| Duplicate Rows               | None found                          |
| Product Name Formatting      | Standardized                        |
| Product ID                   | Split into required fields          |
| Product Brand                | Brand + Product Name                |
| Price Format                 | Currency                            |
| Manufacturing Date           | Limited because year is unavailable |
| Price Conditional Formatting | Data Bars applied                   |
| Electronics Highlighting     | Conditional Formatting applied      |

Key Learnings

Through this project, I learned how to:

* Identify and handle missing values in Excel
* Use median values for missing numerical data
* Impute missing categories using similar records
* Identify and correct text inconsistencies
* Use Excel's Find and Replace feature
* Check and remove duplicate records
* Split columns using Text to Columns
* Combine columns using Excel formulas
* Apply currency and date formatting
* Use Conditional Formatting for data visualization
* Prepare a dataset for further analysis



For GitHub, I’d recommend naming the repository something simple like **`excel-data-cleaning-transformation`** and adding 3–5 screenshots of your Excel work. That will make the project much easier for a recruiter to understand quickly.
