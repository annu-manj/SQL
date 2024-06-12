# SQL

**SQL**
SQL is a language used for relational databases to query or get data out of a database.
"S Q L" is also referred to as "sequel", and is short for it's original name "Structured English Query Language".

**DATA**
Data is a collection of facts in the form of words, numbers, or even pictures.
Data is one of the most critical assets of any business.It is used and collected practically everywhere.

**DATABASES**
A database is a repository of data. It is a program that stores data.
A database also provides the functionality for adding, modifying and querying that data.

**TABLE**
A table is a collection of related things, like a list of employees, or a list of book authors.
In a relational database, you can form relationships between tables.

**DBMS**
A set of software tools for the data in the database is called a database management system.

**RDMS**
RDBMS is a set of software tools that controls the data, such as access, organization, and storage.
Examples of relational database management systems are: *MySQL*, *Oracle* Database, and *DB2* Express-C.

**5 basic SQL commands**
1. insert
2. select
3. delete
4. modify
5. update

# INFORMATION MODEL AND DATA MODEL

An **Information Model** is an abstract, formal representation of entities that includes their properties, relationships and the operations that can be performed on them. The entities being modeled can be from the real world, such as a library. 
An Information Model is at the conceptual level, and defines relationships between objects. 
Example :Hierarchical,typically used to show organization charts. As shown is in this figure, the hierarchical
model organizes its data using a tree structure. 

The *first* **hierarchical database management** system was the **Information Management System** released by IBM in 1968 and was originally built as the database for the Apollo space program. 


**Data Models** are defined at a more concrete level, are specific and include details. A data model is the blueprint of any database system. 
Types are:
-> Relational database model
-> ERD


### ERD
ERD represents entities(called tables) and their relationships 

Entities - rectangle (Entities can be a noun (person, place, or thing))
attributes - ovals (book title, the edition of the book, the year the book was written etc)

Attributes are connected to exactly one entity. The entity Book becomes a table in the database, and the attributes become the columns in a table.



## TYPES OF RELATIONSHIP
The building blocks of a relationship are: entities, relationship sets, and crows foot notations. Entity sets are represented by a rectangle. 
Relationship sets are represented by a diamond, the lines connecting associated entities. Different techniques are used in
representing relationships. 


The **entity**, Book, is drawn as a rectangle, and the attributes are drawn as ovals. 
**Attributes** are certain properties of that entity, for example title, edition, year, price, etc.
Attributes are connected to exactly one entity. For the entity Author, the ER diagram
would look like this. The entity Author has attributes last name, first name, email, city,
country and author ID. Let's see how the entities Book and Author relate to each other.
A book must be written by at least one author. However, a book can be written by two authors.
and a book can be written my many authors. As another example, one author can write
just one book, or two books or multiple books. In both cases, there is a relationship between
the book and the author.

**One-to-one relationship**
The relationship set that comes here is authored-by. One book must be written by one author.The thick lines indicate each entity in the entity set is involved in at least one and exactly one relationship. This is called a one-to-one relationship. 


**One-to-many**
• A book written by many author
• Crows foot notation, less-than symbol
• Many-to-one relationship for many authors write a single book
More than one author can write a book. This can be represented with a different notation called crows foot notation. In this case, a less than symbol. This indicates, that one book entity is participating in more than one relationship in the relationship set. This is called a one-to-many relationship. This could also be called a many-to-one relationship in that many authors write a single book.

**many-to-many relationship**
• Crows foot notation, less-than symbol
• Many books written by many authors
• Many authors writing many books
To represent many authors writing many books, use the greater-than and less-than symbols on either side of the relationship set.This is called a many-to-many elationship. Each entity in the entity set is participating in more than one relationship.Many books being written by many authors, or, many authors writing many books. 


# MAPPING ENTITIES TO TABLES

For example, we use the ERD for entity Book. Entity Book has several attributes.The entity and its attributes will be mapped to a table.

Entity - Book
Attributes - title, description, edition, year, aisle, pages, ISNB, price, year

In this case, 
             
entity book -> table (book)
attributes -> columns


# RELATION MODEL CONCEPT
The building blocks of the Relational Model are: Relation and Sets.

A Relation is made up of 2 parts: Relational Schema and Relational Instance.



# RELATIONAL MODEL CONTRAINTS

**PRIMARY KEY**- Uniquely identifies each row in a table.

**FOREIGN KEY** - is a set columns that identifies primary key another table.

**PARENT TABLE** - A table containing a primary key that is related to at least one foreign key is called a Parent table.

**DEPENTED TABLE/ CHILD TABLE** - A table containing one or more foreign keys is called a dependent table. It might also be referred to as a child table.

# CONSTRAINTS

The following six constraints are defined in a relational database model: 
**Entity integrity constraint**  - 
    This constraint prevents duplicate values in a table.
    The entity integrity constraint states that no attribute participating in the primary key of a relation is allowed to accept null values.
**Referential integrity constraint**
    Referential integrity constraint defines relationships between tables and ensures that these relationships remain valid.
    The validity of the data is enforced using a combination of primary keys and foreign keys. 
**Semantic integrity constraint**
    The semantic integrity constraint refers to the correctness of the meaning of the data.
**Domain constraint**
    A domain constraint specifies the permissible values for a given attribute. For example, in the relation author,the attribute country must contain
    a two letter country code such as CA for Canada or IN for India.If a number value of 34 is entered for the country attribute instead of a two letter country code,
    the value 34 does not have any meaning. 
