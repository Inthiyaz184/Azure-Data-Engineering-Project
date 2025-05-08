# Netflix Azure Data Engineering Project

This project demonstrates an end-to-end data engineering pipeline using Azure and Databricks, following a Medallion architecture to process and analyze Netflix data.

## 📊 Project Overview

The project ingests Netflix-related data from GitHub, processes it through Azure Data Factory (ADF) pipelines, transforms and analyzes it using Databricks with PySpark and SparkSQL, and visualizes results in Databricks notebooks. It also uses Delta Live Tables (DLT) to implement the bronze, silver, and gold layers of the Medallion architecture.

---

## 🏗️ Architecture

![Architecture](https://github.com/user-attachments/assets/c1556b47-4dae-4605-bb61-6c9e33ad95e6)


- **Data Ingestion**: ADF parameterized pipeline copies data from GitHub to ADLS Gen2.
- **Data Validation**: Pipeline checks for specific file arrival in the folder before processing.
- **Data Processing**: Databricks Auto Loader incrementally loads data, transformations done via PySpark & SparkSQL.
- **Orchestration**: Databricks workflows and ADF pipelines orchestrate tasks.
- **Medallion Architecture**:
  - **Bronze**: Raw data ingestion.
  - **Silver**: Cleaned and validated data.
  - **Gold**: Aggregated and business-level data.
- **Visualization**: Databricks notebooks used for exploration and visualization.

---

## ⚙️ Tools & Technologies

- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2 (ADLS Gen2)
- Azure Databricks (PySpark, SparkSQL, Auto Loader, Delta Live Tables)
- GitHub (Source Data)
- Medallion Architecture

---

## 🔑Key highlights:
- Automated file arrival detection
- Incremental loading with Databricks Autoloader
- Data transformation using PySpark and SparkSQL
- Parameterized and reusable pipelines and workflows
- Delta Live Tables for robust data management
- Interactive dashboards and visualizations
