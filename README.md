BASHY - Customize the existing .bashrc script in the following ways:

Customize your prompt to display all in red color, in order listed:
1.    The current time (using a 12-hour clock) |
2.    username@hostname (that is, your user name, the “@” symbol, then the host name)
3.    :: your current working directory
4.    The > character at the end
5.    NOTE: The | and :: are separators within the prompt to be printed as literal strings.  
Example of a solution prompt (variants on 12-hr time display are acceptable):
[04:12 pm] | joebob@drivein.net :: ./movies >

Set up the following commonly used aliases:
1.    Modify the personal command “ll” which invokes “ls” to show the long format (all file permissions) to add suffixes on the file size like Kilobyte, Megabyte 
and Gigabyte; this custom command is in the existing .bashrc for our vLinux.  Don’t delete the other existing behaviors!
2.    Create a personal command “untar” which unpacks an input tar file using verbose mode and filtering it through gzip
3.    Force the default behavior of the rm command to always prompt you for each item being deleted.
4.    Create a personal command “dus” which estimates your disk usage, printing out each item that is no more than 1 or fewer levels below the command line argument 
and measuring by block-size=1K, then sorting the output in order of increasing size.
5.    Write a small function that uses the first positional argument to itself.  It should call cdto the directory specified by that positional argument, then do 
the ls command to show all files there in long, human-readable format.  Then create a personal command called “cdls” which uses the function.  It is reasonable that 
if the cd fails, you don’t want to do the ls—use short-circuiting to implement this in your function!

HUNTER - Search script that takes a string as its input and:

Searches through all files in the current directory (ignoring subdirectories)

For each file found prints on separate lines the following
1.    Prints the file name
2.    Prints the first line of the file
3.    Prints all lines which match the string, preceded by the line number; if there are none, it prints “String not found here.”
4.    Prints a blank line (to add white space between the files)In the event the current directory has no files, hunter prints “Directory is empty.”

QUAVE - Calculate the average of an arbitrary set of integers input by the user.

The inputs for this will NOT be on the command line.  If the user adds arguments, print a line that tells the user that command line arguments aren’t needed for 
this script, then exit.
Assuming the script is called without arguments, first print a line which tells the user to input the next number for the average or input an “f” to finish.  Then 
run a loop that:
1.    Prompts the user for the next input
2.    If the input is an integer, add that number to the total so far
3.    If the input is not an integer or an “f” then tell the user that only integers or “f” are accepted
4.    If the input is the “f” then exit the loop, calculate the average, and print “The average of your numbers is: ave” where ave is the calculated average.

STRINGSEEDER - Accepts a string followed by a space-delimited list of files as its input (and that list could be long), and it:

Searches each file for the string
If the file does contain the string, prints a line saying “string found in filename” where filenameis the name of the file and string is the string sought
If the file does NOT contain the string, it appends the string to the end of the file, then prints “string added to filename” with the same rules as the previous 
step; note that you can use a special redirection symbol >> to more easily accomplish appending!
