# A simple shell

## Description

A recreation of a shell that takes user input (commands with arguments) and outputs accordingly.

Basic loop of a shell:

1. Read command from standard input.
2. Parse commandline string into an executable program and its arguments.
3. Run parsed command.

## Features

- displays a prompt and waits for user to type a command
- can handle commands with options and arguments
- prompt displays again each time command is executed
- uses PATH variable to find executable command
- if executable is not found, prints an error message and displays prompt again
- includes an exit function that exits the shell
- includes an env built-in that prints the current environment

## File Contents
This repository contains the following files:

|   **File**   |   **Description**   |
| -------------- | --------------------- |
| shell.c | the main function |
| shed.h | header file |
| _itoa.c | custom itoa function |
| _strcmp.c | custom strcmp function |
| _strdup.c | custom strdup function |
| _strlen.c | custom strlen function |
| custom_atoi.c | custom atoi function |
| forking_helper.c | contains function to execute command read from commandline |
| free_array.c | contains function to free array and its tokens |
| life.c | contains a mix of important function calls |
| print_env.c | contains function to print environment |
| run_shell.c | contains function checking if user inputed anything |
| smart_cat.c | contains function concatenating the command to its path directory |
| tokenizer.c | contains function that parses the commandline string |
| var_finder.c | contains function to find PATH variable in environment list |

## Usage

1. Enter custom shell by typing "./hsh". You should be prompted with a ($).
2. Type a command of your liking and press "Enter".
3. Appropriate output will appear.
4. Prompt reappears and awaits your next command.
5. Exit shell by typing "exit"

## Installation
Clone the repository. Compile the ".c" files. Run executable.

## Compilation

Enter the following command to compile:
` $ gcc -Wall -Werror -Wextra -pedantic *.c -o hsh `

## Example

Interactive Mode
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

Non-interactive Mode
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```
## Authors

* [**Sunkanmi Otitolaye**](https://github.com/leosuky)
* [**Tope Adebayo**](https://github.com/TopeAdebayo)
