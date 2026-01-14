# Student Performance Analysis

A structured SQL-based analysis exploring how different factors — such as study time, parental education, and preparation courses — affect student performance.  
This project focuses on data modeling, analytical queries, and extracting meaningful insights from real-world-like data.

---

## 📊 Key Objectives

- Understand which factors influence academic outcomes  
- Explore correlations between habits and exam scores  
- Practice SQL joins, grouping, aggregations, and filtering  
- Build a clean and reusable analysis workflow  

---

## 📁 Dataset

The dataset includes the following fields:

```
students(
    id INTEGER PRIMARY KEY,
    gender TEXT,
    parental_education TEXT,
    study_time INTEGER,
    test_preparation TEXT,
    math_score INTEGER,
    reading_score INTEGER,
    writing_score INTEGER
)
```

Dataset preview:  
![dataset](images/dataset-preview.png)

---

## 🧠 Key Questions

### 1️⃣ Does study time correlate with exam scores?
```sql
SELECT study_time, AVG(math_score) AS avg_math
FROM students
GROUP BY study_time;
```

### 2️⃣ Do test preparation courses improve results?
```sql
SELECT test_preparation,
       AVG(math_score) AS math_avg,
       AVG(reading_score) AS reading_avg,
       AVG(writing_score) AS writing_avg
FROM students
GROUP BY test_preparation;
```

### 3️⃣ Does parental education affect performance?
```sql
SELECT parental_education,
       AVG(math_score) AS avg_math
FROM students
GROUP BY parental_education
ORDER BY avg_math DESC;
```

---

## 📌 Insights & Findings

### 🔹 Study Time
Students who studied **2 hours or more** scored significantly higher in math compared to those who studied less.

### 🔹 Test Preparation Courses
Students who completed preparation courses scored on average **12–15% higher** across all subjects.

### 🔹 Parental Education
Higher parental education levels correlated with above-average math and reading performance.

### 🔹 Math vs Reading
Math scores showed a stronger correlation with study time than reading/writing scores.

---

## 🛠 SQL Skills Practiced

- JOIN operations  
- Aggregation functions (AVG, COUNT, SUM)  
- Grouping & filtering  
- Subqueries  
- Data exploration process  
- Translating business questions into SQL queries  

---

## 🚀 Project Structure

```
student-performance-analysis/
├── data/            # Dataset files
├── images/          # Preview visuals
├── sql/             # Query scripts
└── README.md        # Documentation
```

---

## 📌 What I Learned

- How to structure a small SQL-based analytics project  
- Designing a simple but clean database schema  
- Deriving insights from real-world-like tabular data  
- Writing readable and reusable SQL queries  
- Connecting questions → queries → insights  

---

## ✔️ Conclusion

This project improved my ability to analyze datasets using SQL and translate real-world questions into structured queries. It also strengthened my understanding of correlations, grouping logic, and data modeling.

---
