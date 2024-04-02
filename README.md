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
