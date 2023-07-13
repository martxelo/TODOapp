# Pure Python TODO app

You can keep track of different tasks in a simple TODO list.

## Usage

Clone the repository, give execution permission and create a symlink in your `/usr/bin/local` folder:

```bash
user@host:~$ git clone git@github.com:martxelo/TODOapp.git
user@host:~$ chmod +x TODOapp/todo
user@host:~$ ln -s /home/user/TODOapp/todo /usr/bin/local/todo
```

Now you can start adding tasks, listing or removing them:

```bash
user@host:~$ todo add Correct docstrings
Added task to list

user@host:~$ todo
ID   Date        Task
1    2023-07-12  Correct docstrings

user@host:~$ todo add Create GitHub repo
Added task to list

user@host:~$ todo ls
ID   Date        Task
1    2023-07-12  Correct docstrings
2    2023-07-12  Create GitHub repo

user@host:~$ todo rem 2
Removed task from list

user@host:~$ todo
ID   Date        Task
1    2023-07-12  Correct docstrings
```

## Commands

There are only three commands:

- `todo ls` or `todo`: print a list with all tasks.
- `todo add the task`: add a new task to the list.
- `todo rem task_id`: remove the task with its ID.

## Database

A Sqlite database is created in the user folder.