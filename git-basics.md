# Git Basics

## Start a repository

```sh
git init
git status
git add README.md
git commit -m "Add project README"
```

Set your author identity if Git has not been configured on this machine:

```sh
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Inspect changes

```sh
git status --short
git diff
git diff --staged
git log --oneline --graph --decorate
```

Stage and commit only the files you intend to include:

```sh
git add path/to/file
git commit -m "Describe the change"
```

## Work with remotes

```sh
git remote -v
git fetch origin
git pull --rebase origin main
git push -u origin main
```

Fetch before integrating remote work, and review the resulting diff before pushing.

## Undo carefully

Discarding edits is destructive. Inspect the status and diff first. To unstage a file while keeping its edits:

```sh
git restore --staged path/to/file
```

To restore a tracked file to its last committed version (discarding its edits):

```sh
git restore path/to/file
```
