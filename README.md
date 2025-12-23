MovStrem – Fully Integrated Database System
MovStrem is a fully integrated database‑driven system built with Node.js, Express.js, and MySQL. It demonstrates the complete lifecycle of designing a relational database, implementing a backend API, and validating CRUD operations with real sample data.​

Features
Well‑structured relational database schema with primary keys, foreign keys, constraints, and indexes.​

Node.js + Express.js backend exposing RESTful routes for full CRUD functionality.​

Secure MySQL connectivity using a dedicated connection module and parameterized queries.​

Sample data scripts to populate the database for testing and demonstration.​

Tech Stack
Language: JavaScript (Node.js)​

Backend Framework: Express.js​

Database: MySQL (designed and managed via MySQL Workbench / phpMyAdmin)​

Package Manager: npm​

Project Structure
Typical repository layout:


movstrem/
  server.js          # Main Express server and route definitions
  db.js              # MySQL connection configuration
  final.sql          # Full database schema (tables, keys, constraints)
  sample_data.sql    # Sample INSERT statements for test data
  public/            # Optional static UI assets (HTML, CSS, JS)
  package.json       # Project metadata and npm scripts
  package-lock.json  # Locked dependency versions
  Iteration 1/       # Early iterations / backup materials
  node_modules/      # Installed dependencies (auto-generated)

Getting Started
Prerequisites
Node.js and npm installed

MySQL server running locally or accessible remotely

A MySQL user with permissions to create databases and tables​

Setup Steps
Clone the repository
git clone https://github.com/your-username/movstrem-system.git
cd movstrem-system
Install dependencies


npm install
Configure database connection

Update db.js with your MySQL credentials and database name (host, user, password, database, and pool settings as needed).​

Create schema and load sample data

In MySQL (CLI, Workbench, or phpMyAdmin), run:
SOURCE final.sql;
SOURCE sample_data.sql;
This creates all tables, relationships, and inserts sample records.​

Run the backend server
npm start
By default, the Express server listens on the configured port and exposes API endpoints for CRUD operations.​

API Overview
The backend follows a typical REST style using HTTP methods against resource routes:​

POST – Create new records

GET – Retrieve all or specific records

PUT – Update existing records

DELETE – Remove records

All queries are executed using parameterized statements to help prevent SQL injection and preserve data integrity.​

Database Design
Schema: Defined in final.sql, including table definitions, types, keys, constraints, and indexes.​

Normalization: Tables are structured according to relational database principles to reduce redundancy and maintain consistency.​

Integrity: Primary and foreign keys, NOT NULL, UNIQUE, and other constraints enforce valid relationships and data quality.​

Testing and Validation
The system was tested for:​

Successful schema creation and database connectivity

Correctness of CRUD operations for all main entities

Handling of invalid input and error cases

Performance and reliability of common queries

Maintenance of referential integrity across related tables