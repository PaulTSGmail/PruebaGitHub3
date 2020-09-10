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
