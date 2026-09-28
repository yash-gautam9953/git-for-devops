# Branching and Collaboration Workflow

A small feature-branch workflow keeps changes reviewable and makes it easier to coordinate work.

## Create a change

```sh
git switch main
git pull --rebase origin main
git switch -c feature/short-description
```

Make a focused change, then inspect and commit it:

```sh
git status
git diff
git add path/to/changed-file
git diff --staged
git commit -m "Add short description"
```

## Share and review

```sh
git push -u origin feature/short-description
```

Open a pull request, describe the change and its validation, and address review feedback with follow-up commits. Keep secrets, generated output, and unrelated changes out of the branch.

## Integrate and clean up

After approval, merge the pull request using the repository's chosen merge strategy. Then update the local default branch and remove the feature branch:

```sh
git switch main
git pull --rebase origin main
git branch -d feature/short-description
```

Use protected branches and required checks on shared repositories so changes are reviewed and validated before reaching the default branch.
