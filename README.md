# db100-mysql-exercises

SQL exercises against the Sakila sample database, covering `SELECT`, `DISTINCT`,
`WHERE`, `IN`, `BETWEEN`, `LIKE`, `LIMIT`, `ORDER BY`, and `JOIN`s.

## Setup

1. Install [MySQL Community Edition](https://dev.mysql.com/downloads/mysql/) and
   [MySQL Workbench](https://dev.mysql.com/downloads/workbench/).
2. Load the Sakila sample database:
   ```
   mysql -u <username> -p -e "CREATE DATABASE sakila;"
   mysql -u <username> -p sakila < sql/lib/sakila-schema.sql
   mysql -u <username> -p sakila < sql/lib/sakila-data.sql
   ```
3. Install dependencies:
   ```
   npm install
   ```
4. Add a `config.js` file to the project root with your MySQL credentials:
   ```js
   module.exports = {
     username: 'your_mysql_username',
     password: 'your_mysql_password'
   };
   ```
   This file is gitignored and should never be committed.

## Usage

Write your answers in [sql/exercises.sql](sql/exercises.sql), then run the test suite:

```
npm test
```

All 35 tests pass.
