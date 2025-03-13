# Expense Tracker 💰

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A simple command-line expense tracking application built in Python. Perfect for developers looking to manage personal finances or learn basic financial tracking concepts.

## 📜 About
The Expense Tracker is a lightweight Python application designed to help users record, categorize, and analyze their daily expenses through a simple command-line interface. It provides essential functionality for adding expenses, viewing transaction history, calculating total spending, and filtering expenses by category.

## ✨ Features
- Add new expenses with amount and category
- List all recorded expenses with details
- Calculate total spending across all categories
- Filter expenses by specific category
- Simple and intuitive command-line interface

## 🚀 Quick Start

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/fahadelahikhan/Expense-Tracker.git
   cd Expense-Tracker
   ```

2. Run the application:
   ```bash
   python main.py
   ```

### Basic Usage
```python
# Import the main functions
from expense_tracker import add_expense, print_expenses, total_expenses, filter_expenses_by_category

expenses = []

# Add an expense
add_expense(expenses, 45.99, 'Groceries')

# List all expenses
print_expenses(expenses)

# Calculate total spending
total = total_expenses(expenses)
print(f'Total Expenses: ${total:.2f}')

# Filter expenses by category
groceries = list(filter_expenses_by_category(expenses, 'Groceries'))
print_expenses(groceries)
```

### Example Usage
```python
# Adding multiple expenses
add_expense(expenses, 15.75, 'Transportation')
add_expense(expenses, 7.99, 'Entertainment')
add_expense(expenses, 25.50, 'Groceries')

# Filtering expenses
transportation_expenses = list(filter_expenses_by_category(expenses, 'Transportation'))
print_expenses(transportation_expenses)  # Output: Amount: 15.75, Category: Transportation

# Total calculation
total = total_expenses(expenses)  # Output: 49.24
```

## 📖 How It Works
The Expense Tracker uses a simple list of dictionaries to store expense records. Each expense entry contains:
- `amount`: A floating-point number representing the expense amount
- `category`: A string describing the expense category

The application provides functions to:
- Add new expenses to the list
- Print all expenses in a readable format
- Calculate the total of all expense amounts
- Filter expenses by a specific category

## ⚖️ License
Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

> **Note**: This application is intended for personal use and educational purposes. For production financial tracking, consider using established accounting software with robust security and backup features.
