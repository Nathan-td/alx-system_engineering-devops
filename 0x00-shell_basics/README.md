Toggle navigation

0x00. Shell, basics

DevOpsShellBash

 By: Julien Barbier Weight: 1 Project will start Jul 5, 2023 6:00 AM, must end by Jul 6, 2023 6:00 AM Checker was released at Jul 5, 2023 6:00 AM An auto review will be launched at the deadline

About Bash projects

Unless stated, all your projects will be auto-corrected with Ubuntu 20.04 LTS.

Resources

Read or watch:

What Is “The Shell”?NavigationLooking AroundA Guided TourManipulating FilesWorking With CommandsReading Man pagesKeyboard shortcuts for BashLTSShebang

man or help:

cdlspwdlessfilelncpmvrmmkdirtypewhichhelpmanLearning Objectives

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

GeneralWhat does RTFM mean?What is a ShebangWhat is the ShellWhat is the shellWhat is the difference between a terminal and a shellWhat is the shell promptHow to use the history (the basics)NavigationWhat do the commands or built-ins cd, pwd, ls doHow to navigate the filesystemWhat are the . and .. directoriesWhat is the working directory, how to print it and how to change itWhat is the root directoryWhat is the home directory, and how to go thereWhat is the difference between the root directory and the home directory of the user rootWhat are the characteristics of hidden files and how to list themWhat does the command cd - doLooking AroundWhat do the commands ls, less, file doHow do you use options and arguments with commandsUnderstand the ls long format and how to display itA Guided TourWhat does the ln command doWhat do you find in the most common/important directoriesWhat is a symbolic linkWhat is a hard linkWhat is the difference between a hard link and a symbolic linkManipulating FilesWhat do the commands cp, mv, rm, mkdir doWhat are wildcards and how do they workHow to use wildcardsWorking with CommandsWhat do type, which, help, man commands doWhat are the different kinds of commandsWhat is an aliasWhen do you use the command help instead of manReading Man PagesHow to read a man pageWhat are man page sectionsWhat are the section numbers for User commands, System calls and Library functionsKeyboard Shortcuts for BashCommon shortcuts for BashLTSWhat does LTS mean?Copyright - PlagiarismYou are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.You are not allowed to publish any content of this project.Any form of plagiarism is strictly forbidden and will result in removal from the program.RequirementsGeneralAllowed editors: vi, vim, emacsAll your scripts will be tested on Ubuntu 20.04 LTSAll your scripts should be exactly two lines long ($ wc -l file should print 2)All your files should end with a new line (why?)The first line of all your files should be exactly #!/bin/bashA README.md file at the root of the repo, containing a description of the repositoryA README.md file, at the root of the folder of this project, describing what each script is doingYou are not allowed to use backticks, &&, || or ;All your scripts must be executable. To make your file executable, use the chmod command: chmod u+x file. Later, we’ll learn more about how to utilize this command.More Info

Example of line count and first line

julien@ubuntu:/tmp$ wc -l 12-file_type 2 12-file_type julien@ubuntu:/tmp$ head -n 1 12-file_type #!/bin/bash julien@ubuntu:/tmp$ 

In order to test your scripts, you will need to use this command: chmod u+x file. We will see later what does chmod mean and do, but you can have a look at man chmod if you are curious.

Example

julien@ubuntu:/tmp$ ls 12-file_type lll julien@ubuntu:/tmp$ ls -la lll -rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll julien@ubuntu:/tmp$ cat lll #!/bin/bash ls julien@ubuntu:/tmp$ ls -l lll -rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll julien@ubuntu:/tmp$ chmod u+x lll # you do not have to understand this yet julien@ubuntu:/tmp$ ls -l lll -rwxrw-r-- 1 julien julien 15 Sep 19 21:05 lll julien@ubuntu:/tmp$ ./lll 12-file_type lll julien@ubuntu:/tmp$ 

Quiz questions

Great! You've completed the quiz successfully! Keep going! (Show quiz)

Tasks

0. Where am I?

mandatory

Write a script that prints the absolute path name of the current working directory.

Example:

$ ./0-current_working_directory /root/alx-system_engineering-devops/0x00-shell_basics $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 0-current_working_directory

 Done? Help Check your code Get a sandbox

1. What’s in there?

mandatory

Display the contents list of your current directory.

Example:

$ ./1-listit Applications Documents Dropbox Movies Pictures Desktop Downloads Library Music Public $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 1-listit

 Done? Help Check your code Get a sandbox

2. There is no place like home

mandatory

Write a script that changes the working directory to the user’s home directory.

You are not allowed to use any shell variablesjulien@ubuntu:/tmp$ pwd /tmp julien@ubuntu:/tmp$ echo $HOME /home/julien julien@ubuntu:/tmp$ source ./2-bring_me_home julien@ubuntu:~$ pwd /home/julien julien@ubuntu:~$ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 2-bring_me_home

 Done? Help Check your code Get a sandbox

3. The long format

mandatory

Display current directory contents in a long format

Example:

$ ./3-listfiles total 32 -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory -rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 3-listfiles

 Done? Help Check your code Get a sandbox

4. Hidden files

mandatory

Display current directory contents, including hidden files (starting with .). Use the long format.

Example:

$ ./4-listmorefiles total 32 drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 . drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 .. -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory -rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles -rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 4-listmorefiles

 Done? Help Check your code Get a sandbox

5. I love numbers

mandatory

Display current directory contents.

Long formatwith user and group IDs displayed numericallyAnd hidden files (starting with .)

Example:

$ ./5-listfilesdigitonly total 32 drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 . drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 .. -rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory -rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles -rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home -rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles -rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles -rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 5-listfilesdigitonly

 Done? Help Check your code Get a sandbox

6. Welcome

mandatory

Create a script that creates a directory named my_first_directory in the /tmp/ directory.

Example:

$ ./6-firstdirectory $ file /tmp/my_first_directory/ /tmp/my_first_directory/: directory $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 6-firstdirectory

 Done? Help Check your code Get a sandbox

7. Betty in my first directory

mandatory

Move the file betty from /tmp/ to /tmp/my_first_directory.

Example:

$ ./7-movethatfile $ ls /tmp/my_first_directory/ betty $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 7-movethatfile

 Done? Help Check your code Get a sandbox

8. Bye bye Betty

mandatory

Delete the file betty.

The file betty is in /tmp/my_first_directory

Example:

$ ./8-firstdelete $ ls /tmp/my_first_directory/ $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 8-firstdelete

 Done? Help Check your code Get a sandbox

9. Bye bye My first directory

mandatory

Delete the directory my_first_directory that is in the /tmp directory.

Example:

$ ./9-firstdirdeletion $ file /tmp/my_first_directory /tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory) $ 

Repo:

GitHub repository: alx-system_engineering-devopsDirectory: 0x00-shell_basicsFile: 9-firstdirdeletion

 Done? Help 


