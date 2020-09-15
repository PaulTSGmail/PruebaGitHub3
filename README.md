# gitPrueba3____Con colaboradores_

:pppp
Este es para probar la colaboracion.

lo saque de aqui (https://uoftcoders.github.io/studyGroup/lessons/git/collaboration/lesson/)

EXERCISE 1
TWO PERSON COLLABORATION VIA THE CLI - SHARED REPO WORKFLOW (WITHOUT BRANCHES)

This exercise is based on the SWC Git Novice lesson https://swcarpentry.github.io/git-novice/08-collab/

One of you will be the “Owner” and one of you will be the “Collaborator.”

A. OWNER GIVES COLLABORATOR ACCESS TO THEIR REPO.
Go to your GitHub repo
Add a file called “tenlines.txt” and put the text from the etherpad into the file. Commit your changes.
Click on Settings tab.
Click Collaborators
Enter collaborataors username
B. COLLABORATOR CLONES OWNER’S REPO
Go to https://github.com/notifications and accept access to Owner’s repo.
On the CLI, clone the owner’s repo but issuing the commmand:
$ git clone URL-of-Origin-Repo Directory-Address-of-Local-Repo
C. COLLABORATOR WORKS ON CLONE OF OWNER’S REPO
Go to your cloned repo:
$ cd ~/.../yourClone

Open editor and revise working file:
atom tenlines.txt

Commit your changes to your local repo:
$ git add tenlines.txt
$ git commit -m "your commit message"

Push your changes to the Owner’s repo on GitHub:
$ git push origin master

D. OWNER REVIEW AND ACCEPTS CHANGES FROM COLLABORATOR
Look at Owner’s GitHub repo and see new commit(s) from Collaborator.

Download (pull) Collaborators changes to Owner’s local repo:
$ git pull origin master

****************************************************

EXERCISE 2
DEALING WITH MERGE CONFLICTS
This section is based on the SWC Git Novice lesson https://swcarpentry.github.io/git-novice/09-conflict/

When two or more people work on the same files, conflicts are bound to occur. Version control will help notify us when there are conflicts. It will be up to the humans to sort out which changes to retain.

The file “tenlines.txt” currently looks like this:
$ cat tenlinestxt

Let’s say Person A adds a line to the file and review:
$ atom tenlines.txt
$ cat tenlines.txt

and pushes changes to GitHub:
$ git add tenlines.txt
$ git commit -m "added a line in local copy and pushed to remote"
$ git push origin master

Now, Person B modifies her local file without first updating it (pulling the repo) from GitHub:
Add a line to the file and review:
$ atom tenlines.txt
$ cat tenlines.txt

Commit the changes locally:
$ git add tenlines.txt
$ git commit -m "added a line in local copy"

But when we push, Git will not allow this because there were changes to the same line in the two files:
$ git push origin master

To resolve the conflict, you need to pull the changes from GitHub, merge them into your local copy, and then push it back to GitHub
$ git pull origin master

Git tells us there is a conflict and tells you the file it’s in.
Let’s look at the file:
cat tenlines.txt

Git has put some new info in our file:

<<<<<<<<<<<<< HEAD
our text
========
Other persons's text
>>>>>>>>

You need to open your text editor and make the changes which is the accepted version by you and your collaborator:
atom tenfiles.txt

Then, to finish mergining, you need to add, commit, and push your changes back to GitHub:
$ git add tenlines.txt

You can verify the status of your repo first, then commit and push:
$ git status
$ git commit -m "Merged changes from GitHub"
$ git push origin master

Git keeps track that a conflict has been resolved and what was merged into what so when Person A who made the first changes pulls from GitHub, she doesn’t have to fix things and merge again.

Person A pull and sees new version of the file:
$ git pull origina master
$ cat tenlines.txt
