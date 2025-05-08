# Netflix Azure Data Engineering Project

This project demonstrates an end-to-end data engineering pipeline using Azure and Databricks, following a Medallion architecture to process and analyze Netflix data.

## 📊 Project Overview

This project demonstrates an **end-to-end data pipeline** for processing Netflix data using **Azure and Databricks**. It follows the **Medallion Architecture** (Bronze, Silver, Gold) on **Azure Data Lake Storage (ADLS)** and utilizes **Azure Data Factory (ADF)**, **Databricks**, **Delta Live Tables**, and **Databricks Autoloader** for seamless data ingestion, transformation, and orchestration.  

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

## 📁 Folder Descriptions

| Folder                 | Description                                        |
|------------------------|---------------------------------------------------|
| `Azure/`              | ADF pipeline + linked services JSON files         |
| `Data/`               | Sample input data files                           |
| `Databricks_notebooks/` | Databricks notebooks for transformation/analysis  |
| `parameter_file/`     | ADF parameter files for dynamic configuration     |
| `pipelinescreenshots/`| Screenshots of pipelines, workflows, architecture |
