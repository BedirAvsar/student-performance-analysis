# Student Performance Analysis (SQL Project)

## Overview
This project analyzes student academic performance using SQL. 
The goal is to explore how factors such as study time, absences,
and extracurricular activities correlate with GPA.

## Dataset
Source: Public educational dataset  
Rows: ~1000 students  
Attributes include academic, demographic, and behavioral features.

## Technologies
- SQLite
- SQL (aggregation, grouping, filtering)
- Data modeling and analysis

## Key Questions Explored
- How does study time affect GPA?
- Is there a correlation between absences and performance?
- Do extracurricular activities influence academic success?

## Project Structure
- `data/raw`: Original dataset
- `data/processed`: Cleaned and structured data
- `sql/`: SQL scripts for schema creation and analysis

## How to Run
```bash
sqlite3 data/student_performance.db
.read sql/create_tables.sql
.read sql/analysis_queries.sql