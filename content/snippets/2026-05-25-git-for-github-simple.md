---
title: "Git for GitHub: How to use simple Git commands to manage a GitHub repository"
date: 2026-05-25T17:35:40-04:00
draft: true
desctiption: ""
tags: ["git", "github", "version-control", "simple"]
categories: ["engineering"]
showToc: true
TocOpen: false
comments: true
slug: "git-for-github-simple.md"
---


# Git for GitHub: How to use simple Git commands to manage a GitHub repository

Before learning how to manage your project, it helps to understand what Git actually is. Git is overwhelmingly the most popular version control system (VCS), and is completely free to use.

> "By far, the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel."
> - Source: [Atlassian](https://www.atlassian.com/git/tutorials/what-is-git)

In this guide, you will learn how to use the Git version control system (VCS) to manage a GitHub repository by initializing a project, linking it your GitHub repository, and using it to manage your GitHub repository.

## Section 1: Installing and Setting Up Git
In this section, we will navigate to our terminal and install Git.

### Step 1: Opening your terminal
- Windows: Press the `Windows Key`, type Powershell, and hit enter.
- macOS: Press `Cmd + Space`, type Terminal, and hit enter.
- Linux: Press `Ctrl + Alt + T` to open your default shell.

### Step 2: Installing Git
In your terminal, run the following command to determine if you have Git installed

```shell
git --version
```

- If a version number appears, you are ready to go to step 3.
- If the command is not recognized, follow the steps below to install Git.

Windows Installation:

To install Git on Windows, you can do so in one of the following ways.

1. Run the following command to install Git with Winget: `winget install --id Git.Git -e --source winget`
2. Run one of the standalone installers found at [Git-scm](https://git-scm.com/install/windows)


macOS Installation:

To install Git on macOS, you can do so by installing Git with homebrew.

If you do not have homebrew, install homebrew with the following command: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Once you have homebrew, run `brew install git` to install Git.

Linux Installation:

To install Git on Linux, use your distributions package manager.

- Debian/Ubuntu: `apt-get install git`
- Fedora: `dnf install git`
- Arch: `pacman -S git`


### Step 3: Setting up Git (Identity Configuration)

The next step to using git is to set variables that let Git know who you are. These are permanently attached to every commit you do, which allows platforms like GitHub to attack it to your profile card.

```shell
# Set your display name (can be your real name, your GitHub username, or many other things)
git config --global user.name "Your Name"

# Set your email (MUST match your GitHub email)
git config --global user.email "your-email@example.com"
```

## Section 2: Tracking Version History

In this section, we will initialize a local git project and learn how to use basic git commands to track the files.

### Step 1: Initializing local Git Project

In this step, we will initialize our local Git project. First, navigate to the directory you would like to store your project, and run the following command.

```bash
git init -b main
```

`-b main` ensures the default branch is named `main`, matching GitHub's default layout.

### Step 2: Stage and Commit files

In this step, we will stage our files, (which means to tell Git to start tracking the files), and to commit our files (making a snapshot of the file on our local machine.)

To stage the files, type the following command:

```bash
git add .
```

The `.` symbol is our current directory, which tells Git to stage all the files in your current location.

Next, we will commit these files and add a commit message. It is recommended to use imperative mood (e.g. "Optimize", not "Optimized") to match Git's own generated messages.

```bash
git commit -m "Initial commit"
```

The `-m` flag stands for `message`, which is why we put our commit message after it.

## Section 3: Making GitHub repository and linking with local project

In this section, we will make a GitHub repository and link our local project with it.

### Step 1: Initializing Repository

In this step, we will make a GitHub repository, which is where we publish our project. If you do not have a GitHub account, please make one.

1. Navigate to [the GitHub homepage](https://github.com/) and sign in if you are not already.
2. Click the green `New` button located at the top right of the `Top Repositories` menu that is on the left side of your screen. If you are unable to find this button, click on [this link](https://github.com/new) instead, which will take you to the same location.
3. Set a repository name, and make sure that all of the `Add ...` boxes are unchecked.
4. Click `Create Repository`
5. Remember the URL for your repository


### Step 2: Linking local project to repository

In this step, we will link our local project to the GitHub repository we just made.

Navigate to your local project, and run the following command, while ensuring to replace `<REPOSITORY LINK>` with the link you remembered in 3.1.5

```bash
git remote add origin <REPOSITORY LINK>
```

### Step 3: `Push`ing

In this step, we will push to our repository on GitHub. This means that your local project and all the changes you made, along with your commit messages, will be put on GitHub.

Navigate to your local project, and run the following command

```bash
git push -u origin main
```

(The `-u` flag remembers, so next time, you just need to write `git push`)	

## Section 4: Wrapping up and Next Steps

You have successfully initialized a local project, tracked your changes, and pushed your code securely to the cloud on GitHub.

Now that your local project is linked to your remote GitHub repository, your workflow becomes way more simpler.


