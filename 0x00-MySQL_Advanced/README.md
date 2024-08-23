# 0x00. MySQL Advanced

## Overview
This project focuses on advanced MySQL concepts, covering a range of topics including creating tables with constraints, optimizing queries, and implementing stored procedures, functions, views, and triggers in MySQL. These skills are crucial for database management and optimization in complex applications.

## Concepts Covered
- **Advanced SQL**
- **MySQL Performance Optimization**
- **Stored Procedures and Functions**
- **Triggers**
- **Views**

## Resources
To excel in this project, you may find the following resources helpful:
- [MySQL cheatsheet](https://dev.mysql.com/doc/refman/5.7/en/cheat-sheet.html)
- [MySQL Performance: How To Leverage MySQL Database Indexing](https://dev.mysql.com/doc/refman/5.7/en/mysql-indexes.html)
- [Stored Procedures and Functions](https://dev.mysql.com/doc/refman/5.7/en/create-procedure.html)
- [Triggers in MySQL](https://dev.mysql.com/doc/refman/5.7/en/triggers.html)
- [Views in MySQL](https://dev.mysql.com/doc/refman/5.7/en/create-view.html)

## Learning Objectives
By the end of this project, you should be able to:
- Create tables with constraints in MySQL.
- Optimize queries by adding indexes.
- Implement stored procedures and functions.
- Implement views and triggers.

## Requirements
- All files are executed on Ubuntu 18.04 LTS using MySQL 5.7 (version 5.7.30).
- SQL queries must have a comment describing the task.
- SQL keywords should be in uppercase (e.g., `SELECT`, `WHERE`).
- A `README.md` file at the root of the project directory is mandatory.

## Setup Instructions

### Using Container on Demand
1. Request an Ubuntu 18.04 container with Python 3.7.
2. Start MySQL:
   ```bash
   service mysql start
   ```
3. Connect to MySQL using the root user:
   ```bash
   mysql -uroot -p
   ```

### Importing a SQL Dump
```bash
echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
```

## Project Tasks

### 0. We are all unique!
**File:** `0-uniq_users.sql`

Create a `users` table with the following constraints:
- `id`: integer, not null, auto increment, primary key
- `email`: string (255 characters), not null, unique
- `name`: string (255 characters)

### 1. In and not out
**File:** `1-country_users.sql`

Create a `users` table with an additional `country` attribute:
- `country`: enumeration of countries (US, CO, TN), default is US

### 2. Best band ever!
**File:** `2-fans.sql`

Rank the country origins of bands by the number of non-unique fans. 

### 3. Old school band
**File:** `3-glam_rock.sql`

List all bands with Glam rock as their main style, ranked by longevity.

### 4. Buy buy buy
**File:** `4-store.sql`

Create a trigger that decreases the quantity of an item after a new order is added.

## Repository Structure
- **GitHub Repository:** `alx-backend-storage`
- **Directory:** `0x00-MySQL_Advanced`
- **Files:** 
  - `0-uniq_users.sql`
  - `1-country_users.sql`
  - `2-fans.sql`
  - `3-glam_rock.sql`
  - `4-store.sql`

## License
This project is licensed under the MIT License - see the LICENSE file for details.
