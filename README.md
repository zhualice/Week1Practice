### :octocat: Git Your Practice On!


#UBC APP and THAT, WEEK 1: GIT PRACTICE

## Instructions

#####NOTE: If you have questions, don't hestate to post on Piazza!


######1:  Fork and Clone
1. Fork this repository and then clone it onto your local machine
2. Add your name (and whatever else you want) to the *very* bottom of this file
3. Push your changes to *your forked* repository on github (not this one!) 


######2: Fork and Pull

4. Send me (this repo, not yours) a pull request!
5. Replace you name with your github username in README.md and commit your changes
6. Fetch your remote repo and merge it with your local one 


######3:  Issues
7. Create an issue on GitHub called: "Need moar ACII Arts" (or anyother name you want!) on GitHub. 
   Add a description too! I'll close the issue when you've finished this exercise (step 10).


######4:  Branching
8. Create a new branch with the name of your GitHub username.
9. Switch to your new branch and add some ASCII Art [generate it here](http://www.glassgiant.com/ascii/) beside your name
10. Push your branch to your forked repo and then send me a pull request to the origin repo (at /AppsandThat/Week1Practice.git)
12. Switch back to your master branch and merge your new branch into your master branch
11. Delete your branch that you created in part 8 (only on your local repo)


######5:  Finishing Up
12. Push the changes to your forked repo 
13. Send me another pull request with your newly add ASCII Art
14. You're *DONE*! If you are still curious check out [http://www.gitref.com](gitref.com) or look below for more commands. Also try forking and editing our website repository here: [github.com/AppsandThat/AppsandThat.io](Apps n That repo). I've created a few issues for you to solve
 


##HELPFUL RESOURCES
---------------------------------------------------------------------------------------------------------------------

* Git Reference [http://gitref.org/basic](http://gitref.org/basic)
* Git Ready [http://gitready.com](http://gitready.com)
* Quick Command Practice [http://try.github.com](http://try.github.com)
* Git Real [http://www.codeschool.com/courses/git-real](http://www.codeschool.com/courses/git-real)
* How to GitHub: Fork, Branch, Track, Squash and Pull Request [http://gun.io/blog/how-to-github-fork-branch-and-pull-request](http://gun.io/blog/how-to-github-fork-branch-and-pull-request)
* Learn Git Online [http://learn.github.com/p/intro.html](http://learn.github.com/p/intro.html)
* Teach Github [https://github.com/github/teach.github.com](https://github.com/github/teach.github.com)
* Git: The Simple Guide [http://rogerdudler.github.com/git-guide](http://rogerdudler.github.com/git-guide)
* Git Immersion [http://gitimmersion.com](http://gitimmersion.com)
* Git Branching [http://pcottle.github.io/learnGitBranching/](http://pcottle.github.io/learnGitBranching/)


##Useful & Common GIT Commands
---------------------------------------------------------------------------------------------------------------------

```bash
git clone git@github.com:<user_name>/the-repo-you-are-cloning.git
```
Clones your remote origin repo locally

```bash
git fetch upstream
```
Pulls in the remote changes not present in your local repo. Downloads objects and references from another repository.

```bash
git merge upstream/master
```
Merges any changes fetched into your working files

```bash
git add <file>
```
Start tracking new files and also stage changes to already tracked files

``git status`` & ``git diff``
* Tells us what files and assets have been modified and staged

```bash
git status -s
```
This will display what files have been removed, changed or modified. 

* (M)  - modified
* (A)  - added
* (AM) - file has not been altered since it was last added

```bash
git commit -m 'the message goes here for the commit'
```
Records a snapshot of the project into your history at the time of your commit.

```bash
git add '*.<file_extension>'
```
This command adds all file types with the same extension, especially from different directories. Without quotes the command will only execute within the same directory it's been called from.

```bash
git rm --cached <file>
```
Unstages a file from the working tree (i.e. stops tracking the file).

```bash
git log
```
Remembers all the changes we've committed so far, in the order we committed them.

```bash
git log --summary
```
See where new files were added for the first time or where files were deleted.

```bash
git remote add origin git@github.com:<user_name>/<repo_name>.git
```
Creates a brand new remote repository.

```bash
git remote -v
```
Show a list of the current remote repositories

```bash
git reset <file>
```
Removes the desired file from staging area.

```bash
git branch -r
```
List all the remote branches currently tracked

```bash
git remote prune origin
```
Deletes branch locally if it has been removed remotely. Helps to remove stale references.

```bash
git checkout -- <target>
```
Changes the desired target back to the state of the last commit. A target can be a file or a directory (for example).

```bash
git rebase
```
Rebase allows you to [easily change a series of commits, reordering, editing, or squashing commits together into a single commit](https://help.github.com/articles/interactive-rebase).

Be warned: it's considered bad practice to rebase commits which you have already pushed to a remote repo. Doing so may invoke the wrath of the git gods. [https://help.github.com/articles/interactive-rebase](https://help.github.com/articles/interactive-rebase)

### Adding
```bash
git add <list of files>
``` 
(i.e. ``git add readme.md license.txt``. Can be multiples)

```bash
git add --all
```
Add all the new files since last

```bash
git add *.txt
```
Add all txt files in directory

### Staging
```bash
git diff
```
Show unstaged differences since last commit

```bash
git diff --staged
```
Gets the staged differences and displays what has changed since our last commit

### Reverting
```bash
git reset HEAD <file>
```
Head is the last commit on the current branch we are on. What if you stage something you didn't need to be staged? This is the key.

```bash
git checkout -- <file>
```
Reset all changes to a file since last commit

```bash
git reset --soft HEAD^
```
What if you regret a commit? This will undo your last commit. (^ means move commit before HEAD and puts changes into staging).

```bash
git reset --hard HEAD^
```
Traverse through commits and revert back one by one.

```bash
git reset --hard HEAD
```
Undo Last commit and all changes

```bash
git commit --amend -m "added another file to the commit'
```
New commit message will override previous commit message

### Remotes
"Remotes are kinda like bookmarks"

```bash
git remote -v
```
Show the current remote repos

```bash
git remote add <name> <address>
```
Add a new remote repo

```bash
git remote rm <name>
```
Remove remote repo

### Cloning, Branching, Fetching &amp; Merging
```bash
git fetch
```
Pulls down any changes but doesn't merge them

```bash
git branch <branch name>
```
Makes a new branch

```bash
git checkout <branch name>
```
Switching branch and on a different timeline

```bash
git merge <branch>
```
Merges branch into master

```bash
git branch -d <branch name>
```
Deletes branch

```bash
git checkout -b <branch name>
```
Creates a new branch and then switches to it

```bash
:wq + enter
```
VI Editor Quick Key Exit

```bash
g fetch origin

git checkout -t <remote>/<branch>
```
Fetches a remote branch not available locally [also reference issue #7](https://github.com/grayghostvisuals/Practice-Git/issues/7)

### Pushing &amp; Pulling
```bash
git push -u origin master (remote repo name[origin], local branch name[master])
``` 
Lets you just run git push later on without specifying name and branch

```bash
git pull
```
Pull changes in and syncs up your repo. Doesn't update local code

### Branching
```bash
git branch -r
```
List all remote branches

```bash
git remote show origin
```
Show all the remote branches

```bash
git push origin :<branch name>
```
Deletes the remote branch

```bash
git branch -D <branch name>
```
Delete the local repo branch and if you don't want the commits any longer on it then delete them too.

```bash
git remote prune origin
```
Deletes the branch locally if it has been removed remotely. Helps to remove stale references.

### Rebasing
"Merge commits are bad"

```bash
git rebase
```
Move all changes to master local which are not in origin/master remote to a temporary area

### History
```bash
git log
```
Viewing the commits history

```bash
git config --global color.ui true
```
Color codes the commit SHA

```bash
git log --pretty=oneline
```

or 

```bash
git log --graph --oneline --all
```
Commit and history is one line

```bash
git log --pretty=format:"%h
```
Exactly how you want the output using placeholders (use git help log)

```bash
git log --until <value>
```
Date Ranges. For example you could grab everything from the year 2013 using ``git log --until 2013``

### Removal
```bash
git rm <filename>
```
Removes file completely

```bash
git rm --cached <file names>
```
Won't be deleted from your file system, but keeps the local changes still.

### Help
```bash
git help
```
```bash
git help <command>
```


DAVID BALDWIN

ANON~ 
