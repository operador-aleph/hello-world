# hello-world

Hi!

Here is my summary of git terminal commands to:

- Clone a branch 
- Make commits 


## Creating or Accesing a **repository** 
* `git init`: create a new git repository of the working folder 
* `cd [your-repository-name]`: Navigate to the repository  
* `git clone [your-url]`: If the repository does not exist on your computer, make a clone 
* `cd [your-repository-name]`: Change directory 

## Create, Delete, Select and Push a  **brach** 
* `git branch`: Make sure you are working in the correct branch
* `git chekout -b [new-branch-name]`: Create a new branch
* `git checkout [branch-name]`:  Switch branch 
* `git branch -d feature_x`: delete a branch 
    * You can't delete your current working branch?
 * `git push origin [branch-name]` push the brach to make it available in remote 
 
## Add changes to the **index** and create **commits**
* `git add <filename>` or `git add *` : Add changes to the **Index**  
* `git commit -m "[your-commit-message]"`: Committed the files to the **HEAD**
    * Type 55 characters or *less*

## Update and Merge to github
* `git pull`: Update your loval repositoty to the newest commit
* `git push origin [branch-name]` push the changes of the **HEAD** to the **remote repository**
* `git diff <source_branch> <target_branch>`: Preview changes 
* `git merge [branch-name]`: merge another branch into your active branch
* `git add <filename>`: If automatic merge is not posible, change manually and then marked as merged with the command above 

## Replace local changes
* `git checkout -- <filename>`: replace local changes in your working tree (with the last content in **HEAD**), changes added to the **index** and new files, will kept.
* `git fetch origin` `git reset --hard origin/master`: If you instead want to drop all your local changes and commits, fetch the latest history from the server and point your local master branch 

## Log 
* `git log`: Check the repository history 
* `git log --author=bob`: see only the commits of a certain author
* `git log --pretty=oneline`:  To see a very compressed log where each commit is one line
* `git log --graph --oneline --decorate --all`: see an ASCII art tree of all the branches, decorated with the names of tags and branches: 
* `git log --name-status`: See only which files have changed
* `git log --help`: see possible parameters you can use to display the log 

## Tagging 
* `git tag [tag] [10-characters-of-the-commit-ID]`: Add software releases. 
    * You can get the commit id by looking at the log
    * e.g. git tag 1.0.0 1b2e1d63ff

## Hints 
* `gitk`: built-in git GUI
* `git config color.ui true`: use colorful git output
* `git config format.pretty oneline`: show log on just one line per commit 
* `git add -i`: use interactive adding
