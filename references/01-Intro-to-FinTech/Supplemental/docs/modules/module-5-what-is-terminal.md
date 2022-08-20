# Module 5: What Is the Terminal?

## Introduction

The terminal is a place where you can interact with your computer through text. Have you ever right-clicked on your desktop to create a new folder (aka directory)? You can do that in the terminal with a simple text command. Have you ever double-clicked a folder to access a file inside? There's a command for that as well! And how about deleting directories, creating files, finding files, and moving files from one directory to another? All of these actions are easy to do from your terminal with just a few keywords. 

_**Why would I want to use the terminal?**_

The terminal will quickly become a key tool in your tool belt. It will allow you to navigate more quickly and interact with your machine in more sophisticated ways (which will impress your friends and convince them you're a super savvy hacker). More importantly, using the terminal is a necessary skill for interacting with some of the tools we'll be using throughout the course. 

**_What's Git Bash?_** 

While Terminal is the command-line tool for Macs, Windows has its own command-line tools, Command Prompt and Git Bash. On Windows machines, you can perform most actions from either Git Bash or Command Prompt, but the commands themselves are different—kind of like how you can express the same sentiment in English or Spanish, but the words differ.

Git Bash allows Windows users to use the same commands and tooling as Linux/Unix, which is another operating system like Windows or MacOS. Git Bash can be helpful if your team is deploying code to a Linux server. In this course we'll be using Linux-style commands, so you'll need Git Bash to execute them. (But we won't judge you if you decide to use Command Prompt after the course!)  

---

## A Closer Look at the Terminal

Terminal and Git Bash allow you to interact with your computer via text only.

Creating directories and files on your computer through the terminal is more efficient than creating them through the graphical interface. The terminal will also be a vital tool when we start to use version control software, which we'll learn about shortly.

Using the terminal may feel clunky at first, but, with practice, it will make navigation of your directories and files much easier, as well as allow you to interact with some of our technologies.

_**How can I perform simple operations with the terminal?**_

The following list is a cheat sheet for the most commonly used terminal commands. There are many others, but we'll focus on these for now.

* `cd` changes directory

* `cd ~` changes to home directory
  
* `cd ..` moves up one directory

* `ls` lists files in folder

* `pwd` shows current directory

* `mkdir <FOLDERNAME>` creates new directory

* `touch <FILENAME>` creates a file

* `open .` opens the current folder (Mac only) 

* `explorer .` opens a specific file (Windows only)

When typing a file or directory name, we can use the Tab key to auto-complete that file or directory name. Auto-completion only works when we have a _unique_ file or directory name that matches.

---

## Practice

_**What if I want to practice these commands?**_ 

Then you are exactly the kind of student we are looking for: hungry for knowledge and eager to get your hands dirty! 

[This handy video](https://www.youtube.com/watch?v=hor7miwput0) walks you through the following steps.

Open Terminal or Git Bash and do the following, using only the command line:

1. Navigate to your desktop or directory: `cd Desktop`

1. Create a new directory named _test_: `mkdir test`

    **Note:** When naming your directories and files, we recommend using underscores in place of spaces. So, for example, instead of naming a directory `terminal prework`, name it `terminal_prework`.

1. Create a new text file named _sample_: `touch sample.txt`

1. Navigate into the test directory: `cd test`

1. Check the contents of the directory (it should be empty): `ls`

1. Navigate back to your desktop: `cd ..`

1. Move the _sample.txt_ file into the test directory: `mv sample.txt test`

1. Make sure the previous action was successful. Use `cd test`, press **Enter**, and then use `ls`. 

1. Time for some independent learning! Using Google, find a way to rename the _sample.txt_ file to _example.txt_.

Pat yourself on the back! You just took your first steps toward becoming a developer. 

## Prework Support

Looking for pre-work support? Our team of tutors are eager to help! Request a tutor session with the following steps:

1. If not already logged in to BCS, login using your credentials ***(supplied 24 hours after enrollment).***
2. Click **Support** in the top right.
3. Complete the form fields to submit your request:
   * Under **Question Category**, select "Tutor Request”
   * Under **Question Category**, select "Request a Tutor”
   * Under **Currently, Which Sessions Would You Like to Discuss?**, select “Prework assignment”. 
4. Complete the additional fields and submit your request. 
