Sales Analysis & Narrative

This project loads sales data into SQL, performs analysis and EDA in Python, creates visualizations, and generates a narrative summary.

1. Run the SQL Analysis

From the repository root, use SQLite:

sqlite3 sales.db


Inside SQLite, run the schema and seed data first:

.read sql/schema.sql
.read sql/seed_data.sql
.read sql/reports.sql
.quit


This creates the database tables, loads the data, and runs the SQL reports used for the analysis.

2. Run Python Analysis

Install the required Python packages if needed, then run:

python analysis/clean_and_eda.py
python analysis/visualize.py


clean_and_eda.py cleans the CSV data and performs the exploratory analysis. visualize.py generates the charts in visualizations/.

Task 5 — Findings

As part of Part 2, Task 5, the analysis writes the findings used by the narrative step to:

narrator/findings.json


Run the analysis before generating the narrative so this file contains the latest results.

3. Generate the Narrative
With a Gemini API Key

Set your Gemini API key as an environment variable.

macOS/Linux:

export GEMINI_API_KEY="your_api_key_here"
python narrator/generate_narrative.py


Windows PowerShell:

$env:GEMINI_API_KEY="your_api_key_here"
python narrator/generate_narrative.py

Offline Mode — No API Key

To run without a Gemini API key:

python narrator/generate_narrative.py


The script uses the available narrator/findings.json data to produce the offline narrative.

Follow the steps above in order to reproduce the SQL results, analysis, visualizations, findings, and narrative.
