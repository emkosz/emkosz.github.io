---
layout: post
title: Getting friendly with the command line
excerpt: "A cheat sheet to understand the basics of using the terminal"
modified:
tags: [command line, terminal, intro, beginner, tutorial]
comments: true
---
This post is about how to use the terminal on a Mac OS computer.

One huge thing for me while learning to program was to get comfortable using the
terminal. It's empowering and fun. This post will go through some of the most basic things to know about.

### What a terminal is

Before using a terminal most people are used to graphical interfaces. Like the Finder for example. You can go into folders by clicking them and see the content of more folders and files within that folder. The terminal allows you to open, create, modify folders and files by giving text commands instead. By using the terminal to move around in different folders I found that I got a better understanding of the computers hierarchy. It's a helpful start of doing even more powerful things. I want to share a few simple tricks that helped me.

### How to open a new terminal window

The first thing you want to do is to open a new terminal window. The fastest way is to use spotlight search. Hit the magnifying glass in the upper right corner or hit the keyboard short cut. Mine is control space. Write `terminal` — it should be the first hit. You could also find the Terminal by opening a new Finder window and go into Applications and then Utilities.

### Starting off with some basic commands

When opening a new terminal window you are going to be in your home directory. The first command often taught is to change directory with the command `cd`. A directory is the same thing as a folder so you basically give the computer the same command with `cd` as when you click a folder in the Finder's graphical interface.

The `cd` command must be followed by the name of the directory you want to go to.
The directory you want tot go to must also be within the current directory. Let’s say I wanted to go to the `Desktop` from my home directory I will type `cd Desktop` and press enter, like this. (Don’t type the dollar sign, it just represents the Terminal waiting for your input.)

{% highlight ruby %}
$ cd Desktop
{% endhighlight %}

The command will change the current directory so that I’m now in the directory
Desktop. To verify this i can type the command `pwd` that stands for print working directory.

{% highlight ruby %}
$ pwd
/Users/username/Desktop/
{% endhighlight %}

To view or list what is in this directory I can type the command `ls` that stands
for list — this will print all the folders and files within the directory. Try it out.

{% highlight ruby %}
$ ls
{% endhighlight %}

When I started using the terminal I always cd:ed into one directory, did an ls to see what folders and files that was stored in it and then cd:ed into
the next directory I wanted to go to. When you know the whole path
you can also type that without several `cd`s and `ls`. Type the order of the
folders separated by slash like this.

{% highlight ruby %}
$ cd Desktop/AwesomeFolder/AwesomePictures
{% endhighlight %}

This will bring you directly to the the `AwesomePictures` directory.

When developing, it is common to have a folder for development named development or dev for short or source or as in my case src.

Let's go ahead and create a directory like that. First you want to get out of the Desktop directory though. You want to create this new folder in your home directory. Two periods takes you back one step and cd without anything else will always take you to your home directory. Type this into your terminal.

{% highlight ruby %}
$ cd
$ mkdir Development
{% endhighlight %}

`mkdir` is short for make a new directory, that is, making a new folder.
A new directory with the name Development is now created. The new folder is completely empty. How about creating a new file to it.

{% highlight ruby %}
$ touch Development/test.rb
{% endhighlight %}

The `Development/` tells the computer where to store the file. The filename and extension creates a file. Yay! Now you have a file in your Development directory. But let's say you don't like the name of the new file. Well you can rename it. `cd` into the directory first for simplicity.

{% highlight ruby %}
$ cd Development
$ mv test.rb testing.rb
{% endhighlight %}

The first word after `mv` defines the file, the second one defines the new name. Now the file is named `testing.rb`.

You can also move files with `mv` which actually is short for move. You will need to specify where the file should be moved. Try moving the `testing.rb` file to the Desktop by typing the following command.

{% highlight ruby %}
$ mv testing.rb ~/Desktop/testing.rb
{% endhighlight %}

The `~` (tilde) sign represents the home directory followed by the path to the Desktop followed by the name of the file.

If you have made it this far you have now learned how to move around in the computers hierarchy with the command `cd` and `..` for going backwards. You have learned to create a new folder and a file as well as renaming and moving that file. Good job :D
