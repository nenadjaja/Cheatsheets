- creating
$ git branch branchname                         // create new branch
$ git checkout -b branchname                // create and checkout new branch
$ git branch -a                                // show all branches (local and remotes)
$ git branch -r                                // show only remote branches 
$ git branch -v                                // show branches and last commits 
- you can combine flags -rv, -a
- deleting
$ git branch -d branchname                // delete a branch locally
$ git push origin :remotebranch        // delete a remote branch


- other
$ git checkout branchname                // switch to another branch
$ git add filename                                // add new file to staging
$ git rm filename                                // first do $ rm filename
$ git rm -f filename                        // force remove
$ git rm -cached filename                // untrack the file
$ git mv myfile newfile                        // rename the file
$ git commit -m “message”                // commit your changes
$ git commit -am “message”                // commit and stage all changes
$ git status                                        // check untracked files
$ git diff                                        // list unstaged diff since last commit
$ git diff --staged                                // list staged diff since last commit
$ git diff --cached                                // the same as above
$ git log                                                // list of all changes/commits
$ git log        -p                                        // shows diff in each commit
$ git log        --stat                                // see stats for each commit
$ git log --pretty=online                // options:short,full,fuller
$ git log --pretty=format:"%h %s" --graph        // nice print 


Undoing things:


$ git commit --amend                                // ‘append’ to the last commit
- usage:
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend
git reset --soft HEAD~1


$ git pull origin master                // pull from origin
$ git push origin branchname                // push branch to origin
$ git remote add origin https://github.com/user/repo.git        
$ git push origin :branchname        // delete remote branch (at origin)
$ git remote rm destination                // remove remote repo locally
$ git remote rename origin destination        // change remote name
$ git remote set-url origin git@github.roving.com:ES/spui.git


$ git reset filename                        // unstage files
$ git checkout -- filename                // get rid of filename


$ git help                                        // ask for help 
$ git help [command]        
$ git [command] help
$ man git [command]                


- First time you configure git
$ git config --global user.name "Nevena Djaja"
$ git config --global user.email nevena.djaja@gmail.com
$ git config --global color.ui true


- check your settings
$ git config --list


- Clone from remote
$ git clone git://github.com/schacon/grit.git myfolder


- Clone from local
$ git clone mylocalrepo


- Clone only one branch
$ git clone -b mybranch --single-branch git://github.com/schacon/grit.git 
- Pull only one branch from existing repo
$git checkout -b integration origin/integration
$git fetch --all         // will only update existing branches, won’t pull new ones


Cherry-pick specific commits and upload them
- be on the branch you want to push your commits, e.g. integration 
- find a hash number of specific commit (long hash number) 
$git cherry-pick <commit_hash>
$git push origin integration        // after choosing commits, upload to branch






























Resources
http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging
https://wiki.roving.com/display/EngOps/Git+at+CTCT
http://git-scm.com/book
http://git-scm.com/book/en/Git-Branching-Rebasing
http://zachholman.com/talk/more-git-and-github-secrets/?utm_source=buffer&utm_campaign=Buffer&utm_content=buffer24484&utm_medium=facebook
