# SQL-Postgresql-Queries

SQL (Structured Query Language) is a standardized programming language used for managing and manipulating relational databases. 

It is essential for interacting with database systems and allows users to perform a variety of operations such as querying data, updating records, and managing database structures. 
 
* [Types of databases]()
  
* [PostgresQL]()
   * [Indexing]()
   * [Transaction]()
   * [Schemas]()
   * [Views]()
   * [Sequences]()
   * [Functions]()
  
* [MongoDB]()

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

## Core Topics

### Indexing
PostgreSQL supports various types of indexes to improve the performance of database operations by reducing the amount of data that needs to be scanned. 

##### B-Tree Index
Usage: Default index type in PostgreSQL. Suitable for most general-purpose indexing.

Characteristics: Efficient for equality and range queries.

Example:
```sql
CREATE INDEX index_name ON table_name (column_name);
```

##### Hash Index

Usage: Useful for simple equality comparisons.

Characteristics: Not commonly used due to some limitations, such as not being WAL-logged before PostgreSQL 10, making it less crash-safe.

Example:
```sql
CREATE INDEX index_name ON table_name USING HASH (column_name);
```
##### GiST (Generalized Search Tree) Index
   
Usage: Suitable for complex data types, including geometric data types, full-text search, and more.

Characteristics: Flexible indexing structure allowing various types of queries.

Example:
```sql
CREATE INDEX index_name ON table_name USING GIST (column_name);
```

##### SP-GiST (Space-Partitioned Generalized Search Tree) Index
Usage: Optimized for certain data types like geometric data and text search.

Characteristics: Allows partitioning of data in a way that can lead to faster searches for some use cases.

Example:
```sql
CREATE INDEX index_name ON table_name USING SPGIST (column_name);
```

##### GIN (Generalized Inverted Index)
Usage: Ideal for indexing array values and full-text search.

Characteristics: Efficient for indexing composite types and supports fast access to multi-valued columns.

Example:
```sql
CREATE INDEX index_name ON table_name USING GIN (column_name);
```

##### BRIN (Block Range INdex)
Usage: Suitable for very large tables where the data is naturally sorted or clustered on the indexed column.

Characteristics: Provides a lightweight indexing method by summarizing ranges of block values.

Example:
```sql
CREATE INDEX index_name ON table_name USING BRIN (column_name);
```

##### Full-Text Search Index (GIN and GiST)
Usage: Specifically for full-text search capabilities in PostgreSQL.

Characteristics: Can be created using GIN or GiST indexes tailored for text search.

Example:
```sql
CREATE INDEX index_name ON table_name USING GIN (to_tsvector('english', column_name));
```

##### Bloom Filter Index
Usage: Suitable for multiple columns with a high probability of being unique.

Characteristics: Uses Bloom filters to create a space-efficient, probabilistic data structure.
Example:
```sql
CREATE EXTENSION bloom;
CREATE INDEX index_name ON table_name USING bloom (column1, column2);
```

##### Expression Indexes
Usage: Indexes the result of an expression or function.

Characteristics: Allows indexing of complex expressions or function results.

Example:
```sql
CREATE INDEX index_name ON table_name ((lower(column_name)));
```
##### Partial Indexes
Usage: Indexes only a subset of rows in a table.

Characteristics: Improves performance and reduces storage by indexing only rows that meet a specific condition.

Example:
```sql
CREATE INDEX index_name ON table_name (column_name) WHERE condition;
````

### Transactions

**Basic Transaction Commands**

* BEGIN: Starts a new transaction.
* COMMIT: Saves all the changes made during the transaction.
* ROLLBACK: Undoes all the changes made during the transaction.

```sql
BEGIN;

-- SQL statements here
INSERT INTO employees (name, position, salary) VALUES ('Alice', 'Developer', 50000);
UPDATE employees SET salary = 55000 WHERE name = 'Alice';

COMMIT; -- or ROLLBACK if something goes wrong

```

**Savepoints in Transactions**

Savepoints allow you to set a point within a transaction to which you can roll back without affecting the entire transaction.

```sql
BEGIN;

-- First operation
INSERT INTO employees (name, position, salary) VALUES ('Bob', 'Manager', 70000);

SAVEPOINT savepoint1;

-- Second operation
UPDATE employees SET salary = 75000 WHERE name = 'Bob';

