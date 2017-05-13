# Cheat Sheet for Git

Remember to `git status`

# Remotes

A remote is a server that is outside your computer, and stores a copy of your
repository.

# Checkout

Use  git checkout to go from working back to the last commit.

# Class Notes

Centralized Version Control
	CVS, SVN
	One central server (each person checks out and merges changes to main server

Distributed Version Control
	GIT, Mercurial
	All Versions from all time

Goals of GIT

	designed to track linux kernel
	fast
		add to team and code base quickly
	distributed
		failed servers don’t stop music
	local
		few commands needed to talk to server
	corresponding hash
		Tracks changes
	Everyone has local copy of history

$ = command that should be typed

$ git config

	$ git config —global user.name “Your Name Here”
		tells git who you are
	$ git config — global user.email “youremail@goeshere.com”

$ git config — list
	list of commands

cd ~/
	go to home directory

mkdir my-first-repo
cd my-first-repo

	create working directory

git init
git status

	initialize repository with git

$ touch hello_world.txt

	create empty file

$ git add hello_world.txt

	add file to repo to be tracked

(this leads to staging “Hey git, I have some changes”)
	adding to queue to be pushed up
	telling git to track state of file

	put everything next to the car first, then decide how to pack the car (staging)

$ git commit -m “comment on change goes here”

	describe what you did
	collection about changes to the files

dif stat = statistics about differences created, lines changed, etc.

$ git log

	pulls comments associated with commits

$ git diff

	what are the differences?

	— old version
	++ new version

(git reset HEAD <file>) = empty the driveway, last saved checkpoint

$ git commit -a -m

	add all files

$ git checkout (hash number if wanted) filename.txt

	pull version log
	working to committed

$ git reset HEAD filename.txt

	unstage changes
	staged to working

$ git log -p

	adds comments WITH the differences
	hit q to remove

$ git revert

	goes from committed stage to last previous commit

git add

	include file

hashes are unique identifiers for commits in git

branching

master branch = default
accept that time moves forward

develop different code on same base
conduct experimental code without ffecting master branch
incorporate changes to master branch when ready

$ git checkout [ref] <file>

ref = hash or branch
specific file name

$ git branch [ref]

	create branch [name]

$ git checkout [ref]

$ cat

	shows file in terminal

$ git diff master

	shows branch differences

$ git diff exp — stat

	shows statistics how how many changes occurred in between two branches

$ git log —stat

	shows stats with comments

$ git stash

	move stuff off of the branch into a “mystery box”
	no longer belongs to one branch

$ git stash pop

	adds the stuff from the box to the branch you are on

$ git merge [ref branch name] - m

	easy merge (fast forward)
		fast forward, skips commit and breakpoint
		based on contents of files

	merge commit

	merge conflicts
		one branch has conflicting changes

		remove conflicts in command line text editor (VIM)
			shift:
			w
			q
		you can always abort

$ git log --graph --oneline

	get a visual

$ git remote add [ref url from github]
$ git push origin [branch ref]

url.patch [github]

wget it

git am

