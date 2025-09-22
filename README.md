# 📦 EDI Orders ETL Project  

## Overview  
This project demonstrates a low-cost, practical solution for small businesses that need to manage **EDI (Electronic Data Interchange) orders** but cannot afford sophisticated ERP systems.  

Many large companies use EDI to send purchase orders. While they often have access to advanced software for handling these transmissions, smaller suppliers usually rely on **simpler tools**. In this case, EDI orders were received and automatically compiled into **Excel files** designed for human readability.  

The issue?  
- These Excel files are full of **merged cells and formatting**, making them hard to parse programmatically.  
- Orders were being tracked **manually** by copying quantities into another spreadsheet.  
- Historic data and KPIs were not reliable or consolidated.  

This project solves that by:  
1. **Receiving messy Excel exports** (with merged cells).  
2. **Converting them into CSV files** for easier handling.  
3. **Running an ETL pipeline in Python** to clean, normalize, and structure the data.  
4. **Producing a clean, tabular output** ready to be imported into a simple Excel database or KPI monitoring system.  

---

## Input Examples  

### 1. Raw Excel File (as downloaded from the EDI system)  
Messy formatting, merged cells, multiple order blocks stacked one after another:  
![Messy Excel] <img width="1118" height="801" alt="Screenshot 2025-09-22 at 19 06 22" src="https://github.com/user-attachments/assets/639a9370-11c6-4850-b74d-5c7024fa1287" />
 

### 2. CSV Conversion  
Readable as plain text, but still not easy to analyze directly:  
![CSV] <img width="1423" height="632" alt="Screenshot 2025-09-22 at 19 09 41" src="https://github.com/user-attachments/assets/48d210f7-6dcd-469d-bbdd-cc736edb06c2" />
 

---

## Output Example  

After running the ETL pipeline, we get a clean, structured dataset:  

![ETL Output] <img width="1483" height="511" alt="Screenshot 2025-09-22 at 19 11 55" src="https://github.com/user-attachments/assets/8b825130-540a-48f1-a051-1634b73b36b2" />



Example of the normalized schema:  

| product_category     | customer           | po         | order_date | ean            | buyer_code | deliver_to                 | delivery_date         | item                              | cases | qty | unit_price | order_value |  
|----------------------|-------------------|------------|------------|----------------|------------|---------------------------|-----------------------|-----------------------------------|-------|-----|------------|-------------|  
| OAKWOOD DINING TABLE | DESIGNER LIVING CO | 0050920111 | 17/08/2023 | 1012223334445 | 012345678  | Designer Living Warehouse 1 | 18/08/2023 00:00:00 | Oakwood FURNITURE ITEMS – THE WOODS | 1     | 2   | 120.00     | 240.00      |  

---

## Features  
- ✅ Extracts structured data from **unstructured Excel order files**  
- ✅ Normalizes orders across multiple EDI exports  
- ✅ Provides **clean CSV/Excel tables** suitable for databases or KPI dashboards  
- ✅ Allows small businesses to **track order history** without costly ERP software  

---

## Tech Stack  
- **Python** (pandas)  
- **Excel/CSV** for input and output  
- **Jupyter Notebook** for ETL pipeline steps  

---

## Use Cases  
- 🏢 Small suppliers receiving EDI orders from large retailers  
- 📊 Businesses that want to maintain reliable sales & KPI dashboards without ERP systems  
- 💡 Anyone dealing with overly formatted Excel reports needing cleanup before analysis  

---

## Next Steps (Future Improvements)  
- 📥 Automate pulling of raw EDI Excel files from email/FTP  
- 🗄️ Add a **database layer** (SQLite/Postgres) for historical queries  
- 📊 Build a **dashboard** in Excel, Power BI, or Tableau for KPI visualization  

---

## Disclaimer  
This project uses **mocked data** for demonstration. No real company names or sensitive data are included.
