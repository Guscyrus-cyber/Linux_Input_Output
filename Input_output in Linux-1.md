[Activity: Examine input/output in the Linux]{.mark}

As a security professional, it\'s important to understand the concept of
communication with your computer via the shell.

In this scenario, you have to input a specific string of text that you
want the shell to return as output. You'll also need to input a few
mathematical calculations so the OS can return the results[.
**[First]{.smallcaps}**]{.mark}, you'll use the echo command to generate
some output in the shell. **[[Second]{.mark},]{.smallcaps}** you'll use
the **[expr]{.smallcaps}** command to perform basic mathematical
calculations. **[[Next]{.smallcaps}]{.mark}**, you'll use the clear
command to **[clear]{.smallcaps}** the bash shell window.
[**[Finally]{.smallcaps}**,]{.mark} you'll have an opportunity to
explore the echo and expr command further.

The lab starts with your user account, called **[analyst]{.smallcaps}**,
already logged into the Bash shell. This means you can start with the
tasks as soon as you click, the **[start lab]{.smallcaps}** button.

**[Task 1. Generate output with the echo command]{.smallcaps}**

Task 1. Generate output with the [echo]{.mark} command

analyst@8c5cf19110f5:\~\$ [echo hello]{.mark}

[hello]{.mark}

Return the command, but include quotation marks around the string data.
Type "[echo hello"]{.mark}

analyst@8c5cf19110f5:\~\$ [echo hello]{.mark}

[hello]{.mark}

Use the ["echo"]{.mark} command to output your name to the shell.

analyst@8c5cf19110f5:\~\$ [echo "ghasem"]{.mark}

[ghasem]{.mark}

## 

TASK 2. Generate output with the [expr]{.mark} command

Calculate the number of false positives using the [expr]{.mark} command.

analyst@8c5cf19110f5:\~\$ [expr 32 - 8]{.mark}

[24]{.mark}

analyst@8c5cf19110f5:\~\$ [expr 3500 \* 12]{.mark}

[42000]{.mark}

TASK 3. Clear the Bash shell

Type "[clear"]{.mark} into the shell and press enter.

analyst@8c5cf19110f5:\~\$ [clear]{.mark}

analyst@8c5cf19110f:\~5\$

[Activity: Find files with Linux commands]{.mark}

In this scenario, you have to locate an analyze the information of
certain files located in the

[/home/analyst]{.mark} directory.

First, you'll get the information on the current working directory,
You're in and display the contents of the directory. Second, you'll
navigate to the [reports]{.mark} directory and list the subdirectories
it contains. Third, you'll navigate to the [users]{.mark} subdirectory
and display the contents of the [Q1_added_users.txt]{.mark} file.
Finally, you'll navigate to the [logs]{.mark} directory and display the
first 10 lines of a file it contains.

Task 1. Get the current directory information.

. Display your working directory.

analyst@4b65624caa19:\~\$ [pwd]{.mark}

[/home/analyst]{.mark}

. Display the name of the files and directories in the current working
directory.

analyst@4b65624caa19:\~\$ [Ls]{.mark}

[logs projects reports temp]{.mark}

Which directory is your current working directory?

[/home/analyst]{.mark}

How many directories does the current working directory?

[Four directories in the /home/analyst directory. Namely logs, notes,
temp, and reports.]{.mark}

Task 2. Change directory and list the subdirectories.

. Navigate to the [/home/analyst/reports]{.mark} directory.

analyst@4b65624caa19:\~\$ [cd reports]{.mark}

analyst@4b65624caa19:\~/reports\$ [cd /home/analyst/reports]{.mark}

analyst@4b65624caa19:\~/reports\$ [Ls]{.mark}

[users]{.mark}

What is the name of the subdirectories in the /home/analyst/reports
directory?

[Users]{.mark}

Task 3: Locate and read the contents of a file

. Navigate to the /home/analyst/reports/users directory.

analyst@4b65624caa19:\~/reports/users\$ [Ls]{.mark}

Display the contents of the [Q1_added_users.txt files]{.mark}

[Q1_added_users.txt Q1_added_users.txt]{.mark}

The command to complete this step:

[Cat Q1_added_users.txt]{.mark}

analyst@4b65624caa19:\~/reports/users\$ [cat Q1_added_users.txt]{.mark}

employee_id. Username. Department

1001\. bmoreno. Marketing

1026\. apatel. Human Resources

1041 cgriffin Sales

1104 mreed Information Technology

1177 aezra Human Resources

1188\. noshiro. Finance

