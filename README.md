# Student Records Data Warehouse (DW-Student)

## Project Overview
Designed and implemented a relational Data Warehouse (DW) in **Microsoft SQL Server** to manage academic records. The project uses dimensional modeling to enable efficient tracking of student success, module performance, and course statistics.

## Data Model (Snowflake Schema)
The database is structured as a **Snowflake Schema**. This model further normalizes dimensions to reduce data redundancy and improve organizational structure:

**Central Fact Table:** `UspehFact` - Stores core metrics such as exam attempts, success rates, and average grades.
**Normalized Dimensions (Snowflaking):** * `StudentDIM` acts as a primary dimension connected to the fact table.
    * It further branches out into sub-dimensions: `RegionDim`, `ModulDim`, and `StatusDim`.
**Direct Dimensions:** `PredmetDim` - Course details like ESPB and semester.
    * `VremeDim` - Temporal data for exam periods.

---
## Technologies Used
* **Database Engine:** Microsoft SQL Server
* **Management Tool:** SQL Server Management Studio (SSMS)
* **Language:** T-SQL
* **Modeling:** Snowflake Schema / Dimensional Modeling

---
## Database Diagram
![Database Schema](schema-diagram.png)