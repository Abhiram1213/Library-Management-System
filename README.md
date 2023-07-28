Database Creation:

The script begins by creating a new database called "library" using the command CREATE DATABASE library;.
It then switches to using the newly created database with the command USE library;. All subsequent operations are performed within this database.
Table Creation:

The script creates several tables to store different types of information related to the library:
Books: Stores information about books, including ISBN, title, category, rental price, status, author, and publisher.
Branch: Stores information about library branches, including branch number, manager ID, branch address, and contact number.
Employee: Stores information about library employees, including employee ID, employee name, position, and salary.
Customer: Stores information about library customers, including customer ID, customer name, customer address, and registration date.
IssueStatus: Stores information about issued books, including issue ID, customer ID (who borrowed the book), book name, issue date, and book ISBN.
ReturnStatus: Stores information about returned books, including return ID, customer ID (who returned the book), book name, return date, and book ISBN.
Data Insertion:

The script inserts sample data into each of the tables using the INSERT INTO statements.
Sample data is provided for books, branches, employees, customers, issued books, and returned books.
Data Retrieval:

The script uses several SELECT queries to retrieve information from the database:
It selects the book title, category, and rental price from the Books table for books with a status of 'yes'.
It selects the employee name and salary from the Employee table and orders the results by salary in descending order.
It retrieves book titles and customer names from the Books, IssueStatus, and Customer tables by performing joins on related columns.
It selects employee names and positions from the Employee table where the salary is greater than 50,000.
It selects customer names from the Customer table where the registration date is before '2022-01-01' and the customer ID is not found in the list of issued customers in the IssueStatus table.
It selects branch numbers and the total number of employees (managed by the manager) from the Branch and Employee tables and groups the results by branch number using a join operation.
It retrieves distinct customer names from the Customer table by performing a join with the IssueStatus table on customer ID and filtering results based on issue dates in June 2023.
It selects book titles from the Books table where the category is 'History'.
It selects branch numbers and the total number of employees (managed by the manager) from the Branch and Employee tables, groups the results by branch number, and applies a HAVING clause to filter branches with more than five employees.
