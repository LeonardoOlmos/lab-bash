![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Bash

## Introduction

In this lab we are going to practice with [`bash`](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>), a shell and command-line language!

## Setup

1. Fork the repo in your git hub account and then clone the folder "lab-bash" to your machine and navigate to it folder.

2. Check the contents of the folder using the "ls" command

```shell
$ ls
```

and you should see the following:

```shell
exercises  inputs  lorem  lorem-copy  modules  outputs  README.md
```

3. Stay in the same directory/folder and complete the following exercises.

## Exercises

1. Using the echo command print in console "Hello World". Here is some info about echo command [https://discuss.codecademy.com/t/what-are-practical-uses-of-the-echo-command/394788]

```shell
echo "Hello World"
```

2. Create a new directory called `new_dir`.

```shell
$ mkdir new_dir

$ ls

exercices/  inputs/  lorem/  lorem-copy/  new_dir/  outputs/  readme.md
```

3. Delete/Remove the directory `new_dir`.

```shell
$ rm -r new_dir/

$ ls 

exercices/  inputs/  lorem/  lorem-copy/  outputs/  readme.md
```

4. Copy the file `sed.txt` from the `lorem` folder and paste it to the folder `lorem-copy` folder.

```shell
$ cp lorem/sed.txt lorem-copy/

$ ls lorem
at.txt  at.txte  lorem.txt  sed.txt

$ ls lorem-copy/
dummy_file.txt  sed.txt
```

5. Copy the other two files from the `lorem folder` to `lorem-copy` folder in just one line using semicolon `;`.

```shell
$ cp lorem/at.txt lorem-copy/; cp lorem/lorem.txt lorem-copy/ 

$ ls lorem
at.txt  at.txte  lorem.txt  sed.txt

$ ls lorem-copy/
at.txt  dummy_file.txt  lorem.txt  sed.txt
```

6. Show the `sed.txt` file content from the `lorem` folder.

```shell
$ cat lorem/sed.txt
```

7. Show the `at.txt` file and `lorem.txt` file contents from `lorem` folder.

```shell
$ cat lorem/sed.txt lorem/lorem.txt
```

8. Print the first 3 rows in `sed.txt` file from lorem-copy folder.

```shell
$ head -n 3 lorem-copy/sed.txt
```

9. Print the last 3 rows in `sed.txt` file from lorem-copy folder.

```shell
$ tail -n 3 lorem-copy/sed.txt
```

10. Add `Homo homini lupus.` at the end of `sed.txt` file in the `lorem-copy` folder.

```shell
$ echo "Homo homini lupus." >> lorem-copy/sed.txt

$ tail -n 2 lorem-copy/sed.txt

vel illum qui dolorem eum fugiat quo voluptas nulla pariatur?Homo homini lupus
Homo homini lupus.
```

11. Print the last 3 rows in `sed.txt` file from `lorem-copy` folder. You should see `Homo homini lupus.`.

```shell
$ tail -c20 lorem-copy/sed.txt

Homo homini lupus.
```

12. `sed` command is used to replace the text in a file. Use the `sed` command to replace all occurances of `et` with `ET` in the file `at.txt` file present in the folder `lorem`. You can use the following link to refer to `sed` commands [https://www.linode.com/docs/guides/manipulate-text-from-the-command-line-with-sed/]
Check the contents of the sed.txt file using `cat` command.

```shell
$ sed 's/et/ET/g' lorem/at.txt
```

13. Find who is the system user. 

```shell
$ whoami
```

14. Find the current path of the directory you are in.

```shell
$ pwd

/c/Users/leo_k/Documents/Ironhack/class_1/lab-bash
```

15. List all files with the extension `.txt` in lorem folder.

```shell
$ ls lorem/*.txt

lorem/at.txt  lorem/lorem.txt  lorem/sed.txt
```

16. Count the rows in `sed.txt` file from lorem folder. Look concatenate `cat` and `wc` with the pipe `|`.

```shell
$ cat lorem/sed.txt | wc -l

9
```

17. Count the **files** which start with `lorem` in all directories.

```shell
$ ls -d lorem* | wc -l

2
```

## Bonus

20. Store your `name` in a variable with `read` command.

```shell
$ read my_name

Leonardo
```

21. Print that variable.

```shell
$ echo $my_name

Leonardo
```

22. Create a new directory named with variable `name`.

```shell
$ mkdir $my_name

$ ls

Leonardo/  exercices/  inputs/  lorem/  lorem-copy/  outputs/  readme.md
```

23. Remove that directory.

```shell
$ rm -r $my_name

$ ls

exercices/  inputs/  lorem/  lorem-copy/  outputs/  readme.md
```