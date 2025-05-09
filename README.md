# Git Commands Cheat Sheet

## Initializing a Repository
- `git init`  
    Initializes a new Git repository.

## Removing a Repository
- `rm -rf .git`  
    Removes the Git repository from the project folder by deleting the `.git` directory.

## Checking Status
- `git status`  
    Displays the status of the working directory and staging area.

## Configuring Git
- `git config --global user.name "Your Name"`  
    Sets the global username for commits.  
- `git config --global user.email "your@email.com"`  
    Sets the global email for commits.

## Staging and Unstaging Files
- `git add file.etc file2.etc`  
    Adds specific files to the staging area.  
- `git add .`  
    Adds all files to the staging area.  
- `git reset <file-name>`  
    Unstages a specific file.  
- `git reset`  
    Unstages all files.  
- `git restore .`  
    Restores a file to its state in the last commit, discarding any local changes.
- `git restore --staged`  
    Unstages a file while keeping local changes in the working directory.

## Removing files from the index
- `git rm <file-name>`  
    Removes a file from both staging are and working directory.
- `git rm --cached <file-name>`  
    Removes a file from the index (staging area) without deleting it from the working directory.  

## Resetting Commits
- `git reset <commit-hash>`  
    Uncommits changes and reverts to the specified checkpoint.  
- `git reset --hard <commit-hash>`  
    Resets to a specific commit and makes it the HEAD.  
- `git reset --hard HEAD~1`  
    Removes the last commit. The number indicates how far back to go.

## Committing Changes
- `git commit -m "message"`  
    Commits changes with a message.

## Viewing Commit History
- `git log`  
    Displays the history of commits.

## Checking Out Commits
- `git checkout <commit-hash>`  
    Checks out a specific commit.  
- `git checkout master`  
    Returns to the latest commit on the master branch.

## Ignoring Files
- Create a `.gitignore` file in your project folder to specify files to ignore.

## Working with Branches
- `git branch`  
    Lists all branches.  
- `git branch <new-branch-name>`  
    Creates a new branch.  
- `git branch -b <new-branch-name>`  
    Creates and switches to a new branch.  
- `git checkout <branch-name>`  
    Switches to a specific branch.

## Merging and Deleting Branches
- `git merge <branch-name>`  
    Merges a branch into the master branch.  
- `git branch -d <branch-name>`  
    Deletes a branch.

## Pulling and Fetching Changes
- `git pull`  
    Pulls changes from the remote repository.  
- `git fetch`  
    Fetches changes from the remote repository without merging.  
- `git merge`  
    Merges fetched changes into the local branch.

## Pushing Changes
- `git push -f origin master`  
    Force pushes changes to the remote repository.

## Cloning a Repository
- `git clone <repository-link>`  
    Clones a repository to your local machine.

## Stashing Changes
- `git stash save "message"`  
    Saves changes to a stash.  
- `git stash list`  
    Lists all stashes.  
- `git stash clear`  
    Clears all stashes.
- `git stash show <stash@{}>`  
    Displays the changes saved in a specific stash. Use the stash reference (e.g. `stash@{0}`) to view details.
    
---

## Creating a New Repository and Pushing to GitHub
1. `git init`  
     Initializes a new repository.  
2. `git commit -m "message"`  
     Commits changes.  
3. `git branch -M main`  
     Renames the branch to `main`.  
4. `git remote add origin <link-to-github-repository>`  
     Links the local repository to the remote GitHub repository.  
5. `git push -u origin main`  
     Pushes changes to the remote repository.

---

## Pushing Files to an Existing Repository
1. `git remote add origin <link-to-github-repository>`  
     Links the local repository to the remote GitHub repository.  
2. `git branch -M main`  
     Renames the branch to `main`.  
3. `git push -u origin main`  
     Pushes changes to the remote repository.

---

## Getting Help
- `git --help`  
    Opens the Git help manual in your terminal.
- `git <command> --help`  
    Opens the help manual for a specific Git command. For example, `git commit --help`.