# Groundwater Level Detection System

This project involves using data from the Central Ground Water Board (CGWB) dataset to detect groundwater levels in different areas of Maharashtra, India. The data is stored in an Oracle database and includes information about wells, districts, tahsils, and water levels.

## Project Structure

The project is organized as follows:
1. **Tables**:
   - `states`: Contains information about different states in India.
   - `districts`: Contains information about districts within the states.
   - `tahsils`: Contains information about tahsils (sub-districts).
   - `blocks`: Contains information about blocks (smaller administrative units).
   - `wells`: Contains information about wells, including their locations, types, and depth.
   - `water_levels`: Contains data about water levels in different wells at various times.

2. **PL/SQL Procedures**:
   - A procedure to retrieve the groundwater depth at a specific site, based on the site name provided.

3. **SQL Queries**:
   - Various SQL queries to fetch data, including the `SELECT * FROM` commands for each table to view their content.

## Features

- **Insert Data**: The project allows inserting well data and water levels into the database.
- **Data Retrieval**: Using SQL queries, users can retrieve data about the groundwater levels and well depths.
- **PL/SQL Procedure**: A custom procedure retrieves the water depth when the site name (e.g., `Sangamner`) is entered.

## Setup

To set up this project, follow these steps:

1. **Prerequisites**:
   - Oracle Database 12c or later
   - PL/SQL Developer or any database client to interact with Oracle

2. **Database Setup**:
   - Create the tables using the provided SQL scripts.
   - Insert sample data into the `wells` and `water_levels` tables.

3. **PL/SQL Procedure**:
   - Use the provided PL/SQL procedure to query the water depth at a given site.

## Example Usage

### Insert Data:
To insert data into the `wells` table, use the following SQL:

```sql
INSERT INTO wells (site_id, latitude, longitude, site_type, site_name, aquifer_type, depth)
VALUES ('W192100074103001', '19°21''0" N', '74°10''30" E', 'Dug Well', 'Ambikhalsa', 'Unconfined', 17);
