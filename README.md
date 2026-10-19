# Banking Data Lakehouse using PySpark and Azure Databricks

## Project Overview

This beginner-friendly data engineering project demonstrates how to build a banking transaction data pipeline using PySpark in Azure Databricks. It implements the Medallion Architecture to process raw transaction data, identify data quality issues, clean valid records, and generate business summaries.

## Architecture

**Bronze → Silver → Gold**

- **Bronze Layer:** Stores the raw banking transaction records.
- **Silver Layer:** Deduplicates transactions, validates customer IDs, transaction dates, and amounts, and separates valid and rejected records.
- **Gold Layer:** Produces aggregated transaction summaries by payment type and transaction date.

## Technologies Used

- Azure Databricks Free Edition
- PySpark
- Python
- Delta Lake concepts
- Medallion Architecture

## Data Quality Checks

The sample dataset includes duplicate transactions, invalid dates, missing customer IDs, zero amounts, and negative amounts to demonstrate data validation and rejection handling.

## Project Results

Based on the sample notebook execution:

- Raw transactions: 12
- Clean Silver transactions: 7
- Rejected transactions: 4
- Financial reconciliation: Silver and Gold totals match

The pipeline demonstrates data cleaning, deduplication, aggregation, and financial total validation on synthetic sample data.

## Repository Contents

- `Banking_Data_Lakehouse_PySpark.ipynb` — Databricks notebook containing the pipeline implementation and execution results.
- `README.md` — Project documentation.

## How to Run

1. Open Azure Databricks.
2. Import `Banking_Data_Lakehouse_PySpark.ipynb` into your workspace.
3. Attach an available compute resource or serverless environment.
4. Run the notebook cells in order.
5. Review the Bronze, Silver, and Gold layer outputs and data quality checks.

## Disclaimer

This project uses synthetic sample transactions for educational purposes. It does not process real customer or banking data.
