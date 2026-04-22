This project implements a SQL Server transactional replication architecture to enable real-time data synchronization between OLTP and reporting systems. It separates transactional workloads from analytics, improving performance, scalability, and reporting efficiency.

Problem Statement
Traditional single-database systems face performance issues when heavy reporting queries run alongside transactional workloads. This project addresses that by separating OLTP and reporting environments.

Solution
Implemented SQL Server Transactional Replication using Publisher–Distributor–Subscriber model to ensure near real-time data movement from operational database to reporting database.

System Architecture
The solution is built on a SQL Server Transactional Replication architecture following a Publisher–Distributor–Subscriber model.
•	RetailCoreDB (Publisher): Primary OLTP database where all transactional operations occur. 
•	RetailDistDB (Distributor): Central replication database responsible for storing replication metadata, transaction history, and agent coordination. 
•	RetailReportingDB (Subscriber): Read-only reporting database used for analytics, dashboards, and reporting workloads. 

Data Flow: 
1.	RetailCoreDB → 2. Transaction Log → 3. RetailDistDB → 4. RetailReportingDB
