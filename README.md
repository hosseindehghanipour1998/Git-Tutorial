# Git-Tutorial

Here I upload anything I learn from Git.

There's a booklet written by me and tought by jadi (https://github.com/jadijadi ) read it you may find it useful.
If you have a booklet which is better than what I have uploaded please and please share it with me too.
If you found any errors in any of the uploaded files ( Lexical or grammatical or ... errors ) please inform me. I will gladly edit the file.

With Regards,
Hossein Dehghanipour.
#To remove all barriers in the way of science.


### undo Things : 
  - [Checkout]() : goes to a specific commit in read-only mode without changing anything.
  - [Revert]() : goes to a specific commit and removes it from the tree as it had never been existed.
  - [Reset]() : goes to a specific commit and deletes all the commits from that commit till the current commit.
  

##### Checkout
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git checkout <commit hash>`
4.  `git checkout master `

#### Revert 
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git revert <commit hash>`
4.  In order to exit the vs : press `shift + : ` then type `wq` and presss `Enter` 
  *  As you can see, a new commit has been added to your log which means that this new commit has simply _undone_ what ever you had done in that specific commit. As an example if you had removed a  _text file_  in that commit, the _text file_ will be retrieved to your current repository.
  
  
#### Reset
1. `git log --oneline`
2.  Get the hash of the commit you want to travel to.
3.  `git reset <commit hash> --hard`
  *  Now there is no way to retain or revert the codes and files you had made after that specific commit.
  
  
  
