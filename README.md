## Introduction

Dive into the data job market! Focusing on data analyst roles, this project explorestop-paying jobs, in-demand skills, and where high demand meets high salary in data analytics.

- SQL queries? Check them out here: [project_sql folder](/project_sql/)

# Background
Driven by a quest to navigate the data anayst job market more effectively, tis project was born form a desire to pinpoint top-paid and in-demand skills, streamlining others work to optimal jobs.

## The questions I wanted to answer through my queries were:
1. What are the top-paying data analyst jobs?
2. What skills are required for these top-paying jobs?
3. What skills are most in demand for Data Analysts?
4. Which skills are associated with higher salaries?
5. What are the most optimal skills to learn?

# Tools I Used
For my deep dive into the data analyst job market, I harnessed the power of several key tools:

- **SQL**: The background of my analysis, allowing me to query the database and unearth critical insights.
- **PostgresSQL**: The chosen database management system, ideal for handling the job postings data.
- **Visual Studio Code**: My go-to for database managemnt and handling SQL queries.
- **Git and Github**: Essential for version control and sharing my SQL Scripts and analysis, ensuring collaboration and project tracking.
# The Analysis
Each query for this project aimed at investigating specific aspects of the data analysis job market. Here is how I approached the question: 
### 1. Top Paying Data Analyst Jobs
To identify the highest paying roles, I filtered data analyst positions by average yearly salary and location. This query highlights the high paying opportunities in the field.

```sql
    SELECT
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name AS company_name
FROM
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' AND
    job_location = 'Anywhere' AND
    salary_year_avg IS NOT NULL
ORDER BY
    salary_year_avg DESC
LIMIT 10;
```
Here is the breakdown:
- **Wide Salary Range:** The top paying data analyst roles span from $184000 to $650000 indicatingsignificant salary potential.
- **Diverse Employers:** Companies like SmartAsset, Meta, and AT&T are among those offering high salaries, showing a broad interest across different industries.
- **Job Title Variety:** There is a high diversit of job Titles, from Data Analyst to Director of Analytics, reflecting varied roles and specialisations with data analytics.
#  What I Learned
# Conclusions

