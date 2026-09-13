# prog
name = input("Enter your name: ")
balance = float(input("Enter your start balance: "))
expenses = {}
while True:
    print("\n1. Add Expense")
    print("2. View Expenses")
    print("3. View Balance")
    print("4. Exit")
    choice = input("\choose an option: ")
    if choice == "1":
        description = input("Enter expense description: ")
        amount = float(input("Enter expense amount: "))
        expenses[description] = amount
        balance -= amount
        print(f"Expense added {description} ' added succesully.")
    elif choice == "2":
        if len(expenses) == 0:
            print("No expenses recorded.")
        else:
            print("\n expensess =====")
            for expense in expenses:
                print(f"{expense}:" f"${expenses[expense]:.2f}")
    elif choice == "3":
        total_expenses = 0
        for expense in expenses:
            total_expenses += expenses[amount]
            if len(expenses) > 0:
                average_expense = total_expenses / len(expenses)
                highest_expense = max(expenses.values())
                lowest_expense = min(expenses["amount"]
                                     for expense in expenses())
            else:
                average_expense = 0
                highest_expense = 0
                lowest_expense = 0
                print("\n ===== SUMMARY")
                print(f"f Name:{name}")
                print(f"Starting balance: $ {balance + total_expenses}")
                print(f"Total expenses: ${total_expenses:}")
                print(f"Average expense: ${average_expense:.}")
                print(f"Highest expense: ${highest_expense:.}")
                print(f"Lowest expense: ${lowest_expense:.}")
                print(f"remaining balance: ${balance:.}")
    elif choice == "4":
        print(f"\n Goodbye , {name}!")
        break
    else:
        print("Invalid choice. Please try again.")
ramming-learning
my programming learning journery with practical exercises and projects.
