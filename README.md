# Data Cleaning in Power BI

This repository demonstrates a comprehensive **data cleaning and transformation workflow** using Microsoft Power BI's Power Query Editor. It focuses on preparing raw sales data (specifically the `superstore_raw` dataset) for accurate analysis and visualization.

## 📋 Project Overview

Raw data often contains inconsistencies, formatting errors, and structural issues that can compromise analysis. This project documents the step-by-step process of transforming unstructured or "dirty" data into a clean, reliable dataset ready for reporting.

The workflow includes:
- **Data Import:** Connecting to the raw source.
- **Structural Cleanup:** Fixing headers and data types.
- **Standardization:** Ensuring consistent text and number formatting.
- **Enrichment:** Creating new calculated columns for deeper insights.

## 🛠️ Tools Used

- **Microsoft Power BI Desktop** (required)
- **Power Query Editor** (built-in data transformation engine)

## 📂 Dataset Information

- **Source File Name:** `superstore_raw`
- **Domain:** Sales & Retail Analytics
- **Goal:** Transform raw transactional data into an analysis-ready format.

## 🔄 Applied Transformation Steps

The following sequence of transformations was applied within the Power Query Editor. Each step is logged in the "Applied Steps" pane, allowing you to review, reorder, or modify the process at any time.

### 1. Source
- **Action:** Connected to the external data source (e.g., Excel, CSV).
- **Purpose:** Ingested the raw `superstore_raw` file into Power Query.

### 2. Promoted Headers
- **Action:** Moved the first row of the dataset to become the column headers.
- **Purpose:** Ensures that the data is properly labeled and that Power BI recognizes the columns correctly.

### 3. Changed Type
- **Action:** Converted data types for columns (e.g., text to number, text to date).
- **Purpose:** Prevents calculation errors. For example, ensuring dates are recognized as dates allows for time-based analysis (sorting, filtering by month/year).

### 4. Changed Type with Locale
- **Action:** Applied locale-specific formatting rules during type conversion.
- **Purpose:** Handles regional differences in date formats (e.g., MM/DD/YYYY vs. DD/MM/YYYY) and number formatting (e.g., decimal commas vs. periods).

### 5. Capitalized Each Word
- **Action:** Applied "Capitalize Each Word" text transformation to relevant columns.
- **Purpose:** Standardizes text entries (e.g., converting "new york" to "New York" or "furniture" to "Furniture"). This is critical for accurate grouping and filtering in reports.

### 6. Added Custom
- **Action:** Created a new custom column using M language formulas.
- **Purpose:** Typically used for initial calculations, such as extracting year from a date, creating a full name from first/last names, or flagging specific conditions.

### 7. Added Custom1
- **Action:** Added another custom transformation step.
- **Purpose:** Likely used for further data enrichment, such as categorizing customers, calculating profit margins, or splitting complex text fields.

### 8. Added Custom2
- **Action:** Final custom column addition.
- **Purpose:** Completes the data preparation, possibly adding final flags, rankings, or derived metrics needed for the final report.

## 💡 Best Practices Demonstrated

- **Step-by-Step Logging:** Each transformation is recorded, making the process reproducible and auditable.
- **Data Typing Early:** Converting types immediately after importing ensures errors are caught early.
- **Text Standardization:** Cleaning text columns prevents "fuzzy" matching issues in visuals.
- **Use of Custom Columns:** Extending the dataset with calculated fields adds analytical value without altering the source data.

## 🚀 How to Use

1. **Open Power BI Desktop** on your machine.
2. Go to **Home** > **Get Data** and import your source file (e.g., `superstore_raw.csv`).
3. Click **Transform Data** to open the Power Query Editor.
4. In the **Queries** pane on the left, select your query (e.g., `superstore_raw`).
5. Follow the **Applied Steps** shown on the right panel to replicate the transformations:
   - Right-click any step to rename, reorder, or remove it.
   - Click the **fx** icon next to a step to edit the formula.
6. Once all steps are complete, click **Close & Apply** to load the data into the Data Model.
7. Proceed to build your reports and dashboards.

## 📝 Notes

- **Reversibility:** Power Query is non-destructive. You can go back and change any step without affecting the original source file.
- **Performance:** Adding too many custom columns can impact performance; optimize where possible.
- **Error Handling:** If a step fails (like "Changed Type"), Power Query will highlight the error. You can fix the source data or adjust the step logic.

## 📄 License

This project is open-source and available for educational and personal use.

## 👤 About

Created by **RakshanaQ** as a demonstration of data cleaning techniques in Power BI.

---

*For questions or suggestions, please open an issue in the repository.*
