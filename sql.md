---
title: "SQL Notes"
---

# SQL Cheatsheet & Notes

This page contains my favorite SQL patterns and queries.

## 1. The CASE Statement
Use `CASE` to create custom categories on the fly.

```sql
SELECT 
    employee_id,
    salary,
    CASE 
        WHEN salary > 100000 THEN 'High Earner'
        WHEN salary BETWEEN 50000 AND 100000 THEN 'Mid Earner'
        ELSE 'Entry Level'
    END AS salary_category
FROM employees;
