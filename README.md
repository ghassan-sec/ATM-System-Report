customer_name = input("Enter Your Customer Name : ")
balance = 1000



print("1.Deposit")
print("2.Withdraw")



choice = int(input("Choice Operation : "))



if choice == 1:
    amount = float(input("Enter Deposit Amount : "))
    balance = balance + amount
    opreation = "Deposit"



elif choice == 2:
    amount = float(input("Enter Withdraw Amount : "))



if amount <= balance:
    balance = balance - amount
    opreation = "Withdraw"



else:
    print("Insufficient Balance")
    opreation = "Failed Withdraw" 



with open("atm.txt", "a") as a:
    a.write("\n" + customer_name + " | " + opreation + " | " + str(balance))



print("\n-----REPORT-----")
print("Customer:", customer_name)
print("Operation:", opreation)
print("Balance:", balance)

ATM System Report
Introduction
The ATM System is a simple Python application that simulates basic banking operations. It allows customers to perform deposit and withdrawal transactions, updates their account balance, stores transaction records in a text file, and generates a transaction report.

Project Objectives
To understand user input handling in Python.
To perform basic banking calculations.
To apply conditional statements for decision-making.
To use file handling for storing transaction history.
To create and display transaction reports.
System Description
The program begins by displaying a welcome message for the ATM System. It then asks the user to enter their customer name. The account starts with an initial balance of 1000.

The customer can choose one of the following operations:

Deposit
Withdraw
Deposit Operation
When the customer selects the deposit option, they enter the amount they wish to deposit. The program adds the amount to the current balance and updates the account information.

Withdraw Operation
When the customer selects the withdrawal option, they enter the amount they wish to withdraw. The program checks whether the account balance is sufficient:

If the balance is sufficient, the amount is deducted from the account.
If the balance is insufficient, the withdrawal request is rejected, and an error message is displayed.
After processing the transaction, the program saves the customer's name, transaction type, and current balance in a text file called atm.txt.

Finally, the program displays a report showing the transaction details and the updated balance.

Inputs
Customer Name
Transaction Type (Deposit or Withdraw)
Transaction Amount
Outputs
Updated Account Balance
Transaction Status
Transaction Report
Saved Record in atm.txt
