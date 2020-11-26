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
</br>
You can also alies which group the permission is applied to, `u` for user, `g` for group, and `o` for others.
