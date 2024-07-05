
# Git Bash Cheatsheet

## Table of Contents:
[Setup and Config](#setup-and-config)

[Getting and Creating Projects](#getting-and-creating-projects)

[Staging Files](#staging-files)

[Committing Files](#committing-files)

[Branching and Merging](#branching-and-merging)

[Sharing and Updating Projects](#sharing-and-updating-projects)

[Inspection and Comparison](#inspection-and-comparison)

[Undoing Changes](#undoing-changes)

[Stashing](#stashing)

[Tagging](#tagging)

[Additional Commands](#additional-commands)

---

## Setup and Config

### Setting your username.
Sets the name you want attached to your commit transactions.
```bash
git config --global user.name "FirstName LastName (login)"
```
### Setting your email.
Sets the email you want attached to your commit transactions.
```bash
git config --global user.email "youremail@example.com"
```

### Checking your configuration
Lists all settings, shows the current configuration.
```bash
git config --list
```

---

## Getting and Creating Projects

### Clone an existing Repository.
Downloads a project and its entire version history.
```bash
git clone https://github.com/user/repo.git
```

### Create a new local repository
Creates an empty Git repository in the specified directory.
```bash
git init
```

---

## Staging Files

### Add a file to staging area.
```bash
git add filename
```

### Add all files to staging area.
Adds all new and changed files to the staging area.
```bash
git add .
```

## Committing Files

### Commit changes
Commits the staged files with a message.
```bash
git commit -m "Commit message"
```

### Commit with all staged changes
Stages and commits all changes in one step.
```bash
git commit -am "Commit message"
```

---

## Branching and Merging

### List branches
Lists all local branches in the repository.
```bash
git branch
```

### Create a new branch
```bash
git branch <branch_name>
```

### Switch to a branch
Switches to the specified branch and updates the working directory.
```bash
git checkout <branch_name>
```

### Create and switch to a new branch
```bash
git checkout -b <branch_name>
```

### Merge a branch into the current branch
```bash
git merge <branch_name>
```

### Delete a branch
```bash
git branch -d <branch_name>
```

---

## Sharing and Updating Projects

### List remote repositories
```bash
git remote -v
```

### Add a remote repository
```bash
git remote add origin https://github.com/user/repo.git
```


### Fetch changes from remote
Downloads objects and refs from another repository.
```bash
git fetch
```

### Push changes to remote
Pushes all changes on the branch to the remote repository.
```bash
git push origin <branch_name>
```

### Pull changes from remote
Fetches and merges changes on the remote server to your working directory.
```bash
git pull
```

---

## Inspection and Comparison

### Show the commit history
Shows the commit history for the current branch.
```bash
git log
```

### Show commit history with diffs
Shows the commit history with differences introduced in each commit.
```bash
git log -p
```

### Show changes between commits
Shows changes between two commit objects.
```bash
git diff <commit1> <commit2>
```

### Show changes in the working directory
Shows changes between the working directory and the index.
```bash
git diff
```

### Show information about a commit
Shows various objects such as commit, tree, and blob
```bash
git show <commit>
```

---

## Undoing Changes

### Un-stage a file
Removes the specified file from the staging area.
```bash
git reset <file>
```

### Undo all changes in the working directory
Resets the index and working directory to the state of the last commit.
```bash
git reset --hard
```

### Revert a commit by making a new commit
Reverts the specified commit by creating a new commit.
```bash
git revert <commit>
```

### Reset to a specific commit
Resets the index and working directory to the specified commit.
```bash
git reset --hard <commit>
```

---

## Stashing

### Stash changes
Stashes the changes in a dirty working directory away.
```bash
git stash
```

### List stashed changes
Lists all stashed changesets.
```bash
git stash list
```

### Apply stashed changes
Applies the changes in the latest stash.
```bash
git stash apply
```

### Apply and drop stashed changes
Applies the changes in the latest stash and removes it from the stash list.
```bash
git stash pop
```

### Drop a specific stash
Removes a single stashed state from the stash list.
```bash
git stash drop <stash@{n}>
```

---

## Tagging

### List tags
```bash
git tag
```

### Create a new tag
```bash
git tag <tag_name>
```

### Create an annotated tag
```bash
git tag -a <tag_name> -m "Tag message"
```

### Push tags to remote
Pushes the specified tag to the remote repository.
```bash
git push origin <tag_name>
```

---

## Additional Commands

### Show the current status
Displays paths that have differences between the index file and the current HEAD commit.
```bash
git status
```

### Clean untracked files
Removes untracked files from the working directory
```bash
git clean -f
```

### View the commit history in a graph format
Displays the commit history as a graph
```bash
git log --graph --oneline --all
```

---