-- If the second operation fails, roll back to the savepoint
ROLLBACK TO SAVEPOINT savepoint1;

-- Commit the transaction
COMMIT;

```

**Transaction Isolation Levels**

PostgreSQL supports different isolation levels to control the visibility of changes made in a transaction to other concurrent transactions. The isolation levels are:

* Read Committed (default): A statement can see only committed data.
* Repeatable Read: Ensures the data read during the transaction remains consistent.
* Serializable: Provides the strictest isolation level by ensuring complete isolation from other transactions.

### Schemas
In PostgreSQL, a schema is a logical container for database objects such as tables, views, indexes, sequences, functions, and other relations. Schemas help organize and manage these objects in a database, providing a namespace to avoid name conflicts between objects.

#### What is a Schema in PostgreSQL?

1. Namespace:

   A schema acts as a namespace that allows multiple objects to have the same name as long as they belong to different schemas. This helps in organizing and managing database objects more efficiently.
   
2. Organization:

   Schemas allow you to logically group related objects, making it easier to manage permissions and maintain the database structure.

3. Default Schema:

   PostgreSQL has a default schema called public. By default, all database objects are created in the public schema unless specified otherwise.

4. Access and Security:

    Schemas enable fine-grained access control. You can grant or revoke permissions on a schema, thereby controlling access to all objects within that schema.


#### Creating and Using Schemas

**Creating a Schema**

You can create a new schema using the CREATE SCHEMA statement.

```sql
CREATE SCHEMA schema_name;
-- example
CREATE SCHEMA my_schema;
```
**Creating Objects in a Schema**

To create a table or other objects in a specific schema, you need to specify the schema name.

```sql
CREATE TABLE my_schema.my_table (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100)
);
```

**Using Schemas**

To refer to an object within a specific schema, use the schema name as a prefix.

```sql
SELECT * FROM my_schema.my_table;
```

#### Managing Schemas
**Listing Schemas**

You can list all schemas in a database using the `\dn` command in `psql` or querying the `pg_catalog.pg_namespace` system catalog.

```sql
SELECT schema_name
FROM information_schema.schemata;
```
**Changing the Search Path**

The search path determines the order in which schemas are searched when an object name is referenced without a schema. You can change the search path using the `SET search_path` command.

```sql
SET search_path TO my_schema, public;
```

#### Example Workflow

```sql
-- Create a New Schema:

CREATE SCHEMA sales;
-- Create Objects in the Schema:

CREATE TABLE sales.customers (
  customer_id SERIAL PRIMARY KEY,
  customer_name VARCHAR(100)
);

CREATE TABLE sales.orders (
  order_id SERIAL PRIMARY KEY,
  order_date DATE,
  customer_id INTEGER REFERENCES sales.customers(customer_id)
);

-- Querying Objects:

SELECT * FROM sales.customers;

-- Setting the Search Path:

SET search_path TO sales, public;

