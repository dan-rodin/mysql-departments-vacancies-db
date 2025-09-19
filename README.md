# Departments Vacancies Database (MySQL Project)

**Database: rodin22399643 = surname + student number**

This repository contains my MySQL database assignment for **COMP20070 – Database Systems** at University College Dublin.
The database models a company's **departments, vacancies, skills, candidates, and interviews**, based on the scenario provided in the assignment brief.

Includes a *Breaking Bad*–themed candidates dataset, modeled after a tech company based out of Albuquerque, New Mexico (where the TV show is set).

---

## 📖 Project Overview
The goal was to design and implement a relational database that supports:
- Candidates and their personal details/skills
- Departments and the positions they offer
- Interviews between candidates and departments
- Many-to-many relationships between skills, candidates, and positions

---

## 🗄️ Features
- **7 tables** including many-to-many linking tables (`CandidateSkills`, `PositionSkills`)
- **Constraints**: primary keys, foreign keys, uniqueness, and cascading deletes
- **Stored procedures** for inserting into each table
- **Parametric queries** for:
  - Finding candidates by name or ID
  - Querying skills required for positions
  - Counting positions/offers
  - Listing interviews by date
  - Sorting positions by department

---

## ⚙️ Stored Procedures

The database includes parametric stored procedures for inserting data and executing queries.
Below are some examples:

#### Insert Candidate:
```sql
CALL InsertCandidate('Walter', 'White', '308 Negra Arroyo Lane', '0851234567');
```
#### Get Interviews by Date:
```sql
CALL Q9_GetInterviewsByDate('2024-11-10');
```
---

## 📂 Repository Contents
- `rodin22399643.sql` → Full schema, data inserts, and stored procedures
- `ER-Diagram.png` → Entity-Relationship diagram exported from MySQL Workbench
- `queries/` → Example queries with screenshots of results