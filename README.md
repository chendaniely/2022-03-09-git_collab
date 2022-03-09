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
