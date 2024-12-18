Git and Version Control Guide

# Part 1: Introduction to Version Control and Git


### Task 1: Install and Configure Git

Configure Git with your username and email:

git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

2.View your Git configuration

Use git config --list to verify your configuration.
git config --list

### Task 2: Initialize a Repository

git init sets up a Git repository in the current folder.
 The .git folder contains all necessary information for version control.

### Task 3: Create a File and Make Multiple Commits

This demonstrates the core Git workflow: making changes, staging, and committing.
echo for file create
push code to see changes

echo "My First Project" > README.md

git add README.md

git commit -m "Initial commit: Added README.md"

echo "Added a description" >> README.md

git add README.md

git commit -m "Updated README with a description"

git remote add origin https://github.com/your-user-name/name.git

git push -u origin main

### Task 4: Check Status and Log

git status shows the current state of the working directory.

  git status

git log provides a history of commits. The --oneline flag condenses it for readability.

 git log --oneline --graph --decorate

### Task 5: Create and Clone a Repository

for clone

  git clone http://user-name/name-repo.git

### Task 6: Understanding the Git Workflow

Explains the typical cycle of modifying, staging, and committing changes.

    echo "Workflow example" > workflow.md

    git add workflow.md

    git commit -m "Added workflow example"



# Part 2: Working with Repositories

### Task 7: Branching and Merging

git branch creates new branches to isolate features or changes.

  git branch feature-login

  git checkout feature-login

git merge integrates changes from one branch into another.

  git checkout main

  git merge feature-login

### Task 8: Handling Merge Conflicts

Provides hands-on experience with resolving conflicts, a common scenario in team collaboration.

    git branch branch-A

    git branch branch-B

    git checkout main

    git merge branch-A

    git merge branch-B  # Conflict occurs here

    # Resolve conflict in the file manually

    git add README.md

    git commit -m "Resolved merge conflict between branch-A and branch-B"

### Task 9: Renaming and Deleting Branches

git branch -m renames branches, while git branch -d deletes branches no longer needed.

  git branch -m old-branch-name new-branch-name

  git branch -d feature-login

# Part 3: Advanced Git Operations

### Task 10: Using Git Stash

echo for cerate a file but dont use commit

  echo "Temporary work" >> temp.md

Stashing allows you to save changes temporarily without committing them.

  git stash

git stash apply re-applies stashed changes, and git stash drop removes them.

  git stash apply

  git stash drop


### Task 11: Rewriting History with Interactive Rebase

Squashing commits consolidates them for a cleaner history. Use pick for the first commit and squash for subsequent ones in the rebase interface.

   git rebase -i HEAD~3

### Task 12: Cherry-Picking Commits

Lets you apply specific commits from one branch to another without merging the whole branch.

  git cherry-pick <commit-hash>

### Task 13: Tagging Commits

Tags mark important points in your history, like release versions.

  git tag -a v1.0 -m "Version 1.0 release"

  git push origin v1.0

### Task 14: Working with Remote Repositories

git remote add connects your local repo to a remote one, enabling collaboration.

git remote add origin <repository-url>

git push origin main

# Part 4: Additional Practice

### Task 15: Forking and Contributing

Forking allows you to work on someone else's repository. Creating a pull request submits your changes back to the original project.

Fork a repository on GitHub, clone it, create a new branch, make changes, and push:

   git checkout -b fix-typo

   echo "Typo fixed" >> README.md

   git add README.md

   git commit -m "Fixed a typo"

   git push origin fix-typo

### Task 16: Simulate Team Collaboration

Practices resolving real-world issues like merge conflicts during collaborative work.

### Task 17: Git Ignore

.gitignore ensures specific files or directories, such as node_modules/, are not tracked by Git.

   echo "node_modules/" > .gitignore

   git add .


# SUMMARY OF ALL COMMANDS

## Command for Initail Configurations

### git config --global user.name "Your Name"
use to configure the username of the user



### git config --global user.email "your-email@example.com"
use to configure the email of the user


### git config --list
use to show the configurations details list.


### git init
use to initialize the git repository


### echo "My First Project" > README.md
echo use to create a new file with the given message.


### git add README.md
use to add file to the stagging area


### git commit -m "Initial commit: Added README.md"
use to commit the changes to the local system with a given message.


### git status 
use to check the file status of the file at the local system


### git log --oneline --graph --decorate

git log : This command is use to check the commit history of the files.

git log --oneline : This command is use to get the specific commit history fo the files.

git log --graph : This command is used to display a visual representation of the commit history in a Git repository,
git log --decorate : This command used to display the commit history with additional information about references such as branch names, tags, and HEAD pointers.

### git clone http://codinggita.com/example-repo
This command use to clone any repository from the git hub to local system.

### git branch feature-login
This command is use to create a new branch.


### git checkout feature-login
This command is use to switch branch.

### git checkout -b feature-login
This command use to create and switch branch at the same time.

### git checkout main   git merge feature-login
To merge a branch to the main branch, first we have to switch to the main branch and then write the command **git merge [branch name]** to marge that brach to main branch.

### git branch -d [feature-login]
This command use to delete the branch.

### git stash
This command is used to temporarily save changes in your working directory and staging area.

### git stash list 
This command lists all the stashes you've saved

### git stash apply
This applies the most recent stash to your working directory, but does not remove it from the stash list.

### git stash drop 
This command use to delete a added stash

### git cherry-pich {commit-hash}
command is used to apply a specific commit from one branch onto another branch.

### git tag
command is used to create, list, or delete tags in your Git repository.

### git push
This commit use to save the changes of local system to the online git repo.

### git remote add origin {repository-url}
This command use to connect the local repository to the git repository.


### .gitignore file
This file is used in Git to specify which files or directories should not be tracked or committed by Git.