analyst@4b65624caa19:\~/reports/users\$ [cat]{.mark}
[/home/analyst/reports/users/Q1_added_users.txt]{.mark}

employee_id. Username. Department

1001\. bmoreno. Marketing

1026\. apatel. Human Resources

1041 cgriffin Sales

1104 mreed Information Technology

1177 aezra Human Resources

1188\. noshiro. Finance

What department does the employee with the username [aezra]{.mark} work
in?

[Hunan Resources]{.mark}

What is the employee_id of the user [mreed]{.mark} in the information
Technology department?

[1104]{.mark}

Task 4: Navigate to a directory and locate a file

. Navigate to the [/home/analyst/logs directory]{.mark}

The command to complete this step:

[Cd /home/analyst/logs]{.mark}

analyst@4b65624caa19:\~/reports/users\$ [cd /home/analyst/logs]{.mark}

. Display the name of the file it contain

analyst@4b65624caa19:\~/logs\$ [Ls]{.mark}

[server_logs.txt]{.mark}

. Display the first 10 line of this file.

The command to complete this step:

[Head server_logs.txt]{.mark}

analyst@4b65624caa19:\~/logs\$ head server_logs.txt

2022-09-28 13:55:55 info Users logged on successfully

2022-09-28 13:56:22 error The password is incorrect

2022-09-28 13:56:48. Warning The file storage is 75% full

2022-09-28. 15:55:55. Info User logged on successfully

2022-09-28. 15:56:22 error. The username is incorrect

2022-09-28 15:56:48. Warning The file storage is 90% full

2022-09-28. 16:55:55. Info User navigated to settings page

2022-09-28 16:56:22 error The password is incorrect

2022-09-28 16:56:48 Warning The current user's password expires in 15
days

2022-09-29 13:55:55 info User logged on successfully

How many warning messages are in he first 10 lines of the
server_logs.txt file?

[Three]{.mark}

[Activity: Filter with grep]{.mark}

In this scenario, you need to obtain information contained in server log
and user data files. You also need to find files with specific names.

Here, how you'll do this. First, you'll navigate to the logs directory
and return the error messages in the [server_logs.txt]{.mark} file.
Next, you'll navigate to the [users]{.mark} directory and search for
files that contain a specific string in their names. Finally, you'll
search for information contained in users files.

Task 1: Search for error message in a log file

In this task, you must navigate to the [/home/analyst/logs]{.mark}
directory and report on the error messages in the
[server_logs.txt]{.mark} file. You'll also this by using grep to search
file and output only the entries that are for errors.

. Navigate to the [/home/analyst/logs]{.mark} directory using command
[cd logs]{.mark} to complete this step.

analyst@a88c22213e68:\~\$ [cd logs]{.mark}

. Use grep to filter the [server_logs.txt]{.mark} file, and return all
lines containing the next string error.

analyst@a88c22213e68\~/logs\$ [grep error server_logs.txt]{.mark}

2022-09-28 13:56:22 error The password is incorrect

2022-09-28 15:56:22 error The username is incorrect

2022-09-28 16:56:22 error The password is incorrect

2022-09-29 13:56:22 error An unexpected error occurred

2022-09-29 15:56:22 error Unauthorized access

2022-09-29 16:56:22 error Unauthorized access

This grep command will filter [server_logs.txt file,]{.mark} and return
a list of the lines that match the text string [error]{.mark}.

How many error lines are there in the server_logs.txt files?

[Six]{.mark}

Task2: Find files containing specific strings

. Navigate to the [/home/analyst/reports/users]{.mark} directory using
command [cd]{.mark} [/home/analyst/reports/users.]{.mark}

analyst@a88c22213e68\~/logs\$ [cd /home/analyst/reports/users]{.mark}

. Using the pipe character [(\|)]{.mark}. Pipe the output of the
[Ls]{.mark} command to the [grep]{.mark} command to list only the files
containing the string [Q1]{.mark} in their names. Using [Ls \| grep
Q1]{.mark}

analyst@a88c22213e68\~/reports/users\$ [Ls \| grep Q1]{.mark}

Q1_access.txt

Q1_added_users.txt

Q1_deleted_users.txt

analyst@a88c22213e68\~/reports/users\$ Ls \| grep access

Q1_access.txt

Q2_access.txt

Q3_access.txt

Q4_access.txt

How many files in the /home/analyst/reports/users subdirectory contain
"Q1" in their names?

[Three]{.mark}

. List the files that contain the word ["access"]{.mark} in their name
using command [Ls \| grep access]{.mark}

analyst@a88c22213e68\~/reports/users\$ [Ls]{.mark}

