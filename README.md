Download Link: https://assignmentchef.com/product/solved-csci3901-lab7-mysql-connection
<br>
In this lab, you will establish a connection between a Java program and a MySQL database.

Assignment 5 will use the kind of database connection that you establish in this lab.

<h1>Preparation</h1>

<ul>

 <li>Download the mysql java .jar file from <a href="https://dev.mysql.com/downloads/connector/j/">https://dev.mysql.com/downloads/connector/j/</a> If in doubt, use the “platform independent” file.</li>

 <li>Download and install the MySQLWorkbench from <a href="https://dev.mysql.com/downloads/workbench/">https://dev.mysql.com/downloads/workbench/ </a>By some reports, the install for Windows may ask you for pre-requisite modules and/or may not run at the start. I hear that this can happen when trying to install the full MySQL suite. Instead, only look to install the workbench element of the larger download.</li>

</ul>

<h1>Resources</h1>

<ul>

 <li>Database diagram at <a href="http://www.zentut.com/sql-tutorial/sql-sample-database/">http://www.zentut.com/sql-tutorial/sql-sample-database/</a> for the data in this lab</li>

 <li>The csci3901 database available at cs.dal.ca. You will need to be on the Dal network to access this database, so you will want to use the Dal Virtual Private Network (VPN).</li>

</ul>

Alternatively, you can download and install your own copy of the mysql database onto your local computer and install your own copy of the database, with data retrieved from the same web page as the database diagram.

<h1>Procedure</h1>

<h2>Set-up</h2>

<ol>

 <li>Create a new project in your IDE.</li>

 <li>Link the jar file from the preparation section as an external library to your IDE project.</li>

 <li>Download and install the Dal VPN client (from <a href="https://wireless.dal.ca/vpnsoftware.php">https://wireless.dal.ca/vpnsoftware.php)</a> When asked for a server to connect to, use its.dal.ca as the target server.</li>

 <li>Configure MySQLWorkbench to get a TCP/IP connection over SSH via cs.dal.ca to db.cs.dal.ca.</li>

</ol>

<h2>Lab steps</h2>

<h3>Part 1 – Using MySQLWorkbench</h3>

<ol>

 <li>Open the MySQLWorkbench application. Execute the command use csci3901; in the workbench to access the class database.</li>

 <li>Use the command show tables; command to identify and report which tables are in the database.</li>

 <li>Report the outcome of the following SQL statements:

  <ul>

   <li>Select * from orders where OrderID = 10260;</li>

   <li>Select * from orderdetails where OrderID = 10260;</li>

   <li>Select ProductID, ProductName, CategoryID from products where ProductID = 41 or ProductID = 57;</li>

   <li>Select customers.CustomerID, CompanyName from orders, customers where OrderID = 10260 and orders.customerID = customers.CustomerID;</li>

  </ul></li>

</ol>

<h3>Part 2 – Java connection</h3>

<ol>

 <li>Create a program that will ask for an order number from the user and will show the order information on the screen as an invoice. The invoice should include:</li>

</ol>

<ul>

 <li>The order date and order number</li>

 <li>The customer name and address</li>

 <li>The product codes and quantities ordered</li>

 <li>The total cost of the order</li>

</ul>

<strong>Questions</strong>

<ol>

 <li>How could you test the correctness of your program from Part 2?</li>

</ol>