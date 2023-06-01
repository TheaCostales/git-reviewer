# Basic Git Commands
#### The basic commands include initializing the Git repository, saving changes, checking logs, pushing the changes to the remote server, and merging. 
| **Git Command**          | **Description**                                                                                           |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| git init                 | initialize an existing directory as a Git repository.                                                     |
| git remote add origin    | add a git URL as an alias.                                                                                |
| git status               | show modified files in working directory, staged for your next commit.                                    |
| git add                  | add a file as it looks now to your next commit (stage).                                                   |
| git commit               | will create a snapshot of the changes and save it to the git directory.                                   |
| git commit -m            | commit your staged content as a new commit.                                                               |
| git branch               | list all of the branches in your repo. Add a branch argument to create a new branch with the name branch. |
| git branch [branch-name] | create a new branch at the current commit.                                                                |
| git push                 | transmit local branch commits to the remote repository branch.                                            |
| git pull                 | fetch and merge any commits from the tracking remote branch.                                              |
| git checkout             | switch to another branch and check it out into your working directory.                                    |

#### Complete Development with GitHub
![image10_1a4384e5fa.png](images%2Fimage10_1a4384e5fa.png)

# Creating a repository

1. Go to GitHub account
2. Click on the + button
3. Select a new repository 
4. Type repository name 
5. Add description (optional)
![github1.png](images%2Fgithub1.png)
6. Choose repository visibility 

    ![github2.png](images%2Fgithub2.png)
7. If you're importing an existing repository to GitHub, don't choose any of these options, as you may introduce a merge 
   conflict.
    ![github3.png](images%2Fgithub3.png)
8. Click Create Repository 

### Creating a Project 

1. Clone the remote repository to the local directory. Github provides a detailed guide on how to clone, add remote and initialize a Git project.
![github4.png](images%2Fgithub4.png)
2. Following the second set of steps since we will push an existing repository.
3. Go to PyCharm 
4. Create a New Project

*(Note: repository name from GitHub should be the same as the project name created on pycharm as your local directory.)*
![pycharm1.png](images%2Fpycharm1.png)

5. Once project is created, open Terminal View. You can do this by going to View > Tool Windows > Terminal.

6. Initialize a new Git repository in your project's root directory using the 'git init' command
```
git init

(venv) (base) mariatheresacostales@marias-air gianpogi % git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
Initialized empty Git repository in /Users/mariatheresacostales/PycharmProjects/gianpogi/.git/
(venv) (base) mariatheresacostales@marias-air gianpogi % 

```
7. Check the status by using the command 'git status'
```
git status

(venv) (base) mariatheresacostales@marias-air gianpogi % git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .idea/
        main.py

nothing added to commit but untracked files present (use "git add" to track)

```
It shows that we are on the main branch and we didn't commit anything yet.


8. Add remote repository to your local Git repository using the 'git remote add origin -your-repository-url' command. Replace your-repository-url with the URL as seen on the first step under creating a project.
```
git remote add origin your-repository-url

```
9. Stage all the project's files for commit using 'git add' command.
```
git add .

```

10. Commit all changes with a message using the following command:
```
git commit -m "first commit"

```
11. Add branch by using the following command:
```
git branch -M main

```
12. Push changes to the remote repository using the following command: 
```
git push --set-upstream origin main

```
*(Note: If this is the first time you've pushed to the repository, Git will prompt you to enter GitHub username and password.)*

That's it! Your project should now be pushed to your new repository on GitHub.
![github5.png](images%2Fgithub5.png)

## Creating Branches
1. Open the repository you want to create a new branch on GitHub
2. Click the drop-down arrow of the branch you wish to set as the source of your new branch
3. Type the name for you new branch
![github6.png](images%2Fgithub6.png)
4. Click create branch. Now, you have 2 branches.
5. Go to PyCharm and open the terminal window and pull the changes you made on GitHub
```
git pull

(venv) (base) mariatheresacostales@marias-air gianpogi % git pull
From https://github.com/TheaCostales/gianpogi
 * [new branch]      branched-off-from-from-main -> origin/branched-off-from-from-main
Already up to date.

```
It shows that we created a new branch in our GitHub repository.

6. We can now switch to the newly created branch by using the following command:
```
git checkout 'name-of-the-newly-created-branch'

(venv) (base) mariatheresacostales@marias-air gianpogi % git pull
From https://github.com/TheaCostales/gianpogi
 * [new branch]      branched-off-from-from-main -> origin/branched-off-from-from-main
Already up to date.

```
##### Now you can make changes to your new branch locally in PyCharm and commit and push those changes as usual using Git commands.

## How to update repository on your remote server

Someone made some changes on your Github repository. We want to update it in PyCharm to avoid future problems. 

1. On your terminal window, pull the changes you made on GitHub to your local Git repository using the following command:
```
git pull

```
2. PyCharm should now show your updated repository with the changes you made on GitHub.