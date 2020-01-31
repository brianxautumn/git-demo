# Git tutorial

## Git workflow
![git](/git.png)



# Basics

### You want to start a fresh repository
Navigate to a new empty directory. Run the following command:
`git init`
This directory will now be a git repository.

### You have an existing repository
Navigate to a directory where you would like to download. Run the following command:
`git clone <repository>`


# Working on changes
### See which files have been changed
While in your git directory check which files have been changed with 
`git status`

### See which lines have been changed
While in your git directory check which lines have been changed with 
`git diff` or if you want to only see a specific file, `git diff <filename>`


# Snapshots
### Add files to staging
To add files to staging use the add command: `git add <filename>` or `git add <directory>`

### Create a commit
At this point, files are not yet saved to a snapshot. Run the commit command. `git commit -m "Message for your commit"

### Push to remote
After commiting, files will only be available locally. To upload to remote repository use push. `git push`

# Basic reverting
### You accidentally added files to staging
`git reset <filename>`  
This will not undo your changes, it just removes them from staging area

### You want to get rid of your changes
`git reset --hard`  
This is for when you do not want to keep your changes, and want to go back to the last commit you were at.

### Reset specific files
`git checkout -- <filename>`  
`git checkout HEAD -- <filename>`  
This allows you to reset specific files back to the `HEAD` which is essentially hard revert for a single file.

# Advaced reverting

### Reseting to older commit
`git reset --hard HEAD~1`  
Before pushed, its possible to reset to older versions of the branch. Making new commits can cause conflicts though.

### Revert a commit
`git revert <commit id>` 
This will allow you to apply the opposite commit to undo something. If already pushed, this is a very good approach.

### Reset all files 
`git checkout -- . (or directory)`  
`git checkout HEAD -- . (or directory)`  
This will allow you to checkout what an entire directory looked like at the given snapshot or hash. This is useful for going back to a specific commit and making it a new one. This is a good approach if the files have already been pushed.