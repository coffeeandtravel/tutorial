
## First configure git account

- Use it in the root folder with starting with "~" 
```git
git config --global user.name "<--->"
git config --global user.email "<---->"

git config --list
```

## Cloning
- Use it to clone a repository on your computer
```git
git clone <.https link>
```
- use ls to list the files and ls -a to list the hidden files
```
ls
ls -a
```


## Status
- It will show the status of the repository(That means uncommitted or new changes are done in the repo or not).
```git
git status
```

	it will also show the untracked files(new files added without any changes in git)

### Types of Status

`untracked` : Files which are not updated entirely

`modified`:  Changes to files which are already present but not committed

`staged`: Ready to commit

`unmodified`: unchanged


## git add & commit

- Add new or changed files in your working directory

	`git add <filename>`

	uncommitted changes is called staging area.

- commit is the record of the change
	`git commit -m "Some message"`


### now after doing all this the changes are committed in to your local repo and now to upload it into the GitHub you will need to use:

```git
git push origin main
```


#### Creating new repository locally:

```git
git init
```

- After that add and commit the changes.
- Create a new repository on GitHub

##### After Creating a new repository do the following:

```git 
git remote add origin <-link-> 
```

Now you can verify that remote with
```git
git remote -v
```

To check which branch you are working on use:
```git 
git branch
```
- The branch will be master branch and you have to work with main branch so to do that do: 
###### To rename a branch: 
```git 
git branch -M <-branch name->
```

if you write this then all the changes will be done in the origin main file and you don't have to write origin main again and again
```git
git push -u origin main
```

## Git Branches

#### If you want to change/navigate to some other branch then:
```git
git checkout <-branch name-> 
```

#### If you want to create a new branch then:
```git
git checkout -b <-new branch name->
```

#### If you want to delete a branch then:
```git 
git branch -d <-branchname->
```
- You cannot delete the branch on which you are currently on.

#### When you want to push the changes to a specific branch then:
```git
git push origin <-branch name->
```


## Merging branches

When you want to compare two different branches then use:
```git
git diff <-branch name->
```

this will compare you with the current branch and the branch you provided and after that you will use:
```git
git merge <-branch name->
```


### Or you can directly use GitHub using Pull Request to merge files
 
- Pull request tells you tell others about the changes you've pushed to a branch in a repository on GitHub


## When you want to fetch and download content from a remote repo

```git
git pull origin main
```


## Resolving merge conflicts 
An event that takes place when Git is unable to automatically resolve differences in the code between two commits.  

![[Pasted image 20240213010157.png]]

Now we can choose which one change we can have manually or automatically from the given options. 
after all this we can do 
```git
git merge feature1
```
this will merge the changes made into the feature1 branch.


## Undoing changes
### Case 1: staged changes
```git 
git reset <-filename->
git reset
```

### Case 2: Committed changes(for 1 commit)
```git
git reset HEAD~1
```

### Case 3: Using hash of a specific commit.
```git
git reset <-hash of that specific commit-> 
```

- To know the specific log and hash use `git log`

