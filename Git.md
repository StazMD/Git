# git init

### Turn a directory into a Git repository
```
$ git init
```

# git add

### Adds files in the folder to the staging area for Git
```Git Attributes
# To add all files:
$ git add .

# To add a specific file:
$ git add index.html

# To add an entire directory:
$ git add folder
```

# git commit

### Record the changes made to the files to a local repository
```
# Adding a commit with message
$ git commit -m "Commit message in quotes"
```

# git status

### Return the current state of the repository
```Git Config						
# Message when files have not been staged (git add)
$ git status
On branch SecretTesting
Untracked	 files:
  (use "git add <file>..." to include in what will be committed)

  	homepage/index.html

# Message when files have been not been committed (git commit)
$ git status
On branch SecretTesting
Your branch is up-to-date with 'origin/SecretTesting'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   homepage/index.html

# Message when all files have been staged and committed 
$ git status
On branch SecretTesting
nothing to commit, working directory clean
```
