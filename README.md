# Git Repository Guide

This guide will walk you through the basic steps of creating a personal Git repository, committing code, and rolling back changes with commands like `reset --soft` and `reset --hard`. It's intended for beginners who are getting started with Git and version control.

## 1. Creating a Personal Git Repository

### Step 1: Sign Up for GitHub
If you don't already have an account, sign up at [GitHub](https://github.com/).

### Step 2: Create a New Repository
1. Go to [GitHub](https://github.com/) and log in.
2. Click the **New** button in the top right corner or navigate to [this link](https://github.com/new).
3. Fill in the repository name, description (optional), and choose visibility (public or private).
4. Optionally, initialize the repository with a `README` file and a `.gitignore`.
5. Click **Create repository**.

### Step 3: Clone the Repository to Your Local Machine
Run this command to clone the newly created repository to your local machine:
```
git clone https://github.com/your-username/your-repo.git
```

## 2. Committing Local Code to the Repository

### Step 1: Add Files to Your Repository
Navigate to your repository folder and add the files you want to track using Git:

```
git add .
```
or add specific files:

```
git add filename
```

### Step 2: Commit Your Changes
After staging files, commit them with a message:

```
git commit -m "Your commit message"
```
### Step 3: Push Changes to GitHub
To upload your local commits to GitHub, use:
```
git push origin main
```
(Replace main with the name of your branch if it's different.)

## 3. Additional Helpful Commands
To switch to a different branch or restore files, use:
```
git switch branch-name
```
If you want to create a new branch and switch to it:

```
git checkout -b new-branch-name
```
Viewing the Commit History
To see the history of commits in your repository:

```
git log
```
For a shorter view:

```
git log --oneline
```

Merging Branches
To merge changes from another branch into your current branch:

```
git merge branch-name
```
Fetching and Pulling Changes
To sync your local repository with the latest changes from the remote repository:

```
git pull
```
Stashing Uncommitted Changes
If you want to temporarily save your uncommitted changes and come back to them later:

```
git stash
```
To apply the stashed changes back:

```
git stash apply
```

## 4. Rolling Back Changes
Git offers several ways to undo changes. Below are some common commands:
```
git reset --soft 
```
This command rolls back your last commit but keeps your changes in the staging area.

```
git reset --soft HEAD^
```
You can use this if you want to edit your last commit message or add more changes to the commit.

```
git reset --hard
```
This command discards all changes in your working directory and staging area, resetting everything to the last commit.

```
git reset --hard HEAD^
```
Use this carefully, as it cannot be undone.