Q1_access.txt Q2_added_users.txt Q3_deleted_users.txt

Q1_added_users.txt Q2_deleted_users.txt Q4_access.txt

Q1_deleted_users.txt Q3_access.txt Q4_added_users.txt

Q2_access.txt Q3_added_users.txt Q4_deleted_users.txt

How many files in the /home/analyst/reports/users directory contain
"access" in their names?

[Four]{.mark}

Task 3: Search for more file contents

. Display the files in the [/home/analyst/reports/users]{.mark}
directory using command ["Ls".]{.mark}

analyst@a88c22213e68\~/reports/users\$ [Ls]{.mark}

Q1_access.txt Q2_added_users.txt Q3_deleted_users.txt

Q1_added_users.txt Q2_deleted_users.txt Q4_access.txt

Q1_deleted_users.txt Q3_access.txt Q4_added_users.txt

Q2_access.txt Q3_added_users.txt Q4_deleted_users.txt

. Search the [Q2_deleted_users.txt]{.mark} files for the username
"[jhill"]{.mark} using command [grep jhill]{.mark}
[Q2_deleted_users.txt]{.mark}

analyst@a88c22213e68\~/reports/users\$ [grep jhill
Q2_deleted_users.txt]{.mark}

1025 jhill Sales

Did you find the username "jhill" in the Q2_deleted_users.txt file?

[Yes]{.mark}

. Search the [Q4_added_users.txt]{.mark} file to list the users who were
added to the [Human Resources]{.mark} department using command [grep
"Human Resources" Q4_added_users.txt]{.mark}

analyst@a88c22213e68\~/reports/users\$ [grep "Human Resources"
Q4_added_users.txt]{.mark}

1151 sshah Human Resources

1145 msosa Human Resources

analyst@a88c22213e68\~/reports/users\$

How many users were added to the Human Resources department in Q4?

[Two]{.mark}

[Activity: Manage files with Linux commands]{.mark}

In this scenario, you need to ensure that the [/home/analyst]{.mark}
directory is properly organized.

You have to make a few changes to the [/home/analyst]{.mark} directory
and files it contains. You also have to edit a file to record the
changes or update you make to the directory.

Task 1: Creat a new directory

You must create a dedicated subdirectory called [logs,]{.mark} which
will be used to store all future log files.

. Create a new subdirectory called l[ogs]{.mark} in the
[/home/analyst]{.mark} directory using command [mkdir]{.mark}
[logs]{.mark}

analyst@8d16a286690d:\~\$ [mkdir logs]{.mark}

. List the contents of the [/home/analyst]{.mark} directory to confirm
that you've successfully created the new logs subdirectory using command
[Ls]{.mark} to complete this step.

analyst@8d16a286690d:\~\$ Ls

logs notes reports temp

Taks 2: Remove a directory

Next, you must remove the [temp]{.mark} directory as you'll no longer be
placing items in it.

. Remove the [/home/analyst/temp]{.mark} directory using [rmdir
temp]{.mark}

analyst@8d16a286690d:\~\$ [rmdir temp]{.mark}

. List the contents of the /[home/analyst]{.mark} directory to confirm
that you have removed the temp subdirectory using command [Ls]{.mark} to
complete this step.

The [temp]{.mark} directory should no longer be listed

analyst@8d16a286690d:\~\$ [Ls]{.mark}

logs notes reports

Task 3: Move a file

The [Q3patches.txt]{.mark} file contains notes taken on third Quarter
patches and is now in the correct reporting format.

You must move the [Q3patches.txt]{.mark} file from the notes directory
to the r[eports]{.mark} directory.

. Navigate to the /[home/analyst/notes]{.mark} directory using command
[cd /home/analyst/notes.]{.mark}

analyst@8d16a286690d:\~\$ [cd /home/analyst/notes]{.mark}

The previous command used the absolute path, you could use the relative
path as follow using [cd notes.]{.mark}

analyst@8d16a286690d:\~/notes\$ [cd notes]{.mark}

-bash: cd: notes: no such file or directory

. Move the [Q3patches.txt]{.mark} file from the
/[home/analyst/notes]{.mark} directory to the
/[home/analyst/reports]{.mark} directory using [mv Q3pathes.txt
/home/analyst/reports/]{.mark}

analyst@8d16a286690d:\~/notes\$ [mv Q3patches.txt
/home/analyst/reports/]{.mark}

. List the contents of the [/home/analyst/reports]{.mark} directory to
confirm that you have moved the file successfully using [Ls
/home/analyst/reports]{.mark} command to complete this step.

