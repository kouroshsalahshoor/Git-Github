# GitHub
[Udemy - Learn Git, GitHub and GitHub Actions](https://www.bilibili.com/video/BV1MJkQYgExD/?spm_id_from=333.788.videopod.episodes&vd_source=396d99df17169e23716a53b0fa85b893)
- [part2](https://www.bilibili.com/video/BV1MJkQYgE89/?spm_id_from=333.337.search-card.all.click&vd_source=396d99df17169e23716a53b0fa85b893)

![Git](https://raw.githubusercontent.com/kouroshsalahshoor/Git/refs/heads/main/git.png)

## Branch editing rules
settings>branches>add rule>  
- branch name pattern  
- require pull request reviews before merging

## Merge conflicts locally
`git fetch origin`  
`git switch feature/xxx`  
`git merge main` or master  
fix conflicts locally  
`git switch main` or master  
`git merge feature/xxx`  
`git push origin main`  
`git branch -D feature/xxx` delete feature branch locally  
`git pull origin main`  
`git status`  
`git log`  

## Workflow - Never on main
`git fetch origin main`  
`git status`  
`git branch -r`  

`git pull origin main`  
`git checkout feautre/xxx`  
`git switch -` - back to HEAD  

`git switch -c feautre/<xxx>` - new branch  
`git switch feautre/<xxx>`  
`git status`  
`git commit -am "comment"`  
`git push origin feauture/xxx`  

## rebase !!! never do when shared history with others !!!
`git switch feature/xxx`  
`git rebase main`  

## Github Pages
Settings > Pages > choose branch with index.html

## .md file
- [https://markdown-it.github.io/](https://markdown-it.github.io/)

## Pull & Push
`git pull origin <branch>`              - always pull before push  
`git pull`                              - pull current branch  
`git push origin <branch>`  
`git push`                              - push current branch  

## Fetch
`git fetch origin <branch>`

## Remote Branches
`git branch -r`  
`git switch <branch>`                   - recommended  
`git checkout --track origin/<branch>`  - old  
`git checkout origin/<branch>`          - detached HEAD

## Default Branch
settings > branches > main

## Push
`git branch -M main`                    - rename branch  
`git push origin <remote-branch>`       - creates remote branch if missing  
`git push origin <local-branch>:<remote-branch>`  

`git push -u origin main`  
`git push -u origin <remote-branch>`  
`git push -u origin <local-branch>:<remote-branch>`  

`git push`                              - upstream already set  
`git push origin master`  
`git push <remote> <branch>`

## Remote
`git remote add origin <repo-url>`  
`git remote add <name> <repo-url>`  
`git remote -v`  
`git remote rename <old> <new>`  
`git remote remove <name>`

## Clone
`git clone <url>`

# Git

### Revert
`git revert <hash>` — like reset, loses changes to that commit but creates a new commit

### Back to some commit – correcting commit
`git reset --hard <hash>` — loses changes on working directory  
`git reset <hash>` — keeps changes on working directory  
`git log --oneline` — to get the hash

### Unstaging files
`git restore --staged <file name>`  
`git status`

### Discarding workplace file changes
`git restore <file name>` — last commit  
`git restore --source HEAD~1 <file name>`  
`git checkout HEAD <file name>` — latest changes go away, back to where HEAD is (last commit)  
`git checkout -- <file name>`

### Going back in time
`git checkout <hash>` — detached HEAD  
`git switch master` — pointing at the last commit  
`git log --oneline` — to see what is going on  
`git switch -c <new-branch-name>` — create and switch to new branch

### Stash
`git stash`  
`git stash pop`

### Diff
`git diff`  
`git diff HEAD` — all changes vs HEAD  
`git diff --staged`  
`git diff --cached`  
`git diff branch1..branch2`  
`git diff commit1..commit2`

### Merge
`git switch master`  
`git merge <a branch>` — fast forward | commit merge (no conflicts) | conflict

### Checkout – old way
`git checkout <branchname>` — change branch  
`git checkout -b <branchname>` — create & switch to branch  
`git checkout HEAD~1` — parent  
`git checkout HEAD~2` — grandparent

### Branches
`git branch` — list of branches (master is git default, main is GitHub default)

`git switch master`  
`git branch <branchname>` — creates a new branch based on where HEAD is (always commit before)  
`git switch <branchname>` — checkout is the old command  
`git switch -c <branchname>` — create & switch to branch

`git branch -d <branchname>` — delete (must be on a different branch)  
`git branch -D <branchname>` — force delete

`git branch -m <branchname>` — rename (must be on branch)  
`git branch -v` — more info

### Log
`git log` — top row is last  
`git log --oneline`

### Most common ***
`git status` — to see what is happening  
`git add .` — always before commit  
`git commit -m "xxx"` — always present form  
`git commit -a -m "xxx"` — add & commit

`git commit -am "xxx"` — add & commit

### Init
`git init`

### Settings
`git config --global -l`  
`git config user.name`  

`git config --global user.name "xxx"`  
`git config --global user.email "xxx@x.x"`  
`git config --global core.editor "code --wait"`  
`git config --global init.defaultbranch main`  

[Udemy - The Git & Github Bootcamp](https://www.bilibili.com/video/BV1YM7qzWEqo/?spm_id_from=333.337.search-card.all.click&vd_source=396d99df17169e23716a53b0fa85b893)
 - [part 2](https://www.bilibili.com/video/BV1y17izuEJc/?spm_id_from=333.337.search-card.all.click&vd_source=396d99df17169e23716a53b0fa85b893)
