- https://education.github.com/git-cheat-sheet-education.pdf
- https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf

---

- Update global user name: `git config --global user.name "<firstname lastname>"`
- Update global user email`: git config --global user.email "<email@email.com>"`
---

- Create new empty repo: `git init`
- Clone existing remote repo: `git clone <remote-url>`
- Add a remote to existing local repo: `git remote add <remote> <remote-url>`
- Change remote of an existing local repo: `git remote set-url <remote> <remote-url>`
---

- List local branches: `git branch`
- List local and remote branches: `git branch -a`
- Create new local branch from current branch/commit: `git branch <new-branch>`
- Switch to different local branch: `git checkout <new-branch>`
- Create and switch to new local branch: `git checkout -b <new-branch>`
---

- Show modified staged files: `git status`
- Diff of unstaged changes: `git diff`
- Diff of uncommitted, but staged changes: `git diff --staged`
---

- Stage changed/new files: `git add <file-path-1> <file-path-2>`
- Remove a file and stage for commit: `git rm <file-path>`
- Rename a file and stage for commit: `git mv <existing-file-path> <new-file-path>`
- Unstage staged file: `git reset <file-name-1> <file-name-2>`
---

- Commit staged changes: `git commit -m "<commit message>"`
- Update last commit message: `git commit --amend`
- Undo all commits afer a specified commit, preserving changes locally: `git reset <commit-SHA>`
- Discard all history and changes back to specified commit: `git reset --hard <commit-SHA>`
---

- Push commit to remote: `git push <remote> <branch>`
- Push commit to default remote/branch: `git push`
---
## Log / Graph
- View commit log: `git log`
- View graph: `git log --graph --oneline --all`
- ?: `git show <SHA>`
---
## Fetch
- `git fetch [remote] [branch]`
---
## Merge
- Merge branch-1 into current branch: `git merge branch-1`
- Merge current branch's remote tracking branch into current branch: `git merge` (same as being in develop and issuing `git merge origin/develop`)
---
## Pull
- Pull (fetch and merge) remote changes into local repo: `git pull [<remote>] [<branch>]`
- Pull (rebase) remote changes into local repo: `git pull --rebase [<remote>] [<branch>]`
---
## Push
- Push commits from local repo to remote: `git push <remote> <branch>`
- Push commits from local repo to remote, and set remote-tracking branch: `git push --set-upstream <remote> <branch>`
- Push commits from local repo to remote, when remote-tracking branch is already set: `git push`
---
## Update local repo with remote repo changes
```
git checkout <branch>
git fetch [remote] [branch]
git merge [remote/branch]

eg.
git checkout master
git fetch origin master
git merge origin/master

eg.
git checkout master
git fetch
git merge

OR

git checkout <branch>
git pull [remote] [branch]

eg.
git checkout master
git pull origin master

eg.
git checkout master
git pull
```
## Remote Tracking
- Change remote tracking branch: `git branch [branch] --set-upstream-to <other-branch>`
- Change remote tracking branch (shorhand): `git branch [branch] -u <other-branch>`
- See remote tracking branch: `git branch -vv`
- Remove tracking: `git branch --unset-upstream`
---
## Tags
- Create tag (lightweight): `git tag <tag-name>`
- Create tag (annotated): `git tag <tag-name> -m "<message>"`
- Push tag to remote: `git push --tags`

