# Ecommerce Data Platform

![Project Status](https://img.shields.io/badge/status-Finalized-brightgreen)
![Tech Stack](https://img.shields.io/badge/tech-dbt%20|%20Python%20|%20PostgreSQL-blue)

This project simulates a real-world data platform for an e-commerce company starting its digital operations. It is designed to ingest, transform, and analyze data from multiple sources stored in AWS S3, generating actionable business insights.

## Project Goals
- Analyze sales and customer data
- Compare product prices with the market
- Generate data-driven insights for business decisions
- Provide a structured and scalable data transformation pipeline

## Data Platform Structure
The project follows a **bronze → silver → gold** approach in dbt:

- **Bronze Layer:** Raw tables ingested from CSV and Parquet files stored in AWS S3, including products, customers, sales, and competitor prices.
- **Silver Layer:** Cleaned and integrated tables for analysis and reporting.
- **Gold Layer:** Aggregated metrics and KPIs for decision-making (e.g., top products, sales by channel, pricing competitiveness).

## Tech Stack
- **Python (Pandas):** Used only for ingestion of data from S3 into the database.
- **PostgreSQL (Supabase):** Database for storing and querying raw and transformed data.
- **dbt:** For all transformations, testing, and documentation of models.

## Project Features
- Sources are defined in `_sources.yml` under the `models` directory.
- Models are organized by layer (bronze, silver, gold) for incremental transformations.
- Includes detailed column descriptions and table documentation to support dbt docs.
- Ready for further improvements such as seeds, snapshots, and custom macros.

## How to Use
1. Connect dbt Cloud to your repository.
2. Configure the environment to your database (PostgreSQL or other supported).
3. Run the pipeline in order: `bronze → silver → gold`.
4. Use `dbt docs generate` and `dbt docs serve` to explore documentation.

## Project Status
✅ Finalized
