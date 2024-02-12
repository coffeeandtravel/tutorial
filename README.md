
# First configure git account

- Use it in the root folder with starting with "~" 
```git
git config --global user.name "<--->"
git config --global user.email "<---->"

git config --list
```

# Cloning
- Use it to clone a repository on your computer
```git
git clone <.https link>
```
- use ls to list the files and ls -a to list the hidden files
```
ls
ls -a
```


# Status
- It will show the status of the repository(That means uncommitted or new changes are done in the repo or not).
```git
git status
```

	it will also show the untracked files(new files added without any changes in git)

## Types of Status
<hr>

`untracked` : Files which are not updated entirely
`modified`:  Changes to files which are already present but not committed
`staged`: Ready to commit
`unmodified`: unchanged


# git add & commit

- Add new or changed files in your working directory

	`git add <filename>`

	uncommitted changes is called staging area.

- commit is the record of the change
	`git commit -m "Some message"`


## now after doing all this the changes are committed in to your local repo and now to upload it into the github you wil need to use:

```git
git push origin main
```

