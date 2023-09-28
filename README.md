# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
SQL> CREATE TABLE es(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO es(empid,empname,dept,salary)
    values(1,'NAGUL','AIDS',100000);
    INSERT INTO es(empid,empname,dept,salary)
    values(2,'VINOD','AIML',100000);
    INSERT INTO es(empid,empname,dept,salary)
    values(3,'ARVIND','AIML',100000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM es)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```

### Output:
![Screenshot 2023-09-27 153005](https://github.com/Nagul71/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118661118/d7c0a2aa-eb7a-4abe-84d1-70f8fb28f01e)


### Result:
The procedures has been successfully created using PL\SQL
