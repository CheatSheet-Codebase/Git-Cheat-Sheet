# Git Cheatsheet

## Add GIT Credentials in VS Code
1. Install Git.
2. Open VS Code and check with `git --version`.
3. Set your email:
    ```bash
    git config --global user.email "you@example.com"
    ```
4. Set your username:
    ```bash
    git config --global user.name "Your Name"
    ```
5. Verify:
    ```bash
    git config --global --list
    ```

---

## Common Git Commands

- `git clone <repository-url>` - Clone a repository.
- `git status` - Check the status of files.
- `git add .` - Add all files to staging.
- `git add <file>` - Add a specific file to staging.
- `git commit -m "message"` - Commit changes.
- `git commit --amend` - Modify the last commit message or content.
- `git push origin <branch>` - Push to a remote repository.
- `git pull` - Fetch and merge changes from remote.
- `git fetch` - Fetch changes from remote without merging.
- `git merge <branch>` - Merge another branch into your current branch.
- `git log` - View commit history.
- `git reset --hard <commit-id>` - Reset to a specific commit and discard all changes.
- `git reset <file>` - Unstage a file.
- `git stash` - Temporarily save changes.
- `git stash pop` - Apply stashed changes.
- `git diff` - Show changes not staged for commit.
- `git diff --staged` - Show changes that are staged for commit.
- `git reflog` - Show the history of references (e.g., HEAD).
- `git show <commit-id>` - Show changes from a specific commit.
- `git switch <branch-name>` - Switch to another branch (replaces `git checkout` for easier branch switching).
- `git switch -c <new-branch-name>` - Create and switch to a new branch (simplified alternative to `git checkout -b`).
- `git merge --no-ff <branch-name>` - Perform a merge with a merge commit, even if the merge could be fast-forwarded.
- `git reset <commit-id>` - Undo changes and move the HEAD to a specific commit.
- `git cherry-pick <commit-id>` - Apply changes from a specific commit from another branch.
- `git tag` - List tags.
- `git tag <tag-name>` - Create a tag at the current commit.
- `git push --tags` - Push tags to the remote repository.
- `git fetch -p` - Prune remote-tracking branches that no longer exist.
- `git clean -fd` - Remove untracked files and directories.
- `git remote -v` - Show remote repositories.
- `git remote add <name> <url>` - Add a remote repository.
- `git remote remove <name>` - Remove a remote repository.
- `git remote set-url <name> <new-url>` - Change the remote repository URL.
- `git push --force-with-lease` - Force push with a safety check to avoid overwriting others' changes.
- `git pull --rebase` - Fetch changes from remote and apply your commits on top of them.

---

## Setting Up Git Account
1. Set username:
    ```bash
    git config --global user.name "Your Name"
    ```
2. Set email:
    ```bash
    git config --global user.email "you@example.com"
    ```
3. Verify config:
    ```bash
    cat .git/config
    ```

---

## Branch Management

- `git branch` - List branches.
- `git branch <branch-name>` - Create a new branch.
- `git branch -d <branch-name>` - Delete a local branch.
- `git branch -D <branch-name>` - Force delete a local branch.
- `git checkout -b <branch-name>` - Create and switch to a new branch.
- `git switch -c <branch-name>` - Create and switch to a new branch.
- `git checkout <branch-name>` - Switch to an existing branch.
- `git push origin --delete <branch-name>` - Delete a remote branch.
- `git fetch -p` - Clean up remote tracking branches.
- `git branch -m <old-name> <new-name>` - Rename a branch.
- `git branch -v` - View the last commit on each branch.
- `git branch -r` - List all remote branches.
- `git push -u origin <branch-name>` - Push a new branch to remote.
- `git merge <branch-name>` - Merge a branch into the current branch.
- `git cherry-pick <commit-id>` - Apply a specific commit from another branch.

---

## Tagging

- `git tag` - List all tags.
- `git tag <tag-name>` - Create a new tag.
- `git tag -a <tag-name> -m "message"` - Create an annotated tag.
- `git push origin <tag-name>` - Push a tag to the remote.
- `git push --tags` - Push all tags to the remote.
- `git tag -d <tag-name>` - Delete a local tag.
- `git push origin --delete <tag-name>` - Delete a remote tag.

---

## Collaboration

- `git remote -v` - List remote repositories.
- `git remote add <name> <url>` - Add a new remote repository.
- `git remote remove <name>` - Remove a remote repository.
- `git remote set-url <name> <new-url>` - Change the remote repository URL.
- `git pull --rebase` - Fetch changes and reapply your commits on top.
- `git push --force` - Force push changes to the remote branch.

---

## Undoing Changes

- `git reset` - Undo changes in the staging area.
- `git reset <file>` - Unstage a file.
- `git revert <commit-id>` - Revert changes introduced by a commit.
- `git clean -fd` - Remove untracked files and directories.
