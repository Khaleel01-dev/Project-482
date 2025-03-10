# Data Wrangling Documentation

This document explains the data wrangling process applied to the dataset used in this project.

## 1. Handling Missing Values
- **Step 1:** I removed all the **null values** from the dataset to clean the data thoroughly and ensure that the dataset was complete for analysis.

## 2. Removing Duplicates
- **Step 1:** Used the **clean duplicate values** option in **Tableau Prep** to remove any duplicate records in the data, ensuring that each entry was unique.

## 3. Standardizing Formats
- **Step 1:** I changed the format of the **year** values in the dataset. Initially, I faced an issue where changing the format to **year** caused values to become **null**, but after performing a **clean step**, the format change was applied successfully.
- **Step 2:** For the **Provinces** column, I had many numbers in brackets next to the province names, as well as city names. I used the **clean number** and **clean punctuation** options in Tableau Prep to remove unnecessary symbols and numbers.
- **Step 3:** After cleaning, I deleted the **city names** from the dataset to ensure data consistency and then assigned the **State/Province** data role.

## 4. Filtering Unnecessary Columns or Rows
- **Step 1:** I removed unnecessary **columns and rows** from the dataset to simplify it and focus only on the relevant information needed for the analysis.

## 5. Pivoting
- **Step 1:** I pivoted the data as needed, converting **rows to columns** and **columns to rows** based on the specific analysis requirements for the dataset. This ensured that the data was structured in a way that was useful for my visualizations.

## Final Outcome
After performing these wrangling steps, I created **five hyper files** that were then uploaded to Tableau for visualization.
