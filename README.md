# Git-helper-cmd
- [Git doc official](https://git-scm.com/docs)
- [Github doc official](https://docs.github.com/en)

## Git Config
``` git config --global user.name "John Doe"``` ***Git user Config***
 
``` git config --global user.email johndoe@example.com``` ***Git user Config***

```git config --list``` 

```git config --list --show-origin``` ***to see where that setting is defined (global, user, repo, etc...)***


## Git initiation & basics

```git init``` **Initialize Git**

```git add file-name.txt``` **Staged all files** (i.e. staged new files in git & to make ready to push in git repository)

```git status``` **View file status** (View current status of files)

```pwd``` **Present Work Directory**

```ls```  **Show all files in the directory**

```ls -a``` **Show all files <including hidden> in the directory**

```clear``` **Clear Terminal**

```rm dir name```  **Remove directory**
  
```rm -r dir name ``` **Remove recursively directory** 
  
```cd .. ```**Back 1 upper**

```git add --all``` **Added all files to stage**

```git commit -m "msg"``` **Commit message to changed files**

```git commit -am "msg" file1 name file2 name``` **Commit message to all file**

```git commit -am "all 2 Commit" ``` ***Example***

``git switch`` command to do the same since ``git checkout``
 
**Copy changes from one branch to another**
I have a branch named **BranchA** from **master**. I have **some changes in BranchA** ***(I am not going to merge changes from BranchA to master).***
Now I have created another branch from **master** named **BranchB**.
How can I copy the changes from **BranchA** to **BranchB**?

```
git checkout BranchB
git merge BranchA
```

**Instead of merge, as others suggested, you can rebase one branch onto another:**

```
git checkout BranchB
git rebase BranchA
```
 
This **takes BranchB and rebases it onto BranchA**, which effectively looks like BranchB was branched from BranchA, not master.
 
 ``Git pull origin branchName`` **Bring remote changes to local repo**
  
## Ignore files and folder git

[stackoverflow](https://stackoverflow.com/questions/12501324/how-to-use-gitignore-command-in-git)

Some files are **libraries/documentation** you don't want to delete but also don't want to push to github. Let say you have your project in folder your_project and a doc directory: **your_project/doc**

Create git ignore file first-- ``touch .gitignore``

this command to add lines in your gitignore file-- ``echo 'application/cache' >> .gitignore``

And you can exclude a folder by entering the below command in the .gitignore file ``/folderName``

- Remove it from the project directory (without actually deleting it): git rm ``--cached doc/*``
- If you don't already have a ``.gitignore`` , you can make one right inside of your project folder: ``project/.gitignore`` .
- Put ``doc/*`` in the ``.gitignore``
- Stage the file to commit: ``git add project/.gitignore``
- Commit: ``git commit -m "message"``.
- Push your change to github.

We can **unignore** certain files in a deeper structure or a specific subset (ie, you ignore ``*.log`` but want to still track ``important.log``) by specifying patterns beginning with ``!.`` eg: ``*.log !important.log``






























