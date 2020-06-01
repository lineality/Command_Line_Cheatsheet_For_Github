# Github Command Line Cheat Sheet

## Contents:
1. Make a new branch and submitting additions to that
2. submit to an existing branch (note: "master" is a branch too)


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

6. add/change item to your new branch on your local computer

7. Check the status

```$ git status```

8. git add!

```$ git add .```

9. git commit!

```$ git commit -m "message"```

10. Push to master

```$ git push origin master```

11. Push to that branch

```$ git push origin name_of_your_new_branch```

optional

to re-name branch

```$ git branch -m oldname newname```

e.g.

```git branch -m beta_branch testing_branch```





# Steps to add / submit to a branch (no -b means not a new one made):

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



