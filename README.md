# 📊 Inventory Analysis for Wish Platform  

## 🚀 Project Overview  
This project is a **Business Intelligence & Data Warehousing** solution focused on **inventory analysis** for the Wish e-commerce platform. The goal is to analyze **product performance, merchant success, and stock profitability** using a **ROLAP (Relational OLAP) model**, implemented with **PostgreSQL, Python, and Power BI**.  

💡 **Project Highlights:**  
- **Python-powered ETL**: Data extraction and transformation were done in **VS Code using Jupyter Notebooks (`.ipynb`)**.  
- **ROLAP-based Data Warehouse**: PostgreSQL serves as the **data warehouse**, enabling efficient querying.  
- **Interactive Power BI Dashboard**: A **Welcome Page** and a **Dashboard** visualize key inventory insights.  

---

## **📐 Data Warehouse Design**  
This project follows a **Snowflake Schema**, structured as follows:  

### **🔹 Fact Table: `Inventory_Fact_Cleaned.csv`**
- Stores key **measures** (e.g., inventory levels, units sold, ratings) and connects to dimensions.

### **🔸 Dimension Tables:**
| Table | Description |
|--------|------------|
| `Dim_Product_Cleaned.csv` | Contains product details (title, price, rating, country of origin). |
| `Dim_Merchant_Cleaned.csv` | Stores merchant-related data (name, revenue, total sales). |
| `Dim_Shipping_Cleaned.csv` | Includes shipping type and cost details. |
| `Dim_Product_Origin_Country_Cleaned.csv` | Sub-dimension linking products to origin countries. |
| `Dim_Profile_Cleaned.csv` | Sub-dimension containing merchant profile information. |

### **📂 Supporting Files**
- `Computed insight - Success of active sellers.csv`: Original dataset containing merchant-related metrics.
- `cleaned_summer-products-with-rating-and-performance_2020-08.csv`: Cleaned source dataset.
- `combined_dataset.csv`: Merged dataset for better analysis.
- `tables_creation.ipynb`: **Python script that generates the cleaned CSV files from raw data.**

---

## **⚙️ Project Workflow**
This project follows a structured **ETL + ROLAP + Visualization** workflow:

1️⃣ **Extract & Transform** *(Python & Pandas in VS Code)*  
   - Data cleaning and processing were done in **Jupyter Notebooks (`.ipynb` files)** within VS Code.  
   - `products_dataset.ipynb` → Cleans and prepares product data.  
   - `computed_insights_dataset.ipynb` → Cleans the computed insights dataset.  
   - `tables_creation.ipynb` → Processes raw data into cleaned CSV files.  

2️⃣ **Load & Store** *(PostgreSQL - ROLAP)*  
   - The cleaned data was **loaded into PostgreSQL**, enabling **dynamic querying** for analysis.

3️⃣ **Analyze & Visualize** *(Power BI)*  
   - `Inventory Analysis for Wish Platform.pbix` contains:
     - **Welcome Page**: Overview of key KPIs.
     - **Dashboard**: Interactive visualizations on inventory performance.

---

## **📊 Key KPIs & Insights**
📌 **Featured KPIs in the Power BI Dashboard:**
- ✅ **Inventory Turnover Ratio**: Measures how efficiently inventory is being sold and replaced.
- ✅ **Stock Keeping Profitability**: Evaluates the profitability of holding stock for merchants.
- ✅ **Top-Selling Products**: Identifies best-performing products based on sales.
- ✅ **Shipping Cost Analysis**: Examines cost-effectiveness of different shipping options.

🔍 **Additional insights from computed metrics:**
- Merchant performance trends based on **active seller success metrics**.
- Patterns in **inventory depletion and restocking trends**.

---

## **📂 Files & How to Use Them**
| File Name | Purpose |
|-----------|---------|
| `cleaned_summer-products-with-rating-and-performance_2020-08.csv` | Processed dataset ready for analysis. |
| `Inventory_Fact_Cleaned.csv` | Fact table linking sales & inventory data. |
| `Dim_Product_Cleaned.csv`, `Dim_Merchant_Cleaned.csv`, etc. | Dimension tables for analysis. |
| `Inventory Analysis for Wish Platform.pbix` | **Power BI Dashboard**. |
| `tables_creation.ipynb` | **Python script that generates cleaned CSV files** from raw data. |
| `computed_insights_dataset.ipynb` | Cleans and prepares merchant-related computed insights. |

---

## **💡 How to Run This Project**
### **1️⃣ Generate Cleaned Data**
- Download the 2 initial cleaned datasets (`cleaned_Computed insight - Success of active sellers.csv` & `cleaned_summer-products-with-rating-and-performance_2020-08.csv`).
- Open `tables_creation.ipynb` in **VS Code** and run the script to generate cleaned CSVs.

### **2️⃣ Setup PostgreSQL Data Warehouse**
- Load the cleaned CSV files into PostgreSQL.

### **3️⃣ Open the Power BI Dashboard**
- Open `Inventory Analysis for Wish Platform.pbix` in **Power BI**.
- Explore insights through the **Welcome Page & Dashboard**.

### **4️⃣ Run Jupyter Notebooks for Custom Analysis**
- Open `computed_insights_dataset.ipynb` for additional merchant analytics.

---

## **📬 Contact**
📢 Found this project useful? **Give it a ⭐ on GitHub!**  
This project wouldn't have been realized without the support and strong passion of my dear colleague **[Mayssam Hassen](https://www.linkedin.com/in/mayssam-hassen-58a615252/)** 🌟.
For inquiries or collaboration, feel free to reach out via **[LinkedIn](https://www.linkedin.com/in/ahmedmnaouer/) or [Email](ahmedmnaouer101@gmail.com)**.   

---

### **✅ Final Notes**
This README provides a structured overview of the project, detailing the ETL process, data warehouse design, and key insights. By following the steps outlined, users can reproduce the analysis, explore the Power BI dashboard, and gain meaningful inventory insights.
