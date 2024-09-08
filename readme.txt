I have craeted a Public repo 'github' in my github server; 

https://github.com/REWATSING/github.git

-----------------------------------------------------------------------
I have created a local directory 'github2'and created file 'readme.txt', which i have add, commit and push to remote branch origin/main from local main or we can create new branch after adding remote repo. use credentials, brwserlogin or code gernerated to login remote server;


-----------------------------------------------------------------------
<<<<<<< Updated upstream
<<<<<<< Updated upstream
Now i have edited this file on github itself and are going to pull into local and then push with the next update-2 commit.
----------------------------------------------------------------------------------------------------------------------------
=======
=======
>>>>>>> Stashed changes
I have made some changes in local file and then made changes on remote file on the same time on same file, so now i have to first review the changes and have to merge changes or dtash local commit to hold local changes. 

So i have to commit or stach the modification done on local file : 
(error: Your local changes to the following files would be overwritten by merge:
        readme.txt
Please commit your changes or stash them before you merge.)

git fetch is a command used to retrieve the latest changes from a remote repository without applying them to your local working copy. This allows you to see what updates have been made to the remote repository without merging those changes into your code.


git fetch

git log origin/main

When You Merge Without Committing:

If you run git merge origin/main while having uncommitted changes, Git will attempt to merge the changes from the remote branch (origin/main) with your local branch.
Git will stop you if there's a conflict between your uncommitted changes and the incoming changes from the remote. In that case, you must either commit, stash, or discard your local changes before proceeding with the merge.
If you force the merge, it could potentially overwrite uncommitted changes and discard them, leading to data loss.
-----------------------------------------------------------------------------------------------------------
1. Fast-Forward
A fast-forward happens when your local branch has no new commits and is behind the remote branch. In this case, Git simply moves the pointer of your local branch to the latest commit on the remote branch. There’s no need for a merge commit.

It doesn't remove the stash changes list; 
When to Use:
No local commits on your branch since the last pull.
You want a linear history, with no extra merge commits.
-----------------------------------------------------------------------------------------------------------
lets stach then pop later after merge remote file;
 git stash
 git stash list 
 git merge origin/main
 git stash pop

---------------------------------------------------------------------------------------------------------
stash@{0}: WIP on main: 2b93212 Update readme.txt
stash@{1}: WIP on main: ec15a18 commit for update-1 for a demo file
stash@{2}: WIP on main: ec15a18 commit for update-1 for a demo file
------------------------------------------------------------------------------------------------------------
git checkout staging
PS C:\Users\Lenovo\Desktop\github2> git push -u origin staging
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'staging' on GitHub by visiting:
remote:      https://github.com/REWATSING/github/pull/new/staging
remote:
To https://github.com/REWATSING/github.git
 * [new branch]      staging -> staging
branch 'staging' set up to track 'origin/staging'.