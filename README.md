# Frame Geak

## Set up git

### Installation

Download and install [git](https://git-scm.com/downloads) and set up a [Github](https://github.com/) account.
If you are on linux xou can use:

```bash
sudo apt-get install git
```

### Configuration

To configure git, open the git-bash on windows, or your console on linux and type in:

```bash
git config --global user.name USERNAME
git config --global user.email USER@MAIL
```

### Set up ssh
Crate a ssh-key:
```bash
ssh-keygen -t rsa -b 4096 -C "USER@MAIL"
ssh-add ~/.ssh/id_rsa
```
And copy the id_rsa.pub key (open it with any text-viewer) and paste is into your settings on Github

If you using windows, you can find your id in
```bash
C:\Users\name\.ssh
```
and on linux
```bash
~/.ssh/
```

## Using git
To use git you should either use preferably the git console, but if you scared of a productive workflow, you can also get a third party Software like [Gitkraken](https://www.gitkraken.com/).

#### clone a reposetory
On Github you will finde a [clone]() button, where you should make sure that you clone with [ssh]() and not [HTTPS]()!
```bash
git clone "git@github.com:repository-holder/your-repository-name"
```

### startup
Every time you start working on a shared reposetory, you should stash all your changes, pull from the repos, and then merge the stashed changes:

```bash
git stash       //stashes all changes
git pull        //pull newest commit
git stash pop   //merge stashed changes 
```

### commiting your changes
When you are ready with your work. repeat your startup procedure
```bash
git stash       
git pull        
git stash pop 

git add .                                          //add files to your commit
git commit -M "Short discription of your change."  //commit changes
git push                                           //push your changes to the repos
```

### add and switch branches
Checking for exesting local branches
```bash
git branch
```
add a new branch
```bash
git branch NAME
```
change the branch
```bash
git checkout NAME
```
set upstream
```bash
git push --set-upstream origin NAME
```
