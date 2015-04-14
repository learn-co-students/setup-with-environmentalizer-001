---
tags: setup, environment, bash
languages: ruby, bash
---

#Environment Setup

The wizards at Flatiron Labs made a script to set up your machine for development. Checkout the main page [here](https://github.com/flatiron-school/environmentalizer). While getting started, this is how we will set up our development environment.

## Getting Started
The first thing you will need to do is install [Xcode](https://developer.apple.com/xcode/) and the command line tools (now part of Xcode!). Once you've done that, read ["What you need before you begin"](https://github.com/flatiron-school/environmentalizer#what-you-need-before-you-begin) and make sure you have the information you will need on hand. Now that you are ready, let's actually learn what the environmentalizer will do.


##What Will the Environmentalizer do?
Running the environmentalizer will make changes to your system to prepare it for all the development you are about to do. Below you will find the aspects of your computer that will be changed and what those changes will do!

###Changes in:
+ [File Directory](#file-directory)
+ [.bash_profile](#bash_profile)
+ [Homebrew](#homebrew)
+ [Git](#git)
+ [Sqlite3](#sqlite3)
+ [RVM](#rvm)
+ [The Learn Gem](#the-learn-gem)
+ [Sublime Text](#sublime-text)
+ [Sensible Defaults](#sensible-defaults)
+ [Symlinks](#symlinks)
+ [SSH Key](#ssh-key)
+ [Google Chrome](#google-chrome)

#### File Directory
The changes here are simple. The Environmentalizer adds a "Development" folder to the root of your home directory. This gives you a place to organize your code.

Here are a few tips for setting up your directories:
..+When creating directories, except for directories in ~ (the home directory), always use lowercase directory names for ease of access.
..+When creating directory names it is preferable to use a "-" instead of a "_" to denote spaces.
..+Keep all code in one place so you can access it easily.
..+Make sure you have another directory to keep your resourcesand other things that are related to code, but aren't code here you might keep your local copy of [The markdown cheetsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links) or other documentation.
..+Remember to build your folder structure so you can easily navigate in and out of your project directories. 

#### .bash_profile
Your .bash_profile is a script that runs every time you open or login to your shell. It can configure environment variables, like your `PS1` (which stores your command prompt), or `EDITOR` (which is the command other programs will use when they need to launch your default editor).

You can also create aliases for common commands so that they are shorter to use.

And finally, you can also build functions to simplify common workflows.

The Environmentalizer installs the [Flatiron Bash Profile](https://github.com/flatiron-school/dotfiles/blob/master/bash_profile) for you!

Within that bash profile are comments that explain each part. **Make sure to read them!** You can always comment sections in/out to see what they do and how they effect your prompt, shell, and environment.

Just remember, to activate a change in the dotfile, you must **reload your shell**. You can do that via opening a new tab or typing `source .bash_profile` (from the `~` directory).

#### Homebrew
[Homebrew](http://brew.sh/) is a package manager for OSX. Not only will it help you install packages via commands like `brew install wget` but it will also organize the packages you install and add the appropriate locations to your path. As if that weren't enough, Homebrew also ensures that your system configurations are up to date. Commands like `brew doctor` will help you gauge the health of your system and often provide suggestions for how to fix problems. 

#### Git
[Git](http://en.wikipedia.org/wiki/Git_%28software%29) is the most widely used Version Control system in the world. Read about it, YOU WILL USE IT A LOT! In conjunction with GitHub, it will be used as a Version Control system for all of your projects as well as many other things you will learn.

#### Sqlite3
[Sqlite3](http://en.wikipedia.org/wiki/SQLite) is a relational database system. It uses standard SQL Query language and is a great place to start experimenting with databases. Although we will use other databases later on, Sqlite3 is a great place to start. 

#### RVM
[RVM](https://rvm.io/) is short for Ruby Version Manager. After it is installed, it manages and keeps track of the various versions of Ruby installed on your machine. You're able to view the different Ruby versions in your Terminal with commands like 'rvm list' and 'rvm use 2.2.1'. You can also do a lot more so feel free to explore.

#### The Learn Gem
This will install the Flatiron Learn Gem and its dependencies, which you will use to test your labs and make sure you have done everything correctly.

#### Sublime Text
[Sublime Text](http://www.sublimetext.com/) is the text editor we use at The Flatiron School. The Environmentalizer installs Sublime Text with a package manager so you can install cool themes and useful add-ons, like the [Brogrammer Theme](https://github.com/kenwheeler/brogrammer-theme) and [Bracket Highlighter](https://github.com/facelessuser/BracketHighlighter). Make sure you take the time to set it up to your liking, because you will be spending a lot of time with it!

#### Sensible Defaults
Like the `.bash_profile` these are scripts and configuration files that work in different areas. You should read through them all to see the specifics of what they are doing. Each has a specific purpose and works for different things. 
+ `.gitconfig` will contain the settings that you will take advantage of when employing git in your command line. 
+ `.gitignore` is a collection of files that you want git to ignore. Some files that you don't want git to track including, but not limited to, `.DS_Store` and `.env`.
+ `.gemrc` Another settings file, this time for your your interaction with ruby gems.
+ `.irbrc` IRB stands for "Interactive Ruby Shell". By typing the command `irb` in your command line you can open up a ruby shell and write ruby code directly in your terminal. The `.irbc` file will contain any custom settings for your use of IRB.

Remember to look through all of these files to see exactly what settings each contains and learn what effect they have on your computer. 

#### Symlinks
Symlink stands for "Symbolic Link". A symlink is represented as a text string that the is automatically interpreted by the operating system as as a path to another file or directory. In other words a symlink is like a shortcut to another location. One will allow you to type something like `desktop` in bash to `cd` from any file directory to the desktop. It can also be used as a command, for example you will often find yourself typing `subl .` to open up the current file directory in Sublime Text. This is because the text `desktop` is symbolically linked to the desktop path ("~/Desktop") and `subl` is symbolically linked to the location on your computer where Sublime Text is stored. Some symlinks will be installed by Homebrew and others will be installed by the Environmentalizer. However, to really make your computer your own, look into creating your own!

#### SSH Key
SSH stands for "Secure Shell". It is a command interface for communicating with secure servers. SSH keys serve as a means to identify yourself to a SSH server. To set up proper SSH Key Authentication you need a public key (like the one you got from GitHub) and a private key (which will be generated when the Environmentalizer runs). The private key on your computer will allow you to access the Github server with the public key without having to enter a password. 

#### Google Chrome
Google Chrome is a Web Browser, we suggest you use it when developing in rails.

## The Environmentalizer Install
Remember to read [these instructions](https://github.com/flatiron-school/environmentalizer#what-you-need-before-you-begin) and make sure you have all the informaiton you'll need on hand. 

To get everything started, just copy the following code into your Terminal (with an account that has administrator access)
`curl -L "https://raw.githubusercontent.com/flatiron-school/environmentalizer/master/runner.sh" | bash`

Sit back, remember to enter your password when prompted, and watch out for errors!
