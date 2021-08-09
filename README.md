# Git commands that I use in daily work

```bash
git config
git init
git add
git commit
git status
git branch
git checkout
git merge
git remote
git clone
git pull
git push
```

# git config

### These values set what email address and name commits will be from on a local computer
```bash
# Running git config globally
$ git config --global user.email "my@emailaddress.com"
$ git config --global user.name "John Doe"

# Running git config on the current repository settings
$ git config user.email "my@emailaddress.com"
$ git config user.name "John Doe"
```

# git init

### Turn a directory into a Git repository
```bash
$ git init
```

# git add

### Adds files in the folder to the staging area for Git
```bash
# To add all files:
$ git add .

# To add a specific file:
$ git add index.html

# To add an entire directory:
$ git add folder
```

# git commit

### Record the changes made to the files to a local repository
```bash
# Adding a commit with message
$ git commit -m "Commit message in quotes"
```

# git status

### Return the current state of the repository
```bash						
# Message when files have not been staged (git add)
$ git status
On branch main
Untracked	 files:
  (use "git add <file>..." to include in what will be committed)

  	homepage/index.html

# Message when files have been not been committed (git commit)
$ git status
On branch main
Your branch is up-to-date with 'origin/main'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   homepage/index.html

# Message when all files have been staged and committed 
$ git status
On branch main
nothing to commit, working directory clean
```

# git branch

### To determine what branch the local repository is on, add a new branch, or delete a branch.
```bash
# Create a new branch
$ git branch new_feature

# List all remote or local branches
$ git branch -a
* main
  new_feature
  remotes/origin/stable
  remotes/origin/staging
  remotes/origin/master -> origin/main

# Delete a branch
$ git branch -d new_feature
Deleted branch new_feature (was 0254c3d).

# Delete a branch remotely
$ git push origin --delete remoteBranchName
```

# git checkout

### To start working in a different branch
```bash
# Switching to branch 'new_feature'
$ git checkout new_feature
Switched to branch 'new_feature'

# Creating and switching to branch 'staging'
$ git checkout -b staging
Switched to a new branch 'staging'
```

# git merge

### Integrate branches together
```bash
# Merge changes into current branch
$ git merge new_feature
Updating 0254c3d..4c0f37c
Fast-forward
 homepage/index.html | 297 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 297 insertions(+)
 create mode 100644 homepage/index.html
```

# git remote

### To connect a local repository with a remote repository
```bash
# Adding a remote repository with the name of beanstalk
$ git remote add origin git@github.com:StazMD/Git.git

# List named remote repositories
$ git remote -v
origin git@github.com:StazMD/Git.git (fetch)
origin git@github.com:StazMD/Git.git (push)
```

# git clone

### To create a local working copy of an existing remote repository	
```bash
$ git git@github.com:StazMD/Git.git
Cloning into 'repository_name'...
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 5 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (5/5), 3.08 KiB | 0 bytes/s, done.
Checking connectivity... done.
```

# git pull

### To get the latest version of a repository	
```bash
# Pull from named remote
$ git pull origin staging
From github.com:StazMD/Git.git
 * branch            staging    -> FETCH_HEAD
 * [new branch]      staging    -> origin/staging
Already up-to-date.

# Pull from URL
$ git pull git@github.com:StazMD/Git.git staging
From github.com:StazMD/Git.git
 * branch            staging    -> FETCH_HEAD
 * [new branch]      staging    -> origin/staging
Already up-to-date.
```

# git push

### To get the latest version of a repository	
```bash
# Push a specific branch to a remote with named remote
$ git push origin staging
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 734 bytes | 0 bytes/s, done.
Total 5 (delta 2), reused 0 (delta 0)
To git@github.com:StazMD/Git.git
   ad189cb..0254c3d  main -> main

# Push all local branches to remote repository
$ git push --all
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 373 bytes | 0 bytes/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To git@github.com:StazMD/Git.git
   0d56917..948ac97  master -> master
   ad189cb..0254c3d  main -> main
```
