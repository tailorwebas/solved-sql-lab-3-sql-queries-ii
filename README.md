Download Link: https://assignmentchef.com/product/solved-sql-lab-3-sql-queries-ii
<br>
The purpose of this lab is to gain SQL experience using Oracle.   You will get practice creating SQL queries from an established database given to you to load into your own schema in Oracle.

<h1>WHAT YOU WILL NEED FOR THIS ASSIGNMENT</h1>

<ul>

 <li><strong>  </strong>Click <a href="http://codd.franklin.edu/~crawforl/.c281/.ass/CommonLabExpectations.pdf"><strong>HERE</strong></a> to read and understand the Common Lab Expectations you will need to follow for each SQL Lab assignment in this class.</li>

 <li>Click <a href="http://download.franklin.edu/COMP/281/VirtualDesktop.pdf"><strong>HERE</strong></a> for details on how to connect to the virtual desktop for this class and <a href="http://download.franklin.edu/COMP/281/SQLDeveloper.pdf"><strong>HERE</strong></a> for how to run the Oracle SQL Developer software on this platform.</li>

 <li>Click <a href="http://codd.franklin.edu/~crawforl/.c281/.ass/SQLdevVideo.mp4"><strong>HERE</strong></a> for a short video on using SQL Developer. NOTE:  The video mentions downloading SQL Developer to your PC.  You can no longer do this because of possible security vulnerabilities.  You now have to access SQL Developer from the virtual desktop exclusively.  Please ignore all references to your PC and downloading SQL Developer to it in the video.</li>

 <li>Click <a href="https://download.oracle.com/oll/tutorials/SQLDeveloper/index.htm"><strong>HERE</strong></a> for some sample tutorials on SQL Developer.</li>

 <li>Click <a href="http://my.safaribooksonline.com/9781847196262"><strong>HERE</strong></a> for access to the SQL Developer 2.1 guide book on Safari (use your myFranklin login and password to gain access).</li>

 <li>You will also find additional SQL examples and solutions from the back of chapter 7 by clicking <a href="http://codd.franklin.edu/~crawforl/.c281/.ass/Ch07examples.docx"><strong>HERE</strong></a> or <a href="http://codd.franklin.edu/~crawforl/.c281/.ass/Ch07case.docx"><strong>HERE</strong></a><a href="http://codd.franklin.edu/~crawforl/.c281/.ass/Ch07case.docx">.</a></li>

</ul>

<strong>ACTION ITEMS</strong>

<strong> </strong>Initial Setup – Read &amp; Complete First

<strong> </strong>The diagram below shows a relational schema made up of 6 tables with all primary keys underlined. Please make note of foreign keys (<em>most of them carry the same names as the corresponding primary keys they reference</em>): <em>CUS_CODE </em>in INVOICE, <em>INV_NUMBER </em>&amp; <em>P_CODE </em>in LINE, and <em>V_CODE </em>in PRODUCT. The only exception to the naming convention is the <em>EMP_MGR </em>foreign key in <em>EMPLOYEE </em>which references the <em>EMPLOYEE </em>table in a recursive relationship.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/03/946.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2018/03/946.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>




<ul>

 <li>Click <a href="http://codd.franklin.edu/~crawforl/.c281/.ass/myCompany.SQL">HERE</a> to download an SQL script file called <strong><em>sql</em></strong> to your PC or the virtual desktop. This file contains the SQL commands needed to create the tables above and add data to them in Oracle using SQL Developer.</li>

 <li>Transfer the file and/or its contents to the virtual desktop and execute it’s content two (2) times in a row in SQL Developer to see that all errors go away with the second running of the file.</li>

 <li>Go through the file and make sure you understand every line of code in it before you proceed. You will not need to execute this file again for this lab.  The tables and data are stored permanently in your database schema in Oracle.</li>

</ul>




<strong>Part 1: Write SQL Queries into <em>lab3.sql</em> script file</strong>




<h1>Script File</h1>




