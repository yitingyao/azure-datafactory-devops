# Azure Data Factory DevOps Project

## Overview
This project establishes a CI/CD pipeline for Azure Data Factory using Azure DevOps to automate validation, deployment, and data processing workflows. 

---

## Key Features

### Build Pipeline Automation
- **Validation & ARM Template Generation**: Automates validation of Azure Data Factory resources and builds reusable ARM templates for consistent, repeatable deployments.

### Data Pipelines
- **Ingestion Pipelines**: Automates the loading of raw datasets (e.g., cases, deaths, hospital admissions, population data) into Azure Data Lake Storage Gen2, leveraging lookup and batch processing activities.
- **Processing Pipelines**: Transforms data through aggregations, joins with metadata, and pivots to create clean, structured outputs for analysis.
- **SQLize Pipelines**: Formats processed data for storage in SQL databases, ensuring compatibility with downstream analytical tools.

### Data Transformation Flows
- **Scalable Transformations**: Executes column-level transformations like renaming, pivoting, and aggregation to structure data for analysis.
- **Optimized Storage**: Outputs are structured into containers (raw, processed, lookup) in ADLS Gen2 for efficient access.

### Scheduling & Automation
- **Triggering**: Tumbling window triggers ensure pipelines run on a scheduled cadence for consistent data refreshes.
- **Integration**: Seamlessly integrates with Azure DevOps to streamline development and deployment workflows.

---

## Results
- **Automated CI/CD**: Simplifies validation and deployment processes for Azure Data Factory.
- **Efficient Data Processing**: Ensures robust, scalable workflows for managing large datasets and generating structured outputs.

