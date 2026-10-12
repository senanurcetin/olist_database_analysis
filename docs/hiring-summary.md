# Reviewer brief — Olist E-commerce Database Analysis

**Role:** SQL analytics, relational data modeling and exploratory e-commerce analysis. **Dataset:** publicly released historical Brazilian E-Commerce by Olist (2016–2018), not live retail performance.

## Analytical question

How do orders, customers, sellers and products relate across a multi-table commerce dataset, and which exploratory patterns can be reproduced from the relational schema?

| Reviewer interest | Evidence |
|---|---|
| How is the source represented? | [Schema creation](../create_table.sql), [entity diagram](../olist_entity.svg) |
| How can data be imported? | [psql import script](../import_data.sql) and [setup caveats](../README.md#set-up-the-database) |
| What analyses are present? | [Orders](../Frequency_analysis_of_orders/README.md), [Customers](../Customer_analysis/README.md), [Sellers](../Seller_analysis/README.md), [Products](../Product_analysis/README.md) |
| What is executable? | [Jupyter notebooks](../Customer_analysis/Customer_analysis.ipynb) and the linked analysis folders in the [README](../README.md) |
| Are significance claims interrogated? | [Separate statistical reproduction note](https://www.kaggle.com/code/senanuretin/olist-p-0-is-not-a-finding) |

## Engineering and research boundaries

The project explores historical public records; it does **not** claim a deployed data warehouse, business intervention effects, or current Olist KPIs. Statistical significance should not be confused with practical effect size or causality. Original dataset licensing is separate from the software license.

## Local reproducibility

Use a fresh local Python virtual environment and PostgreSQL instance. The `import_data.sql` script uses `psql` `\\copy` commands, and its CSV file paths require adjustment to your machine. Do **not** commit generated `venv/` or notebook checkpoints.

**Start with:** [Project README](../README.md).
