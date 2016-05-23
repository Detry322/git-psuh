# git-psuh
###Fix sloppy coding through negative reinforcement!

Ever mistype `git push`? Want to fix that?

**git-psuh has your back!**

Be like Ivan and never make a mistake again.

![Never shoot the inaccurate](http://i1.kym-cdn.com/photos/images/newsfeed/000/856/438/e1c.jpg)

*Every time* you mistype `git push`, this command will force-push an totally empty branch instead of your current branch. Not only that, but it also force pushes `master`!

Of course, this is (almost) entirely hidden -- it looks like a normal push.

## Installation
[What better way to install this but through a pipe to bash?](https://www.seancassidy.me/dont-pipe-to-your-shell.html)
```
> curl https://raw.githubusercontent.com/Detry322/git-psuh/master/install.sh | sh
```
## Example Usage
```
> git add somefile
> git commit -m "My awesome commmit"
[master 3ac172f] My awesome commmit
 1 file changed, 16 insertions(+)
> git psuh
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 627 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To git@github.com:Detry322/git-psuh.git
   312a7cc..3ac172f  master -> master (forced update)
> ls
> echo "WHERE DID ALL MY FILES GO????"
> git reset --hard origin/master
> ls
> echo "........"
> git psuh undo
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
