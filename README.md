# SQL-Postgresql-Queries

SQL (Structured Query Language) is a standardized programming language used for managing and manipulating relational databases. 

It is essential for interacting with database systems and allows users to perform a variety of operations such as querying data, updating records, and managing database structures. 
 

## Types of Databases

1. 𝗥𝗲𝗹𝗮𝘁𝗶𝗼𝗻𝗮𝗹 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
    * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Organizes data into tables with rows and columns.
    * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: MySQL, PostgreSQL, Oracle, SQL Server.
    * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: ACID compliance, strong data consistency, structured data storage, support for SQL queries, well-suited for complex transactions and reporting.
2. 𝗗𝗼𝗰𝘂𝗺𝗲𝗻𝘁 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
    * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Stores data in semi-structured or JSON-like documents.
    * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: MongoDB, CouchDB, Firebase Firestore.
    * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: Flexible schema, horizontal scalability, support for semi-structured data, well-suited for content management systems and real-time applications.
3. 𝗜𝗻-𝗠𝗲𝗺𝗼𝗿𝘆 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
    * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Stores data entirely in the system's main memory (RAM).
    * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: Redis, Memcached, Apache Ignite.
    * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: Ultra-fast data retrieval, low-latency, suitable for caching, session management, and real-time analytics.
4. 𝗚𝗿𝗮𝗽𝗵 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
   * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Represents data as nodes and edges to model relationships.
   * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: Neo4j, Amazon Neptune, ArangoDB.
   * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: Efficient querying of complex relationships, graph traversal, suitable for social networks, recommendation systems, and fraud detection.
5. 𝗧𝗶𝗺𝗲-𝗦𝗲𝗿𝗶𝗲𝘀 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
   * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Optimized for time-ordered data points, like sensor readings or log files.
   * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: InfluxDB, Prometheus, TimescaleDB.
   * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: Efficient storage and retrieval of time-series data, aggregations, retention policies, ideal for monitoring, IoT, and event data.
6. 𝗦𝗽𝗮𝘁𝗶𝗮𝗹 𝗗𝗮𝘁𝗮𝗯𝗮𝘀𝗲
   * 𝗗𝗮𝘁𝗮 𝗠𝗼𝗱𝗲𝗹: Designed for storing and querying spatial or geographic data.
   * 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀: PostGIS (extension for PostgreSQL), MongoDB Geospatial, Microsoft SQL Server Spatial.
   * 𝗞𝗲𝘆 𝗙𝗲𝗮𝘁𝘂𝗿𝗲𝘀: Geospatial indexing, support for spatial data types (points, polygons, lines), useful for location-based services, GIS (Geographic Information Systems), and map applications.

![Types of databases](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/8dc6d237-fa2a-45be-8e19-9fa108c4cda4)

# Postgres Database

PostgreSQL, often referred to as Postgres is a powerful, open-source relational database management system (RDBMS) known for its robustness, extensibility, and standards compliance. 

It is widely used in both academic and commercial applications due to its advanced features and strong support for complex queries, data integrity, and concurrency. 

**Key Features of PostgreSQL**<br>

* Open Source: PostgreSQL is free to use, modify, and distribute. It is developed by a global community of contributors, ensuring continuous improvement and support.

* Standards Compliance: PostgreSQL adheres to the SQL standard, ensuring compatibility and portability with other SQL-compliant databases.
  
* Advanced Data Types: Supports a wide range of data types, including traditional types `(INTEGER, VARCHAR, DATE)`, `array types`, `JSON`, `XML`, `hstore (key-value pairs)`, and more.

* Complex Queries and Joins: Capable of handling complex queries and multiple joins efficiently, making it suitable for large-scale data analysis and reporting.

* ACID Compliance: Ensures data integrity and reliability through full support for ACID `(Atomicity, Consistency, Isolation, Durability)` properties.
  
* MVCC (Multi-Version Concurrency Control): Provides high concurrency and performance by allowing multiple transactions to access the database concurrently without locking issues.

* Extensibility: Supports custom functions, operators, and data types. Users can write extensions in various languages, such as `PL/pgSQL`, `PL/Python`, `PL/Perl`, and more.

* Full-Text Search: Built-in support for full-text search, allowing efficient text-based searches and indexing.

* Replication and High Availability: Supports various replication methods `(streaming replication, logical replication)` and high availability configurations to ensure data availability and redundancy.

* Security: Offers robust security features, including authentication, authorization, SSL encryption, and row-level security.
  
**Common Use Cases**<br>

* Web Applications: Widely used as the backend database for web applications due to its reliability and scalability.
* Data Warehousing: Suitable for data warehousing and business intelligence applications due to its support for complex queries and large datasets.
* Geospatial Applications: The PostGIS extension enables powerful geospatial data processing and analysis.
* Financial Systems: ACID compliance and strong data integrity features make it suitable for financial and transactional systems.

**Extensions and Ecosystem**<br>

PostgreSQL's extensibility is one of its standout features. Many extensions are available to enhance its capabilities:

* **PostGIS**: Adds support for geographic objects, allowing location queries.
* **pgAdmin**: A popular open-source administration and development platform for PostgreSQL.
* **TimescaleDB**: An extension for time-series data, optimized for fast ingestion and complex queries.
* **Citus**: Transforms PostgreSQL into a distributed database for horizontal scaling.

# MongoDB

## SQL and PostgreSQL cheat sheets

![SQL_P ostgres command](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/26426e07-341c-4499-889f-2c326bccc9ba)


## SQL Database cheat sheets

Image Representations:

![img18](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/d6487aaa-b801-453d-a007-a4c5ca13fc19)

![img19](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/a9ca8461-2cb2-423c-9410-8f9e508eee0b)

![img20](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/b170dacf-8870-4942-9b6a-dee16dc9d7e4)

![img21](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/8d0a27fb-81fd-4ab2-8dfc-14f23d1e9b4e)


## cheat sheets

![sql_page-0001](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/84ceaf67-0d78-47e9-908f-b95a12394745)

![sql_page-0002](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/8fd2d2d9-9261-444b-b175-4c4d97ecae15)

![sql_page-0003](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/1e153457-af48-41fb-9918-2be4639068a9)

![sql_page-0004](https://github.com/kaleeswariP/SQL-Postgresql-Queries/assets/22699303/4cf28bc3-f631-47f3-abaa-da0c533d8fd6)


