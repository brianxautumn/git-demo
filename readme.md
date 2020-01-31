# Git tutorial

## Git workflow
![git](/git.png)

## Basics

### You want to start a fresh repository
Navigate to a new empty directory. Run the following command:
`git init`
This directory will now be a git repository.

### You have an existing repository
Navigate to a directory where you would like to download. Run the following command:
`git clone <repository>`

### You accidentally added files to staging
`git reset <filename>`  
This will not undo your changes, it just removes them from staging area

### You want to get rid of your changes
`git reset --hard`  
This is for when you do not want to keep your changes, and want to go back to the last commit you were at.

### Reseting to older commit
`git reset --hard HEAD~1`  
Before pushed, its possible to reset to older versions of the branch. Making new commits can cause conflicts though.

### Revert a commit
`git revert <commit id>` 
This will allow you to apply the opposite commit to undo something. If already pushed, this is a very good approach.

### Reset specific files
`git checkout -- <filename>`  
`git checkout HEAD -- <filename>`  
This allows you to reset specific files back to the `HEAD`

### Reset all files 
`git checkout -- . (or directory)`  
`git checkout HEAD -- . (or directory)`  
This will allow you to checkout what an entire directory looked like at the given snapshot or hash. This is useful for going back to a specific commit and making it a new one. This is a good approach if the files have already been pushed.