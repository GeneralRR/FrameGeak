# Frame Geak

Alle Rechtschreibfehler sind nur zum Belustigen der Massen gedacht und haben keinen weiteren Zweck zu erfüllen.®

## The Plan!
The goal of this project is the creation of a handheld console.

## Hardware
The inital setup is a [ATMega5260](https://www.microchip.com/wwwproducts/en/ATmega2560) 8-Bit chip on an [Arduino](https://www.elegoo.com/product/elegoo-mega-2560-r3-board-atmega2560-atmega16u2-usb-cable/) platform. Maybe we will try cross Platform support later but for an easier start, we chould stick with one platform

### Peripherals
Peripherals like a WLAN-module for comminication or ultrasonic sensor could be addet while developement.

### Casing
Case and Controller design could be also integrated in this Project

## OS and Drivers

We plan to write a full custom OS with intigrated security features an custom driver support

### Graphics driver/renderer
Because of the limitations of the hardware, we have to find clever solution to overcome the shortcomings of the [display](https://www.elegoo.com/product/elegoo-uno-r3-2-8-inches-tft-touch-screen/), like a grid renderer, which goal should be to push as few pixel changes as possible to the display.

## Games and Software
You are free to offer Game ideas, let your creativity flow. The only limitation here will be the display and the rendering solution, if the drivers-team cannot create a effizent rendering solution, the games have to addabt to the limitation of the screen to garantee an enjoyable experience.

## Other possible sub-projects
Software testing, validation, artisic design or creating a website, there are many other areas, which could be tackled.

# Game Ideas

## Pokemon remake
A reimagend Pokemongame, where the mechanics could be tweaked or new features addet.

## Werwolf
The Digital Assistent for the infamous [POKERABEND]() to help coordinate and manage the increasing complicated and complex sozial game structure.

# Git "Tutorial"

## Installation

Download and install [git](https://git-scm.com/downloads) and set up a [Github](https://github.com/) account.
If you are on linux xou can use:

```bash
sudo apt-get install git
```

## Configuration

To configure git, open the git-bash on windows, or your console on linux and type in:

```bash
git config --global user.name USERNAME
git config --global user.email USER@MAIL
```

## Set up ssh
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

### clone a reposetory
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
