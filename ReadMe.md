# Core: Unix Utilities

_More powerful than the spiky blue shell_

## Working with this GitHub repository

Follow these steps to set up your own repository:

1. Fork this repository on GitHub to create your own version of this repo on your GitHub account, which should also be named `Core-Unix-Utilities`

1. Visit your fork and clone that repository onto your computer:
`git clone https://github.com/<your-username>/Core-Unix-Utilities.git`

1. Push your commits and link the local repo to your remote GitHub repo:
`git push -u origin master`

1. When you've completed a challenge and want to share it for code review, commit your work and push it to your own remote repo with:
`git push`

1. Add this GitHub repository as a _remote_ to the local one on your computer:
`git remote add core https://github.com/Product-College-Labs/Core-Unix-Utilities.git`

1. When you want to access new course materials, just pull from the origin remote repo:
`git pull core master`

## Challenges, Part 1

Challenges within each section are meant to be solved in order.

### Navigation

1.  Print the path of your working directory
    - `pwd`
1.  List the files in your working directory
    - `ls`
1.  List the files with a particular extension, like `.txt`
    - `ls ./Animals/*.txt`
1.  List the files in a subdirectory, like `project`
    - `ls ./Animals`
    - `ls Animals`
    - `ls */*`
    - `ls **/*`
1.  Navigate to a subdirectory, like `project`
    - `cd Animals`
1.  Navigate to the parent directory of your working directory
    - `cd ..`
    - `cd ./..`
1.  Navigate to a nested subdirectory, like `path/to/project`
    - `cd ./Animals`
    - `cd Animals/; cd types/`
    - `cd Animals/ && cd types/`
1.  Navigate to your home directory
    - `cd ~` 
    - `cd `
1.  Navigate back to the previous directory
    - `cd ..`
    - `cd -`

### Variables

1.  Print a sentence, like `Hello world`
    - `echo 'Hello World'`
1.  Print a variable value, like `$USER` or `$PATH`
    - `echo $PATH`
1.  Set a variable `NAME` equal to your first name, then print its value
    - `FIRST_NAME=Phouthalang`
    - `echo $FIRST_NAME`
1.  Set a variable `FULL_NAME` equal to your full name, then print its value
    - `FULL_NAME='Phouthalang Pygnasak'`
    - `echo $FULL_NAME`
1.  Print all environment variables (names and values)
    - `printenv`
    - `env`
1.  Make an alias named `hello` that prints `Hello world`
    - `$GREETING='Hello World'`, `alias hello='echo $GREETING'`
1.  Make an alias named `gocode` that navigates to your code directory
    - `$GOCODE=/make-school`
1.  Print all aliases (names and values)
    - ``

### Getting Help

1.  Print what options a command accepts, like `bash` or `python`
    - `help`
1.  Read the manual for a command, like `echo` or `ls`
    - `man echo`
1.  Print the file path to a command, like `bash` or `python`
    -

### Files

1.  Navigate to the directory `Animals`
    - `cd Animals`
1.  Print the contents of the file `Cats.txt`
    - `cat Animals/Cats.txt`
1.  Print the contents of both files `Cats.txt` and `Dogs.txt`
    - `cat Animals/Cats.txt Animals/Dogs.txt`
1.  Count the words in the file `Cats.txt`
    - `wc Animals/Cats.txt`
1.  Count the words in all files with the extension `.txt`
    - `wc */*.txt`
1.  Copy the file `Dogs.txt` to a new file `BabyDogs.txt`
    - `cp Animals/Dogs.txt Animals/BabyDogs.txt`
1.  Rename the file `BabyDogs.txt` to `Puppies.txt`
    - `mv Animals/BabyDogs.txt Animals/Puppies.txt`
1.  Make a new directory named `Shelter` inside `Animals`
    - `mkdir Animals/Shelter`
1.  Move the file `Puppies.txt` into the directory `Shelter`
    - `mv Animals/Puppies.txt Animals/Shelter/`
1.  Copy the file `Cats.txt` to `Kittens.txt` inside `Shelter`
    - `cp Animals/Cats.txt Animals/Kitten.txt; mv Animals/Kitten.txt Animals/Shelter/`
1.  List the files within the directory `Shelter`
    - `ls */Shelter`
