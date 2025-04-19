# Bigdata-Project
Logistics Shipment Analysis Pipeline with PySpark and HDFS

# ETL pipeline:
•	Extract (RDBMS via Sqoop)
•	Transform (PySpark on HDFS)
•	Load (Transformed data to RDBMS)
•	Followed by visualization in Power BI.


# 🚚 Logistics Shipment Analysis Pipeline – Data Flow

# 1. Data Ingestion
•	Source: RDBMS (e.g., MySQL, PostgreSQL, Oracle)
•	Tool: Sqoop
•	Purpose: Import logistics/shipment data from a relational database into Hadoop Distributed File System (HDFS).

# 2. Storage (HDFS)
•	Storage Medium: Hadoop Distributed File System (HDFS)
•	Purpose: Acts as a data lake to hold large volumes of structured shipment data.
•	Intermediate Step: Raw data is landed and staged here before any processing.

# 3. Transformation
Engine: PySpark (Apache Spark with Python)
Operations:
•	Filter – Remove unwanted records (e.g., incomplete shipments).
•	GroupBy – Group data by region, shipping partner, etc.
•	Join – Merge with other datasets like customer info, delivery logs.
•	Aggregate – Summarize metrics (e.g., total shipments, average delay).
•	Select – Choose specific fields relevant for reporting.

# 4. Serving Layer
Destination: RDBMS (e.g., PostgreSQL, SQL Server)
Purpose: Store the transformed and cleaned dataset in a structured format ready for visualization or business intelligence tools.





# 5. Reporting
Tool: Power BI
Purpose: Create dashboards and reports for logistics KPIs such as:
•	On-time delivery rate
•	Average shipment delay
•	Carrier performance
•	Shipment volume trends
