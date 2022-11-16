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