1.  Count the words in all `.txt` files inside `Shelter`
    - `wc */Shelter/*.txt`
1.  Try to remove the directory `Shelter` (this should fail)
    - `mv Animals/Shelter/ ./`
1.  Remove all `.txt` files inside `Shelter`
    - `rm Shelter/*.txt`
1.  Remove the directory `Shelter` (this should succeed)
    - `rm -rf Shelter/`
1.  Now cry because you just deleted those poor tiny animals
    - ``

### Permissions

1.  Print out your user name
    - `who am i`
1.  List the permissions (and metadata) of all `.txt` files
    - `ls -lR */*.txt`
1.  Give all users write permission on the file `Cats.txt`
    - `chmod 745 Animals/Cats.txt`
1.  List the permissions (and metadata) of the file `Cats.txt`
    - `ls -al Animals/Cats.txt`
1.  Change the owner of the file `Cats.txt` to another user
    - `chown phou Animals/Cats.txt`
1.  Now list the permissions (and owner) of the file `Cats.txt`
    - `ls -al Animals/Cats.txt`
1.  Try to change the owner of the file `Cats.txt` back to yourself
    - ``
1.  Invoke the super-user to make the previous command succeed
    - `sudo chown phou Animals/Cats.txt`
1.  List the permissions (and owner) of the file `Cats.txt` again
    - `ls -al Animals/Cats.txt`


## Challenges, Part 2

These challenges utilize more sophisticated Unix utilities.
Challenges within each section are meant to be solved in order.

### Streams

1.  Print a sentence like `Hello world` into a file named `test.txt`
    - `echo 'Hello World' >> Streams/test.txt`
1.  Append another sentence `Hola Mundo` on a new line of `test.txt`
    - `echo 'Hola Mundo' >> Streams/test.txt`
1.  Print the contents of the file `test.txt`
    - `cat Streams/test.txt` 
1.  Print the contents of the file `numbers.txt`
    - `cat Numbers/numbers.txt`
1.  Print the first 10 lines in the file `numbers.txt`
    - `head -n10  Numbers/numbers.txt`
1.  Print the first 5 lines in the file `numbers.txt`
    - `head -n5  Numbers/numbers.txt`
1.  Print the last 10 lines in the file `numbers.txt`
    - `tail -n10  Numbers/numbers.txt`
1.  Print the last 5 lines in the file `numbers.txt`
    - `tail -n5  Numbers/numbers.txt`
1.  Print lines 6 through 10 in the file `numbers.txt`
    - `sed -n '6,10p' Numbers/numbers.txt`
1.  Sort all lines in the file `numbers.txt`
    - `sort Numbers/numbers.txt`
1.  Print the first 2 characters of each line in `numbers.txt`
    - `cut -c 1-2 Numbers/numbers.txt`
1.  Print only characters 9-16 of each line in `numbers.txt`
    - `cut -c 9-16 Numbers/numbers.txt`
1.  Sort the first 2 characters of each line in `numbers.txt`
    - `cut -c 1-2 Numbers/numbers.txt | sort`
1.  Print only the unique first 2 characters of each line in `numbers.txt`
1.  Replace all `o`s with `0`s in file `test.txt`
1.  Capitalize all letters in the file `test.txt`
    - ` cat Numbers/numbers.txt | awk '{print toupper($0)}' `
1.  Capitalize all letters in the string `Hello world`
    - `echo 'Hello World' | awk '{print toupper($0)}'`

### Search

1.  Find the file named `Cats.txt` in the directory `Animals`
    - ` find ./Animals/ -name 'Cats.txt' `
1.  Find all files ending with `.py` in your code directory
    - ` find /Volumes/ -name '*.py' `
1.  Find all files larger than 100 MB in your movies directory
    - ` find /Volumes/ -size +100M `
1.  Find all lines containing the word `one` in the file `numbers.txt`
    - ` ` 
1.  Find all lines containing the letter `e` at least 3 times in the file `numbers.txt`
    - ` `
1.  Find the `search` function definition in a source code file
    - ` `
1.  Find the `search` function definition in all source code files
    - ` `
1.  Count the lines and words in all source code files
    - ` `
1.  Find all U.S. zip codes in a file containing addresses
    - ` `
1.  Find all U.S. zip codes in a file containing addresses
    - ` `
