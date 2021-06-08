# devops_bootcamp_linux

## Introduction to DevOps and why DevOps/benefits

- Working together with Developers 
- Automating a pipline
- Sharing responsibilities
- Deploying infrastructure as code
- Continuos Integration/Continous Delivery/Continous Deployment

### Linux commends that also work on Bash
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
- If not we can generate new SSH key using `ssh-keygen -t rsa -b 4096 -C [example@email.com]`
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
