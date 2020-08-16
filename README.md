# Git-Tutorial

Here I upload anything I learn from Git.
With Regards,
Hossein Dehghanipour.
## Tutorial

### Install git
`sudo apt-get install git`
or simply download git Desktop application from [here](https://desktop.github.com/)

### Starting a git repository
When We are in a directory and we want to start working with GIT, the first command is :`

  1. `$ git init`  which means from now on this directory is under control of git.
  2. `$ git status` The status of current repository.
  3. `$ git add <file name>`
    - `$ git add .` : adds all files that are not already added or changed somehow.
    - `$ git add –A` :  adds all files that are not already added or changed somehow.
  4. Let’s Tell git who we are and who is going to make changes to the file.
    - `$ git config --global user.email ”<emailAddress>”`  
    > $ git config --global user.email "Hossein.Dehghanipour1998@gmail.com"

    - `$ git config --global user.name ”<Your name>”`
  5. when we make a change, git calls it an __“Untracked File|change “__.
    - `$ git commit –m “*”`
     > instead of the \“\*\”, we write some descriptions of what we have done (the changes) to the files.

  6. `$ git log` tells us what ever we have done to this git repository and who has made what changes.
  7. when we make some files at the “Staged” position but we are not sure if we have made the correct changes. so we use `$ git diff --staged` to see the changes made to the files.  
  8. assume that we have made some changes to a file but we want to Undo the Changes and revert the changes made to the file. `$ git checkout -- <fileName>`
  9. we can see the changes made to the files by : `$ git diff HEAD` and also see our current head.
  10. `$ git branch` : Shows our current branch that we are in `$ git branch <branch name>`
> you should have a commit on the master in order to create a new branch.

  11. If we want to delete a file from git, we write `$ git rm <file name>` this command deletes the following file from both git and file system.
  12. after we have done with our branch and we have merged it, we can delete the branch. so we use the command `$ git branch –d <branch name>`.
  13. ` $ git clone <the address copied from git >`
  14. `$ git push origin master`
    - when we clone a project from github, the remote set to the master of the project is usually ___origin___.
  15. `$ git pull origin master`
  > if we have a public repository, we can pull from it but pushing to a repository requires the owner’s permission.

  >  we can add a remote to our directory. we can make remote to any directory from any other directory. If the directory doesn’t exist, we will face an error that tells us the path/URL we are aiming for doesn’t exist as a GIT repository.

  > our projects can have more than one remotes. We can push our project onto two different servers or pull from two different servers. for example, as a new commit is made we can push it to both gitlab and github simultaneously with two different remotes pointing to different servers.

  16. by entering `git log` command you can see all the commits and their committers. but what else you can see is that it shows you the hash of the commits. by command `$ git show <commit hash>` you can see the details of that commit .

  17. ` $ git remote add <URL>` -> creates a new remote to the project.
    -  we can insert the copied URL into the terminal by pushing ___“ ctrl + insert “___.
  18. `$ git remote –v` -> shows us all the available remotes in the project.

### Labeling

### undo Things :
  - [Checkout](https://github.com/hosseindehghanipour1998/Git-Tutorial#checkout) : goes to a specific commit in read-only mode without changing anything.
  - [Revert](https://github.com/hosseindehghanipour1998/Git-Tutorial#revert) : goes to a specific commit and removes it from the tree as it had never been existed.
  - [Reset](https://github.com/hosseindehghanipour1998/Git-Tutorial#reset) : goes to a specific commit and deletes all the commits from that commit till the current commit.


##### Checkout
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git checkout <commit hash>`
4.  `git checkout master `

#### Revert
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git revert <commit hash>`
4.  In order to exit the vs : press `shift + : ` then type `wq` and press `Enter`
  *  As you can see, a new commit has been added to your log which means that this new commit has simply _undone_ what ever you had done in that specific commit. As an example if you had removed a  _text file_  in that commit, the _text file_ will be retrieved to your current repository.


#### Reset
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git reset <commit hash> --hard`
  *  Now there is no way to retain or revert the codes and files you had made after that specific commit.


### Change Git Editor
`git config --global core.editor "nano" `
