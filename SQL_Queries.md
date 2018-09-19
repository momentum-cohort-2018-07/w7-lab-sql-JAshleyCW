## SQL Queries HW

### Find all time entries. 
SELECT * FROM time_entries

**500** rows returned in 8ms 

### Find the developer who joined most recently.
SELECT * FROM developers  
ORDER BY joined_on DESC;

50 rows returned in 1ms  
**ID:34 Dr. Danielle McLaughlin**

### Find the number of projects for each client.
SELECT projects.id, clients.name  
FROM projects  
INNER JOIN clients ON projects.client_id=clients.id  
GROUP BY clients.name  

**9** rows returned in 1ms

### Find all time entries, and show each one's client name next to it.
SELECT time_entries.project_id, projects.client_id, clients.name  
FROM ((time_entries  
INNER JOIN projects ON time_entries.project_id = projects.id)  
INNER JOIN clients ON projects.client_id = clients.id);  

**500** rows returned in 7ms (a few listed below)

Entry |         Client Name
------|-------------------------------
   1  | Eichmann, Altenwerth and Morar
   2  | Zieme-Ortiz
   3  | Ortiz, Gislason and Rutherford

### Find all developers in the "Ohio sheep" group.


### Find the total number of hours worked for each client.


### Find the client for whom Mrs. Lupe Schowalter (the developer) has worked the greatest number of hours.


### List all client names with their project names (multiple rows for one client is fine). Make sure that clients still show up even if they have no projects.


### Find all developers who have written no comments.