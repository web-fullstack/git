# git branch


```sh
# list all branch(local)
$ git branch --list
$ git branch -l
# OR
$ git branch

# list all remote branches
$ git branch -a
# Q === quit

# create branch
# $ git checkout -b <branch_name>
$ git checkout -b test
# OR
# $ git branch <branch_name>
$ git branch test

# delete branch
# -d safe delete
# $ git branch -d <branch_name>
$ git branch -d test
# Deleted branch test (was 686c96b).

# -D force delete
# $ git branch -D <branch_name>
$ git branch -D test

# rename the current branch
# $ git branch -m <branch>
$ git branch -m test

# change branch
$ git checkout branch flutter-app

```

https://www.atlassian.com/git/tutorials/using-branches

```code
  flutter-app
  test
* master

```

```code
  flutter-app
  test
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/gh-pages
  remotes/origin/master

```

## git remote

https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes

https://git-scm.com/docs/git-remote

```sh
# git remote [-v | --verbose]
# git remote add [-t <branch>] [-m <master>] [-f] [--[no-]tags] [--mirror=<fetch|push>] <name> <url>
# git remote rename <old> <new>
# git remote remove <name>
# git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
# git remote set-branches [--add] <name> <branch>…​
# git remote get-url [--push] [--all] <name>
# git remote set-url [--push] <name> <newurl> [<oldurl>]
# git remote set-url --add [--push] <name> <newurl>
# git remote set-url --delete [--push] <name> <url>
# git remote [-v | --verbose] show [-n] <name>…​
# git remote prune [-n | --dry-run] <name>…​
# git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)…​]

```

## git create remote branch

```sh
# Create a new branch and check it out
$ git checkout -b <branch-name>

# The remote branch is automatically created when you push it to the remote server. 
# <remote-name> is typically origin
$ git push <remote-name> <branch-name> 

$ git push <remote-name> <local-branch-name>:<remote-branch-name>

$ git push --set-upstream <remote-name> <local-branch-name> 

```

```sh
# create a new branch & check it out
$ git checkout -b test

# local & remote  with the same name
$ git push origin test

# local & remote with a different name
$ git push origin test:dev

# ❌ delete remote branch bug, if only `:<remote-branch-name>` 
$ git push origin :dev


# delete remote branch 💩⚠ ❌
$ git push origin --delete test
# OR
$ git push origin :test

```

https://tecadmin.net/how-to-create-a-branch-in-remote-git-repository/

https://stackoverflow.com/questions/1519006/how-do-you-create-a-remote-git-branch



## git remote add


https://www.atlassian.com/git/tutorials/syncing

https://docs.github.com/en/github/using-git/adding-a-remote

```sh
$ git remote add origin https://github.com/user/repo.git
# Set a new remote

$ git remote -v
# Verify new remote
> origin  https://github.com/user/repo.git (fetch)
> origin  https://github.com/user/repo.git (push)

```


https://stackoverflow.com/questions/42830557/git-remote-add-origin-vs-remote-set-url-origin

```sh
$ git remote add origin git@github.com:User/UserRepo.git

$ git push -u origin master
```
