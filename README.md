# Github Command Line Cheat Sheet

```
git fetch origin -p
git fetch origin --prune
git branch -D <branch-name>
```



1. ssh git clone

2. check to see you are on the correct branch (check often)
```bash
$ git branch -a
```

3. Create a new branch for your changes: You can create a new branch and switch to it using 
$ git checkout -b name_of_your_new_branch

4. check to see you are on the correct branch (check often)
```
$ git branch -a
```

5. Make your changes: Edit files, create new ones, and so on.

6. Check the status of your changes: This step is optional but recommended. 
$ git status 

7. "Stage" your changes for commit: 
$ git add . 

to add all changes,

6. Check the status of your changes: This step is optional but recommended. 
$ git status 

8. "Commit" your changes and add a descriptive message 
$ git commit -m "Your message"

9. Push the changes to the new branch on the remote repository: 
$ git push origin name_of_your_new_branch

10. Create a pull request: You can use the GitHub CLI to create a pull request with 
```
$ gh pr create
```
You'll be prompted for details like the pull request title and body, and which branch you want to merge your changes into.

# To compare branches (and make file of compare text)

1. compare to branch
- if you are on branch1
```bash
git diff branch2
```
or
```bash
git diff branch1 branch2
```
or
```bash
git diff branch1..branch2
```

1. save file
```bash
git diff branch1..branch2 > diff_output.txt
```

# To pull code from one branch to another:

1. update all repo files
```
$ git fetch origin
```

2. check to see you are on the correct branch (check often)
```
$ git branch
$ git status
```

3. move to branch you want to update (if not there already)
```
$ git checkout OUT_OF_DATE_BRANCH
```
4. pull with 'rebase'
```
$ git pull origin UPDATED_BRANCH --rebase
```
4. push
```
$ git push origin OUT_OF_DATE_BRANCH --force
```

1. remove or delete a branch:
```bash
$ git branch -D <branch-name>
```

# To pull code from one branch to another:

1. check to see you are on the correct branch (check often)
```
$ git branch -a
```

2. go to branch to want to put code into:
$ git checkout <branch_name>


3. Pull the latest code from the branch
This command will fetch the latest code from the specified branch and merge it into your currently checked out branch.
$ git pull origin <branch_name>


/////////////////////////////////////

# To Reset a broken branch to a good-target branch:
- in terms of old-branch (to be updated) new branch (current-code) 

## 1 Fetch the Latest Data from the Remote Repository:
# This updates information about all remote branches, 
# including 'new-branch'
$ git fetch origin 

## 2 Hard Reset the Old Branch to the State of the Remote New Branch:
# Ensure you are on the old branch
$ git checkout old-branch      

# Reset it to match the remote new branch
$ git reset --hard origin/new-branch  

## 3 Force-Push the Old Branch to the Remote Repository:
$ git push --force origin old-branch
$ git checkout old-branch
$ git rebase --continue






/////////////////////////

#### Note: 
As Github changes token and Multi Factor Authentication (MFA) options, you may need to configure your device, terminal, account settings, etc., in order to get the process working:

Github CLI resources: 
#### Setting your login
```
$ gh auth login
````
#### Docs

https://cli.github.com/manual/ 

https://docs.github.com/en/github/setting-up-and-managing-your-github-user-acc
ount/managing-email-preferences/setting-your-commit-email-address 


## Contents:
1. update in brief
2. submit to an existing branch (note: "master" is a branch too)
3. Make a new branch and submitting additions to that

# Update In Brief

1. Check where you are:
```$ git branch -a```

2. Check git status
```$ git status```

3. git add
```$ git add .```

4. Check git status
```$ git status```

5. Git commit
```$ git commit -m "message"```

6. push (update the branch)
```$ git push origin master```




# Steps to add / submit to a branch (no -b means not making a new branch):

2. clone the repo
a green button on the repo page should say "Download or clone"
clicking that button will give you the link 

```$ git clone URL_from_github```

e.g.

```git clone https://github.com/lineality/geoffrey_gordon_ashbrook.github.io.git```

