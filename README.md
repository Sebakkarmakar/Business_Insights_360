# 📊 Business Insights 360 | Power BI

## 📌 Project Overview

**AtliQ Hardware** is a rapidly growing hardware company that operates across multiple countries and sells computers and computer accessories through different channels.

Due to rapid expansion, the company faced challenges in making **data-driven business decisions**. One of the major setbacks occurred when AtliQ Hardware opened a store in the American market based mainly on surveys, intuition, and Excel-based analysis, which resulted in an unexpected loss.

To overcome these challenges and compete with organizations that have strong analytics teams, AtliQ Hardware decided to build a **data analytics and business intelligence system using Power BI**.

The goal of this project is to provide actionable insights across different business functions, including:

* 💰 Finance
* 📈 Sales
* 📢 Marketing
* 🚚 Supply Chain
* 👔 Executive Management

This project was developed by following the **Codebasics Power BI course**.

---

### 📊 Live Power BI Report

👉 [View Live Power BI Dashboard](https://lnkd.in/dT3_S3GU)

### 📁 GitHub Repository

The complete project files, documentation, and supporting resources are available in this repository.

---

# 🛠️ Tech Stack

| Technology           | Purpose                                     |
| -------------------- | ------------------------------------------- |
| **SQL / MySQL**      | Data extraction and analysis                |
| **Power BI Desktop** | Dashboard development and visualization     |
| **Power Query / M**  | Data transformation and date-table creation |
| **DAX**              | Measures, KPIs and calculations             |
| **Excel**            | Data analysis and validation                |
| **DAX Studio**       | DAX performance optimization                |
| **Power BI Service** | Publishing and sharing reports              |
| **GitHub LFS**       | Managing large project files                |

---

# 📚 Power BI Skills & Techniques Learned

During this project, I learned and implemented the following Power BI concepts:

### 🔹 Project Planning

Before starting dashboard development, it is important to understand the business requirement and stakeholder expectations.

* Understanding project objectives
* Identifying stakeholder requirements
* Defining project success criteria
* Understanding project deadlines
* Identifying risks and challenges
* Understanding required datasets and resources
* Gathering dashboard design requirements
* Understanding stakeholder expectations

### 🔹 Data Transformation & Modeling

* Data cleaning and transformation
* Creating calculated columns
* Creating calculated measures
* Data modeling
* Creating relationships between tables
* Implementing **Snowflake data modeling**
* Creating a date table using **M language**
* Data validation

### 🔹 DAX

* Creating DAX measures
* Using `DIVIDE()` to prevent divide-by-zero errors
* Creating dynamic titles
* KPI calculations
* Time intelligence calculations
* YTD and YTG calculations
* Conditional calculations
* Filter-based calculations

### 🔹 Dashboard Development

* Bookmarks to switch between visuals
* Page navigation using buttons
* Dynamic titles based on applied filters
* KPI indicators
* Conditional formatting
* Icons and background-color formatting
* Interactive filters and slicers
* Mockup-based dashboard development

### 🔹 Power BI Service

* Publishing reports to Power BI Service
* Creating Power BI Apps
* Workspace management
* Collaboration
* Access permissions
* Setting up a personal gateway
* Configuring automatic data refresh

### 🔹 Performance Optimization

* Using DAX Studio
* Optimizing DAX measures
* Improving report performance
* Following Power BI data-modeling best practices

---

# 🏢 Company Background

**AtliQ Hardware** is a hardware company that has expanded rapidly across different countries.

The company sells:

* 💻 Computers
* 🖥️ Computer accessories
* 🖱️ Peripherals
* 🌐 Networking products
* 💾 Storage products

### Sales Channels

The company sells its products through three major channels:

1. **Retailers**
2. **Direct**
3. **Distributors**

### Platforms

The business operates through:

* **Brick & Motors** – Physical/offline stores
* **E-commerce** – Online platforms such as Amazon and Flipkart

---

# 🎯 Business Problem

AtliQ Hardware faced difficulties in making effective data-driven decisions.

A major example was the company's expansion into the **American market**, where the decision was based largely on:

* Surveys
* Business intuition
* Excel-based analysis

The expansion resulted in an unforeseen loss.

At the same time, competitors had dedicated analytics teams that used data to make better strategic decisions.

Therefore, AtliQ Hardware decided to build a strong analytics system to:

* Make data-driven decisions
* Understand business performance
* Identify problem areas
* Improve profitability
* Monitor sales
* Optimize supply chain operations
* Improve marketing decisions
* Compete more effectively in the market

---

# 🚀 Project Kick-Off

Before developing the dashboard, it is important to clearly understand **what the business wants and why the dashboard is required**.

## Questions to Ask Before Starting a Power BI Project

### 🎯 Business Objectives

* What is the objective of building this Power BI dashboard?
* What business problem are we trying to solve?
* What decisions should the dashboard help stakeholders make?
* In what terms will the success of this project be measured?

### ⏰ Project Planning

* What is the project deadline?
* Is a preview expected before the final release?
* What are the major project milestones?
* What can go wrong while building the project?

### 👥 Stakeholder Requirements

* Who will use the dashboard?
* What will each stakeholder use the dashboard for?
* What are the stakeholders expecting from the dashboard?
* What are their hopes and concerns?
* Are there any specific design requirements?
* Which KPIs are most important to stakeholders?

### 📊 Data Requirements

* What data is required?
* Where is the data stored?
* How frequently is the data updated?
* What resources are required to build the dashboard?
* Are there any data-quality issues?

---

# 🗄️ Dataset Understanding

Understanding the available data is one of the most important steps before beginning analysis.

The project database contains **dimension tables** and **fact tables**.

## Dimension Tables

Dimension tables generally contain descriptive or relatively static information about business entities such as customers, products, and markets.

## Fact Tables

Fact tables contain transactional or measurable business data such as sales quantity and forecast quantity.

---

# 🗃️ Database: `gdb041`

## 👥 `dim_customer`

Contains customer-related information.

Key information:

* **75 distinct customers**
* **27 distinct markets**
* 2 platforms:

  * Brick & Motors
  * E-commerce
* 3 channels:

  * Retailer
  * Direct
  * Distributor

---

## 🌎 `dim_market`

Contains market and geographical information.

Key information:

* **27 distinct markets**
* **7 sub-zones**
* **4 regions**

### Regions

* APAC
* EU
* LATAM
* NA

---

## 📦 `dim_product`

Contains product-related information.

### Divisions

* P & A
* Peripherals
* Accessories
* PC
* N & S
* Networking
* Storage

### Product Categories

The dataset contains approximately **14 different product categories**, such as:

* Internal HDD
* Keyboard
* And other hardware categories

There are also multiple **variants** available for the same product.

---

# 📈 `fact_forecast_monthly`

This table contains the **forecast quantity** expected from customers.

Forecasting helps the business with:

* Better customer satisfaction
* Inventory planning
* Warehouse optimization
* Reducing unnecessary storage costs
* Better supply chain planning

### Important Characteristics

* The table is denormalized for analytical purposes.
* Monthly dates are represented using the **start date of the month**.
* Forecast quantity represents the expected customer demand.

---

# 💰 `fact_sales_monthly`

This table contains monthly sales information.

It is similar to `fact_forecast_monthly`, but instead of forecast quantity, it contains the actual:

> **Sold Quantity**

This allows us to compare:

**Forecast Quantity vs Actual Sold Quantity**

and identify forecast accuracy and supply chain issues.

---

# 🗄️ Database: `gdb056`

The second database contains additional business-related information.

## 🚚 `freight_cost`

Contains:

* Freight costs
* Other transportation-related costs
* Market information
* Fiscal year information

---

## 💵 `gross_price`

Contains:

* Product codes
* Gross prices

---

## 🏭 `manufacturing_cost`

Contains:

* Product codes
* Manufacturing costs
* Fiscal year

---

## 📉 `pre_invoice_deductions`

Contains:

* Customer information
* Pre-invoice deduction percentage
* Fiscal year

---

## 📉 `post_invoice_deductions`

Contains:

* Post-invoice deductions
* Other deduction-related information

---

# 🔌 Importing Data into Power BI

The project database is based on **MySQL**.

The datasets were imported into Power BI by connecting Power BI Desktop directly to the MySQL database using the required database credentials.

### Basic Flow

```text
MySQL Database
       ↓
Power BI
       ↓
Power Query
       ↓
Data Transformation
       ↓
Data Model
       ↓
DAX Measures
       ↓
Dashboard
```

---

# 🧩 Data Model

Data modeling plays a vital role in Power BI and acts as the **foundation of the entire report**.

All visuals, measures, filters, and calculations depend on the underlying data model.

A poor data model can result in:

* Poor report performance
* Incorrect calculations
* Difficult DAX
* Slow visuals
* Complicated relationships

Therefore, following proper data-modeling practices is essential.

For this project, a **Snowflake Data Model** was implemented.

## 📊 Data Model

![Business Insights 360 Data Model] <img width="1554" height="847" alt="data model" src="https://github.com/user-attachments/assets/dfeb4a1c-7377-45e4-9e3e-64b9de718183" />


---

# 🎨 Dashboard Design

After understanding the requirements and creating the data model, the dashboard was developed based on the provided business mockups.

The report consists of the following major views:

1. 🏠 Home
2. ℹ️ Info
3. 💰 Finance View
4. 📈 Sales View
5. 📢 Marketing View
6. 🚚 Supply Chain View
7. 👔 Executive View
8. 🆘 Support

---

# 🏠 Home View

The **Home View** acts as the navigation page for the entire report.

Users can navigate to different business views using interactive buttons.

### Available Views

* ℹ️ Info
* 💰 Finance
* 📈 Sales
* 📢 Marketing
* 🚚 Supply Chain
* 👔 Executive
* 🆘 Support

This makes the report more interactive and user-friendly.
 <img width="1423" height="845" alt="Screenshot 2026-10-05 113824" src="https://github.com/user-attachments/assets/9c9159d2-d012-4f72-a805-68cee9cc4b79" />


# 💰 Finance View

The Finance View provides insights into the company's financial performance.

It helps stakeholders analyze metrics such as:

* Net Sales
* Gross Margin
* Gross Margin %
* Net Profit
* Net Profit %
* Cost of Goods Sold
* Year-to-Date performance
* Year-to-Go performance

---  <img width="1419" height="842" alt="Financeview" src="https://github.com/user-attachments/assets/37906beb-cbdc-4214-8609-9d3771cc1531" />


# 📈 Sales View

The Sales View helps analyze sales performance across:

* Customers
* Products
* Markets
* Regions
* Channels
* Time periods

It helps identify high-performing and underperforming areas of the business.

---  <img width="1465" height="840" alt="Sales View" src="https://github.com/user-attachments/assets/cdbc3a8d-5121-4425-bdac-2f08b9a30c40" />


# 📢 Marketing View

The Marketing View provides insights into:

* Product performance
* Customer segments
* Markets
* Regions
* Sales performance
* Profitability

This helps the marketing team understand where business opportunities exist.

--- <img width="1427" height="843" alt="Marketingview" src="https://github.com/user-attachments/assets/8edde3c4-5568-433c-954f-02a3e3b015e7" />


# 🚚 Supply Chain View

The Supply Chain View focuses on:

* Forecast quantity
* Actual sold quantity
* Forecast accuracy
* Net error
* Product demand
* Customer demand
* Supply chain performance

This helps identify gaps between **forecasted demand and actual demand**.

---  <img width="1426" height="851" alt="Screenshot 2026-10-05 114014" src="https://github.com/user-attachments/assets/b2c77551-9ef4-41e5-b225-71db20aebb27" />


# 👔 Executive View

The Executive View provides a high-level summary of the company's overall performance.

It allows senior management to quickly understand:

* Overall sales
* Profitability
* Gross margin
* Customer performance
* Market performance
* Product performance
* Supply chain performance

---  <img width="1429" height="843" alt="Executive view" src="https://github.com/user-attachments/assets/e4db07e9-2b3e-4f83-bc1a-1d85cb36a9d6" />

* ℹ️ Info
 <img width="1423" height="849" alt="info" src="https://github.com/user-attachments/assets/45d237ed-9e7b-4b28-80c1-27244798ee94" />
* 🆘 Support 
<img width="1424" height="848" alt="support" src="https://github.com/user-attachments/assets/de38bf21-5c48-4c24-b774-fb4a7a1c8ae5" />

# 📖 Business Terminology

During this project, I learned and implemented several important business concepts.

| Term                       | Meaning                                      |
| -------------------------- | -------------------------------------------- |
| **Gross Price**            | Initial price of a product before deductions |
| **Pre-Invoice Deduction**  | Deduction applied before invoicing           |
| **Post-Invoice Deduction** | Deduction applied after invoicing            |
| **Net Invoice Sale**       | Sales value after applicable deductions      |
| **Net Sales**              | Revenue after deductions                     |
| **Gross Margin**           | Net Sales minus Cost of Goods Sold           |
| **Net Profit**             | Profit after applicable costs and expenses   |
| **COGS**                   | Cost of Goods Sold                           |
| **YTD**                    | Year to Date                                 |
| **YTG**                    | Year to Go                                   |
| **Direct**                 | Products sold directly to customers          |
| **Retailer**               | Products sold through retail businesses      |
| **Distributor**            | Products sold through distribution partners  |

---

# 📂 GitHub Large File Management

The project contains large Power BI-related files.

To manage large files efficiently, I learned how to use **Git Large File Storage (Git LFS)**.

### Topics Covered

* Uploading large files using Git LFS
* Tracking specific file extensions
* Managing large Power BI project files
* Working with GitHub repositories

Example:

```bash
git lfs install
git lfs track "*.pbix"
git add .
git commit -m "Add Power BI project"
git push
```

---

# 🎯 Key Learning Outcomes

This project helped me gain practical experience in the complete **Business Intelligence workflow**:

```text
Business Requirement
        ↓
Project Kick-Off
        ↓
Dataset Understanding
        ↓
Data Extraction
        ↓
Data Cleaning
        ↓
Data Modeling
        ↓
DAX Calculations
        ↓
Dashboard Development
        ↓
Data Validation
        ↓
Performance Optimization
        ↓
Power BI Service
        ↓
Report Publishing
        ↓
Business Insights
```

### Major Skills Developed

✅ SQL
✅ Power BI
✅ DAX
✅ Power Query
✅ Data Modeling
✅ Data Visualization
✅ Business Intelligence
✅ KPI Development
✅ Data Validation
✅ Dashboard Design
✅ Performance Optimization
✅ DAX Studio
✅ Power BI Service
✅ Git & GitHub LFS

---

# 🙏 Acknowledgement

This project was developed by following the **Codebasics Power BI course**.
---

# ⭐ Conclusion

The **Business Insights 360** project provided hands-on experience in transforming raw business data into an interactive and decision-supporting Power BI solution.

The project helped me understand not only the technical aspects of Power BI, SQL, and DAX, but also the importance of:

> **Understanding the business problem before building the dashboard.**

This project strengthened my understanding of **Data Analytics, Business Intelligence, Data Modeling, DAX, and Power BI reporting**.
