[![CI](https://github.com/jessc0202/Sizhe_Chen_mini_Project_7/actions/workflows/rust.yml/badge.svg)](https://github.com/jessc0202/Sizhe_Chen_mini_Project_7/actions/workflows/rust.yml)

# **Sizhe Chen IDS706 Project 7 – Rust Command-Line Tool**

## **Project Purpose**

This project demonstrates the creation of a simple command-line utility using the Rust programming language. The utility supports basic arithmetic operations, including multiplication, addition followed by multiplication, and averaging. The tool takes two numbers as input via the command line and performs the specified operation.

## **Project Structure**

The project is structured as follows:

``` bash
.
├── .devcontainer         # Development environment files
│   ├── devcontainer.json  # Configuration for the development container
│   └── Dockerfile         # Dockerfile for the development environment
├── .github/workflows      # GitHub Actions workflow for CI/CD
│   └── rust.yml           # GitHub Actions configuration file for Rust
├── mylib                  # Python library containing utility functions
│   ├── __init__.py        # Init file for the mylib package
│   └── lib.py             # Python library with arithmetic and database functions
├── src                    # Rust source code for the arithmetic operations
│   └── main.rs            # Main Rust file for the project
├── target                 # Directory for Rust build output
├── .gitignore             # Git ignore file
├── Cargo.lock             # Cargo lock file for Rust dependencies
├── Cargo.toml             # Rust project configuration file (dependencies and metadata)
├── Dockerfile             # Dockerfile for building the project
├── LICENSE                # License for the project
├── Makefile               # Makefile for automation tasks (build, test, etc.)
├── README.md              # Project documentation (this file)
├── requirements.txt       # Python requirements file for dependencies
├── setup.sh               # Setup script for the project
└── user_guide.md          # User guide for how to use the command-line tool
```

## **File Descriptions**
Cargo.toml: This file contains the dependencies and project metadata for the Rust project. It defines which crates are used, including clap for parsing command-line arguments.

src/main.rs: The main source file written in Rust that implements the arithmetic logic. It includes functions for performing multiplication, addition followed by multiplication, and averaging. It also handles parsing command-line arguments.

## **Project Functionality**
This project provides two main functionalities:

## Arithmetic Operations:

The Rust and Python implementations both provide basic arithmetic operations including multiplication, addition followed by multiplication, and calculating averages.
These operations are accessible via the command line.

## SQL Database Interaction:

The Python component uses Databricks SQL connectors to interact with databases, performing tasks such as querying and loading data.

## **Usage Instructions**

## Prerequisites
Rust: Ensure that Rust is installed. If not, you can install it from Rust official website.

Python: Ensure Python 3.x is installed. Install the necessary Python dependencies using:

```bash
pip install -r requirements.txt
```

## **Running the Arithmetic Functions in Rust**
To run the arithmetic functions using Rust, use the following commands in the terminal:

```bash
cargo run -- 3 5
```
This will output the multiplication of 3 and 5.

## **Running the Python Functions**
For Python, you can run the arithmetic functions directly from ``lib.py``:
```bash
from mylib.lib import multiply

result = multiply(4, 5)
print(result)
```
## **Working with the SQL Database**
To interact with the SQL database (using Databricks):
1. Set the SERVER_HOSTNAME and other necessary environment variables.
2. Use the functions in lib.py to query or load data from the database:
```bash
from mylib.lib import query

result = query()
print(result)
```

## **CI/CD Integration**
The project is integrated with a CI/CD pipeline using GitHub Actions. The pipeline runs automated tests, builds the project, and ensures code quality with linting tools. Any commits or pull requests will trigger the workflow.