
Personal Expense Tracker
Writeup and overview

	A Python-based command-line application for personal finance management that helps users:
- Track expenses across categories
- Real-time budget vs expense comparisons
- Set and monitor monthly budgets
- Analyze spending patterns
- Maintain financial records in .CSV files

An interactive menu:  main() and print_menu()
(Keep the program running until the user exits)
There are 5 options for user retailed to 5 main functions:

1. Add new expenses
	 `add_expenses()` | Handles expense entry with validation |
		-  Add expenses
		- Data entry verification
		- Date validation (YYYY-MM-DD format)
		- Category restriction (Food/Closing/Car/Misc)
2. See my expenses
	`view_expenses()` | Displays sorted by date expense records |
		- Sort the list of expenses by date YYYY-MM-DD
		- Present the data to the user in a tabular format
3. Track the budget
	`track_budget()` | Manages budget creation/analysis |
		- Set monthly budgets
		- Matches expense dates to budget periods
		- Automatically calculates monthly totals
		- Visual alerts for budget overruns
		- Historical budget analysis
4. Save expenses to the file
	`save_to_file()` | Universal CSV saving function |
  		 - `all_expenses_01.csv` (expense records)
   		 - `budget_editable_2.csv` (budget plans)
		 - Automatic saving of data
5. Save the expenses and exit
	`save_and_exit()` | Saving function and exit |
		  - Final saving and exit

Six additional functions help execute code:

def read_from_file() | Universal CSV reading function, helps extract data from .csv |

def in_category () | Validates if an expense category is included in a set  |

def if_empty() | Makes sure that the description of expenses is not empty |

def print_budget() | Print budget in tabular format |

def str_to_float() | Universal function to convert numbers from string format to float |

def is_valid_date() | Validates date format |


global veriaebles:

category_list = ['Food', 'Closing', 'Car', 'Misc']  

		- list of restrictions by expenses categories
csv_budget_file = 'budget_editable_2.csv' 

		- budget amounts and total monthly expenses analisys
csv_expenses_file = 'all_expenses_01.csv'

		- data of all expenses
all_expenses = []

		- the list helps manage expenses 
budget_list = []

		- the list helps manage budget 
