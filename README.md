---
tags: setup, environment, bash
languages: ruby, bash
---

#Environment Setup

The wizards at Flatiron Labs made a script to set up your machine for development. Checkout the main page [here](https://github.com/flatiron-school/environmentalizer). While getting started this is how we will set up our development environment.

## Getting Started
The first thing you will need to do is install [Xcode](https://developer.apple.com/xcode/) and the command line tools (now a part of Xcode!). Once you've done that read ["What you need before you begin"](https://github.com/flatiron-school/environmentalizer#what-you-need-before-you-begin) and make sure you have the information you will need on hand. Now that you have done all that lets actually learn what the environmentalizer will do.


##What Will the Environmentalizer do?
Running the environmentalizer will make changes to several areas of your system to prepare it for all the development you are about to do. Below you will find the aspects of your computer that will be changed and what those changes will do!

###Changes in:
+ [File Directory](#File-Directory)
+ [.bash_profile](#.bash-profile)
+ [Homebrew](#Homebrew)
+ [GIT](#GIT)
+ [SQLITE3](#SQLITE3)
+ [RVM](#RVM)
+ [The Learn Gem](#The-Learn-Gem)
+ [Sublime Text](#Sublime-Text)
+ [Sensible](#Sensible)
+ [Symlinks](#Symlinks)
+ [SSH Key](#SSH-Key)
+ [Google Chrome](#Google-Chrome)

<a name="File-Directory"/>
####File Directory
The changes here are simple, the environmentalizer adds a "Development" folder to the root of your home directory. This gives you a place to organize your code.
Here are a few tips for setting up your directories:
..+Except for directories in ~, always use lowercase directory names.
..+Prefer - to _ or to separate words in directory names.
..+Keep all code in one place.
..+Have a place for resources and other things that are related to code, but aren't code.
..+Be able to get in/out of different code projects easily.

<a name=".bash-profile"/>
####.bash_profile
Your bash_profile is a script that runs every time you open or login to your shell. It can configure environment variables, like your `PS1`, which stores your prompt, or `EDITOR`, which is the command other programs will use when they need to launch your default editor.

You can also create aliases for common commands so that they are shorter to use.

And finally, you can also build functions to simplify common workflows.

The environmentalizer installs the [Flatiron Bash Profile](https://github.com/flatiron-school/dotfiles/blob/master/bash_profile) for you!

Within that Bash Profile are comments that explain each part. **Make sure to read them!** You can always comment sections in/out to see what they do and how they effect your prompt, shell, and environment.

Just remember, to activate a change in the dotfile, you must **reload your shell**. You can do that via opening a new tab or typing `source .bash_profile` (from the `~` directory).

<a name="Homebrew"/>
####Homebrew
[Homebrew](http://brew.sh/) is a package manager for OSX. Not only will it help you install packages via commands like `brew install wget` but it will also organize the packages you install and add the appropriate locations to your path. As if that weren't enough Homebrew can also be used to ensure your system is healthy. Commands like `brew doctor` will help you gague the health of your system and often provide suggestions for how to fix problems. 

<a name="GIT"/>
####GIT
[GIT](http://en.wikipedia.org/wiki/Git_%28software%29) is the most widely used revision control system in the world. Read about it, YOU WILL USE IT ALOT! In conjugation with GitHub you will be able to use it to keep up to date versions of all your projects, standardize code bases with project groups, roll back changes you decide you don't like, and so much more.

<a name="SQLITE3"/>
####SQLITE3
[SQLITE3](http://en.wikipedia.org/wiki/SQLite) is a relational database system. It uses standard SQL Query language and is a great place to start experimenting with databases. While will use other databases later on SQLITE3 is a great place to start. 

<a name="RVM"/>
####RVM
[RVM](https://rvm.io/) is short for Ruby Version manager and after it is installed you can use it to keep track of and change between the various versions of Ruby installed on your computer with commands like `rvm list` and `rvm use 2.2.1`. RVM can also do a lot more so feel free to explore!

<a name="The-Learn-Gem"/>
####The Learn Gem
This will install the Flatiron Learn Gem and it's dependencies, which you will use to test your labs and make sure you have done everythign correctly. Specifically 

<a name="Sublime-Text"/>
####Sublime Text
[Sublime Text](http://www.sublimetext.com/) is the text editor we use at the flatiron school. The environmentalizer installs Sublime Text with a package manager so you can install cool themes and useful add-ons like the [Brogrammer Theme](https://github.com/kenwheeler/brogrammer-theme) or [Bracket Highlighter](https://github.com/facelessuser/BracketHighlighter). Make sure you take the time to set it up how you like because you will be spending a lot of time in it!

<a name="Sensible"/>
####Sensible
Like the `.bash_profile` these are scripts and configuration files that work in different areas. You should read through them all to see the specifics of what they are doing. Each has a specific purpos and works for different things. 
+ `.gitconfig` will contain the settings that you will take advantage of when employing git in your command line. 
+ `.gitignore` is a collection of files that you want git to ignore. Some files that you don't want git to track including, but not limited to, `.DSstore` and `.env`.
+ `.gemrc` Another settings file, this time for your your interaction with ruby gems.
+ `.irbrc` IRB stands for "Interactive Ruby Shell" by typing the command `irb` in your command line you can open up a ruby shell and write ruby code directly in your terminal. The `.irbc` file will contain any custom settings for your use of IRB.
Remember to look through all of these files to see exactly what settings they have installed on your computer.

<a name="Symlinks"/>
####Symlinks
Symlink stands for "Symbolic Link" Homebrew will create some symlinks for you, the environmentalizer will create others, and you can later create more. A symlink is like a shortcut in command line. It will allow you to type something like `desktop` in bash to `cd` from any file directory to the desktop. It can also be used as a command, for example you will often find yourself typing `subl .` to open up the current file directory in Sublime Text. 

<a name="SSH-Key"/>
####SSH Key
SSH keys serve as a means to identify yourself to and SSH server using a public key and a response authentication. This means that you will be able to identify yourself to a server without entering a password. In this case they public key you got from GitHub before you started and the key the environmentalizer sets up will work to let you access your GitHub account without entering a password each time. 

<a name="Google-Chrome"/>
####Google Chrome
Google Chrome is a Web Browser, we suggest you use it when developing in rails.

##The Environmentalizer Install
Remember to read [these instructions](https://github.com/flatiron-school/environmentalizer#what-you-need-before-you-begin) and make sure you have all the informaiton you will need on hand. 

To get everything started just copy the following code into your terminal (with an account that has administrator access)
`curl -L "https://raw.githubusercontent.com/flatiron-school/environmentalizer/master/runner.sh" | bash`

Sit back, remember to enter your password when prompted and watch out for errors!
