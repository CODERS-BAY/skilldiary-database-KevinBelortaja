# 1.DB - 10.2

Entity - Objekt (square)<br>
Relationshiop - Beziehung (rhombus)<br>
Attribut - Eigenschaften (circle)

1:1 (country and currency)<br>
1:n (person has shoes) <br>
n:1 (students in school)<br>
n:m (family and car)

participant (Nr: int; Name: varchar) <br>

primary key identiefies an entity


# 2.DB - 17.2

DBMS Types<br>
-Hierarchical DBMS´s<br>
-Network-type DBMS´s<br>
-Relational DBMS´s<br>
-Invertial Lists DBMS´s<br>
-Object relational DBMS´s<br>
-Object oriented DBMS´s<br>
presantation about invertial Lists DBMS´s <br>

Entity:<br>
-noun <br>
-singular <br>

Relationship: <br>
-verb <br>

| one <br>
O zero <br>
^ more <br>

Synonym: <br>
-Different designation for one word (entity) <br>

Homonym: <br>
-One designation for more words (entitys) <br>

Primary key: <br>
-can´t be changed, identifies an unique objekt <br>

Foreign key: <br>
-is an attribute which stands to relationship with another primary key <br>

N:M
Instead of connecting two n:m (E1 - E2) entitys with one relationship, you should connect the first entity (E1) with the previous two entitys (E1_E2) and that with the second entity from the previous one (E2) <br>

E1 n:---------------------:M E2 <br>
E1 1:-----:n E1_E2 n:-----:1 E2 <br>

## 3. DB 24.2

Generalisation - Specialisation <br>
A car consists of a engine and auto body <br>

Redundancy: <br>
A company saves after every order the costumer ID, name and address <br>

Anomaly: <br>
Student# | Lecture# | Student name | Student address | Lecture name
---|---|---|---|---
S21 | 8754 | Bob | Linz | Database
S33 | 8750 | Ben | Wels | Java

## Update Anomaly:
If something changes, everything needs to be changed <br>

## Insert Anomaly:
Nothing can be empty

## Delete Anomaly:
If something is deleted, everything in this row should be deleted too.


### 1NF
Functional dependent from the total-key

### 2NF
no functional dependence from key-parts

### 3NF
no functional dependence from non-key-attributes
