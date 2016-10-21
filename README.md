# GitHub Tutorial

_by Kelly Lai_

---
## Git vs. GitHub
**Git** - keeps track of a timeline of "snapshots" or commits that developers have made in their file while working on the project during specific times.
* Allows developers to refer back to the code that they have already written and apply additional changes or debug the code to make it functional
* Allows developers to organize different directories and files
* Runs in the Command Line 
* Git **DOES NOT** require Github 

**GitHub** - stores the code that developers have written on the local machine, the computer, into the cloud, also know as the internet or the website. [Github.com](https://github.com/)
* Allows multiple developers to contribute and collaborate on files easily
* Allows developers to visually track changes that other developers made
* GitHub **REQUIRES** Git

---
## Initial Setup
To create a GitHub account  
1. Go to [Github.com](https://github.com/)
2. Press the green sign up button on the top right corner
3. Insert personal information

To set up SSH key   
(_Note_: It is better to use the SSH rather than the HTTPS because SSH only requires one-time setup while HTTPS requires to enter login info every time)  
1. 



---
## Repository Setup
1. Type the command `cd ~/workspace`, which goes directly to the home folder. In this case, the highest we can go is `/workspace`.
2. Type `mkdir <directoryname>` to create a new directory under the home folder.
2. Move into the directory by typing `cd <directoryname>`.
3. Once inside the directory, type the command `git init` on the command line, which initializes Git in this directory and change the directory into a repository. (_Note_: This is only being done once at the beginning)
4. Create a file, it can be a `README.md`, by typing the command `touch <file.extension>` to create an empty file. Open the file in a new tab by typing `c9 <file>` into the command line
5. (_Optional, but recommended_) Type `git status` in the command lineto check what files or changes are needed to be added to the staging area.
6. Type `git add <file>` or `git add .` (only when there is one file in the repository) to add the file that was created to the staging area inorder to commit.
7. After the file is being added to the stage, type `git commit -m "message"` in the command line to commit the code. In other words, this command takes a "snapshot" of the code.
8. Go to [Github.com](https://github.com/) and log into GitHub account
9. Click the "+" sign next to profile picture and click "New repository"
[insert image]
10. Name the repository EXACTLY the same as the name of the directory/repository on Git and create repository.
[insert image]
11. Make sure SSH is selected for the URL
12. Copy the two lines of code one at a time and paste it into the command line to connect the repository to the remote
[insert image]
* 


---
## Workflow & Commands
The ongoing workflow 









