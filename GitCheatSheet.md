# Git Cheatsheet

A couple of commonly used git commands and their functions

## Configuring and Initializing

**Check your git version**.

```bash
git --version
```

**Configure default username and email**.

```bash
git config --global user.name [yourusername]

git config --global user.email [youremail]
```

**View Username and Email from global configurations**.

```bash
git config --global user.name
git config --global user.email
```

**Initialize a git repository**.

```bash
git init
```

## Staging a Repo

**Check uncommitted modifications made in the repository**.

```bash
git status
```

**Staging modified files**.

```bash
# Stage a single file
git add [file|path to file]

# Stage all modified files
git add .
```

## Committing to a Repository

**Make a commit**.

```bash
git commit -m "[your commit message]"
```

**View commit history**.

```bash
# View a detailed history of commits
git log

# View just commit history messages
git log --oneline
```

**View a repository's version at a given point in time**.

Checkout a commit at a given point in time without altering the commit history in any shape or form, using the id of the commit from the `git log --oneline` command.

```bash
git checkout [commit id]

# Checkout the latest commit on the master branch
git checkout master
```

**Revert/undo a commit in the commit history**.

```bash
git revert [commit id]
```

**Reset to a given point in time**.

Delete all commits in the history up to the specified point using the commit id.

Reset the commit while preserving the changes made to the repository after the commit id.

```bash
git reset [commit id]
```

Reset the commit without preserving the changes made to the repository, meaning that all changes made to the files in the repository after the commit id will be removed.

```bash
git reset [commit id] --hard
```
