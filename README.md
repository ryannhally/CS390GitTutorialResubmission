# Welcome!
Welcome to my Git from the command line tutorial!

Git is a **version control system** for developers. In other words, Git allows you to manage changes to code. Once you master Git, you will be able to use it to track changes to your code and collaborate more easily with other developers, among other things.

In this tutorial we will cover the basics of using Git from the command line. You will learn how to...
* Create a repository
* Add files to the repository
* Commit changes
* Branch
* Merge
* Stash

## Getting Started
### Requirements 
First, there are a few things you will need in order to successfully complete this tutorial.
1. A Mac

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Since this is a tutorial on using Git from the command line, we will be interacting with Git and the files we create through  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; commands. The commands featured in this tutorial are compatible with terminal on Mac. For resources on using Git with other operating 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; systems, please see here: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

2. Have GIT installed

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Of course, to use Git we will need to have Git! If you don't already have Git installed or aren't sure, please see the "Install Git" 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; section below.

3. A text editor

## Some notes on this tutorial

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; There are several points in this tutorial where you will need to give your files, folders, etc. names. I will use all capital letters 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; to indicate what part of the command should be replaced with a name of your choice. In the following example,
```
mkdir FILENAME
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; the all capital letters of FILENAME indicate it is the part where you will enter the name of your file.


### Install GIT

1. Open terminal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; First, you will need to open up terminal.
  
2. Install Git <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you aren't sure whether or not you've installed Git, you can check to see if it is already installed by running
   ```
   git --version
   ```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you don't already have Git installed, click [here](https://docs.gitlab.com/ee/topics/git/how_to_install_git/index.html) for a &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; tutorial on how to install.

### Set up Git 
3. Pick a username

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; First, we will need to pick and enter a Git username. Once you have picked a username, run the following command to set it:

```
git config --global user.name "USER NAME"
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Note - the use of "global" means you are setting this as your username for all of your repositories.

4. Set your email address

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; For this tutorial we will need to select an email address to be associated with the changes we make to Github. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This should be the same email address that is associated with your Github account. Run

```
git config --global user.email "EMAIL ADDRESS"
```

## Creating a local repostiory
First, we will create a **local** repository. 

Git can be used to manage both **local** and **remote** repositories. **Local** repositories live on your computer while **remote** repositories are kept on a server. If you'd like to collaborate with others on your code or access it if your computer breaks, it's important to be able to use remote repositories. In this tutorial, we will create a local repository and **push** (transfer local commits to a remote repo) changes to a Github repo. 

### Create a local repository

create fold mkdir
move into folder cd
Move to the folder you'd like your project to be stored in and run
```
git init
```
You've created a local respository!


## Adding files to your repository
### Create a file
Before you create a file, make sure you have moved into the folder you want the file stored in. Then create the file with the touch command

```
touch FILENAME.text
```

### Add the file to the staging enviornment
Just because you've created a file does not mean Git is tracking changes to the file! You must add the file to the **staging enviornment** or **index**. This is where Git tracks what will go into your next **commit** (next up).
Run:

```
git add FILENAME
```
Now the file is in our staging enviornment. 

## Commiting changes
Now that we've created a file and Git is tracking the changes we make to it, we can start to **commit**. Making a commit is like saving changes on a word document. You are saving the current state of the code. Every commit has a **commit message**, which you can use to add a brief description of the changes you've made. Here is how to commit:

```
git commit -m "COMMIT MESSAGE"
```

## Commiting changes 

## Branching

### Create a branch
Say you want to focus in on changing a specific component of your code, like a feature. You might want to create a **branch** so you can work on it without affecting the rest of your code, and then combine it with the rest of your project once its finished. In summary, a branch is just a seperate version of the repository you can later combine with the main one (called the **main** branch). Here is a visual:

<img src="https://wac-cdn.atlassian.com/dam/jcr:a905ddfd-973a-452a-a4ae-f1dd65430027/01%20Git%20branch.svg?cdnVersion=1441"
     alt="Git Branch Diagram"
     style="float: left; margin-right: 10px;" />

     
To create a new branch run

```
git branch BRANCHNAME
```
You've created a branch!

### Switch to a branch
Just because you've created a branch doesn't mean you are working on that branch, ie, your changes are being commited to it and not the main branch. You will have to switch to the branch by running

```
git switch BRANCHNAME
```

The active branch is called the **head** branch. 

## Merging
When you've finished working on a branch, you can integrate it back with the main branch through **merging**. Be aware that when you merge, the entire commit history of the branch is added onto the main branch in just one commit. Here is a visual:
<img src="https://wac-cdn.atlassian.com/dam/jcr:c6db91c1-1343-4d45-8c93-bdba910b9506/02%20Branch-1%20kopiera.png?cdnVersion=1441"
     alt="Git Merge Diagram"
     style="float: left; margin-right: 10px;" />

### Check head
To merge a branch, first check that the head is pointed at the branch you'd like to merge with by running

```
git status
```

### Merge branches
If the head is pointed at the correct branch, run

```
git merge BRANCHNAME
```

## Stashing

### Stash changes
What if you wanted to save some changes you've made, but aren't quite ready to commit them? The answer to this is **stashing**. When you use the **stash** command, Git saves your changes but away from your working copy. All you need to do is run

```
git stash
```

### Pop changes
If you'd like to reapply the changes to your working copy, you can use **pop** to do so. Simply run

```
git stash pop
```
Note - this does not commmit the changes, it simply reapplies them to the working copy of the code.

## Conclusion

You've completed the tutorial! Now you know how to use create a repository, add files to it, commit the changes you've made, navigate branches, and stash. I hope you feel empowered to keep learning! Good luck!

