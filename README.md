handy git commands:
---------------------------------------------------------------------

git clone 				 <=== to clone repo to local

git remote 				 <=== to check remotes

git branch  				 <=== to check current branch

git checkout -b name-of-the-branch       <=== to create new branch

git checkout name-of-the-branch	         <=== to switch between branches

git merge name-of-the-branch		 <=== to merge two branches current and name-of-the-branch
git merge --abort			         <=== to undo merge

git diff name-of-the-branch		 <=== to check difference between current and name-of-the-branch

git pull origin main		         <=== pulls updated code from remote to local repo 

git branch -d name-of-the-branch	 <=== deletes branch from local repo

git commit -am "message"		 <=== git commit and add at the same time onlt works for modified

git reset or git reset name-of-the-file  <=== undo add 

git reset HEAD~1 			 <=== undo commit, HEAD means last commit 
					      ~1 means go 1 commit before last commit

git log					 <=== see all commit logs

git reset hash-of-the-commit		 <=== resets to specific commit, hash you can find in logs
git reset --hard hash-of-the-commit      <=== resets and deletes from local file lines 


Do NOT use rebase on commits that you've already pushed on a remote repo
Insted, use it for cleaning up your local commit history before merging it into a shared team branch
git rebase name-of-the-branch		 <=== the process of moving or combining a sequence of commits to a new base commit
git rebase --abort		         <== to undo rebase



*Logic of using pull request when working in team:*
---
1. clone original repo
2. create new branch
3. add features, make changes, fix bugs
4. add commit and push
5. go to github and you will see "compare & pull request" tap
6. create pull request


Golden rules of committing
---
Only combine changes from same topic to single commit
It means don't use git add . and add all the changes from different topics to single commit

we can go further and use:
1. git add -p name-of-the-file <=== -p gives us option to choose what line of changes to commit in this file


You can use fork in github to make a complete copy of others repo


creating new repo
---
echo "# some-code" >> README.md

git init

git add README.md

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/AlisherAlseiit/some-code.git

git push -u origin main
