# Java-with-Junit
Simple bank app via Java with Junit 

****************************
* Simple bank app via Java *
****************************

i. Domain design
ii. Assumptions
iii. Test cases and edge considerations
iv. How to run code/tests
v. Improvements

***
***
***

I. The bank domain was designed by identifying the class, attributes and methods.

Class
=====
BankAccount

Object/Instance Attributes
==========================
customerAccountNo
customerBalance
customerName

Class Attribute
=================
bankBalance 

Methods
=======
deposit()
withdraw()

The class, attributes and methods were translated into code by the use of the Java IDE named Eclipse. Note that the attribute 'bankBalance' was declared as 'private static' so that it will be accessible anywhere in the BankAccount class. The rest of the attributes were declared as 'private' and only accessible within the object/instance itself. Empty constructor was created, as well as constructor with parameters. Getters and setters were also created. The toString method was also created. Then the two methods were created, deposit method and withdraw method. In the deposit method, the customer can deposit any amount, and it will be added to the customer balance. Also, this amount will also be added to the bank balance. I then added a code that will not allow a negative deposit.  In the withdraw, the customer can withdraw any amount not exceeding their current customer balance, and it will be deducted to the customer balance. Also, this amount will also be deducted to the bank balance. I then added a code that will not allow a negative withdrawal.

***
***
***

II. The BankAccount class was created with the following assumptions:
1. The customer have only 3 attributes, account number, balance and name. Account number have a data type of string. Name does not consider the middle name and/or last name.
2. The bank have only 1 attribute which is bank balance.
3. The empty constructor was created with the following default values:
customerAccountNo = "C9999"
customerBalance = 0.0
customerName = "JohnDoe"
bankBalance = 0.0
4. An 'IllegalArgumentException' was thrown as well as a display message for negative and insufficient fund transactions.
5. There were no amount limit set when depositing or withdrawing.

***
***
***

III. Test cases and edge considerations
There were 10 test cases created. Test cases for the constructors, setters and getters were not created. I concentrated my test cases with the two methods, deposit() and withdraw() as well as using the getter for customer balance as well as getter for bank balance, and transaction by multiple customers.
Test Cases 1,3,6,and 7: Valid deposit and valid withdraw transactions
Test Cases 2 and 4: Invalid deposit and invalid withdraw transactions because of negative amount
Test Cases 5: Invalid withdraw transaction because of insufficient fund
Test Cases 8: Valid customer balance using sequential deposit and withdraw transactions by 1 customer
Test Cases 9: Valid bank balance using sequential transactions by 1 customer
Test Cases 10: Valid customer balances using deposit and withdraw transactions by multiple customers

***
***
***

IV. How to run the code and tests
Pre-requisite: You need to have a Java project file 
1. Launch Eclipse IDE and select ‘Import’ from ‘File’ menu.
2. In the displayed ‘Import’ dialog, expand the ‘General’ folder. Select ‘Archive’. In the 'From Archive file:', hit browse and navigate to the location of the zipped file named 'src.zip'. In the 'Into folder:', hit browse and navigate to the location of the Java project directory And finally click ‘Finish’.
3. Select ‘Show View’ from ‘Window’ menu and hit 'Project Explorer'. In the 'Project Explorer', select your Java project, expand it to see 'src' folder, expand it furthermore and you will see the 'banking' package and under it are the 3 files: BankAccount.java, BankAccountTest.java and readme.txt
4. BankAccount.java is the source code for the BankAccount class. Double click it to see the source code in another window. Ensure that ‘Build Automatically’ is ticked from ‘Project’ menu to compile the source code.
5. BankAccountTest.java are the test unit cases for the BankAccount class. Double click it to see the source code in another window. Select ‘Run’ from ‘Run’ menu to execute the test unit cases. Alternatively, you can hit the Run button, green circle with the right triangle icon. Or, you can use shortcut key CTRL + F11. Console Window will open up where the displays in the code will be seen. The Junit window will also open up and it will show the number of runs, errors and failures. The expected run is 10/10, 0 errors and 0 failures.     
 
***
***
***

V. Improvements
1. Customer attributes can be enhanced and improved by adding customer information such as email, address, full name, mobile number and other important information about the customer,
2. Bank attributes can be enhanced and improved by adding bank information like bank name, branch name, branch number, telephone number and other important bank information.
3. The 'IllegalArgumentException' for the negative deposit and withdraw transactions can be replaced with a more appropriate exception.
4. The 'IllegalArgumentException' for the insufficient fund transaction can be replaced with the 'InsufficientFundsException'
5. The test cases for the bank balance (Test Case # 9) can be separated because the program uses a static variable named 'bankBalance'. A static variable will retain its value between unit tests. If unit test case # 1 sets it, then unit test case # 2 could pick up that value,  which makes for an awful and confusing unit test.
6. The test cases can be created in a parameterized way.

