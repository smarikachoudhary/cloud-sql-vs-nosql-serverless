# cloud-sql-vs-nosql-serverless
Draw.io architecture diagram comparing SQL (RDS + EC2) vs NoSQL (DynamoDB + Lambda)
# Cloud Database Paradigms (SQL vs NoSQL) & Serverless Architecture (FaaS)

Weekly assignment: Draw.io architecture diagram comparing two backend stacks handling the same user traffic.

## Stack A: Managed Relational Infrastructure
- Load Balancer -> EC2 virtual machine (stateful, always-on) -> RDS SQL (PostgreSQL/MySQL)
- Persistent open connection (LB to EC2) and persistent connection pool (EC2 to RDS)
- Data model: structured, schema-based tables

## Stack B: Serverless Non-Relational Infrastructure
- API Gateway -> AWS Lambda (stateless, ephemeral) -> DynamoDB / MongoDB Atlas
- Event-driven trigger (API Gateway invokes Lambda on-demand) and stateless HTTPS API calls to the database
- Data model: schemaless documents / key-value pairs

## Diagram
![Architecture Diagram](sql_vs_nosql_serverless.png)

Source file: `sql_vs_nosql_serverless.drawio` (open with app.diagrams.net)
