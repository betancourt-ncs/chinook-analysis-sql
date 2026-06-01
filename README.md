# Chinook Database Analysis

A SQL and Python analysis of the [Chinook database](https://github.com/lerocha/chinook-database), a sample SQLite dataset representing a digital music store. This project explores sales data to answer key business questions using SQL queries, Pandas DataFrames, and Matplotlib visualizations.

---

## Technologies Used

- Python 3
- SQLite3
- Pandas
- Matplotlib
- Jupyter Notebook

---

## Project Structure

```
chinook-analysis/
├── chinook_analysis.ipynb   # Main analysis notebook
├── Chinook_Sqlite.sqlite    # Source database
└── README.md
```

---

## Business Questions

| # | Question | SQL Concepts Used |
|---|----------|-------------------|
| 1 | Which are the 10 best-selling tracks? | JOIN, GROUP BY, SUM, ORDER BY, LIMIT |
| 2 | Which country generates the most revenue? | GROUP BY, SUM, alias |
| 3 | Who is the top-performing sales employee? | Multi-table JOIN, GROUP BY, SUM |
| 4 | Which artists have more than 10 tracks in the store? | JOIN, GROUP BY, COUNT, HAVING |
| 5 | Which tracks have never been sold? | LEFT JOIN, NULL filtering |

---

## Visualizations

Results from the business questions are loaded into Pandas DataFrames and visualized with Matplotlib.

- **Bar chart** — Top 10 best-selling tracks
- **Pie chart** — Revenue breakdown by country
- **Horizontal bar chart** — Sales performance by employee
- **Horizontal bar chart** — Top 10 artists by track count

---

## Setup

1. Clone the repository
   ```bash
   git clone https://github.com/betancourt-ncs/chinook-analysis-sql.git
   cd chinook-analysis-sql
   ```

2. Create and activate a virtual environment
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies
   ```bash
   pip install pandas matplotlib jupyter
   ```

4. Launch Jupyter Notebook
   ```bash
   jupyter notebook
   ```

5. Open `chinook_analysis.ipynb` and run all cells

---

## Key Takeaways

**What does JOIN do?**
JOIN connects two tables that share a column or key in common, allowing data to be fetched from both simultaneously. By default, it returns only rows where a match exists in both tables — the intersection of their data.

**When would I use SQL vs Pandas?**
SQL is the better choice when retrieving data with precision — filtering, grouping, and joining at the database level before it reaches Python. Pandas is better suited for loading that retrieved data into a structured format (dataframes) for further analysis, transformation, and visualization.

For more info visit https://roadmap.sh/projects/querying-sql-python.
