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

