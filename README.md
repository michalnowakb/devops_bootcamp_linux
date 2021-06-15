# devops_bootcamp_linux


## Introduction to DevOps and why DevOps/benefits

- Working together with Developers 
- Automating a pipline
- Sharing responsibilities
- Deploying infrastructure as code
- Continuos Integration/Continous Delivery/Continous Deployment

### Linux commands that also work on Bash
- Create a Dir `mkdir name_of_the_dr`
- Go inside the Dir `cd name_of_the_dir`
- Come out of the Dir `cd ..` or `cd`
- Who am I `uname -a`
- Where am I `pwd`
- Create a file `touch name_of_the_file` or `nano file_name` you land inside the file
- Exit from nano `ctrl x` then `y` then `enter`
- List all `ls -a` or `ls` (by adding -a we can see hidden files as well)
- To see the content of the file terminal `cat file_name`
- Clear your screen `clear`
- Delete a folder `rm -rf name_of_the_folder`  (by adding -rf we will delete folder/file for good)
- To delete all of the files and any sub-folders it contains we can `rm -R`


## Using SSH keys for GitHub

### Connecting to SSH directory on Windows
- Navigate to C:\Users\user_name\.ssh  by using command `cd ~/.ssh`
- Use `ls` command to check if you have a file called "id_rsa.pub" is under that directory
- If not we can generate new SSH key using `ssh-keygen -t rsa -b 4096 -C [example@email.com]
- Now if we will check files under SSH directory we should be able to see file called "id_rsa.pub"
- To see content of that file we can type `cat id_rsa.pub`

### Connecting SSH key to your GitHub Account
- Go to GitHub website and login to your account 
- Click on your profile picture on the top right of the screen 
- Select "Settings" from 
drop down menu 
- On the left you will see "Account settings", select "SSH and GPG Keys" 
- On the Top right you will find button saying 
"New SSH Key" press that button 
- As a title you can type "SSH Key" but naming it is up too the user 
- In the "key" area we can paste our key from `id_rsa.pub` file and press "Add SSH key"


## More Linux commands
display linux processes `top`.
To become root user `sudo su`.
To see the history of commands `history`.
To check the status of a process `systemctl status process_name`.
To stop a process `systemctl stop process_name`.
To restart a process `systemctl restart process_name`.
To make a script you must write `#!/bin/bash` at the start of the file and use a `.sh` file type.
To run a file type sudo bash `./file_name.sh` or just `./file_name.sh`.
To change a files mode to executable `sudo chmod +x file_name.sh`.
Once executable, run a script by making it `sudo ./provision.sh`.
To view a snapshot of the current processes `ps`
To kill a process `kill [process id]`
kill -9 Meaning the process will be killed by the kernel; this signal cannot be ignored. 9 means KILL signal that is not catchable or ignorable
`sudo chmod +x file_name makes` the bash file executable
`ll` or `ls -al` to check the permissions of the files
File permissions:
`r` - gives read permission
`w` - gives write permission
`x` - gives executable permission
`777` - gives full control
`400` - allows the owner to read
`600` - owner can read and write
`Tail` is a command which prints the last few number of lines (10 lines by default) of a certain file, then terminates.
`Head` command will obviously on the contrary to tail, it will print the first 10 lines of the file.
The `sort` command arranges text lines in useful ways. This simple tool can help you quickly sort information from the command line.
`nl` - Sometimes you may required to count number of lines in a file on Linux command line or shell scripting.
`wc` - The wc command as described can be used to get the number of newlines, words or bytes contained in a file specified.
The “pipe” command is readily available on UNIX/Linux platforms. This command pipes the output of the previous command to the next command. There are literally TONS of situations where this method offers serious value.Before jumping deeper, there’s something to know of. Every single program in the UNIX/Linux system has 3 built-in data streams.
`STDIN` (0) – Standard input
`STDOUT` (1) – Standard output
`STDERR` (2) – Standard error
When we’re going to work with “pipe” tricks, “pipe” will take the STDOUT of a command and pass it to the STDIN of the next command.
Wildcard Pattern Matching
`?` – matches any single character * – Matches any sequence of characters (including the empty sequence)
Example (Wildcard)
`Text = "baaabab",`

`Pattern = “baab", output : true`

`Pattern = "baaa?ab", output : true`

`Pattern = "ba*a?", output : true`

`Pattern = "a*ab", output : false`

Reference

`How to Hide Files`

The period `(.)` at the beginning of the new filename indicates that it’s `hidden`:

`mv test.txt .test.txt`

To verify the file is now hidden, display the contents of the current directory:

`ls –a`
