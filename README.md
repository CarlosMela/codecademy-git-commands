This page contains all commands included in [Codecademy free Git course](https://www.codecademy.com/learn/learn-git "https://www.codecademy.com/learn/learn-git"). If any of these git commands doesn't sound to you please go and do it.

# 1. BASIC GIT WORKFLOW

**git init**

Creates a new Git repository.

**git status**

Inspects the contents of the working directory and staging area.

**git add file1.txt file2.txt**

Adds files from the working directory to the staging area.

**git diff file.txt**

Shows the difference between the working directory and the staging area.
> Enter q to finish

**git commit -m "My message"**

Permanently stores file changes from the staging area in the repository.

**git log**

Shows a list of all previous commits.

# 2. GIT BACKTRACKING

**git show HEAD**

Shows the log message and textual diff for that commit.
>HEAD is the current/latest commit

**git checkout HEAD file.txt**

Unstages file changes in the staging area.

**git reset HEAD file.txt**

Discards changes in the working directory.

**git reset 5d69206**

Can be used to reset to a previous commit in your commit history.
>5d69206 are the first 7 characters of the commit_SHA

# 3. GIT BRANCHING

**git branch**

Show repository branches.
>asterisk * is showing you what branch you’re on

**git branch myNewTask**

Create new branch.

**git checkout myNewTask**

Switch current branch to my-new-task.

**git merge branchToMergeIntoCurrent**

Include all changes made in branch-to-merge-into-current in the current (checkouted) branch.
>if there is a merge conflict resolve the differences and remove git markings. Add to index (staging area). Then commit.

```
 <<<<<<< HEAD
 =======
 >>>>>>> branch-to-merge-into-current
```

**git branch -d branchName**

Will delete the specified branch from your Git project.

# 4. GIT TEAMWORK

**git clone remoteLocation cloneName**

Copy a remote repository in your local workspace.

**git remote -v**

List of remotes.
>By default 'origin' is the remote the repository was cloned from

**git fetch**

Brings changes from the remote repository (origin) to our copy of the remote repository.
>This will update our local copy of the remote branches origin/master,...

**git merge origin/master**

Updates the current local branch with the changes fetched from remote (merges origin/master into your local branch).

**git push origin branchToBeSendToOrigin**

Push your local branch up to the remote, origin. In the remote repo the branch can be merged to master.

### WORKFLOW:
 1. Fetch and merge changes from the remote
 2. Create a branch to work on a new project feature
 3. Develop the feature on your branch and commit your work
 4. Fetch and merge from the remote again (in case new commits were made while you were working)
 5. Push your branch up to the remote for review

>Steps 1 and 4 are a safeguard against merge conflicts. Step 5 involves git push.
