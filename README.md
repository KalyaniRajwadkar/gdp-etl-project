# gdp-etl-project
Python ETL project to extract, transform and load world GDP data.
# 🌍 GDP ETL Pipeline

<p align="center">

## 📊 World GDP Data Engineering Project

**Extract • Transform • Load • Store • Query**

A Python-based ETL pipeline for extracting real-world GDP data, transforming it from USD Million to USD Billion, and storing the processed data in JSON and SQLite database formats.

</p>

---

## 🚀 Project Overview

This project demonstrates a complete **ETL (Extract, Transform, Load) pipeline** using Python and real-world GDP data.

The project extracts country-wise nominal GDP information from an archived Wikipedia source, cleans and transforms the data, converts GDP values from **USD Million to USD Billion**, and stores the processed information in both **JSON** and **SQLite database** formats.

The project also performs SQL queries to identify countries with GDP greater than **100 billion USD**.

---

## 🎯 Project Objectives

- Extract real-world GDP data from a web source
- Clean and process the extracted dataset
- Convert GDP values from USD Million to USD Billion
- Round GDP values to 2 decimal places
- Store processed data in JSON format
- Store processed data in a SQLite database
- Create and query a database table
- Maintain an ETL process log
- Demonstrate a complete Python-based ETL workflow

-----------

## 🔄 ETL Workflow

