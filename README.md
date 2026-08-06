# Git Set Go 2.0 - Hands-On Lab

Welcome to the hands-on lab! This repository contains the reference commands from the session[cite: 1] and a sandbox to practice resolving a merge conflict[cite: 1].

## 1. Basics: The Three Trees
Every file moves through the Working Directory, Staging Area, and Local Repository[cite: 1].

*   `git init` - Initialize a repository[cite: 1]
*   `git status` - See what's changed or staged[cite: 1]
*   `git add <file>` - Move changes to the staging area[cite: 1]
*   `git commit -m "msg"` - Save a permanent snapshot[cite: 1]
*   `git commit --amend` - Fix your last commit message[cite: 1]

## 2. Git Internals: Under the Hood
Git acts as a key-value store, assigning a SHA-1 hash to content[cite: 1]. 

*   `git hash-object <file>` - See the mathematical hash Git generates for a file[cite: 1]
*   `git cat-file -p <sha>` - Print the raw contents of a blob, tree, or commit[cite: 1]

## 3. Branching & Merging
Branching is cheap, so experimentation is the default[cite: 1].

*   `git branch <name>` - Create a new branch[cite: 1]
*   `git switch <name>` (or `git checkout <name>`) - Move to another branch[cite: 1]
*   `git checkout -b <name>` - Create and switch in one step[cite: 1]

### 🚨 Live Lab: Resolve a Merge Conflict 🚨
This repository has a built-in conflict waiting for you. Follow these steps:
1. Make sure you are on the main branch: `git switch main`[cite: 1]
2. Merge the feature branch: `git merge feature-update`[cite: 1]
3. **Conflict!** Open `conflict-demo.txt` in your editor.
4. Delete the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) and keep the text you want.
5. Save the file.
6. Stage the resolution: `git add conflict-demo.txt`
7. Complete the merge: `git commit -m "resolve merge conflict"`

## 4. Remotes & History
Syncing your local history with the outside world.

*   `git remote add origin <url>` - Link a remote repository[cite: 1]
*   `git fetch` - Download new commits without merging[cite: 1]
*   `git pull` - Fetch and merge in one step[cite: 1]
*   `git push` - Upload your local commits[cite: 1]
*   `git log --oneline --graph` - See a visual history of your branches[cite: 1]
