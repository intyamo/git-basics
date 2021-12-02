# Git Basics

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
# potentially destructive
git rm <file>
git rm --cached <file>

# /!\ potentially destructive operation! /!\
# restores to the current commit
git restore <file>

# preserve changes
git restore --cached <file>

# unstage a file, preserve changes
git reset HEAD -- <file>
```
