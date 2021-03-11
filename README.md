# comp20-midterm

## Group One - Abe, Gun, Sally, Jason
https://abepark26.github.io/comp20-midterm/

## MealPrep Package selling website
We are creating a business website that sells meal prep packages. 

## Seven pages
1. Home Page: Abe (in progress)
2. About Page: Gun (in progress)
3. Product Page-Vegan: 
4. Product Page-Protein: Jason (in progress)
5. Product Page-Low carb
6. Event(promotion) Page: Sally (in progress)
7. FAQs Page

## Example website
https://www.rankingdak.com/ \
https://www.kurly.com/shop/main/index.php \
https://www.prepmymeal.de/?lang=en \
https://www.myprotein.com/

## Initial setup
The working steps are: 
1. clone the remote (online) repository to your local computer
2. work and test/debug your codes locally
3. push what you have done locally to the remote repository to share your codes with other team members.

Git provides codes for each step: 
1. In terminal, move (cd) to the directory where you want to save the repository. Then, type: 
```
git clone https://github.com/abepark26/comp20-midterm.git
```
2. Before you start the work for the day, you want to update your local repository from the remote repository because other team members might have made some changes. To pull new updates/changes from the remote repository, go to the root directory (i.e. Desktop/github/comp20-midterm), and type: 
```
git pull origin master
```
3. When you are done with your work locally, you want to update the remote repository with new codes. To update the remote repository, go to the root directory and type: 
```
git push -u origin master
```
"origin" is a shorthand name for the remote repository that a project was originally cloned from. \
"master" is the name of the default branch.

## Start a local server
To run and test out jquery functions on the local machine, 
you need to host a local server. \
First on the terminal, cd into the root directory of the repository, and type in the python command: 
```
python -m http.server 8000
```
Then on web, go the url: 
```
http://localhost:8000/
```
which will show the content in our index.html.

## How to work with git branch
To avoid merge conflicts, you want to make your own working branch, test your codes, and merge into master branch when there is no error within your branch.

This is how I work with git branch using MAC OS terminal and surely there will be more efficient ways of doing things by using bitbucket or other git hosting service programs.

The git code to make branch locally is:
```
git checkout -b [branch-name]
```
i.e. git checkout -b team-1
Here, team-1 is the name of the new branch. Everyone will have an issue assigned. One common naming convetion for your working branch is to name after the assigned issue. *Each issue will focus on only ONE feature at a time.

Now in terminal, type: 
```
git branch
```
to check the saved branches in your local computer. If you have checked out a new branch, you will have 'master' and i.e. 'team-1'. Branch in color or the one with a star before the name is the branch you are currently working in locally.
```
Please checkout into your working branch before begin your work and not work on the master branch.
```

Before beginning your work of the day, you want to update your local branches with changes made in the remote repository. The merging steps are:  
1. update your local master branch
2. merge your local master branch and your working branch

To update your local master branch, cd to the root directory and type:
```
git checkout master

git pull origin master
```
After you are sure that the local master branch is up to date with the remote master branch, merge your local working branch with the local master branch. In terminal, type: 
```
git checkout [branch_name]

git merge master
```
If there are merge conflicts, you want to resolve them first, or you won't be able to merge the branches. Normally, terminal or editor program (I'm using VSCode) tells you where the conflicts are.

After you are done with your codes, you want to commit changes from the local working branch to the remote working branch. To do that, type: 
```
git branch (to make sure you have worked in your working branch and not on the master branch)

git status (displays what files are changed)

git add . (to update all the files that you changed locally)
or
git add [file_name] (to specify which files to update)

git commit -m "[brief comment about what changes you made]"

git push -u origin [branch_name]
```

At the end of the day, you want to update the master branch with changes you made in your working branch. To open a pull request, go to our online github repository and open a pull request that compares from your working branch to the master branch. *Make sure to select your working branch before opening a pull request.

Please refer to https://guides.github.com/activities/hello-world/ or other stackoverflow posts if you have any questions. 
