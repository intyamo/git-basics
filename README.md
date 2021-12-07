# Git Basics a

## Initial Setup

```sh
git config --global user.name 'V. Pupkin'
git config --global user.email 'vpupkin@mail.com'

# set default editor
git config --global core.editor "'C:\Program Files\Notepad++\notepad++.exe' -multiInst -notabbar -nosession -noPlugin"
```

Reference: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup

## Create a new repo

```sh
mkdir new_project
cd new_project
git init
```

## Basic flow

```sh
# stage new files for commit
git add *.py

# check what we're going to commit
git status

# commit!
git commit -m "Message for new commit"

# check recent history (3 last commits)
git log --oneline -n 3
```

## More on working with staging area

```sh
# restore an unstaged file to the version of the current commit (HEAD)
git restore <file>

# unstage a file
git restore --staged <file>
# or
git reset -- <file>
```

## .gitignore

Just take one from https://github.com/github/gitignore

For Python:

https://github.com/github/gitignore/blob/master/Python.gitignore

## Branches

```sh
# view  all branches
git branch

# create a new branch
git branch 'new-branch-name'

# switch to a branch
git switch 'new-branch-name'

# create and switch
git switch -c new-branch
git switch --create new-branch
```

### Merge

```
# switch to target branch
git switch master

# merge new-branch into master
git merge new-branch

# remove fully merged branch
git branch -d new-branch
```
