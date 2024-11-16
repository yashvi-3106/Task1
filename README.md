My First Project
git init
The command git init is used to create an empty Git repository. 
After the git init command is used, a .git folder is created in the directory with some subdirectories. Once the repository is initialized, the process of creating other files begins.

git add
Add command is used after checking the status of the files, to add those files to the staging area.
Before running the commit command, "git add" is used to add any new or modified files.
git add .

git commit
The commit command makes sure that the changes are saved to the local repository.
The command "git commit –m <message>" allows you to describe everyone and help them understand what has happened.
git commit -m “commit message”

git status
The git status command tells the current state of the repository.
The command provides the current working branch. If the files are in the staging area, but not committed, it will be shown by the git status. Also, if there are no changes, it will show the message no changes to commit, working directory clean.
git status

git config
The git config command is used initially to configure the user.name and user.email. This specifies what email id and username will be used from a local repository.
When git config is used with --global flag, it writes the settings to all repositories on the computer.
git config --global user.name “any user name”
git config --global user.email <email id>

git branch
The git branch command is used to determine what branch the local repository is on.
The command enables adding and deleting a branch.
# Create a new branch
  git branch <branch_name>

# List all remote or local branches
  git branch -a

# Delete a branch
  git branch -d <branch_name>


git checkout
The git checkout command is used to switch branches, whenever the work is to be started on a different branch.
The command works on three separate entities: files, commits, and branches.
# Checkout an existing branch
  git checkout <branch_name>

# Checkout and create a new branch with that name
  git checkout -b <new_branch>

git merge
The git merge command is used to integrate the branches together. The command combines the changes from one branch to another branch. 
It is used to merge the changes in the staging branch to the stable branch.
  git merge <branch_name>


git remote 
The git remote command is used to create, view, and delete connections to other repositories. 
The connections here are not like direct links into other repositories, but as bookmarks that serve as convenient names to be used as a reference.
git remote add origin <address>

git clone
The git clone command is used to create a local working copy of an existing remote repository.
The command downloads the remote repository to the computer. It is equivalent to the Git init command when working with a remote repository.
git clone <remote_URL>

git pull 
The git pull command is used to fetch and merge changes from the remote repository to the local repository.
The command "git pull origin master" copies all the files from the master branch of the remote repository to the local repository.
git pull <branch_name> <remote URL>


git push
The command git push is used to transfer the commits or pushing the content from the local repository to the remote repository.
The command is used after a local repository has been modified, and the modifications are to be shared with the remote team members.
git push -u origin master

git stash
The git stash command takes your modified tracked files and saves it on a pile of incomplete changes that you can reapply at any time. To go back to work, you can use the stash pop.
The git stash command will help a developer switch branches to work on something else without committing to incomplete work.
# Store current work with untracked files
  git stash -u

# Bring stashed work back to the working directory
  git stash pop

git log
The git log command shows the order of the commit history for a repository.
The command helps in understanding the state of the current branch by showing the commits that lead to this state.
git log

git diff
To see the changes you've made in your working directory (files that are modified but not yet staged for commit):
git diff --cached  or git diff --staged
To see the changes you've staged but haven't yet committed:
git diff <commit1> <commit2>
To compare two commits (using their commit hashes):
git diff <commit>
To compare a commit with your current working directory:
git diff <branch1> <branch2>
To see the difference between two branches:
git diff main feature-branch
git diff <source> <target> -- <file-path>
To compare specific files between two commits, branches, or other references:
git diff main feature-branch -- src/app.js
