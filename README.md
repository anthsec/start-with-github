# Learn how to use git & github



## 0 Introduction

I am a personal code enthusiast, it's the first time I started learning git. I can not ensure all the guides bellow are correct.

I am will to update this document from time to time if I found some problems.

## 1 Download and Install Git

This is very simple, and I won't go into details here.

## 2 Add User and Setup SSH

### 2.1 Add User

```bash
#add your github user name
git config --global user.name "anthony"
#add your github sign-in email address
git config --global user.email anthony@somewhere.com
```

### 2.2 Setup SSH

[Something Unimportant]

Where is .SSH direction of MAC OS? [/Users/anthony/.ssh]
If it's invisible, you can press [command]+[shift]+[.]

```bash
#Create your SSH
ssh-keygen -t rsa -C "anthony@somewhere.com"
#Keep all the config default and press [Enter] three times
```

Now, you can copy what's showing on your terminal to Github https://github.com/settings/keys

You can test the connection via the command bellow

```bash
ssh -T git@github.com
```

## 3 Create Your First Git Project

### 3.1 Create a new repository on Github

```bash
#…or create a new repository on the command line
echo "# start-git" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/anthsec/start-git.git
git push -u origin main
#…or push an existing repository from the command line
git remote add origin https://github.com/anthsec/start-git.git
git branch -M main
git push -u origin main
```

### 3.2 Create a local repository and connect to remote repository

```bash
cd git
#Create an .gitignore file to tell git files you don't want to upload
#If you want to ignore .DS_Store on Mac, just add a line ".DS_Store" in the file ".gitignore"
touch .gitignore
#Create a git init
git init
#Create a branch
git branch -M main
#Add an origin to tell where is remote repository
git remote add origin https://github.com/anthsec/start-git.git

#Then, write some codes or files. After that.
git add .
git commit -m "message"

#Push your code to remote repositroy
#First time or if you want push to another branch, use command bellow
git push -u origin main
#Second time or if you do not want to change the branch
git push
```

## 4 Some Useful Commands (update at any time)

```bash
#[Common]
#pull from github
git pull [url]

#Clear cache and change status to untrack (maybe it's wrong)
git rm -r --cached .
git add .
git commit -m "message"

#[New Branch]
#Show current branch
git branch
#Create local branch and switch to new branch
git checkout -b dev
#push new branch to github
git push origin HEAD -u
```

## 5 Update Log

```
2022.4.22 Create this document
...
```

