# GitHub Tutorial

_by Kelly Lai_

---
## Git vs. GitHub
**Git** - keeps track of a timeline of "snapshots" or commits that developers have made in their file while working on the project during specific times.
* Allows developers to refer back to the code that they have already written and apply additional changes or debug the code to make it functional
* Allows developers to organize different directories and files
* Runs in the Command Line 
* Git **DOES NOT** require Github 

**GitHub** - stores the code that developers have written on the local machine, the computer, into the cloud, also know as the internet or the website ([Github.com](https://github.com/))
* Allows multiple developers to contribute and collaborate on files easily
* Allows developers to visually track changes that other developers made
* Also runs in the Command Line
* GitHub **REQUIRES** Git

---
## Initial Setup
#### To create a GitHub account  
1. Go to [Github.com](https://github.com/)
2. Press the green sign up button on the top right corner  
![Sign Up](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/1.PNG?_c9_id=livepreview8&_c9_host=https://ide.c9.io)   
3. Insert personal information
* Username and Password should be the same username and password as hstat email  
![Insert Info](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/2.PNG?_c9_id=livepreview0&_c9_host=https://ide.c9.io)      
* Press the Green button for the next two pages
4. When finish signing up, check email and verify with Github 

#### To set up SSH key   
(_Note_: It is better to use the SSH rather than the HTTPS because SSH only requires one-time setup while HTTPS requires to enter login info every time)  
1. Log into [Cloud9](https://c9.io) with Github account   
2. Follow the following steps:
![Copy SSH key](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/9.PNG?_c9_id=livepreview11&_c9_host=https://ide.c9.io)
3. Go to [Github.com](https://github.com/)  
4. On the top-right corner, click the profile image and go to settings  
![Settings](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/3.PNG?_c9_id=livepreview13&_c9_host=https://ide.c9.io)  
5.Follow the following steps:    
![New SSH Key](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/10.PNG?_c9_id=livepreview12&_c9_host=https://ide.c9.io)  
6. Go back to to c9 and open github-learning IDE  
7. Enter `ssh -T git@github.com` into the command line and `Hi <username>! You've successfully authenticated, but GitHub does not provide shell access.` will appear.

---
## Repository Setup
1. Type the command `cd ~/workspace` on the command line after logging into c9, which goes directly to the home folder. In this case, the highest we can go is `/workspace`.  
(_Note_: To open the Terminal in c9, click "Window" and then click "New Terminal") 
2. Type `mkdir <directoryname>` to create a new directory under the home folder.
3. Move into the directory by typing `cd <directoryname>`.
4. Once inside the directory, type the command `git init` on the command line, which initializes Git in this directory and change the directory into a repository. (_Note_: This is only being done once at the beginning and notice that (Master) will appear next to the name of the directory when initialized successfully)
    * If `git init` was use in the wrong directory, this can be fixed by typing `rm -rf .git` to uninitialize Git recursively and forcefully. 
5. Create a file, it can be a `README.md`, by typing the command `touch <file.extension>` to create an empty file. Open the file in a new tab by typing `c9 <file>` into the command line
6. (_Optional, but recommended_) Type `git status` in the command lineto check what files or changes are needed to be added to the staging area.
7. Type `git add <file>` or `git add .` (Includes all changed files in current directory) to add the file that was created to the staging area in order to commit.  
(_Note_: Type the command `git reset HEAD <file>` to unstage a file)
8. After the file is being added to the stage, type `git commit -m "message"` in the command line to commit the code. In other words, this command takes a "snapshot" of the code and the message describe the changes in a short, present-tense, and specific way.
9. Go to [Github.com](https://github.com/) and log into GitHub account
10. Click the "+" sign next to profile picture and click "New repository"  
![Create New Repo](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/5.PNG?_c9_id=livepreview7&_c9_host=https://ide.c9.io)
11. Name the repository **EXACTLY** the same as the name of the directory/repository on Git and click "Create repository".  
![Create repo](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/6.PNG?_c9_id=livepreview6&_c9_host=https://ide.c9.io)
12. Make sure SSH is selected for the URL
13. Copy the two lines of code one at a time and paste it into the command line to connect the repository to the remote    
It should look like this:    
```
git remote add origin git@github.com:[username]/repo-name.git 
//sets up a connection between local repo and repo located in Github and adds remote to a certain location[URL]
git push -u origin master
//push commits to main branch and git remembers to push to orgin master once "git push" is typed
```
 
---

_Note_: Type `rm -rf <repositoryname>` to remove a repository completely (Local & Remote)

---
## Workflow & Commands
#### **Ongoing Workflow For Git** 
* Type `cd <file.extension>` to move into the file and type `c9 <file.extension>` to open the file and edit the file.  
(_Note_: Make sure to turn on Auto-save or press Ctrl+S)
* (_Optional_) Type `git status`, which displays the files that have been edited since the last commit.
  * This will appear in RED
* Type `git add <file.extension>` or `git add .`(Adds all changed file in current directory) to put the files on the stage, so the files are ready to commit.
* (_Optional, Recommended_) Type `git status` to view the files that are staged and ready to commit
  * This will appear in GREEN 
* Type `git commit -m "message"` to commit the files or take a "snapshot" of the code
  * The message should be written in present-tense, short, and specifically describe the changes made in the file
* Type `git push` to send the commits that were made from the local repository (Computer) to the remote repository (Github).
  * It should look like this:
  ```bash
  <username>:~/workspace/github-tutorial (master) $ git push
  Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
  Counting objects: 3, done.
  Delta compression using up to 8 threads.
  Compressing objects: 100% (3/3), done.
  Writing objects: 100% (3/3), 445 bytes | 0 bytes/s, done.
  Total 3 (delta 2), reused 0 (delta 0)
  remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
  To github.com:<username>/github-tutorial.git
   f02e2fe..3e525a8  master -> master
  ```
  
---
## Collaboration 
#### Fork and Clone
* **Fork** - When forking someone else's repository, it gives developers a remote copy of that person's remote repository. Now, the developer is given the permission to clone the remote to their own computer and able to push changes to their remote.
* **Clone** - When cloning someone else's repository, it creates a copy of that person's remote repository in the developer's computer. The command for cloning a repository is `git clone <URL>`, copy the SSH clone URL and paste it after `git clone`.(_Note_: make sure to `cd` into the directory after cloning it) However, the developer is not given the permisson to push their changes into that person's remote. In order to push changes, the developer must send a **pull request** and have the owner of the remote repository accept the request. Once the pull rquest is approved, the owner of the remote repository can now use the command `git pull` to view or edit the developer's changes in their own computer.  
**How to Fork and Clone:**  
![Steps to Fork&Clone](https://preview.c9users.io/zhiyinl5633/github-learning/github-tutorial/8.PNG?_c9_id=livepreview10&_c9_host=https://ide.c9.io)  
**How to Send Pull Requests:**   
 1. Fork and clone the repository
 2. Make changes to the files
 3. Save, Add, Commit, Push
 4. Go to the repository and click on "New pull request" and then click the green button, "Create pull request"
