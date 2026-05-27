# Minishell

![42](https://img.shields.io/badge/42-black?style=for-the-badge&logo=42&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)

## Overview

**Minishell** is a simplified reproduction of the Bash shell developed in C as part of the 42 curriculum.

The goal of this project is to understand how a Unix shell works internally by implementing command parsing, process management, pipes, redirections, environment variables, and built-in commands.

---

## Features

### Built-in Commands

| Command | Options / Arguments | Description |
|---------|---------------------|-------------|
| `echo` | `-n` | Display text in the standard output |
| `cd` | `path` | Change the current working directory |
| `pwd` | none | Print the current working directory |
| `export` | `KEY=value` | Create or update environment variables |
| `unset` | `KEY` | Remove environment variables |
| `env` | none | Display environment variables |
| `exit` | `code` | Exit the shell with a status code |

---

### Operators & Expansions

| Operator | Description |
|----------|-------------|
| `>` | Redirect output to a file |
| `<` | Redirect input from a file |
| `>>` | Append output to a file |
| `<< EOF` | Heredoc support |
| `$VAR` | Environment variable expansion |
| `$?` | Expand the last exit status |

---

## Project Structure

```bash
Minishell/
├── includes/
├── src/
├── builtins/
├── parsing/
├── execution/
├── signals/
├── Makefile
└── minishell
```

---

## Installation

### Clone the repository

```bash
git clone git@github.com:Ernst-Devan/42_Minishell.git Minishell
```

### Compile the project

```bash
cd Minishell
make
```

---

## Usage

Launch the shell with:

```bash
./minishell
```

Example:

```bash
minishell$ echo Hello World
Hello World

minishell$ ls -la | grep minishell

minishell$ export USERNAME=marvin
minishell$ echo $USERNAME
marvin
```

---

## Learning Objectives

This project covers important Unix and system programming concepts such as:

- Process creation with `fork`
- Program execution with `execve`
- File descriptors and redirections
- Pipes
- Signal handling
- Environment management
- Command parsing
- Memory management

---

## Contributors

- [@dernst](https://github.com/Ernst-Devan)
- [@njooris](https://github.com/rayseur123)

---

## Resources

- [Writing Your Own Shell](https://www.cs.purdue.edu/homes/grr/SystemsProgrammingBook/Book/Chapter5-WritingYourOwnShell.pdf)
- Bash Manual
- Unix Process Management Documentation

---

## License

This project was developed for educational purposes as part of the 42 School curriculum.
