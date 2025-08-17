# 🏢 Real Estate Analytics – Power BI Dashboard Project

This Power BI project provides a dynamic, insightful dashboard for analyzing tenant activity and rental revenue in the real estate sector. Built from AI-generated data, it simulates the real-world needs of a property manager or investor.

---

## 📊 Project Overview

The report consists of **two interactive dashboards**:
- **Tenant Summary**: Gives detailed insight into tenants, their contributions, and lease activity.
- **Rent Summary**: Shows performance across properties and regions, helping with financial and operational analysis.

---

## 🧠 Business Value & Storytelling

### 🎯 Why These Dashboards Matter:

**Real estate decision-makers** rely on clear, actionable data to:
- Monitor rent inflow and delinquency
- Identify top and underperforming properties
- Understand tenant patterns for retention and marketing

## 🗺️ Data Model: Star Schema

![Schema](images/schema-diagram.png)

## 💡 Technical Context & Challenges

This project was built entirely on macOS using Power BI Service — without access to Power BI Desktop.

**Key Challenge: Manual Schema Modelling in Power BI Web**

Power BI Service does not offer a drag-and-drop model view by default, and since Desktop isn’t available on macOS, I manually built a semantic model within the warehouse. This required:

- Creating a **star schema** from scratch by understanding business entities and how they relate.
- Manually linking dimension tables (Tenants, Properties, Funds) to the fact table (Rentals) using foreign key logic.
- Verifying **cardinality and referential integrity** without visual modelling support (as in Desktop’s Diagram View).
- Relying on a structured, AI-generated CSV file that was **clean enough to bypass Power Query** entirely — meaning schema accuracy and modelling became the key focus.

This approach tested my knowledge of dimensional modeling, data relationships, and how analytical models support end-user reporting — **especially under platform constraints**.

---

### 🧱 Why a Star Schema?

A star schema was chosen to:
- Simplify report navigation and performance
- Enable intuitive filtering and drill-down across Tenants, Funds, and Properties
- Support measures like `Total Rent`, `Avg Rent`, and `Tenant Activity` without ambiguous joins

Each table has a single, well-defined role:
- **DimTenants** enables grouping and performance analysis by tenant
- **DimFunds** supports investment portfolio breakdowns
- **DimProperties** ties together physical locations with rental transactions
- **FactRentals** contains the metrics needed for business KPIs


## 🔗 Live Report
> [👉 View the dashboard here (Public Power BI link)](https://app.powerbi.com/links/KF_B8HuPyE?ctid=8775661c-d343-4930-a990-8a3360e2ca1f&pbi_source=linkShare)

## 📌 About This Project
This project was developed to demonstrate Power BI data modelling, visualisation, and storytelling capabilities for real estate analytics. Suitable for property management, real estate investors, or business analysts.

---

**⚠️ Note:** This is a public project with AI-generated data — no real customer or financial information is used.

t
