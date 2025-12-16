# End-to-End-Azure Data Engineering Project
This project demonstrates a production-style end-to-end data engineering pipeline built on Microsoft Azure  covering ingestion, transformation, data quality, analytics and visualization using real-world e-commerce data. The pipeline follows a Medallion Architecture and is designed to be scalable and metadata-driven.

## Tech Stack

Azure Data Factory (ADF) – Orchestration & ingestion
Self-Hosted Integration Runtime (SHIR) – Local data ingestion
Azure Data Lake Gen2 – Storage
Azure Databricks (PySpark) – Transformations
Delta Lake – ACID tables & incremental processing
Power BI – Analytics & visualization

## Architecture
Local CSV (E-commerce)
        |
        | (ADF + SHIR)
        v
     RAW (ADLS)
        |
        | (Databricks)
        v
   BRONZE (Delta)
        |
        | (Databricks)
        v
   SILVER (Clean + Join)
        |
        | (Databricks)
        v
    GOLD (KPIs)
        |            
        | (Power BI)
        v
   Business Dashboards    