analyst@8d16a286690d:\~/notes\$ [Ls /home/analyst/reports]{.mark}

Q1patches.txt Q2patches.txt Q3patches.txt

Task 4: Remove a file

Next, you must delete an unused file called [tempnotes.txt]{.mark} from
the /[home/analyst/notes]{.mark} directory.

. Remove the [tempnotes.txt]{.mark} file from the
/[home/analyst/notes]{.mark} directory using [rm]{.mark}
[tempnotes.txt]{.mark} command.

analyst@8d16a286690d:\~/notes\$ [rm tempnotes.txt]{.mark}

. List the contents of the /[home/analyst/notes]{.mark} directory to
confirm that you've removed the file successfully using [Ls]{.mark}
command.

analyst@8d16a286690d:\~/notes\$ [Ls]{.mark}

Tak 5: Creat a new file

Now, you must create a file named [tasks.txt]{.mark} in the
/[home/analyst/notes]{.mark} directory that you'll use to document
completed tasks.

. Use the [touch]{.mark} command to create an empty file called
[tasks.txt]{.mark} in the /[home/analyst/notes]{.mark} directory using
[touch tasks.txt]{.mark} command.

analyst@8d16a286690d:\~/notes\$ [touch tasks.txt]{.mark}

. List the contents of the /[home/analyst/notes]{.mark} directory to
confirm that you have created a new file using [Ls]{.mark} command.

analyst@8d16a286690d:\~/notes\$ [Ls]{.mark}

[tasks.txt]{.mark}

Task 6: Edit a file

Finally, you must use the [nano text]{.mark} editor to edit the
[tasks.txt]{.mark} file and add a note describing the tasks you've
completed.

. Using the [nano text]{.mark} editor, open the [tasks.txt]{.mark} file
that is located in the /[home/analyst/notes]{.mark} directory using
[nano tasks.txt]{.mark}

analyst@8d16a286690d:\~/notes\$ [nano tasks.txt]{.mark}

This action changes the shell from the normal bash interface to the
[nano text]{.mark} editor interface.

. Copy and paste "managed file structure in [/home/analyst]{.mark} into
the text input area of the [nano]{.mark} edito.

Completed task

. Press [CTRL+X]{.mark} to exit the [nano text]{.mark} editor

This triggers a prompt asking save modified bufferer.

. Press [Y]{.mark} to confirm that you want to save the new data to your
file. (Answering ["no"]{.mark} will discard changes)

. Press [Enter]{.mark} to conform that file Name to Write is
[tasks.txt]{.mark}

