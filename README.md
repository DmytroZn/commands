
## git stash
https://git-scm.com/docs/git-stash

When you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the HEAD commit.
```
$ git stash
$ git stash save "add style to our site"
```

List the stash entries that you currently have
```
$ git stash list
```

Remove one the stash entry
```
$ git stash drop 1
```
Remove all the stash entries
```
$ git stash clear
```

Apply it on top of the current working tree state
```
$ git stash apply 1
```


## git checkout
Make new branch and switch to new branch
```
$ git checkout -b feature/new_branch
```
Make clone branch from orign branch. However before better do ```git fetch --all```:

```
$ git checkout -b feature/new_branch origin/feature/new_branch
```


$ git checkout feature/new_branch

```
