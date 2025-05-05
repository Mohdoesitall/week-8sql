# Project Title
Library Management & Task Manager CRUD API

## Description
This repository contains two deliverables:

1. **Library Management Database** (`library.sql`)  
   A fully-featured MySQL schema for a library:  
   - `Authors`, `Books`, `Members`, `Loans`  
   - Proper PK, FK, UNIQUE, NOT NULL constraints  
   - Sample data inserts

2. **Task Manager CRUD API** (`task-api/`)  
   A FastAPI service backed by MySQL to create, read, update, and delete tasks.  
   - `main.py` with FastAPI endpoints  
   - SQL initialization script for the `tasks` table  
   - `requirements.txt` for Python dependencies

## Getting Started

### Prerequisites
- MySQL Server (≥5.7)
- Python 3.8+  
- (Optional) virtualenv or conda

### Setup & Run

#### 1. Library Database
```bash
# Create or select your database
mysql -u <user> -p -e "CREATE DATABASE librarydb;"
# Import schema + data
mysql -u <user> -p librarydb < library.sql





# 1) Create MySQL database
mysql -u <user> -p -e "CREATE DATABASE taskdb;"

# 2) Import schema
mysql -u <user> -p taskdb < task-api/database_init.sql

# 3) Install dependencies
cd task-api
pip install -r requirements.txt

# 4) Run the API
uvicorn main:app --reload
