# ☁️ Azure Data Fundamentals Projects

> **DP-900 Azure Data Fundamentals | Microsoft Azure | SQL | Microsoft Fabric | Cloud Data Services**

![Microsoft Azure](https://img.shields.io/badge/Microsoft%20Azure-Data%20Fundamentals-blue?style=flat-square)
![DP-900](https://img.shields.io/badge/DP--900-Azure%20Data%20Fundamentals-0078D4?style=flat-square)
![SQL](https://img.shields.io/badge/SQL-Data%20Analysis-orange?style=flat-square)
![Microsoft Fabric](https://img.shields.io/badge/Microsoft-Fabric-yellow?style=flat-square)

---

## 🔎 Overview

This repository contains practical exercises and projects completed during **Microsoft Azure Data Fundamentals (DP-900)** training as part of my Data Technician Bootcamp.

The training introduced the core concepts involved in storing, processing and analysing data in the cloud using different Microsoft Azure data services.

The work covered:

- ☁️ Cloud computing fundamentals
- 🗄️ Relational data with **Azure SQL Database**
- 📦 Non-relational data with **Azure Storage Accounts**
- 🌐 NoSQL data with **Azure Cosmos DB**
- 🏞️ Analytical workloads using **Microsoft Fabric Lakehouse**
- ⚡ Real-time data ingestion using **Eventstreams**
- 🔄 Data ingestion and integration methods
- 🧮 SQL querying and data analysis
- 📊 Large-scale and real-time analytics

---

## ☁️ Cloud Computing Fundamentals

The training introduced the core principles of cloud computing and how organisations can use cloud technologies to store data, run applications and access computing resources without relying entirely on local infrastructure.

Key concepts included:

- Scalability
- Flexibility
- Remote accessibility
- Reduced dependency on physical infrastructure
- Backup and disaster recovery
- Cloud pricing and consumption models
- Security considerations
- Public, private, hybrid and community cloud models

---

## 🏗️ Cloud Service Models

The differences between the main cloud service models were explored:

| Model | Description |
|---|---|
| 🖥️ **IaaS** | Infrastructure such as virtual machines, networking and storage provided through the cloud |
| 🛠️ **PaaS** | Managed platforms used to build, deploy and manage applications without managing the underlying infrastructure |
| 🌐 **SaaS** | Complete software applications accessed through the internet |

Understanding these models helped demonstrate how different organisations can choose the appropriate level of infrastructure control and management.

---

# 🗄️ Relational Data – Azure SQL Database

Azure SQL Database was used to explore how **relational data** can be stored and queried in the cloud.

Relational databases organise information into structured tables containing:

- Rows
- Columns
- Primary keys
- Foreign keys
- Relationships between tables

This approach is particularly suitable for structured business information such as:

- Customer records
- Product information
- Orders
- Sales transactions
- Inventory
- Employee information

---

## 🧮 SQL Data Analysis

SQL was used to retrieve, filter, organise and summarise structured data.

### SELECT

`SELECT` was used to retrieve specific columns from a table.

```sql
SELECT ProductName, Price
FROM Products;
```

---

### 🎯 WHERE

`WHERE` was used to filter records based on specified conditions.

```sql
SELECT *
FROM Sales
WHERE Country = 'United Kingdom';
```

This can be used to answer questions such as:

- Which customers are located in a particular country?
- Which products exceed a certain price?
- Which sales transactions belong to a particular region?

---

### ↕️ ORDER BY

`ORDER BY` was used to sort query results.

```sql
SELECT ProductName, Revenue
FROM Sales
ORDER BY Revenue DESC;
```

This makes it possible to identify:

- Highest-performing products
- Lowest-performing products
- Largest sales
- Highest-value customers

---

### 📊 GROUP BY

`GROUP BY` was used to aggregate data into categories.

```sql
SELECT Category, SUM(Revenue) AS TotalRevenue
FROM Sales
GROUP BY Category;
```

This can be used to compare performance across:

- Product categories
- Countries
- Regions
- Customer groups
- Sales periods

---

### 🔗 JOINs

`JOIN` operations were used to combine related data stored across multiple tables.

```sql
SELECT
    Customers.CustomerName,
    Orders.OrderID,
    Orders.OrderDate
FROM Customers
INNER JOIN Orders
    ON Customers.CustomerID = Orders.CustomerID;
```

Using JOINs demonstrates how relational databases can connect information without storing everything in a single table.

---

## 🛍️ Retail & Sales Analysis

SQL techniques were applied to business-style datasets to extract useful insights.

Examples of analytical questions included:

✅ Which products generate the most sales?  
✅ Which customers have placed orders?  
✅ Which regions generate the most revenue?  
✅ What is the average product value?  
✅ How do sales differ between product categories?  
✅ Which customers or products meet specific criteria?  
✅ How can related customer, order and product information be combined?  

This demonstrates how SQL can turn structured transactional data into information that supports business decision-making.

---

# 📦 Non-Relational Data – Azure Storage

Azure Storage was explored as a way to store large amounts of cloud-based data that may not fit a traditional relational database structure.

Storage Accounts can support different types of storage, including:

- 📄 Blob storage
- 📁 File storage
- 📬 Queue storage
- 📋 Table storage

This provides flexible storage for structured, semi-structured and unstructured information.

---

## 📁 Data Formats

Different file formats can be used depending on the type of workload.

| Format | Typical Use |
|---|---|
| `CSV` | Raw tabular data and imports |
| `JSON` | Semi-structured application and API data |
| `Parquet` | Efficient analytical workloads and large datasets |

Understanding these formats demonstrated how the same data can be stored differently depending on whether the priority is compatibility, flexibility or analytical performance.

---

# 🌐 Azure Cosmos DB

Azure Cosmos DB was explored as a **non-relational / NoSQL database service**.

Unlike traditional relational databases, NoSQL systems are designed to support flexible data structures and can be useful when applications require:

- High scalability
- Flexible schemas
- Large volumes of data
- Globally distributed access
- Fast application response times

This introduced the difference between relational database workloads and modern non-relational data solutions.

---

# 🏞️ Microsoft Fabric Lakehouse

Microsoft Fabric was used to explore **large-scale analytical workloads**.

The **Lakehouse** approach combines characteristics of a data lake and a traditional data warehouse, allowing organisations to store large quantities of data while still supporting structured analytical workloads.

A Lakehouse can contain data from multiple sources, including:

- Business applications
- Databases
- CSV files
- JSON data
- Streaming sources
- Operational systems

This provides a central location where data can be prepared for reporting, analytics and further processing.

---

## 🔄 Data Ingestion

A key part of working with cloud analytics platforms is moving data from source systems into analytical storage.

The training covered different approaches to ingestion, including:

- Uploading files
- Importing structured datasets
- Connecting to database sources
- Data pipelines
- ETL processes
- Azure Data Factory concepts
- Real-time streaming using Eventstreams

These approaches demonstrate the difference between **batch ingestion** and **real-time ingestion**.

---

## ⚡ Real-Time Data with Eventstreams

Microsoft Fabric **Eventstreams** were used to explore how continuously generated data can be ingested and processed.

Rather than waiting for a scheduled data import, streaming data can enter an analytical environment as events occur.

Example use cases include:

- Live sales transactions
- Website activity
- IoT sensor readings
- Application events
- Operational monitoring

This demonstrated how modern analytics platforms can support both historical and real-time analysis.

---

## 🔁 Example Data Flow

A simplified cloud analytics workflow explored through the training can be represented as:

```text
Data Sources
     ↓
Data Ingestion
     ↓
Azure Storage / Azure SQL / Cosmos DB
     ↓
Microsoft Fabric Lakehouse
     ↓
Transformation & Analysis
     ↓
Reports / Business Insights
```

For real-time data:

```text
Live Data Source
     ↓
Eventstream
     ↓
Microsoft Fabric
     ↓
Lakehouse / Analytics
     ↓
Real-Time Insights
```

---

# 📊 Analytical Workloads

The course demonstrated the difference between **transactional** and **analytical** workloads.

### Transactional workloads

Used for everyday business operations such as:

- Recording orders
- Updating customers
- Managing inventory
- Processing transactions

Azure SQL Database is an example of a service that can support structured transactional data.

### Analytical workloads

Used to analyse larger amounts of historical or aggregated information to identify trends and patterns.

Examples include:

- Sales trend analysis
- Customer behaviour analysis
- Product performance
- Revenue analysis
- Business reporting

Microsoft Fabric provides tools for these larger analytical workloads.

---

## 🔄 Azure Data Factory & ETL Concepts

Azure Data Factory was explored as a cloud data integration and ETL service.

The core process can be described as:

**Extract → Transform → Load**

It can be used to:

- Connect to different data sources
- Collect data
- Move data between systems
- Transform datasets
- Automate pipelines
- Schedule processing
- Prepare data for reporting and analytics

This demonstrated how organisations can automate data movement rather than manually transferring datasets between systems.

---

## 🧠 Azure Services & Workloads

| Service | Data / Workload |
|---|---|
| 🗄️ **Azure SQL Database** | Structured relational data |
| 📦 **Azure Storage Account** | Files and non-relational cloud storage |
| 🌐 **Azure Cosmos DB** | NoSQL and flexible application data |
| 🏞️ **Microsoft Fabric Lakehouse** | Large-scale analytical data |
| ⚡ **Eventstreams** | Real-time data ingestion |
| 🔄 **Azure Data Factory** | Data integration and ETL |
| 📊 **Microsoft Fabric** | Analytics and data processing |

---

## 🎨 Data Architecture Understanding

The exercises helped build an understanding that organisations rarely use one data technology for every task.

A modern data environment may use:

- **Azure SQL Database** for structured transactional information
- **Azure Storage** for files and raw datasets
- **Cosmos DB** for flexible non-relational application data
- **Fabric Lakehouse** for consolidated analytical workloads
- **Eventstreams** for real-time data
- **Data Factory** for automated movement and transformation

Choosing the appropriate service depends on the **structure, volume, velocity and intended use of the data**.

---

## 💡 What I Practised

Through the DP-900 training, I developed practical experience and understanding in:

✅ Cloud computing fundamentals  
✅ Microsoft Azure data services  
✅ Relational and non-relational data concepts  
✅ Azure SQL Database  
✅ Azure Storage Accounts  
✅ Azure Cosmos DB  
✅ Microsoft Fabric  
✅ Lakehouse architecture  
✅ Large-scale data analytics  
✅ Batch and real-time data ingestion  
✅ Eventstreams  
✅ Data integration and ETL concepts  
✅ Azure Data Factory  
✅ SQL `SELECT` statements  
✅ Filtering with `WHERE`  
✅ Sorting with `ORDER BY`  
✅ Aggregating with `GROUP BY`  
✅ Combining tables using `JOIN`  
✅ Analysing retail and sales data  
✅ Selecting appropriate services for different data workloads  

---

## 🎯 Key Skills

`Microsoft Azure` • `DP-900` • `Cloud Computing` • `Azure SQL Database` • `SQL` • `Azure Storage` • `Azure Cosmos DB` • `Microsoft Fabric` • `Lakehouse` • `Eventstreams` • `Azure Data Factory` • `ETL` • `Data Ingestion` • `Relational Data` • `NoSQL` • `Data Analytics` • `SELECT` • `WHERE` • `ORDER BY` • `GROUP BY` • `JOIN`

---

## 📚 Project Context

This work was completed during **Azure Data Fundamentals (DP-900)** training as part of my Data Technician Bootcamp.

The project demonstrates foundational knowledge of how data can be **stored, ingested, queried, processed and analysed across different Microsoft Azure services**, providing practical exposure to the cloud data concepts relevant to **Data Technician, Data Analyst and entry-level cloud data roles**.
