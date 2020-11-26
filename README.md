# Cheatsheet

This repository will focus on terminal commands and explaining some advanced topics.

## Files

- No extensions files are just files that can have different formats
- Case sensitive
- Spaces are hard - should be avoided

```bash
mkdir my documents
mkdir "my documents"

cd my\ documents/
```

- `rm`
- `rm -rf` for directiories
- Hidden files and folders are defined with `.` at the beginning
- Display all files with `ls -a` or `ll -a` even hidden
- Flags for bash commands are options
- Check options using `man <command>`

## Wild Cards

- `*` for any number of characters
- `[]` for a list of specific characters
- `???` for a specific number of characters

Example:

- `*.md` any file ending with `.md`.
- `??.md` any files with two character name ending in `.md`.
- `*.??` any name of a file that the extension is two characters long.

You can use these with `ls`, `grep` and other commands.

## Permissions

There are user, group and other permissions in linux.
</br>
We can set permissions using binary with:

- 1 for execute
- 2 for write
- 4 for read

You can combine these to make a maximum of 7 options.
</br>
You can also use the add and remove permission flags with `r` (read), `w` (write), `x` (execute). If you would like to add the permission use `+` followed by the flag letter, and if you want to remove it use `-`. For example `+x` to add the execute permission.

```bash
chmod +x example.txt
```

</br>
You can also alies which group the permission is applied to, `u` for user, `g` for group, and `o` for others.

```bash
chmod g+x example.txt
```

## Root user

Root is the superuser. You can also escalate privilages using the `sudo` command. You can also make user `sudo users` list in the system to make other users super users.

## Head, tail and sort

Head drints 10 lines from the top of the file, while tail from the bottom. Sort, sorts the file alphabetically or numerically based on the first character in a line. You can also use the `-n` flag to specify a custom amount of lines.

```bash
head -n 2 example.txt
tail -n 2 exmaple.txt
```

## Streams

- Standard in (STDIN) = Standard input of a command
- Standard out (STDOUT) = Standard output of a command
- Standard error (STRERR) = Standard error output of a command

## Pipping and redirecting

### Redirecting

Redirecting is the ability to capture the standard output of a program and redirect it into another file.

- `>` truncates a file.
- `>>` appends to file.

### Pipping

Pipping is the ability to redirect to another program. For this we can use `|` syntax.

## Process Management

- `ps`
- `ps aux`
- `&` sends the process to the background

We can use pipping and redirection to get more useful data.

## Grep

Example:

- `ps aux | grep "vagrant"` this will pipe the grep command that will only list a process with the name "vagrant"

## Process killing

`kill <process_id>`

## Bash Variables

Example of how to definie a local variable:

```bash
MY_VAR=Some_value
```

Calling the variable:

```bash
echo $MY_VAR
```

This will only be available in the current terminal and removed when the terminal is killed.

## PATH

A bunch of files it reads in an order. Specific files and locations that the terminal executes and reads before opening and allowing you, the user, or another program to interact with. This is a great location to get some variables. These can then be used by child procceses.
</br>
To make a global variable we need to use `EXPORT` to make it available in another terminal. Although when both are killed then the variable is deleted.
