# Git Learning Repository 
This repository serves as a guide and resource for understanding and mastering the essential concepts and commands in Git.  

## Table of Contents 
1. [Git](#git)  
2. [Git Add and Commits](#git-add-and-commits)  
3. [Staging Area](#staging-area)  
4. [Commit Hash](#commit-hash)  
5. [Reverting and Resetting Changes](#reverting-and-resetting-changes)  
6. [Git Servers](#git-servers)  
7. [Git Branching](#git-branching)  
8. [Branch Merge and Rebase](#branch-merge-and-rebase)  

## Git 
Git is a distributed version control system used for tracking changes in source code during software development. It allows multiple developers to work collaboratively on the same project while maintaining a complete history of changes.  

### Key Features: 
- Distributed version control.  
- Branching and merging.  
- Easy collaboration via Git servers like GitHub, GitLab, and Bitbucket.  
- Lightweight and fast performance.  



## Git Add and Commits 
### `git add` 
The `git add` command adds changes in your working directory to the **staging area**, preparing them to be committed.  

Example:  
```bash
	git add <file> # Adds a specific file
	git add .      # Add all changes in the current directory       
```
### `git commit`

The `git commit` command saves changes in the staging area to the repository. A commit represents a snapshot of your project at a specific point in time.


``` bash
	git commit -m "Your commit message"
 ```
 
## Staging Area

The **staging area** is an intermediate space where changes are listed before being committed. It acts as a buffer, allowing you to prepare and review changes before making them a part of the repository history.

###  Key Commands:
-   `git status`: Check which files are in the staging area.
-   `git diff --staged`: View staged changes.

## Commit Hash

Each commit in Git is assigned a unique 40-character SHA-1 hash. This hash identifies the commit and can be used to reference it for various operations like viewing, resetting, or reverting changes.

### Example:
``` bash
commit 1a79a4d60de6718e8e5b326e338ae533  # Unique hash for a commit
git show <commit-hash>
```

## Reverting and Resetting Changes

### Revert

Reverting creates a new commit that undoes the changes made in a previous commit.
``` bash
	git revert <commit-hash>
```
### Reset

Resetting moves the current branch pointer to a specific commit, optionally modifying the working directory and staging area.

-   `--soft`: Keeps changes in the staging area.
-   `--mixed` (default): Keeps changes in the working directory.
-   `--hard`: Discards all changes.
``` bash
	git reset --hard <commit-hash>
```
## Git Servers

Git servers host repositories remotely, enabling collaboration and version control. Examples include:

-   **GitHub**: Popular for open-source and private projects.
-   **GitLab**: Known for DevOps features.
-   **Bitbucket**: Integrates with Atlassian tools.

### Common Commands:

-   Clone a repository:
```bash
	git clone <repository-url>
```
- Push Changes:
``` bash
	git push origin <branch-name>
```
## Git Branching

Branches are parallel versions of a repository that allow you to work on features or fixes without affecting the main codebase.

### Commands:

-   Create a branch:
``` bash
	git branch <branch-name>
```
-  Switch branches:
``` bash
	git checkout <branch-name>
```
-  View all branches:
``` bash
	git branch -a
```
## Branch Merge and Rebase

### Merge

Combines two branches and creates a **merge commit**.
``` bash
	git merge <branch-name>
```
### Rebase

Reapplies commits from one branch onto another, resulting in a linear commit history.
``` bash
	git rebase <branch-name>
```
