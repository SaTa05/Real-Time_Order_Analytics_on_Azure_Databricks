# Restaurant Analytics Lakehouse Pipeline

An end-to-end data pipeline on Azure Databricks that combines streaming and batch restaurant data into analytics-ready tables and dashboards.

## Summary

This project ingests real-time order events and historical order data, processes them through a Bronze → Silver → Gold medallion architecture, and surfaces restaurant performance and customer sentiment in BI dashboards. All data is governed through Unity Catalog.

## Architecture

- **Sources:** Azure Event Hub (streaming orders) and Azure SQL Database (batch/historical data)
- **Ingestion:** LakeFlow Connect (CDC from SQL) and Spark Declarative Pipelines (streaming from Event Hub)
- **Processing:** Bronze (raw) → Silver (cleaned, enriched) → Gold (aggregated)
- **AI:** Sentiment analysis and issue categorization on customer reviews using `AI_QUERY`
- **Orchestration:** Databricks Workflows
- **Analytics:** Databricks AI/BI dashboards for chain performance and customer sentiment
- **Orchestration with Apache Airflow** *(add when done)*
- **Data quality checks and sensitive-field masking** *(add when done)*
- **Star-schema model loaded into Snowflake** *(add when done)*

## Tech Stack

Azure Databricks, Azure Event Hub, Azure SQL Database, Unity Catalog, Spark Declarative Pipelines, Databricks Workflows, SQL, Python
