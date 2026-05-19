# Python-project-week-2
This Python program is an Expense Tracker application designed to help users manage and monitor their daily expenses. It allows users to add expenses, view all records, calculate total expenses, and identify the highest expense


Code:
print("")
print("      WELCOME TO EXPENSE TRACKER")
print("")

# Store all expenses
expenses = []

# Infinite loop
while True:
    print("\nChoose an Option:")
    print("1. Add Expense")
    print("2. View All Expenses")
    print("3. Show Total Expense")
    print("4. Show Highest Expense")
    print("5. Exit")

    choice = input("Enter your choice (1-5): ")

    # Add Expense
    if choice == '1':
        try:
            amount = float(input("Enter expense amount: ₹"))
            expenses.append(amount)
            print("Expense Added Successfully!")
        except:
            print("Invalid Amount! Please enter numbers only.")

    # View Expenses
    elif choice == '2':
        if len(expenses) == 0:
            print("No expenses added yet.")
        else:
            print("\n------ Expense List ------")
            for i, expense in enumerate(expenses, start=1):
                print(f"{i}. ₹{expense}")

    # Total Expense
    elif choice == '3':
        total = sum(expenses)
        print(f"\nTotal Expense: ₹{total}")

    # Highest Expense
    elif choice == '4':
        if len(expenses) == 0:
            print("No expenses available.")
        else:
            highest = max(expenses)
            print(f"Highest Expense: ₹{highest}")

    # Exit
    elif choice == '5':
        print("\nThank You for Using Expense Tracker!")
        print("Project Completed Successfully.")
        break

    # Invalid Choice
    else:
        print("Invalid Choice! Please select between 1 to 5.")
