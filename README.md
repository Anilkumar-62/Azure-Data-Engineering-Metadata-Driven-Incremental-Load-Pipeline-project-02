# Azure-Data-Engineering-Metadata-Driven-Incremental-Load-Pipeline-project-02
A comprehensive Data Engineering project demonstrating an end-to-end Incremental Data Loading framework using Azure Data Factory(ADF).This project implements a Metadata-driven approach using SQL Watermark tables to efficiently capture and process delta records from an Azure SQL Database to ADLS Gen2,ensuring optimized data movement and scalability.
Implemented an efficient Delta Load strategy using Azure Data Factory to optimize data ingestion. This project focuses on capturing new or changed data using a watermark-based approach, reducing processing costs and time. Features dynamic partitioning and automated metadata updates.

Project Overview

Developed a production-ready Incremental Loading (Delta Load) pipeline to solve the challenge of large-scale data ingestion. Instead of reloading the entire dataset, the pipeline identifies and fetches only the records added or updated since the last successful execution.

Tech Stack

Orchestration: Azure Data Factory (ADF)

Storage: Azure Data Lake Storage (ADLS) Gen2

Database: Azure SQL Database

Logic: Watermark-based Incremental Ingestion

Security: Azure Key Vault

Key Features & Implementation

Watermark Logic: Engineered a robust watermark mechanism to track the last processed timestamp, ensuring only new delta data is ingested from source tables.

Dynamic Partitioning: Configured dynamic sink paths in ADLS Gen2 to automatically organize output files into date-specific folders (e.g., dd-MMM-yyyy), improving data discoverability.

Automated Metadata Updates: Used Lookup activities and Stored Procedures to dynamically fetch and update watermark values in a control table after every successful pipeline run.

Error Handling: Built-in validation checks to ensure data integrity during the incremental transfer between Azure SQL and Data Lake.

Performance Optimization: Significantly reduced execution time and storage costs by implementing a "Load-by-Exception" strategy rather than full data reloads.
