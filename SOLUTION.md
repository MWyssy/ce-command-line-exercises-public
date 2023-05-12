# Solutions

## UNIX Commands

### 1.

You want to see the size of files within the current directory

```
ls -s
```

- This lists the sizes of all of the files in the current directory

### 2.

You are concerned about the amount of disk space remaining on the server, what command could you run to check this?

```
df -ah
```

- This lists the disk usage of all drives in a human-readable format, and shows it's percentage usage of the total space available.

### 3.

You need to create a new text file called `info.txt`

```
touch info.txt
```

- This creates a new file called 'info.txt' inside the current directory.

### 4.

You need to create a new directory on the machine with the path `apps/backend/src` - the **apps** folder, **backend** folder and **src** folder all don't exist but you want to make the folders with a single command, using command line options with `mkdir` how can you make all the required directories in one single command?

```
mkdir apps apps/backend apps/backend/src apps/backend/src/new_directory
```

- This first creates an 'apps' directory, then creates the 'backend' dir inside, and the 'src' inside that, then finally creates the 'new_directory'. Putting spaces in between each command acts like it's a new command, and specifying the path creates the directory inside the path.

### 5.

You need to debug whether a server can access an API, specifically it is this end point `https://jsonplaceholder.typicode.com/users` which returns a list of users. You want to do this just via the terminal which tool could you run and what is the command?

```
curl https://jsonplaceholder.typicode.com/users
```

- This will connect to the API and print the response to the terminal. If the connnection is successful, then you receive the intended response, if not you get an error saying 'Could not resolve host'

### 6.

You want to check the last 20 log entries from the [access.log](./access.log) file, what command do you run?

```
tail access.log -n20
```

- The tail command will print the end of a file to the console. Using the -n flag allows you to specify how many lines back you want to go.

### 7.

Users are reporting that the web server is giving back a 404 status on some occassions, you need to find out how many times it has happened using a command to explore the [access.log](./access.log)

- 💡 Hint: You will need to use the `|` pipe character with 3 different commands to get the answer

```
cat access.log | grep '" 404' | wc -l
```

or

```
grep -c '" 404' access.log
```

- To find the number of occurances of a 404 error, you can either pipe the result of printing the access log into a grep command to find instances of '" 404' (including the " helps to filter out the error codes from other arbitary numbers that may include 404), then pipe the result of that into a word count with the line flag to count the lines. Or, to simplify it, you could run one grep command with the 'count' flag (-c) to search for the '" 404' in access.log

## Exercise 2

TBC

```
tbc
```
