#lets Analyse git in detail..

Git --> git is a tool that is used in project management basically a file tracking system 
        and basically it is a stuff that is used to track who has done what.

Github ---> A cloud platform where one can host a company code

# Concepts

git init --> Intialises an empty git repository.
    so basically when we run this command git starts to track our Project

Now for example we create a new file in our Project notes.txt

There are basically three states you should understand:

1. Untracked
You create a new file
        ↓
Git doesn't know about it

Example:

 notes.txt

2. Tracked + modified

Suppose notes.txt has already been committed.

You edit it:

notes.txt

Git now says:

modified: notes.txt

Git is tracking the file, but you've changed it since the last commit.

3. Staged

You then do:

git add notes.txt

Now Git says:

Changes to be committed:
    modified: notes.txt

Your change is now sitting in the staging area, waiting for a commit.


# git add ---> Add changes to the staging area ,just like we are on stage about to click a photo

# git commit -m "message" ----> Your photograph is been clicked and changes are saved now

# git stash --> is a Git command used to temporarily save uncommitted changes in your working directory so you can work on something else without committing those changes.

If you want to check whether you currently have anything stored in Git stash, the main command is:

# git stash list
If you have stashes

You'll see something like:

stash@{0}: WIP on main: abc1234 Initial commit
stash@{1}: WIP on feature-login: def5678 Login page

This means you have 2 stashes.

stash@{0} → most recent stash
stash@{1} → older stash

if we need to bring back a particular stash
git stash pop stash@{1}

This will:

Apply the changes from stash@{1}
Remove that stash from the stash list
If you want to bring it back but KEEP the stash

Use:

git stash apply stash@{1}

Difference:

git stash pop stash@{1}
       ↓
Apply + delete stash


git stash apply stash@{1}
       ↓
Apply + keep stash

# dealing with commit now