**Null constraint**
    The null constraint specifies that attribute values cannot be null.
**Check constraint**
    The check constraint enforces domain integrity by limiting the values that are accepted by an attribute.
    The relation author does not have a suitable attribute to explain the check constraint, so we will use the relation book. In the relation book, the attribute year is the year in which a particular book is published.If this was still the year 2010, it would not be meaningful to have a year greater than the current year.
    The check constraint would enforce the domain integrity by limiting the values that are accepted by the attribute year.
    
**Primary Keys**
If a relation schema has more than one key, then each key is called a candidate key.One of the candidate keys is designated as the primary key, and the others are called secondary keys.

In a practical relational database, each relation schema must have a primary key.

**Rules for primary keys:**
The value of the Primary Key must be unique for each instance of the entity.

There can be no missing values( ie. Not Null) for Primary Keys. If the Primary Key is composed of multiple attributes, each of those attributes must have a value for each instance.
The Primary Key is immutable.i.e., once created the value of the Primary Key cannot be changed.
If the Primary Key consists of multiple attributes, none of these values can be updated.
 

**Semantic Integrity**
Semantic integrity ensures that data entered into a row reflects an allowable value for that row. The value must be within the domain, or allowable set of values, for that column. For example, the quantity column of the items table permits only numbers. If a value outside the domain can be entered into a column, the semantic integrity of the data is violated.

 

**Semantic Constraints**
Semantic Constraints are constraints that cannot be directly expressed in the schemas of the data model. Semantic constraints are also called application-based rules or business rules.  They are additional rules specified by users or database administrators. For example, a class can have a maximum of 30 students; salary of an employee cannot exceed the salary of the employee’s manager.

**Domain constraints** specify that within a tuple the value of each attribute must be an element from the domain of that attribute. The data types associated with the domains include:

Integers (short integer, integer, long integer)
Real numbers (float and double precision float)
Characters
Booleans
Fixed-length strings and variable length strings
Date, time, timestamp
Money
Other special data types
Other possible domain values may be a sub-range of values from a data type or as an enumerated data type in which values are explicitly listed.


# SQL STATEMENTS
SQL Statements are used for interacting with Entities (that is, tables), Attributes (that is, columns) and their tuples (or rows with data values) in relational databases.

# DDL
Used to define,change or drop data
-> CREATE
-> ALTER
-> TRUNCATE
-> DROP

**CREATE**: which is used for creating tables and defining its columns;

        CREATE TABLE table_name(
            column_name1 datatype optional parameters,
            column_name2 datatype,
            column3 datatype
        )

        
**ALTER**: is used for altering tables including adding and dropping columns and modifying their datatypes;
**TRUNCATE**: is used for deleting data in a table but not the table itself;
**DROP**: is used for deleting tables.

# DML
Data Manipulation Language (or DML) statements are used to read and modify data in tables.
-> INSERT
-> READ
-> UPDATE 
-> DELETE

**INSERT**: is used for inserting a row or several rows of data into a table;
        
        INSERT INTO tablename <{(column_names)}> VALUES <{(values)}>;


**SELECT**: reads or selects row or rows from a table;

        SELECT columName FORM tablename;
        SELECT * FROM tablename;

    restricting the result set:-
         
        select columnName from tableName where predicate;
        select columnName from tableName where colunmae_name = value;


**UPDATE**: edits row or rows in a table;

        update tableName 
        set columnName = Value
        wher condition

**DELETE**: removes a row or rows of data from a table.

        delete from tableName
        where condition

DDL or Data Definition Language statements are used for defining or changing objects in a database such as tables.

DML or Data Manipulation Language statements are used for manipulating or working with data in tables.


**WHERE CLAUSE PREDICATE**

# LIKE
Like predicate is used in a where clause to search for a pattern in a column

        select * from tablename 
        where firstname like 'R%'

        %r , %r%

        % - wildcard character

# >= AND <=

# between value and value


**SORTING RESULT SET**

        select * from tablename
        order by title asc/desc;

        default : asc 

**GROUPING RESULT SET**
The GROUP BY clause groups a result into subsets that has matching values for one or more columns.
        select distinct(country) from author;
        distinct eliminates duplicate values

        select country, count(country) from tablename 
        group by country


To set a condition to a GROUP BY clause, we use the keyword *HAVING*.
WHERE clause is for the entire result set, but the HAVING clause works only with the GROUP BY clause.

# JOIN
A JOIN combines the rows from two or more tables based on a relationship between certain columns in these tables.

**INNER JOIN**
An inner join matches the results from two tables and displays only the result set that matches the criteria specified in the query. An inner join returns only the rows that match.

**OUTER JOIN**
Outer joins, like inner joins, return the rows from each table that have matching values
in the join columns.
Unlike inner joins, outer joins also return the rows that do not have a match between
the tables.

**LEFT JOIN**
Left Join matches all the rows from the left table and combines the
information with rows from the right table that match the criteria specified in the query.

SELECT column1, column2, ...
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;


**RIGHT JOIN**
In a right outer join, all the rows from the first table (on the left side of the join
predicate) are included, and only the matching rows from the second table (on the right side
of the join predicate).

SELECT column1, column2, ...
FROM table1
RIGHT JOIN table2
ON table1.common_column = table2.common_column;


**FULL OUTER JOIN**
A FULL OUTER JOIN returns all rows when there is a match in one of the tables. It returns NULL for columns of the table that does not have a match.

SELECT column1, column2, ...
FROM table1
FULL OUTER JOIN table2
ON table1.common_column = table2.common_column;