or

```git clone https://github.com/lineality/Perceptron_Studies.git```


2. Go into the branch directory(folder) of the repo on your computer, open a terminal

3. Check to see what branch you are in and what branches there are
Note: It is good to do this very very often, especially if you have different terminals open.

```$ git branch -a```

4. To go into a specific existing branch, use "checkout"
Git checkout: active git in that branch

```$ git checkout name_of_branch_you_want```

5. Update your local copy of that branch

```$ git pull origin the_branch_name```

6. Add your new changes and updates (after pulling the recent updates) on your local computer.
	
7. check to see you are on the correct branch (check often)

```$ git branch -a```

8. git add!

```$ git add .```

9. Check git status

```$ git status```

10. Git commit!

```$ git commit -m "message"```

11. push (update the branch)

```$ git push origin name_of_your_new_branch```

(optional) 

sometime later make pull request to add that content to master

```$ git push origin master```














# Steps to make and submit a new branch (-b makes a new branch):

1. go into or make a directory(folder) on your computer 
where you want to save the github repo files
open a terminal in that folder/directory

2. clone the repo
a green button on the repo page should say "Download or clone"
clicking that button will give you the link 

```$ git clone URL_from_github```

e.g.

```git clone https://github.com/lineality/geoffrey_gordon_ashbrook.github.io.git```

or

```git clone https://github.com/lineality/Perceptron_Studies.git```


3. Go into the folder of the repo

```$ cd cloned_git_directory_name```

4. Make sure the files are all up to date

```$ git pull```

5. Create a branch (using "-b")

```$ git checkout -b name_of_your_new_branch```

6. check to see you are on the correct branch (check often)

```$ git branch -a```

7. add/change item to your new branch on your local computer

8. Check the status

```$ git status```

9. git add!

```$ git add .```

10. git commit!

```$ git commit -m "message"```

11. Push to master

```$ git push origin master```

12. Push to that branch

```$ git push origin name_of_your_new_branch```

13. create pull request:
```$ gh pr create```


optional

to re-name branch

```$ git branch -m oldname newname```

e.g.

```git branch -m beta_branch testing_branch```





# Steps to add / submit to a branch (no -b means not making a new branch):

1. Clone branch if not done already (see above)

2. Go into the branch directory(folder) of the repo on your computer, open a terminal

3. Check to see what branch you are in and what branches there are
Note: It is good to do this very very often, especially if you have different terminals open.

```$ git branch -a```

4. To go into a specific existing branch, use "checkout"
Git checkout: active git in that branch

```$ git checkout name_of_branch_you_want```

5. Update your local copy of that branch

```$ git pull origin the_branch_name```

6. Add your new changes and updates (after pulling the recent updates) on your local computer.
	
7. check to see you are on the correct branch (check often)

```$ git branch -a```

8. git add!

```$ git add .```

9. Check git status

```$ git status```

10. Git commit!

```$ git commit -m "message"```

11. push (update the branch)

```$ git push origin name_of_your_new_branch```

(optional) 

sometime later make pull request to add that content to master

```$ git push origin master```



# procedure to rebase a branch (in this case preprod):


Make sure you have a local checkout available of BOTH branches before rebasing to a branch that may only be remote.


1. Follow these steps on a test branch first:
```bash
git checkout -b test_branch_xxx
```


2.
```bash
git checkout branch_you_want_to_change
```


3.
```bash
git rebase target_brach_to_match_history_of
```


4. in vsCode, manually fix merge conflicts
which will be notated/annotated by the rebase process starting


5.
```bash
git add .
git rebase --continue
```


6. repeat steps 4,5 if needed


7. do unix-diff and git diff to check


8.
```bash
git push --force-with-lease origin branch_you_want_to_change
```

