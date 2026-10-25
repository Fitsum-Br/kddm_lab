# KDDM Assignment 1: Olist E-Commerce Data Warehouse & ERD Analysis

This repository contains the database setup, relational data modeling, data quality profiling, and analytical SQL queries for **Assignment 1** in **Knowledge Discovery in Databases and Data Mining (KDDM)**.

---

## 🛠 Project Architecture & Setup

The project uses a lightweight, modern data engineering stack for local persistence and analysis:

* **Database Engine**: DuckDB (Persistent storage located at `data/warehouse/kddm.duckdb`)
* **Environment**: Python 3.12+, Jupyter Notebooks, `uv` package manager
* **Data Sources**: Olist Brazilian E-Commerce public dataset (`data/raw/*.csv`)

### Repository Structure & Deliverables

```text
kddm_lab/
├── 01_explore_source_data.ipynb  # Primary Jupyter notebook containing SQL queries & data profiling
├── ERD2.md                       # The Main ERD file that is Text-based Mermaid ERD source file (Markdown format)
├── olist_erd.drawio.png          # High-resolution graphical schema export generated via Draw.io
├── SHORT_NOTE.md                 # Theoretical & business logic responses for Assignment 1
├── README.md                     # Comprehensive project documentation & architectural overview
├── data/
│   ├── raw/                      # Raw Olist CSV files
│   └── warehouse/                # Local DuckDB database file
└── pyproject.toml                # Project environment configuration & dependency definitions