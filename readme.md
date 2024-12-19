# Azure Data Factory DevOps Project

## Overview
This project implements a CI/CD pipeline for Azure Data Factory, automating validation, ARM template generation, and deployment. It supports ingestion and transformation of COVID-related datasets with robust data pipelines and Azure DevOps automation.

---

## Key Features

### Build Pipeline Automation
- **Validation & Deployment**: The `adf-build-pipeline.yml` validates Azure Data Factory resources and generates ARM templates for deployment.
- **Artifact Publishing**: Automatically packages and publishes ARM templates to Azure DevOps for release pipelines.

### Data Transformation Flows
1. **Data Flow: `df_transform_cases_deaths`**
   - Filters European cases and performs pivot transformations to summarize cases and deaths by country.
   - Enriches datasets using metadata lookups and outputs results to Azure Data Lake Storage Gen2.

2. **Data Flow: `df_transform_hospital_admissions`**
   - Aggregates hospital admission data into weekly and daily summaries.
   - Joins with date and country dimensions, pivoting results for standardized reporting.

### Data Ingestion Pipelines
- **Pipeline: `pl_ingest_ecdc_data`**  
  - Automates ingestion of ECDC data with lookup and `ForEach` activities for batch processing.
- **Pipeline: `pl_ingest_population_data`**  
  - Processes raw population datasets, cleans columns, and formats data for analysis.

### Storage Integration
- **Azure Databricks Mounts**: Configured raw, processed, and lookup containers in ADLS Gen2 using secure credentials.

### Scheduling & Automation
- **Tumbling Window Triggers**: Automated pipeline executions based on scheduled intervals for consistent data processing.

---

## Results
- **Streamlined Automation**: CI/CD integration with Azure DevOps simplifies validation and deployments.
- **Efficient Data Processing**: Data flows handle large datasets with robust transformations and scalable storage solutions.
