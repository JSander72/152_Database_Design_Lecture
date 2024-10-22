### Database Design and Planning with ERDs

#### **Lesson Overview**

This lesson provides a comprehensive recap of SQL databases, followed by an in-depth exploration of SQL database design with a focus on Entity-Relationship Diagrams (ERDs). The goal is to reinforce your understanding of SQL databases and introduce you to the principles and practices of effective database design.

### **SQL Databases Recap**

#### **Introduction to SQL Databases**

A **SQL database** is a type of relational database that uses Structured Query Language (SQL) for defining and manipulating data. SQL databases are widely used in various applications because they provide a systematic and organized way of storing, retrieving, and managing data.

**Key Concepts:**

*   **Tables**: The fundamental structure within a SQL database, organized into rows and columns. Each table represents an entity (e.g., Customers to store information about customers).
    
*   **Records (Rows)**: Each row in a table represents a single instance of the entity (e.g., a single customer).
    
*   **Fields (Columns)**: Each column represents an attribute of the entity (e.g., customer\_name, customer\_email could be fields in our customer table).
    
---
#### **Common SQL Commands**

SQL commands are divided into different categories, mainly **Data Definition Language (DDL)** and **Data Manipulation Language (DML)**.

**DDL Commands:**

*   `CREATE`: Used to create new tables and other database objects.
    
*   `ALTER`: Used to modify the structure of an existing table (e.g., adding a new column).
    
*   `DROP`: Deletes tables or other database objects.
    

**DML Commands:**

*   `SELECT`: Retrieves data from the database.
    
*   `INSERT`: Adds new records to a table.
    
*   `UPDATE`: Modifies existing data in a table.
    
*   `DELETE`: Removes records from a table.

[SQL Commands Refresher Video](https://www.loom.com/share/be5a39069b9a46ff86aed7843a22beca?sid=90f37e88-ebab-408e-908b-0d9f6cfa76bf)

---

#### **Relationships in SQL Databases**

In relational databases, **relationships** between tables are crucial. These relationships allow data to be organized efficiently and reduce redundancy by allowing multiple entries from TableA relate to an entry in TableB instead of restoring that information over an over.
* **Primary Key**: 99% of tables will have a primary key. Primary Keys are always unique and specific to a single entry in that table, which allows look up specific entries based on their unique ID

*   **Foreign Key**: A field in one table that links to the primary key of another table, establishing a relationship between the two tables.
    

    


    

### **SQL Database Design with Emphasis on ERDs**

#### **Introduction to Database Design**

Database design is the process of creating a detailed data model of a database. This involves defining the tables, fields, and relationships necessary to support the data requirements of a system.

**Key Benefits of Good Database Design:**

*   **Data Integrity**: Ensures accuracy and consistency of data.
    
*   **Efficiency**: Optimizes database performance and query speed.
    
*   **Scalability**: Allows the database to grow and adapt to new requirements without major restructuring.
    

#### **Entity-Relationship Diagrams (ERDs)**

An **Entity-Relationship Diagram (ERD)** is a visual representation of the entities (tables), attributes (fields), and relationships in a database. ERDs are essential tools for database design, helping to clarify and communicate the structure of a database. The previous diagrams depicting each type of relationship are all examples of ERDs.

**Components of an ERD:**

*   **Entities**: Represented as rectangles. An entity corresponds to a table in the database.
    
*   **Attributes**: Attributes are the fields in the table, and are written into the table with their corresponding datatype.
    
*   **Relationships**: Are shown with a line connecting the two related tables, typically connecting from the primary key of one table to the foreign key of another table.
    
*   **Primary Keys**: Is a unique field in a table, usually an id that is marked with a PK.
    
*   **Foreign Keys**: Are primary keys from one table, that show up in another table and is marked with an FK.

To make our ERD's we will be using [Lucidchart](https://lucid.app/documents)

In SQL and relational database design, relationships define how tables are connected to each other. These relationships are crucial for organizing data efficiently and ensuring data integrity. The three primary types of SQL relationships are:

#### **One-to-One (1:1) Relationship**

In a one-to-one relationship, each record in Table A corresponds to exactly one record in Table B, and vice versa. This type of relationship is not as common but can be used when you need to split data between two tables for organizational or security reasons.

**Example:**

*   **Tables**: Person and Passport.
    
*   **Relationship**: Each person has one unique passport.
    
*   **Implementation**: Use a foreign key in one table that references the primary key of the other table.
    

#### **One-to-Many (1) Relationship**

In a one-to-many relationship, a single record in Table A can be related to one or more records in Table B, but each record in Table B relates to only one record in Table A. This is the most common type of relationship in relational databases.

**Example:**

*   **Tables**: Department and Employee.
    
*   **Relationship**: One department can have many employees, but each employee belongs to only one department.
    
*   **Implementation**: The child table (Employee) has a foreign key that references the primary key of the parent table (Department).
    

#### **Many-to-Many (M) Relationship**

In a many-to-many relationship, records in Table A can be related to multiple records in Table B, and vice versa. Since relational databases don't directly support many-to-many relationships, they are required to use a junction (or association) table to facilitate the connection.

**Example:**

*   **Tables**: Student and Course.
    
*   **Relationship**: A student can enroll in multiple courses, and each course can have multiple students.
    
*   **Implementation**: Create a junction table (Enrollment) with foreign keys referencing the primary keys of both related tables.
    

#### Summary

*   **One-to-One**: Each record in one table is linked to one record in another table.
    
*   **One-to-Many**: A single record in one table is linked to multiple records in another table.
    
*   **Many-to-Many**: Multiple records in one table are linked to multiple records in another table,  **REQUIRES** a junction table.
    

#### **Steps to Create an ERD**

Using what we know about SQL and the relationships that connect each table, let's go over how we can design an ERD to lay the road map for our database.

### Task:
Imagine you are tasked with designing a database to help manage a Library. Before we lay down a single line SQL to create this database we need to plan and design an ERD.


**Step 1: Identify Entities**

*   For a library management system, entities could include books, members, loans.
    

**Step 2: Identify Attributes**

*   Example: books might have id, title, author, genre.
    
*   What information do you think would be included in members and loans?
    

**Step 3: Define Relationships**

*   Example: A Member can make multiple Loans, a single Loan could contain multiple Books, but a Book can only be on one Loan at a time.
    

**Step 4: Draw the ERD**

*   Join me as we create this ERD in [LucidChart](https://www.lucidchart.com) to give ourselves a good idea on what our Library Management System looks like.