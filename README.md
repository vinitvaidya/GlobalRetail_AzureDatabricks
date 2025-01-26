# GlobalRetail_AzureDatabricks
# 🌍 Data Solutions for Global Retail

## Project Overview  
This project focuses on building a modern, scalable data pipeline for a global retail company operating in **27 countries**, with **11,000+ physical stores** and a robust e-commerce platform. The goal was to transform raw data into analytics-ready datasets using **Databricks** and **Apache Spark**, leveraging the **Medallion Architecture** to enable real-time, company-wide analytics.  

---

## 🚀 Problem Statement  
The retail giant generates **massive daily data volumes** from diverse sources:  
- **Customer Data (CRM)**: 500M records (CSV)  
- **Product Catalog**: 1M SKUs (JSON)  
- **Transaction History**: 10B annual records (Parquet)  

### Challenges  
1. **Data Quality Issues**: Inconsistencies and missing values across datasets  
2. **Varied Data Formats**: Different file types and schemas across regions  
3. **Complex ETL**: Managing large-scale, multi-country data ingestion and transformation  

---

## 💡 Solution Architecture  

The project was implemented using the **Medallion Architecture**:  
1. **Bronze Layer**: Ingest raw data using **Apache Spark** for distributed, high-performance processing.  
2. **Silver Layer**: Clean and standardize the data to resolve inconsistencies and apply business rules.  
3. **Gold Layer**: Aggregate and optimize data for analytics and reporting.  

### Tools & Technologies  
- **Databricks**: Unified analytics platform for scalable data engineering  
- **Apache Spark**: High-speed distributed data processing for ETL workflows  
- **Delta Lake**: Reliable data architecture with ACID transactions and versioning  
- **Databricks SQL**: High-performance query engine for analytics  
- **Power BI**: Business intelligence dashboards for insights (secondary focus)  

---

## 📊 Data Pipeline Flow  

```mermaid
graph TD;
    A[Raw Data] -->|Bronze Layer| B[Ingested Data];
    B -->|Silver Layer| C[Cleaned Data];
    C -->|Gold Layer| D[Analytics-Ready Data];
    D --> E[Power BI Dashboards];
