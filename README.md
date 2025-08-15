# sqLWB (SQLight Weight Baby)

This project is a light-weight SQLite-ish database written in C. It is a command-line interface (CLI) based database system that persists data to a file.

## Features

*   **Persistent Storage**: Data is saved to a file and can be retrieved later.
*   **B-Tree Implementation**: Uses a B-Tree to store data, which allows for efficient insertion and retrieval.
*   **Basic SQL Operations**: Supports `insert` and `select` statements.
*   **Meta-commands**: Provides meta-commands like `.exit`, `.btree`, and `.constants` for interacting with the database.
*   **Simple REPL**: A simple Read-Eval-Print Loop for executing commands.

## How to Build and Run

### Prerequisites

*   A C compiler (like `gcc` or `clang`)
*   Ruby and Bundler for running the tests

### Building the Database

You can compile the C code using `gcc`:

```bash
gcc -o main main.c
```

### Running the Database

To start the database CLI, provide a filename as an argument:

```bash
./main mydatabase.db
```

If the file does not exist, it will be created.

## Usage

Once the CLI is running, you can enter SQL-like commands or meta-commands.

### SQL Commands

*   **Insert a record:**

    ```
    db > insert <id> <username> <email>
    ```

    Example:

    ```
    db > insert 1 jdoe john.doe@example.com
    ```

*   **Select all records:**

    ```
    db > select
    ```

### Meta-commands

*   **`.exit`**: Exit the CLI.
*   **`.btree`**: Display the structure of the B-Tree.
*   **`.constants`**: Show database constants like `ROW_SIZE` and `PAGE_SIZE`.

## How to Run Tests

The tests are written in Ruby using RSpec. First, install the dependencies:

```bash
bundle install
```

Then, run the tests:

```bash
bundle exec rspec
```
