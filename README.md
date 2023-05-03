Download Link: https://assignmentchef.com/product/solved-create-database-star
<br>
<strong>1.CREATE DATABASE Star;</strong>

Executing the above statement in SQL Server will create two files: Star. (blank) and Star_log.(blank).The first file holds the data for the Star database and the second one keeps a log of any changes made to Star. (each is a file extension) “fill in the (blanks)”

2. Create Table ( blank ) <strong> (SID varchar(7) (blank) (SID LIKE ‘ (blank)  ‘)); F</strong>ill in the three blanks of the above statement such that it creates a table Student in schema CSE. This table contains only one column SID with a constraint which requires the second character of every SID value to be a digit ‘8’.

3. Will attack the table in the attach files section for this question<img decoding="async" src="https://www.coursehero.com/qa/attachment/2621819/" alt="PK_FK.png">

X and Y are two tables, where c1 and d1 are the primary key of each table, respectively. To complete the relationship in above diagram, the crow’s foot notation should be added to the end of the line that connects table (blank)

To create table Y, we should execute

CREATE TABLE Y (d1 int PRIMARY KEY, c1 int (blank) X(c1)); –one word

In the diagram of Question 3, if every row of Y must associate with one row of X, then we need to insert ______________ right after ‘c1 int’ of the CREATE TABLE Y statement. (two words)

In the diagram of Question 3, if we want to remove c2 column out of X, we must execute

ALTER TABLE X ____________ c2;  –two words

4.Complete the following statement to create a view called EmpOfBiggestDept, which returns all employees of the department(s) that has the most employees. (the 2nd blank contains two words)

<strong>CREATE VIEW EmpOfBiggestDept</strong>

<strong>AS SELECT * FROM Employee</strong>

<strong>   WHERE Dept_ID in (SELECT TOP 1 WITH TIES(blank)</strong>

<strong>From</strong>

<strong>(Blank) </strong><strong> Dept_ID</strong>

<strong>ORDER BY COUNT(*) DESC);</strong>

5. Suppose the MailBoxes table contains three columns, BoxNo, StuID, and MonthlyFee. Complete the UPDATE statement below to change MonthlyFee to $13 of students whose StuID begins with ‘G’. MonthlyFee of all others should be changed to $11. <em>Hint: each blank is one word.</em>

<strong>UPDATE MailBoxes</strong>

<strong>SET MonthlyFee = (blank)</strong>

<strong>(blank) </strong><strong> StuID like ‘G%’ (blank) 13</strong>

<strong>(blank) 11</strong>

<strong>(blank);</strong>

<strong>6. </strong>It is assumed that a student could have zero or one or more mailboxes but mailboxes cannot be shared. In the following statements, all columns of MailBoxes table can accept nulls except BoxNo.

<strong>SELECT StuID FROM Students</strong>

<strong>EXCEPT</strong>

<strong>SELECT StuID FROM MailBoxes;</strong>

Fill in the blank of each of the statements below such that each returns the same as the above one.

<strong>SELECT StuID</strong>

<strong>FROM Students </strong>

<strong>WHERE StuID (blank)  (SELECT StuID FROM MailBoxes); </strong>–two words

<strong>SELECT s.StuID</strong>

<strong>FROM Students s (blank)  outer join MailBoxes m on s.StuID = m.StuID </strong>–one word

<strong>WHERE BoxNo is null;</strong>

<strong>SELECT StuID</strong>

FROM Students st

<strong>WHERE not (blank) (SELECT * FROM MailBoxes WHERE StuID = st.StuID); </strong>–one word

7. Suppose Region is a schema of a database called CRM and Kathy is a user of CRM. Complete the following statement so Kathy can insert data into applicable objects in Region.

GRANT (blank ) ON (blank)  TO Kathy;

8. <strong>use AP</strong>

<strong>go</strong>

<strong>create function TwoOrMoreDashInvoices()</strong>

<strong>returns @Inv table(InvID int, InvNum varchar(50), InvTotal money)</strong>

<strong>as</strong>

<strong>begin</strong>

<strong>  insert into @Inv</strong>

<strong>    select InvoiceID, InvoiceNumber, InvoiceTotal</strong>

<strong>    from Invoices</strong>

<strong>    where InvoiceNumber like ‘ (blank)  ‘;</strong>

<strong>(blank) ;</strong>

<strong>end</strong>

Fill in both blanks to complete the above statement to create a table-valued function called TwoOrMoreDashInvoices, which returns invoices whose InvoiceNumber contains two or more ‘-‘ (e.g., 111-92R-10097 or RTR-72-3662-X)

8b. Which of the following can be executed to test the function create in Question 14?

a. print TwoOrMoreDashInvoices()

b. exec TwoOrMoreDashInvoices()

c. select * from TwoOrMoreDashInvoices()

8c. The same function of Question 14 can be created by a different statement below, if the blank is filled in correctly.

<strong>use AP</strong>

<strong>go</strong>

<strong>create function TwoOrMoreDashInvoices()</strong>

<strong>returns (blank)</strong>

<strong>return</strong>

<strong>(select InvID=InvoiceID, InvNum=InvoiceNumber, InvTotal=InvoiceTotal</strong>

<strong> from Invoices</strong>

<strong> where ……….);</strong>