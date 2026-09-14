# Customer Sign-Up Behaviour & Data Quality Audit

A data cleaning and analysis project built with Python and pandas, auditing a messy
customer sign-up dataset and turning it into clean, business-ready insights.

## What this project does

- Loads a raw customer sign-up dataset (515 records) with realistic data quality
  issues: duplicate records, inconsistent category spelling, missing values, and
  implausible data entries.
- Audits and documents every issue found, with a severity rating and business
  impact for each.
- Cleans the data with clearly justified decisions (e.g. flagging vs. imputing
  vs. dropping missing values, depending on the field).
- Analyzes sign-up trends, acquisition sources, plan selection, and marketing
  opt-in behaviour.
- Joins a second dataset (support tickets) to measure how quickly customers on
  different plans contact support after signing up.

## Tools used

- Python, pandas, matplotlib
- Jupyter Notebook

## Key findings

- **Google is the dominant acquisition channel**, bringing in more sign-ups
  than the next two sources combined.
- **8.2% of records were missing a region** — the largest single data quality
  gap in the dataset.
- **Age has little effect on marketing opt-in rate** (a ~13-point spread across
  age groups, no clear trend).
- **Basic is the most-selected plan overall**, though Pro edges it out in the
  core 26-35 age group.
- **Pro and Premium customers contact support early at nearly double the rate
  of Basic customers** (29.1% and 27.5% vs. 15.8% within 14 days of signing up) —
  a signal that onboarding for higher-tier plans could be improved.

## Files

- `Signup_Audit.ipynb` — full analysis notebook, with markdown explanations
  of every cleaning decision
- `Customer_Signup_Audit_Report00.pdf` — a plain-language summary report for
  non-technical stakeholders
- `Signup_Audit Notebook_Code_Export.pdf` — a PDF export of the notebook's
  code and outputs, for anyone who wants to view it without opening Jupyter

*Note: source data is not included in this repo, as it contains sample
personal information (names, emails).*

## What I learned

This project was my first hands-on introduction to Python and pandas — built
from scratch, cell by cell, including debugging real issues like execution
order in Jupyter, regex validation, and reasoning through cleaning decisions
(e.g. why median imputation over dropping rows, why flagging beats guessing
for categorical data).