Create a new <strong><em>lab3.sql</em></strong> script file using Notepad or Notepad++ on your VD.  The first two commands in this file should be (you should only have these in your <strong><em>lab3.sql</em></strong> file once):




<em>set echo on; </em>

<em>set serveroutput on;</em>




Follow the format given to you in the <strong><em>myCompany.sql</em></strong> file above.  Each SQL query should have a comment before it stating the question number in it.  For example, let’s say the first question asks you to display all records in the line table and the second question asks you to display all records in the vendor table.  The content you should add to the <strong>lab3.sql</strong> file is as follows:




<em>/* 1 */ </em>

<em>select * from line; </em>

<em> </em>

<em>/* 2 */ </em>

<em>select * from vendor;</em>




You will use this file to insert your comments and SQL query commands for the 15 questions detailed below.  NOTE: You should test your commands first in SQL Developer before placing them into your <strong><em>lab3.sql</em></strong> file to make sure they give you the output you desire.




<ol>

 <li>S. Your queries should be generic enough to return proper results EVEN if the data inside the database tables changes. For example, if I ask you to display the products provided by vendors located in TN, you can’t manually extract the V_CODE for vendors in TN and use the results to search the PRODUCT table for the corresponding products; instead, your query should be written using a join between the two tables with a WHERE clause for TN or something similar.</li>

</ol>




<h1>Questions (0-30 points)</h1>

<strong><em> </em></strong>

<ol>

 <li>Display all product information for products that contain the string ‘<em>saw</em>’ in their description.</li>

</ol>




<ol start="2">

 <li>Display all product information for products currently selling for less than <em>$20.00 <strong>and </strong></em>which have more than 100 units in stock (recorded in attribute <em>P_QOH </em>or quantity on hand).</li>

</ol>




<ol start="3">

 <li>Display all product information for products currently selling for less than <em>$20.00 <strong>or </strong></em>which have more than 100 units in stock (recorded in attribute <em>P_QOH </em>or quantity on hand).</li>

</ol>




<ol start="4">

 <li>Display the product code, description and price for products provided by vendor <em>21344</em>.</li>

</ol>




<ol start="5">

 <li>Display the product code, description, price and price <strong><em>after </em></strong>discount (a computed column that uses the <em>P_PRICE </em>and <em>P_DISCOUNT (a percent discount) </em>— name the computed column <strong><em>NewPrice</em></strong>) for products for which no vendor is specified in table <em>PRODUCT</em>.</li>

</ol>




<ol start="6">

 <li>Display the product code, product description and vendor name for products provided by vendors located in the state of TN.</li>

</ol>




<ol start="7">

 <li>Display the full names of employees who manage other employees, ordered by last name.</li>

</ol>




<ol start="8">

 <li>Display the count of <strong><em>distinct </em></strong>products ordered so far by customers (i.e. exist in table <em>LINE</em>).</li>

</ol>




<ol start="9">

 <li>For every manager, display the manager employee code along with the total number of employees s/he manages.</li>

</ol>




<ol start="10">

 <li>Display the product description, the full customer name and the customer balance for products ordered by customers having a customer balance between $100.00 and $500.00 (inclusive of both). Order by customer last name, then first name, then initial.</li>

</ol>




<ol start="11">

 <li>For every invoice, display the invoice number, <strong><em>invoice date </em></strong>and the total dollar amount for all products purchased in the invoice, ordered by invoice number in descending order and then by invoice date in ascending order.</li>

</ol>




<ol start="12">

 <li>Create an SQL view called <em>VENDOR_PRODUCTS_TOTALS </em>that shows the vendor name, vendor code and the total number of products provided by the vendor but only for vendors</li>

</ol>

providing two or more products. When done, issue a <em>select * from </em>

<em>VENDOR_PRODUCTS_TOTALS </em>statement to display the contents of view