```text

 🌐 GDP DATA SOURCE
                        │
                        ▼
                   📥 EXTRACT
                        │
                        ▼
                 🧹 DATA CLEANING
                        │
                        ▼
                  🔄 TRANSFORM
             USD Million → USD Billion
                        │
                        ▼
                    📦 LOAD
                ┌───────┴───────┐
                ▼               ▼
             📄 JSON          🗄️ SQLite
                │               │
                └───────┬───────┘
                        ▼
                   🔎 SQL QUERY
                        │
                        ▼
                  📊 GDP ANALYSIS

## ⭐ Key Features

- ✅ Real-world web data extraction
- ✅ Data cleaning and transformation
- ✅ USD Million → USD Billion conversion
- ✅ GDP values rounded to 2 decimal places
- ✅ JSON data generation
- ✅ SQLite database creation
- ✅ `Countries_by_GDP` database table
- ✅ SQL querying
- ✅ ETL process logging
- ✅ Successful execution in Skills Network Labs

---

# 📂 Project Structure

    GDP-ETL-Project/
    │
    ├── etl_project_gdp.py
    ├── Countries_by_GDP.json
    ├── World_Economies.db
    ├── etl_project_log.txt
    ├── requirements.txt
    ├── README.md
    │
    └── screenshots/
        ├── 01_gdp_project_code.png
        ├── 02_gdp_output.png
        ├── 03_gdp_sql_query.png
        └── 04_gdp_project_completion.png

---

# 📥 1. EXTRACT

GDP information was extracted from an archived Wikipedia page containing country-wise **GDP (nominal)** data.

The extraction process collects:

- Country name
- GDP value

The data is extracted and processed using Python libraries such as **Requests** and **BeautifulSoup**.

---

# 🔄 2. TRANSFORM

The original GDP values are provided in **USD Million**.

The ETL pipeline converts these values into **USD Billion** and rounds them to **2 decimal places**.

### Conversion

    USD Million ÷ 1000 = USD Billion

### Example

    26,854,599 Million USD
              ↓
    26,854.599 Billion USD
              ↓
    26,854.60 Billion USD

---

# 📦 3. LOAD

The transformed dataset is loaded into two formats.

### 📄 JSON File

    Countries_by_GDP.json

### 🗄️ SQLite Database

    World_Economies.db

The database contains the following table:

    Countries_by_GDP

### Database Columns

| Column | Description |
|---|---|
| `Country` | Country name |
| `GDP_USD_billion` | GDP in billion USD |

---

# 🔎 4. SQL QUERY

The project uses SQL to identify countries with GDP greater than **100 billion USD**.

    SELECT *
    FROM Countries_by_GDP
    WHERE GDP_USD_billion > 100;

The query successfully returned **69 countries**.

---

# 📊 Sample Results

| Country | GDP (USD Billion) |
|---|---:|
| 🇺🇸 United States | 26,854.60 |
| 🇨🇳 China | 19,373.59 |
| 🇯🇵 Japan | 4,409.74 |
| 🇩🇪 Germany | 4,308.85 |
| 🇮🇳 India | 3,736.88 |
| 🇰🇪 Kenya | 118.13 |
| 🇦🇴 Angola | 117.88 |
| 🇴🇲 Oman | 104.90 |
| 🇬🇹 Guatemala | 102.31 |
| 🇧🇬 Bulgaria | 100.64 |

---

# 📸 PROJECT SCREENSHOTS

The following screenshots are included in the `screenshots` folder and displayed below.

---

## 💻 Screenshot 1 — Python ETL Code

<img width="635" height="685" alt="01_gdp_project_code" src="https://github.com/user-attachments/assets/aca2cf4d-5d5c-4d73-a9dd-c3713ee06ddc" />


    screenshots/01_gdp_project_code.png

This screenshot shows the Python ETL implementation used for the GDP project.

<p align="center">
<img src="screenshots/01_gdp_project_code.png" width="900">
</p>

---

## 📊 Screenshot 2 — Successful GDP Output

<img width="1200" height="720" alt="02_gdp_output" src="https://github.com/user-attachments/assets/87df4e2e-dc1f-4dc0-a168-1a911a754ee4" />

    screenshots/02_gdp_output.png

This screenshot shows the successful execution output containing the processed GDP dataset.

<p align="center">
<img src="screenshots/02_gdp_output.png" width="900">
</p>

---

## 🗄️ Screenshot 3 — SQL Query

<img width="1095" height="430" alt="03_gdp_sql_query" src="https://github.com/user-attachments/assets/08e1849b-02ca-4b5f-8d7d-ea2b7a12d34b" />

    screenshots/03_gdp_sql_query.png

This screenshot shows the SQL/database query used to analyze the GDP data.

<p align="center">
<img src="screenshots/03_gdp_sql_query.png" width="900">
</p>

---

## ✅ Screenshot 4 — Project Execution

<img width="1410" height="580" alt="04_gdp_project_completion" src="https://github.com/user-attachments/assets/c20e29d8-deb9-4100-91a7-443341a0a3ad" />

    screenshots/04_gdp_project_completion.png

This screenshot shows the successful execution of the ETL project in the Skills Network Lab environment.

<p align="center">
<img src="screenshots/04_gdp_project_completion.png" width="900">
</p>

---

# 📝 ETL Logging

The project maintains an ETL process log:

    etl_project_log.txt

The log records important stages of the pipeline, including:

    ETL process started
    Data extraction completed
    Data transformation completed
    Data loaded into JSON
    Database connection initiated
    Data loaded into database
    SQL query executed
    ETL process completed

This provides a record of the ETL execution and helps monitor the pipeline.

---

# 🗃️ Database Information

### Database

    World_Economies.db

### Table

    Countries_by_GDP

### SQL Query

    SELECT *
    FROM Countries_by_GDP
    WHERE GDP_USD_billion > 100;

---

# 📄 Output Files

### `etl_project_gdp.py`

Main Python program containing the complete ETL pipeline.

### `Countries_by_GDP.json`

Contains the transformed GDP data in JSON format.

### `World_Economies.db`

SQLite database containing the processed GDP data.

### `etl_project_log.txt`

Contains log entries showing the progress and execution of the ETL process.

### `requirements.txt`

Contains the Python dependencies required for the project.

---

# 📚 Data Source

The GDP data was obtained from the archived Wikipedia page:

**List of Countries by GDP (Nominal)**

https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29

---

# 🎓 Skills Demonstrated

This project demonstrates practical knowledge of:

- 🐍 Python Programming
- 🔄 ETL Pipelines
- 🌐 Web Data Extraction
- 🧹 Data Cleaning
- 📊 Data Transformation
- 📄 JSON Data Handling
- 🗄️ SQLite Database Management
- 🔍 SQL Queries
- 📝 ETL Logging
- 📁 File Management
- 💻 Skills Network Labs

---

# 💡 Learning Outcomes

Through this project, I gained hands-on experience in building an ETL pipeline from start to finish.

I learned how to extract information from a real-world web source, clean and transform the data using Python, store the processed data in JSON and SQLite formats, and perform SQL queries for further analysis.

The project strengthened my understanding of practical **Data Engineering workflows** and working with real-world datasets.

---

# 🏆 Project Highlights

    🌐 Real-world Data
           ↓
    📥 Extraction
           ↓
    🧹 Cleaning
           ↓
    🔄 Transformation
           ↓
    📄 JSON + 🗄️ SQLite
           ↓
    🔎 SQL Analysis
           ↓
    📊 Final Results

---

# 👩‍💻 Author

## Kalyani Rajwadkar

**Data Engineering | Python | SQL | ETL | Data Analytics**

---

# ⭐ Conclusion

This GDP ETL project demonstrates how real-world data can be extracted, transformed, stored, and queried using Python.

The complete workflow covers **Extraction, Transformation, Loading, Database Management, SQL Querying, and Logging**, providing practical experience with fundamental Data Engineering concepts.

---

<p align="center">

### ⭐ Thanks for visiting this project!

**Built with Python 🐍 | SQL 🗄️ | ETL 🔄 | Data Engineering 📊**

</p>
