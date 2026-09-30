# Sales Analysis & Narrative

This project loads sales data into SQL, performs analysis and EDA in Python, creates visualizations, and generates a narrative summary.

## 1. Run the SQL Analysis

From the repository root, create/open the SQLite database:

```bash
sqlite3 sales.db


.read sql/schema.sql
.read sql/seed_data.sql
.read sql/reports.sql
.quit
