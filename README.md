# ETL Practice — Sales Data (MySQL + Python/Jupyter + XAMPP)

This project implements a full **ETL (Extract–Transform–Load)** workflow using a sample `sales.csv` file, Python (Jupyter), and a MySQL database hosted via XAMPP.

The steps include **reading**, **cleaning**, **normalizing**, **loading** into MySQL, and **verifying** the final dataset.

---

## 1. Project Workflow Overview

### Extract (Read `sales.csv`)
- Load the CSV using safe encoding fallbacks and confirm shape/columns.

### Transform (Clean, Integrate, Enrich)
- Perform data type corrections  
- Drop duplicates  
- Parse dates  
- Convert numeric fields  
- Trim whitespace  
- Normalize the dataset into logical tables:  
  - `Customers`  
  - `Products`  
  - `Orders`  
  - `OrderDetails`

### Load (Store into MySQL/XAMPP)
- Use the SQL Schema Block to create the normalized MySQL database (`sales_db`) in phpMyAdmin.  
- In the notebook:  
  - Connect to MySQL  
  - Insert Customers & Products  
  - Retrieve and map generated primary keys  
  - Insert Orders & OrderDetails while maintaining referential integrity  

### Verification
- Validate row counts, joins, top-selling products, and foreign key consistency using verification queries.

---

## 2. File Structure

```
📁 project-root
│── README.md
│── sales.csv
└── etl_sales.ipynb        # Jupyter notebook with all ETL steps
```

---

## 3. Quick Start Guide (Full Runnable Checklist)

### Prerequisites
- XAMPP installed and running (MySQL service ON)
- VS Code with Jupyter extension
- Python 3.10.11 + the following libraries:
  ```
  pandas
  mysql-connector-python
  numpy
  ```

---

## 4. Execution Steps (Run in Exact Order)

### Step 1 — Start MySQL
1. Open **XAMPP Control Panel**
2. Start **MySQL**

---

### Step 2 — Extract & Transform
1. Open **VS Code → Jupyter Notebook**
2. Place the notebook in the same folder as `sales.csv`
3. Run all **Extraction**, **Cleaning**, and **Normalization** sections.
4. Inspect intermediate DataFrames to ensure no malformed rows.

---

### Step 3 — Create MySQL Schema
1. Open **phpMyAdmin**
2. Create database: `sales_db`
3. Paste & execute the **SQL Schema Block**

---

### Step 4 — Load into MySQL
1. Return to the Jupyter notebook
2. Run all sections under **Load**
3. Fix any errors (often missing ID mappings)

---

### Step 5 — Verify Load
1. Run the **Verification** section in the notebook
2. Execute the SQL Verification block in phpMyAdmin.

---

## 5. Notes
- All code is rerunnable; truncate tables before reloading.
- Encoding fallback protects against malformed CSVs.
- Normalization enforces referential integrity.

---

## 6. Technologies Used
- **Python (pandas, numpy, mysql-connector)**
- **MySQL (XAMPP)**
- **phpMyAdmin**
- **Jupyter Notebook (VS Code)**