. Using the ["clear]{.mark}" command to clear the bash shell window and
remove any traces of the [nano]{.mark} [text]{.mark} input area.

. Display the contents of the [tasks.txt]{.mark} file to confirm that it
contains the update task details using [cat tasks.txt]{.mark} command.

GNU nano 3.2 tasks.txt

Completed tasks

Managed file structure in /[home/analyst]{.mark}

Save? [NO]{.mark}

analyst@8d16a286690d:\~/notes\$

analyst@8d16a286690d:\~/notes\$ [cat tasks.txt]{.mark}

Completed tasks

Managed file structure in /[home/analyst]{.mark}

analyst@8d16a286690d:\~/notes\$

Completed tasks

[Activity: Manage authorization]{.mark}

In this scenario, you must examine and manage the permissions on the
files in the /home/researcher2/projects directory for the researcher2
user.

The researcher2 user is part of the research_team group.

You must check the permissions for all files in the directory, including
any hidden files to make sure that permissions align with the
authorization that should be given. When it doesn't you must change the
permissions.

First, you check the user and group permissions for all files in the
project's directory. Next, you check whether any files have incorrect
permissions and change the permissions as needed. Finally, you'll check
the permissions of the /home/researcher2/projects/drafts directory and
modify these permissions to remove any unauthorized access.

Task 1: Check file and directory details

In this task, you must explore the permission of the [projects]{.mark}
directory and the files it contains. The lab starts with
/[home/researcher2]{.mark} as the current working directory. This is
because you're changing permissions for files and directories belonging
to the researcher2 user.

. Navigate to the [projects]{.mark} directory using [cd projects]{.mark}
command.

Researcher2@3ac1665d1326:\~\$ [cd projects]{.mark}

. List the contents and permission of the [projects]{.mark} directory
using [Ls -1]{.mark} command.

Researcher2@3ac1665d1326:\~/projects\$ [Ls -1]{.mark}

drafts

project_k.txt

project_m.txt

project_r.txt

project_t.txt

List the files and directory without hidden files using [Ls -1]{.mark}

draft

project_k.txt

project_m.txt

project_r.txt

project_t.txt

List the files and directory including hidden file using [Ls -1a]{.mark}
or [Ls -a]{.mark}

Researcher2@3ac1665d1326:\~/projects\$ [Ls -1a]{.mark}

project_x.txt

drafts

proect_k.txt

project_m.txt

project_r.txt

project_t.txt

Researcher2@3ac1665d1326:\~/projects\$ [Ls -a]{.mark}

Project_x.txt project_k.txt project_r.txt

draft project_m.txt project_t.txt

What is the name of the group that owns the files in the
[projects]{.mark} directory?

Research_teams

Which of these files is hidden file in the [projects]{.mark} directory?

Project_x.txt

Task 2: Change file permissions

. Check whether any files in the [projects]{.mark} directory have write
permissions for the owner type of other using [Ls -1]{.mark} command.

List the files and directory without hidden files using [Ls -1]{.mark}

draft

project_k.txt

project_m.txt

project_r.txt

project_t.txt

Which file grants other users write permission?

Project_k.txt

. Changing the permissions of the file identified in the previous step
so that the owner type of other doesn't have write permissions we'r
using [chmod o-w project_k.txt]{.mark} command.

. The file [project_m.txt]{.mark} is a restricted file and should not be
readable or writable by the group or other, only the user should have
these permission on the file. Listing the contains and permissions of
the current directory and checking if the group has read or write
permission we use [Ls -1]{.mark} command to complete this task.

What are the group permissions on the [project_m.txt]{.mark}?

Read only

. Use the [chmod]{.mark} command to change permissions of the
[project_m.txt]{.mark} file s that the group doesn't have read or write
permission using [chmod g-r project_m.txt]{.mark}

Researcher2@3ac1665d1326:\~/projects\$ [chmod g-r project_m.txt]{.mark}

Researcher2@3ac1665d1326:\~/projects\$ [Ls -1a]{.mark}

Total 32

drwxr-xr-x 3 researcher2 research_team 4096 Oct 19 22:39

drwxr-xr-x 3 researcher2 research_team 4096 Oct 19 23:55

-rw- -w\-\-\-- 1 researcher2 research_team 46 Oct 19 39 .project_x.txt

drwx- -x\-\-- 2 researcher2 research_team 4096 Oct 19 22:39 drafts

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_k.txt

-rw\-\-\-\-\-\-- 1 researcher2 research_team 46 Oct 19 22:39
project_m.txt

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_r.txt

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_r.txt

Task 3: Change file permissions on a hidden file

The file [project_x.txt]{.mark} is a hidden file that has been archived
and should not be written to by anyone. (The user and, group should
still be able to read this file).

. Check the permissions of the hidden file [project_x.txt]{.mark} and
answer the question that follows using [Ls -1a]{.mark} command.

Researcher2@3ac1665d1326:\~/projects\$ [Ls -1a]{.mark}

Total 32

drwxr-xr-x 3 researcher2 research_team 4096 Oct 19 22:39

drwxr-xr-x 3 researcher2 research_team 4096 Oct 19 23:55

-rw- -w\-\-\-- 1 researcher2 research_team 46 Oct 19 39 .project_x.txt

drwx- -x\-\-- 2 researcher2 research_team 4096 Oct 19 22:39 drafts

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_k.txt

-rw\-\-\-\-\-\-- 1 researcher2 research_team 46 Oct 19 22:39
project_m.txt

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_r.txt

-rw-rw-r\-- 1 researcher2 research_team 46 Oct 19 22:39 project_r.txt

Which owner type has the incorrect write permission?

The user and the group owner type

. Change the permissions of the file [project_x.txt]{.mark} so that both
the user and the group can read, but not write to the file using [chmod
u-w, g-w, g+r]{.mark} .[project.x.txt]{.mark}

researcher2@3ac1665d1326:\~/projects\$ [chmod u-w, g-w, g+r]{.mark}
.[project.x.txt]{.mark}

Task4 : Change directory permissions

. Check the permissions of the drafts directory using [Ls -1]{.mark}

researcher2@3ac1665d1326:\~/projects\$ [Ls -1]{.mark}

drafts

project_k.txt

project_m.txt

project_r.txt

project_t.txt

Does the group have permissions set to access the drafts directory and
its contents?

Yes

. Remove the execute permission for the group from the drafts directory
using [chmod g-r]{.mark} drafts

researcher2@3ac1665d1326:\~/projects\$ [chmod g-x drafts]{.mark}

researcher2@3ac1665d1326:\~/projects\$
