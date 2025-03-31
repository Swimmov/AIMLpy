
### Course-End Project: Task Manager with User Authentication
## Writeup and overview

### A Python-based CLI (command-line interface) task manager:

### Problem Statement:
In today’s world, individuals often need to keep track of various tasks in a structured
way. You are tasked with building a Task Manager that allows users to manage their
tasks. The system should include user authentication, meaning each user has to log
in with a username and password. Once logged in, users can create, view, update,
and delete their tasks. Each user’s tasks should be stored separately, and only the
authenticated user can access their tasks.
Objectives:
1. Design and implement a user authentication system (login and registration)
2. Create a task management system that allows users to:
a. Add, view, mark as completed, and delete tasks
3. Use file handling to store user credentials and tasks persistently
4. Create an interactive menu-driven interface to manage tasksSteps to Perform:
1. User Authentication:
• Registration:
o Create a function to prompt the user to enter a username and
password
o Ensure that the username is unique, and hash the password for
security before storing it in a file
•
Login:
o Create a function to prompt the user for their username and
password, validate the credentials by comparing them with the stored
data, and grant access to the task manager upon successful login
2. Add a Task:
•
Create a function that prompts the user for a task description. Assign a
unique task ID and set the status to Pending
•
Store the task in a file, and confirm that the task was added
3. View Tasks:
•Create a function to retrieve and display all tasks for the logged-in user
•Each task should show the task ID, description, and status (Pending or
Completed)
4. Mark a Task as Completed:
•
Create a function that allows the user to select a task by its ID and update
its status to Completed
5. Delete a Task:
•
Create a function that allows the user to select a task by its ID and delete
it from their task list6. Create an Interactive Menu:
• Build a menu that allows users to choose between:
oAdd a Task
oView Tasks
oMark a Task as Completed
oDelete a Task
oLogout
For each option, call the corresponding function, and loop back to the menu until
the user logs out.

##################################################################################

final code:

## Secure Password Handling

Uses getpass to hide password input.

Properly hashes passwords with PBKDF2 and salts.

## Task Management

Dynamic task numbering per user.

Global unique task IDs.

Clean file I/O with read_read_file() and write_file().

## Error Handling

Catches malformed lines in files.

Validates task numbers during deletion/completion.

## User Experience

Clear menus and prompts.

Auto-login after registration.

## Areas for Improvement
	
 ### Efficiency:
* File Writing: Avoid overwriting the entire file for single-task updates (use a database for scalability).

### User Feedback:
* Success Messages: Add confirmations for task additions/completions/deletions.

### Security:
* Password Complexity: Enforce minimum password length/complexity during registration.

### Use a Database: SQLite or TinyDB for efficient querying.
