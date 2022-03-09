# 2022-03-09-git_collab

- `git clone <URL>`: "downloads" the git repository to current directory
    - `git init`: creates a git repo locally

## Branches

- `git branch <NAME>`: creates <NAME> where HEAD is
    - `git branch -a`: list all your branches
- `git switch <NAME>`: switch to branch <NAME>
    - `git checkout <NAME>`: "older" way to switch branches
    - shortcut: `git switch -c <NAME>`: create and move in 1 step
    - `git checkout -b <NAME>`: older way to create and move
- The PR (pull request) will update if you push new changes

- Cleaing up after PR merge
    - Delete the branch on the remote
    - `git fetch --prune`: update local history
    - `git branch -d <NAME>`: delete the branch <NAME>
        - Note: lower-case d (use -D for force delete)

Changes to b1 commit 1
Changes to b1 commit 2
Changes to b2 commit 1
Changes to b2 commit 2

setup for rebase conflict

```
git checkout -b conflict_branch_1
echo "Changes to b1 commit 1" >> README.md
git status
git add README.md
git commit -m "b1 c1"
echo "Changes to b1 commit 2" >> README.md
git add README.md
git commit -m "b1 c2"

git checkout main

git checkout -b conflict_branch_2
echo "Changes to b2 commit 1" >> README.md
git add README.md
git commit -m "b2 c1"
echo "Changes to b2 commit 2" >> README.md
git add README.md
git commit -m "b2 c2"

git push origin conflict_branch_2
git push origin conflict_branch_1
```