-- Now you can reference the table without the schema prefix
SELECT * FROM customers;
```

### Views
### Command Line Interface


## Questions and Answers

#### What is PostgreSQL?

PostgreSQL is a powerful, open-source relational database management system known for its robustness, extensibility, and standards compliance. It supports advanced data types, and complex queries, and is ACID-compliant.

#### What is a primary key in PostgreSQL?
A primary key is a column or a set of columns that uniquely identifies each row in a table. It ensures uniqueness and provides a unique index for faster access.

#### What is a foreign key in PostgreSQL?

A foreign key is a column or a set of columns in a table that establishes a link between data in two tables. It ensures referential integrity by enforcing a link between the foreign key column(s) and the primary key column(s) of another table.

#### What is a transaction in PostgreSQL?

A transaction is a sequence of one or more SQL operations that are executed as a single unit of work. PostgreSQL transactions are ACID compliant, ensuring atomicity, consistency, isolation, and durability.

#### How do you start a transaction in PostgreSQL?
You start a transaction using the `BEGIN` statement and end it using `COMMIT` or `ROLLBACK`:

```sql
BEGIN;
-- SQL statements
COMMIT;  -- or ROLLBACK;
```

#### How do you create an index in PostgreSQL?

You create an index using the CREATE INDEX statement:
```sql
CREATE INDEX index_name ON table_name (column_name);
```
#### What is a partial index in PostgreSQL?

A partial index is an index built on a subset of a table. It is defined by adding a `WHERE` clause to the `CREATE INDEX` statement:
```sql
CREATE INDEX index_name ON table_name (column_name) WHERE condition
```

#### How can you improve the performance of a PostgreSQL database?

* Using indexes to speed up query execution.
* Optimizing queries by analyzing execution plans with `EXPLAIN`.
* Using appropriate data types and normalization.
* Configuring PostgreSQL parameters for better performance `(e.g., work_mem, shared_buffers)`.
* Archiving old data and partitioning large tables

#### What are sequences in PostgreSQL, and how are they used?

Sequences are special database objects designed for generating unique numeric identifiers. 

They are often used for auto-incrementing primary key values:

```sql
CREATE SEQUENCE seq_name;
SELECT nextval('seq_name');
```

#### What is a `VIEW` in PostgreSQL?

A view is a virtual table based on the result set of an SQL query. It can be used to simplify complex queries, enhance security by restricting access to specific columns, and encapsulate complex logic.

```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```

#### do we insert new row without one column in postgresdb?

**Yes**, you can insert a new row without specifying a value for one or more columns in PostgreSQL, provided those columns allow null values or have default values defined.

If a column is defined to accept null values, it will automatically be set to NULL if you don't provide a value.

If a column has a default value, that default will be used.

Example

```sql
CREATE TABLE example_table (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  age INTEGER,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

INSERT INTO example_table (name) VALUES ('John Doe');

SELECT * FROM example_table;

```

# MongoDB
MongoDB is a popular open-source NoSQL database that uses a flexible, document-oriented data model to store, manage, and retrieve data. It is designed for scalability, high performance, and ease of development. 

MongoDB is widely used in modern web applications due to its flexibility and powerful querying capabilities.

## Core Concepts of MongoDB

### Document-Oriented Database:
MongoDB stores data in flexible, JSON-like documents, which means fields can vary from document to document, and data structure can change over time.

### Collections:
Documents are grouped into collections. A collection is a group of MongoDB documents that are similar in structure, akin to tables in relational databases.

### Documents:
The basic unit of data in MongoDB, similar to rows in relational databases. Documents are stored in BSON (Binary JSON) format and can contain arrays and subdocuments.

Example of a MongoDB document:
```json
{
  "_id": ObjectId("507f1f77bcf86cd799439011"),
  "name": "John Doe",
  "age": 29,
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  },
  "hobbies": ["reading", "travelling"]
}
```

### Schema-less:
MongoDB is schema-less, meaning that documents in a collection do not need to have the same set of fields, and data types for the fields can vary across documents.

### Indexes:
Indexes in MongoDB function similarly to those in relational databases. They improve the performance of search queries.

Example of creating an index:
```javascript
db.collection.createIndex({ "name": 1 });
```

### Replication:
MongoDB provides high availability through replication. A replica set is a group of MongoDB servers that maintain the same data set, providing redundancy and automatic failover.

Example of starting a replica set:
```javascript
rs.initiate()
```
### Sharding:
Sharding is MongoDB's method for handling large data sets and high throughput operations by distributing data across multiple servers.

Example of enabling sharding:
```javascript
sh.enableSharding("myDatabase");
```

### Aggregation Framework:
MongoDB's aggregation framework allows for the processing of data records and returning computed results. It provides operations like filtering, grouping, and sorting data.

Example of an aggregation query:
```javascript
db.orders.aggregate([
  { $match: { status: "A" } },
  { $group: { _id: "$cust_id", total: { $sum: "$amount" } } }
]);
```

### CRUD Operations:
MongoDB supports basic CRUD operations: Create, Read, Update, and Delete.

Create: Insert documents into a collection.
```javascript
db.collection.insertOne({ name: "John Doe", age: 29 });
```

Read: Query documents from a collection.
```javascript
db.collection.find({ age: { $gte: 18 } });
```

Update: Modify existing documents in a collection.
```javascript
db.collection.updateOne({ name: "John Doe" }, { $set: { age: 30 } });
```

Delete: Remove documents from a collection.
```javascript
db.collection.deleteOne({ name: "John Doe" });
```

### Flexible Data Model:
MongoDB’s schema-less nature allows for a more flexible and dynamic data model that can evolve with the needs of the application without requiring a predefined schema.

### Ad-hoc Queries:
MongoDB supports a rich query language that allows for ad-hoc queries, indexing, and real-time aggregation.

## Types of Indexing in MongoDB

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


