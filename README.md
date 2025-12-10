```{=html}
<!-- Visual & Modern README -->
```
```{=html}
<p align="center">
```
`<img src="https://img.icons8.com/?size=100&id=90572&format=png&color=000000" width="120"/>`{=html}
```{=html}
</p>
```
```{=html}
<h1 align="center">
```
📦 E-Commerce Sales ETL Pipeline
```{=html}
</h1>
```
```{=html}
<p align="center">
```
`<b>`{=html}DSA2040VA --- Data Analytics
Coursework`</b>`{=html}`<br>`{=html} `<b>`{=html}Author:`</b>`{=html}
Geoffrey C. Mwangi
```{=html}
</p>
```

------------------------------------------------------------------------

## 🎯 **Project Purpose**

Turn raw sales CSV data into a clean, structured MySQL database using a
real-world **ETL pipeline**:

```{=html}
<p align="center">
```
`<img src="https://img.icons8.com/?size=100&id=82769&format=png&color=000000" width="70"/>`{=html}
➜
`<img src="https://img.icons8.com/?size=100&id=108784&format=png&color=000000" width="70"/>`{=html}
➜
`<img src="https://img.icons8.com/?size=100&id=13665&format=png&color=000000" width="70"/>`{=html}
```{=html}
</p>
```
**Extract → Transform → Load**

------------------------------------------------------------------------

## 🗂️ **Folder Structure Overview**

    📁 ETL_DSA2040VA/
    │
    ├── 📁 data/
    │     └── sales.csv
    │
    ├── 📁 etl/
    │     ├── extract.py
    │     ├── transform.py
    │     ├── load.py
    │     └── etl.py
    │
    ├── 📁 notebooks/
    │     └── analysis.ipynb
    │
    └── README.md

------------------------------------------------------------------------

## ⚙️ **ETL Workflow Overview**

### 🔵 1. **Extract**

```{=html}
<p align="center">
```
`<img src="https://img.icons8.com/?size=100&id=23107&format=png&color=000000" width="80"/>`{=html}
```{=html}
</p>
```
-   Auto-detect CSV encoding\
-   Loads data using Pandas\
-   Reports rows, columns, missing values

------------------------------------------------------------------------

### 🟡 2. **Transform**

```{=html}
<p align="center">
```
`<img src="https://img.icons8.com/?size=100&id=82769&format=png&color=000000" width="80"/>`{=html}
```{=html}
</p>
```
Includes:

✔ Cleaning text fields\
✔ Fixing dates\
✔ Standardizing numeric columns\
✔ Removing duplicates\
✔ Feature creation:\
- `order_year`\
- `order_month`\
- `revenue_per_unit`

------------------------------------------------------------------------

### 🟢 3. **Load**

```{=html}
<p align="center">
```
`<img src="https://img.icons8.com/?size=100&id=13665&format=png&color=000000" width="80"/>`{=html}
```{=html}
</p>
```
-   Loads cleaned data into MySQL/MariaDB\
-   Uses SQLAlchemy\
-   Builds table: **fact_sales**\
-   Enforces schema & key constraints

------------------------------------------------------------------------

## 🗄️ **Database Schema (Visual)**

    ┌───────────────────────┐
    │      fact_sales        │
    ├───────────────────────┤
    │ orderNumber (PK)       │
    │ orderDate              │
    │ quantityOrdered        │
    │ priceEach              │
    │ sales                  │
    │ status                 │
    │ productCode            │
    │ customerNumber         │
    │ order_year             │
    │ order_month            │
    └───────────────────────┘

------------------------------------------------------------------------

## 🚀 **How to Run the Project**

### **1. Install Requirements**

``` bash
pip install -r requirements.txt
```

### **2. Configure MySQL (XAMPP)**

Edit inside `etl/load.py`:

    HOST     = "localhost"
    USER     = "root"
    PASSWORD = ""
    DATABASE = "sales_dw"

### **3. Run Complete ETL**

``` bash
python etl/etl.py
```

### **4. Launch Jupyter Notebook**

``` bash
jupyter notebook notebooks/analysis.ipynb
```

------------------------------------------------------------------------

## 📊 **Example Visual Outputs**

-   Sales trend plots\
-   Revenue per region\
-   Customer segmentation\
-   Missing value heatmaps\
-   Cleaned dataset previews

------------------------------------------------------------------------

## 📈 **Sample Visual: ETL Pipeline Diagram**

        ┌────────────┐
        │   Extract   │
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │  Transform  │
        └──────┬──────┘
               │
        ┌──────▼──────┐
        │     Load     │
        └──────────────┘

------------------------------------------------------------------------

## 🤝 Contributing

    git clone https://github.com/<username>/ETL_DSA2040VA.git

------------------------------------------------------------------------

## 🎓 Acknowledgements

This project was created for the **DSA2040VA -- Data Analytics** module,
applying real-world ETL industry practices.
