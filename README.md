# GitHub and GIT Basic Guide

## Prerequisites

1. GIT
2. github account

## Ways to use git

1. Command Line
2. Tools like gitKraken

## Setting up with Git

1. Set Username

```bash
git config --<system_flag~~> user.name "<name>"
```

2. Set email

```bash
git config --<system_flag> user.email "<user_email>"
```

System flag can be set as:

- local : Repository-specific settings
- global : User-specific settings. This is where options set with the --global flag are restored.
- System : System-wide settings

### Example for setting config for the github

Create a shortcut for a Git command.
This is a powerful utility to create custom shortcuts for commonly used git commands.
A simplistic example would be

```bash
git config --global alias.ci commit
```

Now instead of "git commit", I can do "git ci" to start commit my changes.

## Copy a git repo

```bash
git clone <link_to_github_repo>
```

Example : We want to copy this demo repo

1. click on the Code.
2. Make sure you have selected the HTML option[1]
3. copy the link in the textbox
4. Run the following command in the terminal.

<img src="./imgs/sakshambedifinal-project-3380 COMP3380 final project fall 2020 httpwww.cs.umanitoba.ca~kleungcomp3380indexAll.html.png" style="width:75%;padding:10px">

```bash
git clone https://github.com/sakshambedi/final_project_3380.git
```

You have successfully copied the repo to your local machine.

## Making a new Repo

1. Open the working directory in the terminal
2. Initiate a repo

```bash
git init
```

3. Make a git ignore file. A git ignore is a simple file used to disregard files that are not useful to share. You can download a git ignore template from github's [gitignore](https://github.com/github/gitignore) link, depending upon the type of project the user is working on. [More info on git ignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore).
4. Make a README.md file (optional)
5. Use "add" to add all the files you want to start keeping track of. -A flag = ALL which means it will add all the files except the ones mentioned in the .gitignore

```bash
git add -A
```

5. Commit your changes with the commit command. Use the -m = Message to add a message for the commit for reference.

```bash
git commit -m "<your message here>"
```

6. Now go to github and login into your account.
7. Click on ["NEW"](https://github.com/new) button on the top left. Give it a name, description (optional)  and access (Private/Public). You do not need to a README.md file and a gitignore file. Choose a license if necessary and click "Create Repository"
8. Now you can push the local code to the existing repository on github. To do so follow the instructions in the "push an existing repository from the command line : "

<img src="./imgs/github_instructions.jpg" style="padding:10px; width:75%; align=center">

## Creating a new branch

```bash
git checkout -b <name_of_new_branch>
```

<img src="./imgs/make-new-branch.png" style="padding:10px; width:75%; align=center">

This how you create a new  branch.

## How branching works

Branching in github can be really useful to work in team without disturbing the production code.
[GUIDE TO BRANCHING](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

## Change working branch

```bash
git checkout <branch_name>
```

**NOTE :** Using the -b flag will create a new branch.
