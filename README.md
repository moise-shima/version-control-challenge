# Study Notes Hub
**Author:** MITALI Shima Moise
## Description
This repository contains beginner study notes for version control practice.
## Topics Covered
- Git basics
- GitHub workflow
- Collaboration
## How to Use This Repository
Open the files and review the notes.
# Git & GitHub Version Control Guide

## What is Version Control?

Version control is a system that tracks changes made to files over time. It helps developers:

* Keep a history of changes
* Restore previous versions of files
* Work together without overwriting each other’s work
* Manage different versions of a project safely

The most popular version control system is **Git**, while **GitHub** is a platform used to store and share Git repositories online.

---

# Basic Git Workflow

## 1. Configure Git (First Time Only)

Before using Git, set your username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check your configuration:

```bash
git config --list
```

---

## 2. Create a Repository

A repository (repo) is a folder tracked by Git.

### Create a new local repository

```bash
mkdir my-project
cd my-project
git init
```

### Clone an existing GitHub repository

```bash
git clone https://github.com/username/repository-name.git
```

---

# Important Git Commands

| Command                       | Purpose                             |
| ----------------------------- | ----------------------------------- |
| `git init`                    | Initialize a new repository         |
| `git clone URL`               | Copy a repository from GitHub       |
| `git status`                  | Show file changes and branch status |
| `git add file`                | Stage a specific file               |
| `git add .`                   | Stage all changed files             |
| `git commit -m "message"`     | Save changes with a message         |
| `git push`                    | Upload changes to GitHub            |
| `git pull`                    | Download latest changes from GitHub |
| `git fetch`                   | Download changes without merging    |
| `git merge branch-name`       | Combine branches                    |
| `git branch`                  | Show all local branches             |
| `git branch branch-name`      | Create a new branch                 |
| `git checkout branch-name`    | Switch branches                     |
| `git checkout -b branch-name` | Create and switch to a branch       |
| `git log`                     | View commit history                 |
| `git diff`                    | Show file differences               |
| `git rm file`                 | Remove a file from Git              |
| `git mv old new`              | Rename or move a file               |
| `git stash`                   | Temporarily save unfinished changes |
| `git stash pop`               | Restore stashed changes             |
| `git reset --hard`            | Reset repository to last commit     |
| `git remote -v`               | View connected remote repositories  |

---

# Understanding Branches

## What is a Branch?

A branch is a separate version of your project where you can work on new features or fixes without affecting the main project.

Think of branches like parallel workspaces:

* The `main` branch contains the stable version of the project.
* Other branches are used for development, testing, or experiments.

This allows multiple developers to work at the same time safely.

---

## Why Branches are Important

Branches help teams:

* Develop features independently
* Fix bugs without affecting the main code
* Test ideas safely
* Collaborate more efficiently

---

## Branch Workflow Example

### Create a new branch

```bash
git branch login-feature
```

### Switch to the branch

```bash
git checkout login-feature
```

### Create and switch in one command

```bash
git checkout -b login-feature
```

### Push the branch to GitHub

```bash
git push origin login-feature
```

### Merge the branch into main

```bash
git checkout main
git merge login-feature
```

---

# Understanding Pull Requests

## What is a Pull Request?

A Pull Request (PR) is a request to merge changes from one branch into another branch.

Pull requests are mainly used on GitHub for:

* Reviewing code
* Discussing changes
* Detecting mistakes before merging
* Collaborating with teams

---

## Pull Request Workflow

### Step 1: Create a branch

```bash
git checkout -b new-feature
```

### Step 2: Make changes and commit

```bash
git add .
git commit -m "Added new feature"
```

### Step 3: Push branch to GitHub

```bash
git push origin new-feature
```

### Step 4: Open a Pull Request on GitHub

After pushing:

1. Go to your GitHub repository
2. Click **Compare & pull request**
3. Add a title and description
4. Click **Create pull request**

---

## What Happens After Creating a Pull Request?

Team members can:

* Review your code
* Suggest changes
* Approve the work
* Merge it into the main branch

Once approved, the branch is merged into `main`.

---

# Common GitHub Workflow Example

```bash
# Clone repository
git clone https://github.com/username/project.git

# Enter project folder
cd project

# Create a branch
git checkout -b feature-page

# Make changes to files

# Stage changes
git add .

# Commit changes
git commit -m "Created feature page"

# Push branch
git push origin feature-page
```

Then create a Pull Request on GitHub.

---

# Git Status File Colors Explained

| Status    | Meaning                          |
| --------- | -------------------------------- |
| Red       | File changed but not staged      |
| Green     | File staged and ready to commit  |
| Untracked | Git is not tracking the file yet |

---

# Difference Between Git and GitHub

| Git                            | GitHub                       |
| ------------------------------ | ---------------------------- |
| Version control software       | Online hosting platform      |
| Works locally on your computer | Works online                 |
| Tracks file changes            | Stores repositories online   |
| Used through terminal/CLI      | Used through browser and Git |

---

# Best Practices

* Commit regularly with clear messages
* Use branches for new features
* Pull before pushing to avoid conflicts
* Keep the `main` branch stable
* Review pull requests carefully
* Write meaningful commit messages

---

# Example Commit Messages

Good examples:

```bash
git commit -m "Fixed login bug"
git commit -m "Added responsive navbar"
git commit -m "Updated README documentation"
```

Bad examples:

```bash
git commit -m "stuff"
git commit -m "changes"
```

---

# Conclusion

Git and GitHub are essential tools for modern software development. They help developers track changes, collaborate efficiently, and manage projects safely.

Understanding:

* Git commands
* Branches
* Pull requests
* Repository workflows

is an important step toward becoming a professional developer.


