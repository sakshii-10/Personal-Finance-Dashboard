# 📊 Personal Finance Dashboard — Power BI

This repository contains a complete **Personal Finance Dashboard** built using **Excel + Power BI**.  
It tracks income, savings, and expenses across multiple months/years and helps visualize spending patterns and savings performance.

---

## 🔧 Tools & Technologies

- **Power BI Desktop**
- **Microsoft Excel**
- **Power Query**
- **DAX (Data Analysis Expressions)**

---

## 📁 Project Files

| File                         | Description                                                     |
|------------------------------|-----------------------------------------------------------------|
| `Finance Dashboard.pbix`     | Main Power BI report / dashboard file                          |
| `Finance Database.xlsx`      | Source data file used to feed the Power BI model               |
| `README.md`                  | Project documentation (this file)                              |

---

## 🛠 Data Preparation Steps

The Excel file was cleaned and transformed before and/or inside Power BI:

1. **Fixed Month–Year Headers**
   - Converted headers like `Jan-18`, `Feb-18`… from text into real date values.
   - Ensured years (2018, 2019, 2020, 2021, etc.) are correctly recognized in Power BI.

2. **Unpivoted Data**
   - Original sheet was in a wide format (one column per month).
   - Using **Power Query**, the data was unpivoted into a long format with:
     - `Type`
     - `Component`
     - `Date`
     - `Value` (amount)

3. **Data Types & Formatting**
   - Set proper data types: `Date` for dates, `Text` for categories, `Decimal/Whole Number` for values.
   - Checked for missing / inconsistent values and corrected them where required.

---

## ## 📈 Dashboard Features

The Power BI report includes the following:

### ⭐ KPI Cards
- **Total Income**
- **Total Savings**
- **Total Expenses**
- **Savings %** and **Expense %**

### 📊 Visuals
- **Bar Chart:** Total Expense by Component  
- **Trend Line:** Income / Savings / Expense over time  
- **Category Breakdown:** Spending classifications by type and component  

### 🎛 Interactivity
- **Slicers** for:
  - Date / Year  
  - Type (Income, Savings, Expense)  
  - Component (Rent, Groceries & Food, Salary, Mutual Funds, etc.)  
- Dynamic filtering of visuals based on selected components and time period.

---

## 🚀 How to Open & Use This Project

### 1️⃣ Download the files
- `Finance Dashboard.pbix`
- `Finance Database.xlsx`

### 2️⃣ Open the Power BI report
- Double-click **Finance Dashboard.pbix** to open in **Power BI Desktop**.

### 3️⃣ Update the data source path (if needed)
If Power BI cannot locate your Excel file:
1. Go to **Home → Transform data → Data source settings**
2. Select the Excel file source  
3. Click **Change Source**
4. Choose the correct location of `Finance Database.xlsx`
5. Click **OK → Close → Apply**

### 4️⃣ Refresh the report
- Click **Refresh** under the **Home** tab to load the latest data from Excel.

### 5️⃣ Explore the dashboard
- Use slicers to filter by **Year**, **Type**, or **Component**  
- Hover over charts to see detailed tooltips  
- Examine trends to understand:
  - Which components contribute most to expenses  
  - How savings change month-over-month  
  - Major spending patterns  

---

## 🎯 Learnings & Skills Demonstrated

- **Excel Data Cleaning**  
  - Managed raw personal finance data  
  - Fixed Month–Year headers  
  - Corrected date structures and formatting  

- **Power Query (ETL skills)**  
  - Converted text dates to real dates  
  - Unpivoted wide-format data into long-format  
  - Created a clean tabular structure for analysis  

- **Power BI Data Modeling**  
  - Built a star-schema–friendly structure  
  - Created a dedicated **Key Measures** table  
  - Set correct data types and relationships  

- **DAX Measures**  
  - Created KPIs: Total Income, Total Savings, Total Expense  
  - Calculated Savings % and Expense %  
  - Implemented dynamic filtering logic  

- **Dashboard Design & Data Storytelling**  
  - Built interactive visuals  
  - Added intuitive slicers  
  - Created meaningful financial insights  

---



Expense % =
DIVIDE ( [Total Expense], [Total Income] )
