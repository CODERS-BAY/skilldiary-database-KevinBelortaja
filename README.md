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

# 3. DB 24.2

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


#### Example 3NF:

Person# | Name | Department# | Department name
---|---|---|---
100|Hans|1|Chemistry
101|Paul|2|English
102|Georg|2|English

becomes ->

Person#|Name|Department#
---|---|---
100|Hans|1
101|Paul|2
102|Georg|2

and...

Department#|Department name
---|---
1|Chemistry
2|English


# Fortsetzung

## Select

Wählt das aus was du haben willst und gibt es aus

## Where

Bei der Auswahl beziehungsweise Filterung mithilfe von WHERE innerhalb der SELECT-Anweisung kann man Vergleichsoperatoren anwenden <br>
>= gleich <br>
<> ungleich  <br>
(>) größer als  <br>
(>=) größer gleich als  <br>
< kleiner als  <br>
<= kleiner gleich als  <br>
NOT der Wahrheitswert einer Bedingung wird umgekehrt <br>
AND alle Bedingungen müssen zutreffen <br>
OR mindestens eine Bedingung muss zutreffen <br>

## Joins

Joins verbindet zwei oder mehrere Relationen miteinander

### Cross Join
Jede Zeile von R1 verbunden mit jeder Zeile von R2

### INNER JOIN
Verbindet alle Zeilen von R1 und R2 miteinander, wo ein Match gefunden wird.

### OUTER JOIN
Verbindet alle Zeilen von R1 und R2 miteinander, wo ein Match gefunden wird. Wo keiner gefunden wird, wird der Rest mit NULL aufgefüllt.

### LEFT JOIN
Jede Zeile von R1 verbunden mit dazupassenden Zeilen von R2

### RIGHT JOIN
Jede Zeile von R2 verbunden mit dazupassenden Zeilen von R1

### NATURAL JOIN
Natürlicher Verbund von R1 und R2 bei gleichnamiger Spalte <br>

Beispiel: <br>
SELECT employees.last_name, departments.department_name <br>
FROM employees <br>
JOIN departments <br>
ON employees.department_id = departments.department_id; <br>


## Konzeptionelles Schema

Beschreibung der logischen Dateien und der darin enthaltenen Record - Typen (nicht aber Angaben zur physischen Implementierung) <br>
Beschreibung der Felder, die in einem bestimmten Satztyp vorkommen <br>
Beschreibung der Beziehungen (Relationen) zwischen den logisch zusammengehörenden Satztypen einer Datenbank <br>
Beschreibung der Gültigkeitsbereiche einzelner Felder <br>

## Sub-Supertyp
Bei der Spezialisierung wird ein Entitätstyp als Teilmenge eines anderen, ‚übergeordneten‘ Entitätstyps angenommen. Im Supertyp sind alle Attribute, die den Subtypen gemeinsam sind. Im Subtyp 1 findet man alle Attribute, die nur dort und nicht in den anderen Subtypen oder dem Supertyp vorkommen. Damit generalisiert der Supertyp.

