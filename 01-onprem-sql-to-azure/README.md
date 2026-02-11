# On-Prem SQL Server → Azure SQL Migration using Azure Data Factory

## 📌 Project Overview

This project demonstrates a hybrid data migration pipeline that copies data from an on-premises SQL Server database to Azure SQL Database using Azure Data Factory (ADF) and a Self-Hosted Integration Runtime.

The goal is to simulate a real enterprise migration scenario where legacy on-prem systems are modernized into cloud infrastructure.

---

## 🧱 Architecture

![Pipeline](01-onprem-sql-to-azure/screenshots/Onprem to Azure.png)

### Flow Explanation

1. Azure Data Factory triggers a pipeline
2. Pipeline communicates with Self-Hosted Integration Runtime (SHIR)
3. SHIR securely connects to on-prem SQL Server
4. Data is copied into Azure SQL Database
5. Pipeline logs execution results

SHIR acts as a secure bridge between local infrastructure and Azure.

---

## 🛠 Tools & Services Used

* Microsoft SQL Server (On-Prem)
* Azure SQL Database
* Azure Data Factory
* Self-Hosted Integration Runtime
* SQL Server Management Studio
* GitHub (version control)
* ARM Template (infrastructure export)

---

## 🚀 Implementation Steps

### Step 1 — Create On-Prem Database

* Created BikeStores sample database
* Defined schemas and relational tables

### Step 2 — Create Azure SQL Database

* Provisioned Azure SQL target database
* Configured firewall access

### Step 3 — Setup Azure Data Factory

* Created ADF instance
* Installed Self-Hosted Integration Runtime

### Step 4 — Create Linked Services

* On-prem SQL connection
* Azure SQL connection

### Step 5 — Build Copy Pipeline

* Created Copy activity
* Configured source & sink datasets
* Executed pipeline

### Step 6 — Validate Migration

* Verified rows copied successfully
* Confirmed schema integrity

---

## ✅ Result

✔ Successful hybrid data migration
✔ Secure on-prem → cloud transfer
✔ Automated pipeline execution
✔ Reproducible deployment using ARM template

---

## 📂 Repository Structure

```
/pipelines
/datasets
/linkedServices
/integrationRuntimes
/screenshots
README.md
```

---

## 📸 Screenshots

Add your screenshots inside `/screenshots` folder and reference them here:

![On-prem Linked services](01-onprem-sql-to-azure/screenshots/onprem-linked-services.png)

![Azure Linked services](01-onprem-sql-to-azure/screenshots/azure-linked-services.png)

![SHIR status online](01-onprem-sql-to-azure/screenshots/shir-status-online.png)

![Azure Data Factory pipeline canvas](01-onprem-sql-to-azure/screenshots/pipeline-canvas.png)

![Pipeline run succeeded](01-onprem-sql-to-azure/screenshots/pipeline-success.png)

![OnpremSQL table with copied rows](01-onprem-sql-to-azure/screenshots/onprem-rows.png)

![AzureSQL table with copied rows](01-onprem-sql-to-azure/screenshots/azure-rows.png)

---

## 💡 Key Learning Outcomes

* Hybrid cloud architecture design
* Azure Data Factory pipeline creation
* Self-Hosted Integration Runtime configuration
* Secure enterprise data movement
* Infrastructure export using ARM templates
* Cloud cost awareness and lifecycle management

---

## 🔄 Rebuild Instructions

This project can be redeployed using the exported ARM template:

1. Azure Portal → Deploy custom template
2. Upload ARM template
3. Select resource group
4. Deploy

SHIR can be reinstalled locally in minutes.

---

## 👤 Author

Built as a hands-on cloud data engineering lab project
to practice enterprise migration workflows.

---

## 📜 License

Educational project — free to reuse and modify.
