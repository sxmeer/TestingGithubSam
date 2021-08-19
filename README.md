# git commands list with short explanations of each

1. git init => to initialize git in a particular directory.
2. git status => to check the current status of the directory, like untracked files, changed files, deleted files, new files.
3. git add => to add files into staging area.  
   examples:  
   git add . => to add all the files into staging area.  
   git add filename => to add a particular file into staging area.
4. git commit -m "commit message" => committing the changes into git
5. git restore --staged filename => to unstage the staged files.
6. git log => shows the commit history
7. git reset hasdID => takes the repo to that version of the repo.
8. git stash => to put the staged changes to the stash area and the repo version is upto date with head
9. git stash clear => to clear the changes in the stash area
10. git stash pop => to take the changes and merge in the current working version (may contain merge conflict)

# github commands

1. git remote add origin {link} => remote means working with links, origin is an alias for our repo
2. git remote -v => to show if remote repo is linked
3. git push origin {master} -f => origin is the alias and master is the branchname. f flag is for force push.

4. git clone {link} => cloning repository from github
5. git remote add upstream {link} => adding upstream as a repo link from which current project was forked.
6. git branch => lists all the branches a particular repo has.
7. git branch {branchname} => this command creates branches.
8. git checkout {branchname} => this selects the given branch.
9. git checkout -b {branchName} => creation and checkout in one step

## steps to get the latest commits from forked repo.

1. git checkout {Mainbranch} => select main branch
2. git fetch --all --prune => fetch all the commits and even the prune one's deleted
3. git reset --hard upstream/main => reseting the main branch to upstream's main branch
4. git push origin main => pushing the changes to the origin.

- or

1. git pull upstream main
1. git push origin main

- or  
  fetch upstream on github

## squashing commits (how to merge commits)

1. git rebase -i hashID => select pick commit to create the commit and s to merge the commit to previous pick commit
