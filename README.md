# Git_practice

####  A commit represents a snapshot of your project's changes at a specific point in time. A commit captures the state of your files. Only changes that have been staged (git add) are included in the commit.

### Git configuration
```
step1:
    download git from:  https://git-scm.com/downloads

step2:
    install it 

step3:
    open git bash and cofigure username and email by below commands

    git config --global user.name "vikesh das"
    git config --global user.email "vk@gmail.com"
```

### create git repository locally
#### it will create git folder inside currect directory which makes a folder git repository. 
```
Git inti repo_name
```

### 3 stages

* Working directory: A folder contains your files or we can say repo on local.

* Staging area: when we run command "git add" it moves changes from working directory to staging area.

### add and commit in single command 

```
git commit -am "Your commit message"
```

### unstage a file (revert back a file from staging area )

```
git reset HEAD file_name
```

### Discard changes in a file
```
git checkout -- file_name
```

### .ignorefile

we can put all files in gitignore file which we don't want to push on githut

*.log : in gitignore file will ignore all files end with .log.

after adding files in gitignore push gitignore file.

### Merge two brnach 

Lets say we we have a brnach "update" and we want to merge "update" branch into "main" branch.

step1: switch to main brnach

step2: merge brnach "update" and "main"
```
git merge update
```
above command will be merged with corrent brnach.

### Conflicts

if Developer A creates new brnach A from master brnach and made changes in a file and commit. Developer B also create new brnach B from master before merging brnach A with master and made changes in same line where developer B made and commit it . In that case we will get conflicts.

### Git reset

git reset is a powerful command used to undo changes by moving the HEAD pointer.

Let’s assume we have a Git repository with below commit history:
```
Commit C (HEAD)   - "Added feature Y"  
Commit B          - "Added feature X"  
Commit A          - "Initial commit"  
```
```
command: git reset --soft HEAD~1
```
* HEAD moves back to Commit B (undoing Commit C).
* hanges from Commit C remain staged (git status shows them as ready to commit).

#### Types of reset command
* soft : Moves the HEAD pointer back to the specified commit,it Keeps all changes on local only removes commit,keep all changes in stage area. 
* mixed: Unstages all changes , Keeps changes in working directory
* hard :  Moves the HEAD pointer back to the specified commit,Removes all changes from staging area,Removes all changes from working directory