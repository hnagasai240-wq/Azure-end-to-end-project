# Azure Databricks End-to-End Project 🚀

This project demonstrates an **end-to-end data engineering pipeline** built using **Azure Databricks, Delta Lake, and Power BI**. It covers the complete workflow from **data ingestion → ETL → Delta Live Tables → Star Schema → Data Warehouse → Reporting**.

---

## 📌 Architecture Overview
<img width="733" height="356" alt="Architecture" src="https://github.com/user-attachments/assets/d51b5706-cdae-4555-946a-865fdd31fc32" />


The pipeline is designed as follows:  

1. **Data Ingestion**
   - Source data is stored in **Azure Data Lake Gen2** in `.parquet` format.  
   - GitHub is used for version control and collaboration.  
   - Security is managed using **Azure Active Directory (AAD)** and **Key Vault**.  

2. **ETL (Extract, Transform, Load)**
   - **Databricks & PySpark** are used to perform transformations.  
   - Data is ingested from the **bronze layer** (raw data) and processed into the **silver layer** (clean/curated data).  

3. **Delta Live Tables**
   - Delta Live Tables are leveraged to create **automated, reliable, and incremental data pipelines**.  
   - Data is modeled into a **Star Schema** (Fact + Dimension tables).  

4. **Data Warehouse**
   - Processed data is stored in **Azure Synapse Analytics** (Warehouse layer).  

5. **Reporting**
   - **Power BI** dashboards are connected to Synapse to visualize insights.  

---

## 📂 Repository Structure  

```plaintext
📦 Databricks-ETE-Project
 ┣ 📜 Databricks ETE Project.dbc     # Databricks notebook archive
 ┣ 📜 README.md                      # Project documentation
 ┣ 📜 customer_first.parquet         # Customer dataset (raw)
 ┣ 📜 customers_second.parquet       # Customer dataset (curated)
 ┣ 📜 orders_first.parquet           # Orders dataset (raw)
 ┣ 📜 orders_second.parquet          # Orders dataset (curated)
 ┣ 📜 products_first.parquet         # Products dataset (raw)
 ┣ 📜 products_second.parquet        # Products dataset (curated)
 ┣ 📜 regions.parquet                # Regions dimension data
