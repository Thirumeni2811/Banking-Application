# Banking-Application

1.Banking app : 

   Overview
      The BankingApp project is a console-based banking system application that allows multiple users to manage their bank accounts. It provides functionalities to create new accounts, display account details, deposit and withdraw money, and search for accounts by account number. This project demonstrates the fundamental concepts of object-oriented programming in Java, including encapsulation, classes, and methods. This code allows for the creation of multiple customers.

Features

   1. Account Creation:
      Users can open new accounts by providing details such as account number, account type, name, and initial balance.
      
   2. Display Account Details:
      The application can display the details of all accounts, including the account holder's name, account number, account type, and balance.
      
   3. Deposit Money:
      Users can deposit money into their accounts by specifying the account number and the amount to be deposited.
      
   4. Withdraw Money:
      Users can withdraw money from their accounts by specifying the account number and the amount to be withdrawn. The application checks if the balance is sufficient before allowing the withdrawal.
      
   5. Search Account:
      Users can search for an account by its account number. If the account exists, its details are displayed.


Implementation Details

   1. BankDetails Class:

      a) Attributes:
         accno (String): Stores the account number.
         name (String): Stores the account holder's name.
         acc_type (String): Stores the type of the account (e.g., Savings, Checking).
         balance (long): Stores the current balance of the account.

      b) Methods:
         openAccount(): Prompts the user to enter account details and initializes the account.
         showAccount(): Displays the account details.
         deposit(): Prompts the user to enter an amount to deposit and updates the balance.
         withdrawal(): Prompts the user to enter an amount to withdraw and updates the balance if sufficient funds are available.
         search(String ac_no): Searches for an account by its account number and displays the details if found.

      2. BankingApp Class:
         
         a) Attributes:      
            C (BankDetails[]): An array to store multiple BankDetails objects, representing multiple user accounts.
         
         b) Methods:       
            main(String[] args): The main method that drives the application. It prompts the user to input the number of customers, initializes the accounts, and provides a menu for the user to interact with the banking system.


User Interaction

   1. Opening New Accounts:
      The user specifies the number of accounts to create. For each account, the user enters the account number, account type, name, and initial balance.

   2. Banking Menu:   
      The application displays a menu with options to display account details, search for an account, deposit money, withdraw money, or exit the application. The user selects an option by entering the corresponding number.
   
   3. Depositing and Withdrawing Money:
      The user enters the account number and the amount to deposit or withdraw. The application validates the account number and updates the balance accordingly.
   
   4. Searching for Accounts:  
      The user enters the account number to search for. The application displays the account details if the account is found, otherwise, it notifies the user that the account does not exist.


2.Bank Application : 
     
   Overview 
      The BankingApplication is a simple command-line based banking system designed for single-user interactions. It allows a user to perform basic banking operations such as checking balance, depositing money, withdrawing money, and viewing previous transactions. This code allows for the creation of only one customer.
   
Features

   1. Account Initialization
   
      When the program starts (main method in BankingApplication class), it initializes a BankAccount object with a customer name and ID.
      The user's name and ID are prompted and stored.

   2. Operations Supported
   
      Check Balance (A): Displays the current balance of the account.
      Deposit (B): Allows the user to deposit a specified amount into their account.
      Withdraw (C): Allows the user to withdraw a specified amount from their account, ensuring sufficient balance.
      Previous Transaction (D): Shows the details of the last transaction (whether deposit or withdrawal).
      Exit (E): Ends the banking session.
   
   3. Transaction Handling
   
      Each transaction updates the account balance (balance) and records the amount of the transaction (previousTransaction).
   
   
Implementation Details
   
   1. BankAccount Class
   
      a) Attributes:
         balance (int): Stores the current balance of the account.
         previousTransaction (int): Stores the amount of the last transaction (positive for deposit, negative for withdrawal).
         customerName (String): Stores the customer's name.
         customerId (String): Stores the customer's ID.
      b) Constructor:
         BankAccount(String cname, String cid): Initializes the customerName and customerId attributes.
      c) Methods:
         deposit(int amount): Adds the specified amount to the balance.
         withdraw(int amount): Subtracts the specified amount from the balance, if sufficient funds are available.
         getPreviousTransaction(): Prints the details of the last transaction (previousTransaction).
         showMenu(): Displays a menu for the user to interact with the banking system. It handles user input, processes operations based on the selected option, and continues until the user chooses to exit.
      
      2. BankingApplication Class
      
         Main Method:
            Initializes a BankAccount object (obj1) with a predefined customer name ("ABC") and customer ID ("BA0012").
            Invokes the showMenu() method on obj1 to start the banking operations for the user.

         
   User Interaction
      1. The program interacts with the user through a console interface.
      2. Upon startup, the user is prompted to enter their name and ID.
      3. They are presented with a menu of options (A to E), and they select an option by entering the corresponding letter.
      4. Each operation updates the account state and provides feedback to the user about the action taken.

      
   Summary
      The BankingApplication project demonstrates foundational concepts in Java programming, including class definition, object instantiation, method invocation, user input handling, conditional statements (switch-case), and loop control (do-while). It provides a basic framework for extending functionality such as adding more complex banking operations, implementing security features, or integrating with a persistent data storage system.
   
This project serves as a good example for understanding object-oriented principles in Java and can be expanded upon for more comprehensive banking applications or educational purposes.
