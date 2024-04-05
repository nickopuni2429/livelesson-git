# Git Notes

## Working with git locally

- `git init`: initialize current folder as a git repository
- `git clone <URL>`: brings the git repo from <URL> to the current folder
- `git status`: tells us what we need to know about our repository

- `git add <FILE>`: adds <FILE> to the staging area
- `git commit`: open a text editor to write commit message
	- `git commit -m "MESSAGE"`: writes MESSAGE as a commit without a text editor

- `git log`: shows the log (history) of our commits
	- `git log --oneline`: shows the shorter oneline commit

- `git diff`: compare current uncommited state with last known git state
	- `git diff --staged`: runs git diff between the staging area and the last known state
- `git diff HEAD~<NUMBER>`: compares HEAD with commit <NUMBER> ago (relative)
- `git diff <HASH>`: compares HEAD with the commit in <HASH>

- `git restore --source <HASH OR HEAD~> <FILE>`: restore file to <HASH OR HEAD~>
	- `git checkout <HASH OR HEAD~> <FILE>`: restores file to <HASH OR HEAD~>
		- `git checkout <HASH OR HEAD~>`: if you forget the file, you'll end up in detached HEAD state.
		- `git checkout master`: go back to master
		- `git switch master`: go back to master

## Working With Remotes

- `git remote add <NAME> <URL>`: adds the <URL> as a remote with the name <NAME>
	- <NAME> is by convention called `origin`
- `git remote rm <NAME>`: removes the remote called <NAME>
- `git remote -v`: look at all the remotes you have
- `git push <WHERE> <WHAT>`: pushes the <WHAT> branch to <WHERE>
	- `git push origin main`
- `git pull <WHERE> <WHAT>`: pulls the <WHAT> branch in the <WHERE> to the local computer

## BRANCHES

- `git branch <NAME>`: create branch <NAME> where you are (HEAD)
- `git switch <NAME>`: move to the branch <NAME>
	- `git checkout <NAME>`: also move to the branch <NAME>
- `git swich -c <NAME>`: create and move to the branch <NAME> in 1 command
	- `git checkout -b <NAME>`: also create and move to branch <NAME> in 1 command

- `git merge <BRANCH>`: merge <BRANCH> into your current branch
- `git rebase`: command to change the history of a commit
	- Commits from `git merge` can be automatically combined
- `git rebase <BRANCH>`: incorporate changes from <BRANCH> into current branch

- main commit 1
- main commit 2
