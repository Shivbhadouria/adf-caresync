# 🏥 CareSync Health Network — End-to-End Data Engineering Platform

**An end-to-end healthcare data engineering project built with Azure Data Factory, Azure Databricks, PySpark, Delta Lake, and a Medallion Architecture.**

<p align="center">
  <img src="CareSync%20Data%20Platform%20Architecture.png" alt="CareSync Data Platform Architecture" width="100%">
</p>

Databricks Code Reference

Reference repository: Databricks Data Engineering Repository
https://github.com/Shivbhadouria/caresynce-adb-repo

Purpose: Reference material for Databricks notebooks, data transformation patterns, and implementation guidance.

Project adaptation: CareSync integrates the relevant concepts into its healthcare data platform, including the Medallion Architecture, Bronze/Silver/Gold processing, and analytics workflows.


## 📌 Project Overview

CareSync Health Network is a hands-on data engineering project focused on building a scalable, metadata-driven data platform for healthcare analytics.

The platform integrates data from multiple source systems, orchestrates ingestion workflows, processes data through Bronze, Silver, and Gold layers, and delivers analytics-ready datasets through Databricks dashboards and Genie.

The project emphasizes reusable pipelines, incremental data processing, execution auditing, secure configuration, and maintainable data workflows.

## 🎯 Project Objectives

- Build reusable, metadata-driven ingestion pipelines.
- Ingest data from PostgreSQL and file-based sources.
- Implement a Medallion Architecture using Databricks and Delta Lake.
- Support full-load and incremental/merge processing.
- Track pipeline execution through control and audit tables.
- Manage secrets securely using Azure Key Vault.
- Integrate GitHub for source control and CI/CD workflows.
- Automate pipeline summary notifications.
- Enable analytics and natural-language data exploration.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Azure Data Factory (ADF) | Pipeline orchestration and ingestion |
| PostgreSQL (Neon) | Relational source data |
| Azure Blob Storage | Data storage |
| Azure SQL Database | Metadata, control tables, and audit logging |
| Azure Databricks | Distributed data processing |
| PySpark / Apache Spark | Data transformation |
| Delta Lake | Reliable lakehouse tables |
| Azure Key Vault | Secrets management |
| GitHub | Version control and deployment workflows |
| Azure Logic Apps | Pipeline summary email notifications |
| Unity Catalog | Data governance and access management |
| Databricks Dashboards | Healthcare analytics and reporting |
| Databricks Genie | Natural-language data querying |

## 🏗️ Architecture and Data Flow

The platform follows a layered architecture consisting of data sources, orchestration, data transformation, governance, and consumption.

### 1. Data Sources

- PostgreSQL hosted on Neon
- Files stored in Azure Blob Storage

### 2. Orchestration and Metadata Management

Azure Data Factory coordinates pipeline execution and manages ingestion workflows.

Metadata and audit tables in Azure SQL Database support configuration-driven processing and pipeline execution tracking.

### 3. Medallion Architecture

The platform organizes data into three logical layers.

**🥉 Bronze — Raw Data**

- Stores ingested source data.
- Preserves source information for downstream processing.
- Provides the foundation for subsequent transformations.

**🥈 Silver — Cleansed and Standardized Data**

- Applies data cleansing and standardization.
- Supports data quality and consistency checks.
- Prepares data for analytical use.

**🥇 Gold — Business-Ready Data**

- Produces curated datasets for reporting.
- Supports business-level aggregations and analytical queries.
- Feeds dashboards and downstream consumption.

### 4. Governance and Security

- Azure Key Vault for managing secrets.
- Azure SQL control and audit tables for execution tracking.
- Unity Catalog for data governance.
- GitHub for source control and collaborative development.

### 5. Data Consumption

- Databricks Dashboards for analytical reporting.
- Databricks Genie for natural-language querying.
- Azure Logic Apps for pipeline summary notifications.

## ⚙️ Key Engineering Features

### Metadata-Driven Pipelines

Configuration-driven ingestion allows pipeline behavior to be controlled through metadata rather than hardcoding every source table into a separate workflow.

### Full and Incremental Loads

The platform supports full-load and incremental/merge processing patterns to accommodate different ingestion requirements.

### Pipeline Monitoring and Auditing

Control and audit tables capture pipeline execution information, supporting traceability and troubleshooting.

### Secure Configuration

Azure Key Vault is used to manage secrets without embedding sensitive credentials directly in pipeline code.

### GitHub and CI/CD

GitHub provides version control for project artifacts and supports the configured development and deployment workflow.

### Automated Notifications

Azure Logic Apps integrates pipeline execution summaries with email notifications.

## 📊 Databricks Dashboard

The CareSync Executive Overview dashboard presents healthcare analytics using KPIs and visualizations, including:

- Total patients
- Total hospitals
- Total laboratory tests
- Abnormal test rate
- Critical tests
- Patient distribution by state and gender
- Insurance-provider distribution

The dashboard demonstrates how curated data can be presented to support analytical exploration.

> Dashboard metrics depend on the project's sample dataset and should not be interpreted as real-world healthcare statistics.

<!-- Upload your dashboard screenshot to the repository and update this path. -->
<!-- Example: docs/executive-overview.png -->

## 📂 Repository Structure

```text
adf-caresync/
├── README.md
├── CareSync Data Platform Architecture.png
├── adf/
│   ├── pipeline/
│   ├── dataset/
│   ├── linkedService/
│   └── trigger/
├── databricks/
│   ├── bronze/
│   ├── silver/
│   ├── gold/
│   └── genie/
├── sql/
│   ├── control_tables.sql
│   └── audit_tables.sql
├── logic-apps/
└── docs/
    └── executive-overview.png
```

*Adjust this structure to match the actual files and folders in your repository.*

## 🚀 Setup and Execution

The following is the intended high-level deployment sequence. Add the exact configuration and execution instructions for your implementation.

1. Configure the required Azure services and source database.
2. Create the storage containers and database objects.
3. Configure credentials and secret references securely.
4. Import or deploy the Azure Data Factory pipelines.
5. Configure the Databricks workspace, notebooks, and Delta tables.
6. Configure metadata, control, and audit records.
7. Execute ingestion pipelines and validate the resulting data.
8. Run the Bronze, Silver, and Gold transformation workflows.
9. Configure notification workflows and the GitHub deployment process.
10. Validate the final datasets and dashboard outputs.

## 🔐 Security Considerations

- Never commit credentials, access keys, tokens, or connection strings.
- Use Azure Key Vault or another approved secrets-management mechanism.
- Use synthetic or appropriately licensed sample data.
- Do not publish identifiable patient information.
- Review repository files before making the repository public.

## 📈 Learning Outcomes

This project provides hands-on practice with:

- Cloud-based data engineering architecture
- Azure Data Factory orchestration
- Metadata-driven ETL/ELT design
- PySpark transformations and Delta Lake
- Full and incremental data loading
- Pipeline control, auditing, and monitoring
- Cloud security and governance
- Source control and deployment workflows
- Analytics and natural-language data access

## 👨‍💻 About This Project

CareSync Health Network is a portfolio project developed to demonstrate practical data engineering skills using Azure and Databricks technologies.

I welcome feedback, technical discussions, and suggestions for improving the architecture and implementation.

**Interested in Data Engineering opportunities and Azure data platform projects.**

## 🏷️ Topics

`azure-data-factory` · `azure-databricks` · `pyspark` · `delta-lake` · `data-engineering` · `medallion-architecture` · `etl` · `sql` · `healthcare-analytics`
