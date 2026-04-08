# Git-Cheat-sheet


# 📘 Git Cheat Sheet

A quick reference guide for essential Git commands 🚀

---

## 🚀 Getting Started

### Initialize a Repository
```bash
git init

#Clone a Repository
git clone <url>

#Add Files
git add <file>      # Add specific file
git add .           # Add all files
git add -p          # Add parts of a file

#Move / Delete Files
git mv <old> <new>
git rm <file>
git rm --cached <file>   # Remove from Git but keep locally

#Unstage Changes
git reset <file>
git reset

#check status
git status

#Make Commits
git commit                 # Open editor
git commit -m "message"   # Commit with message
git commit -am "message"  # Add + commit tracked files

#Switch Branch
git switch <name>
# OR
git checkout <name>


#Create Branch
git switch -c <name>
# OR
git checkout -b <name>

#List Branches
git branch
git branch --sort=-committerdate

#Delete Branch
git branch -d <name>
git branch -D <name>

#Diff changes
git diff            # Unstaged changes
git diff --staged   # Staged changes
git diff HEAD       # All changes

#Diff Commits
git show <commit>
git diff <commit1> <commit2>
git diff <commit> <file>
git diff <commit> --stat
git show <commit> --stat

#Discard Changes
git restore <file>
git restore --staged --worktree <file>
git reset --hard
git clean
git stash

#Edit history
git reset HEAD^              # Undo last commit
git rebase -i HEAD~6         # Squash commits
git commit --amend           # Edit last commit

#undo failed rebase
git reflog BRANCHNAME
git reset --hard <commit>

#code history
git log
git log --oneline
git log --graph
git log <file>
git log --follow <file>
git log -G "text"
git blame <file>

#merge and rebase
git switch feature
git rebase main

#Merge
git switch main
git merge feature

#Squash Merge
git merge --squash feature
git commit

#Cherry Pick
git cherry-pick <commit>

#Restore Files
git checkout <commit> <file>
# OR
git restore --source <commit> <file>

#Remote Repository
git remote add <name> <url>

#Push changes
git push origin main
git push
git push -u origin <branch>
git push --force-with-lease
git push --tags

#pull changes
git fetch origin main
git pull --rebase
git pull

#Configure git
git config user.name "Your Name"
git config --global user.email "you@example.com"
git config alias.st status

#view config
man git-config
