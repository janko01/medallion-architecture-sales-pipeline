# Medallion Architecture Sales Data Pipeline

> Using the Medallion Architecture to aggregate sales data and surface insights for performance analysis.

## Project Overview

This project demonstrates how to build a scalable data pipeline using the **Medallion Architecture** on **Databricks**. The goal is to clean, transform, and aggregate retail sales data to help identify performance trends across products and stores.

The pipeline was created as part of a junior data engineering challenge for a company case task.

---

## Architecture Layers

### Bronze Layer
- Ingests raw CSV sales data into a Delta table
- Performs minimal parsing and standardization
- Stores the unfiltered historical source

### Silver Layer
- Cleans and validates records (nulls, schema mismatches)
- Enriches data with additional fields (e.g., total_price = qty × unit_price)
- Normalizes column types and formats

### Gold Layer
- Aggregates key business metrics:
  - Total revenue per store
  - Top-selling products
  - Monthly sales trends
- Provides curated tables for downstream analytics and reporting

---

## Tech Stack

- **Databricks (Community Edition)**
- **PySpark**
- **Delta Lake**
- **Notebook-based development**
- **Medallion Architecture principles**

---

## Output Metrics

The Gold layer provides:
- Total revenue per store
- Monthly revenue trends
- Product sales distributions



