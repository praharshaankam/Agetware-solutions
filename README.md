# Agetware

Assignment
System Architecture
A classic 3-tier architecture:

Frontend (Presentation Layer):
➤ ReactJS single-page app to interact with users.

Backend (Application Layer):
➤ Node.js with Express.js handles REST APIs, business logic, EMI, payments, ledger, etc.

Database (Data Layer):
➤ PostgreSQL or SQLite to store all data (customers, loans, payments). Structured and reliable.

RESTful API Design
All API endpoints start from /api/v1. The system has four core functions:
Data Model / Database Schema
Tables:
Customers:
customer_id, name, created_at
Loans:
loan_id, customer_id, principal_amount, total_amount, monthly_emi, status, created_at, etc.
Payments:
payment_id, loan_id, amount, payment_type, payment_date

Assumptions & Design Decisions
Simple Interest:
I=P×N×R/100
EMI=(P+I)/(N×12)
Lump sum:
Reduces balance and recalculates EMIs.
Customer Management:
Assumes customer already exists.
Database:
Chose SQL (Postgres/SQLite) for reliability.
Statelessness:
Every API call is independent.

Recommended Stack
Frontend: React.js
Backend: Node.js with Express
Database: PostgreSQL or SQLite
