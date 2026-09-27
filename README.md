# SkillDemand360


### Job Posting Skill Demand Analytics using Databricks & Snowflake

SkillDemand360 is a data engineering and analytics project that analyzes job postings to identify technology skill demand, monthly trends, quarter-on-quarter growth, and skills that frequently appear together in the same job posting.

The project uses **Databricks** for data generation, cleaning, transformation, and analytical processing, and **Snowflake** for storing and querying the processed data.

---

## 📌 Problem Statement

A training company wants to decide which technical skills should be included or emphasized in its future training curriculum.

To support this decision, job posting data is analyzed to answer questions such as:

1. What are the top 10 skills by job posting count for each month?
2. Which skills are growing fastest quarter over quarter?
3. Which skills frequently appear together in the same job posting?

The dataset intentionally contains duplicate records, missing skills, invalid dates, unknown companies, inconsistent separators, and inconsistent formatting to simulate real-world data quality problems.

---

## 🎯 Objectives

- Generate a realistic synthetic job posting dataset.
- Store raw data in a Bronze layer.
- Clean and validate the data in the Silver layer.
- Normalize and explode job skills into individual skill records.
- Create Gold analytical datasets.
- Analyze monthly skill demand.
- Identify quarter-on-quarter skill growth.
- Analyze relationships between skills appearing on the same posting.
- Load analytical data into Snowflake for SQL-based analysis.

---

## 🏗️ Architecture

```text
                    Raw Job Posting CSV
                            |
                            v
                    +---------------+
                    |   Databricks  |
                    +---------------+
                            |
                            v
                     Bronze Layer
                    Raw Delta Data
                            |
                            v
                     Silver Layer
                Cleaning + Validation
                            |
                            v
                      Gold Layer
                  Analytical Tables
                            |
                            v
                    +---------------+
                    |   Snowflake   |
                    +---------------+
                            |
                            v
                    SQL Analytics
