
## git stash
https://git-scm.com/docs/git-stash

When you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the HEAD commit.
```
$ git stash
```
```
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
Make new branch and switch to new the branch
```
$ git checkout -b <branch>
$ git checkout -b feature/new_branch
```

Make clone branch from orign branch. However before better do `git fetch --all` and see all branches `git branch -a`
```
$ git checkout -b <branch> origin/<branch>
$ git checkout -b feature/new_branch origin/feature/new_branch
```

Just switch to branch
```
$ git checkout <branch>
$ git checkout feature/new_branch
```

## git branch
https://git-scm.com/docs/git-branch

Show branches
```
$ git branch
```

Show remote branches
```
$ git branch -r
```

Show all branches
```
$ git branch -a
```

Rename branch
```
$ git branch -m | -M [<oldbranch>] <newbranch>
$ git branch -m | -M feature/my_branch_test feature/my_branch
```

Delete branch
```
$ git branch -d | -D <branch>
$ git branch -d | -D feature/new_branch
```
Delete in remote repository 
```
git push origin --delete <branch>
git push origin --delete feature/new_branch
```

Just create new branch
```
$ git branch <branch>
$ git branch feature/new_branch
```

## git rebase
https://git-scm.com/docs/git-rebase

```
$ git rebase -i HEAD~2
```

## Squash Commits
https://www.git-tower.com/learn/git/faq/git-squash

For instance we want to squash last two commits
```
$ git rebase -i HEAD~2
```
Then will open editor and we need to change `pick` -> `squash` or just `s`
And make push
```
$ git push --force
```


## git merge

We want to make merge in branch feature/my_branch
```
$ git merge main
```

## git reset 
https://initialcommit.com/blog/git-reset#what-is-git-reset
https://git-scm.com/docs/git-reset

Before make
```
$ git fetch --all
```
Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded. Any untracked files or directories in the way of writing any tracked files are simply deleted.  
```
$ git reset --hard origin/develop
```
or 
`soft`  
Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it.
```
$ git reset --soft origin/develop
```