<em>VENDOR_PRODUCTS_TOTALS</em>.   You should use the <em>CREATE OR REPLACE VIEW VENDOR_PRODUCTS_TOTALS AS SELECT</em> … command for this question.




<ol start="13">

 <li>Execute a <em>select * from product; </em> Create and run an SQL update statement which changes the <em>P_DISCOUNT </em>to 0.03 percent for all products that currently have a discount of 0. Issue another <em>select * from product; </em>statement after the update. Do a rollback.</li>

</ol>




<ol start="14">

 <li>Execute a <em>select * from product; </em> Create an SQL update statement which doubles the <em>P_DISCOUNT </em>for all products provided by vendors in TN or FL. Issue another <em>select * from product; </em>statement after the update. Do a rollback.</li>

</ol>




<ol start="15">

 <li>Execute a <em>select * from LINE; </em> Create an SQL delete statement to delete invoice lines that include 2 or more units of product code ‘<em>23109-HB</em>’. Issue another <em>select * from LINE; </em>statement after the delete. Do a rollback.</li>

</ol>




<h2>Part 2: Execute Your <em>lab3.sql</em> script File and Save Results in a Word Document called <em>lab3.docx</em></h2>

<strong> </strong>

From within SQL Developer, execute the content of your <strong><em>lab3.sql</em></strong> script file (which should now include all commands for the 15 questions above.  Copy and paste the output into a Word document called <strong><em>lab3.docx</em></strong> with your name, date, assignment number, and class in the header.  The output should include a comment with each question clearly marked, the SQL command, and its corresponding output immediately after.  For example, the content of my Word document with the commands listed above would be the following (I changed the font size to 8 and the font type to Courier New to get the columns to line up):













&gt; set serveroutput on

&gt; /* 1 */

&gt; select * from line

INV_NUMBER LINE_NUMBER P_CODE     LINE_UNITS LINE_PRICE

———- ———– ———- ———- ———-

1001           1 13-Q2/P2            1      14.99

<ul>

 <li>2 23109-HB 1       95</li>

 <li>1 54778-2T 2       99</li>

 <li>1 2238/QPD 1      95</li>

</ul>

1003           2 1546-QQ2            1      39.95

<ul>

 <li>3 13-Q2/P2 5      99</li>

 <li>1 54778-2T 3       99</li>

 <li>2 23109-HB 2       95</li>

 <li>1 PVC23DRT 12       87</li>

 <li>1 SM-18277 3       99</li>

</ul>

1006           2 2232/QTY            1     109.92

1006           3 23109-HB            1       9.95

<ul>

 <li>4 89-WRE-Q 1     99</li>

 <li>1 13-Q2/P2 2      99</li>

 <li>2 54778-2T 1       99</li>

 <li>1 PVC23DRT 5       87</li>

</ul>

1008           2 WR3/TT3             3     119.95

1008           3 23109-HB            1       9.95




18 rows selected




&gt; /* 2 */

&gt; select * from vendor

V_CODE V_NAME                              V_CONTACT       V_AREACODE V_PHONE  V_STATE V_ORDER

———- ———————————– ————— ———- ——– ——- ——

<ul>

 <li>Bryson, Inc. Smithson        615        223-3234 TN      Y</li>

 <li>SuperLoo, Inc.       Flushing        904        215-8995 FL      N</li>

</ul>

21231 D&amp;E Supply                          Singh           615        228-3245 TN      Y

21344 Gomez Bros.                         Ortega          615        889-2546 KY      N

22567 Dome Supply                         Smith           901        678-1419 GA      N

23119 Randsets Ltd.                       Anderson        901        678-3998 GA      Y

24004 Brackman Bros.                      Browning        615        228-1410 TN      N

24288 ORDVA, Inc.                         Hakford         615        898-1234 TN      Y

25443 B&amp;K, Inc.                           Smith           904        227-0093 FL      N

25501 Damal Supplies                      Smythe          615        890-3529 TN      N             25595 Rubicon Systems                     Orton           904        456-0092 FL      Y




11 rows selected