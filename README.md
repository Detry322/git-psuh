# git-psuh
###Fix sloppy coding through negative reinforcement!

Ever mistype `git push`? Want to fix that? git-psuh has your back!

Be like Ivan and never make a mistake again!

![Never shoot the inaccurate](http://i1.kym-cdn.com/photos/images/newsfeed/000/856/438/e1c.jpg)

*Every time* you mistype `git push`, this command will force-push an totally empty branch instead of your current branch. Not only that, but it also force pushes `master`!

## Installation
...

## Usage
Simply run in any repo!

```
git psuh
```

## More details

```
usage: git psuh [undo] [--version] [--help]
Fix mistakes through negative reinforcement!

This command:
  - Commits any current changes
  - Moves master to master_old
  - Creates a new empty branch called master
  - Force pushes it
  - Also does the above to your current branch if you're not on master

Undo should only be called immediately after a psuh, but
it restores everything, and uncommits what was committed at the beginning
```
