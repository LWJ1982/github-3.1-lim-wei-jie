# github-3.1-lim-wei-jie 😊
<!-- “Ctrl + Shift + V” (on Windows) or “Cmd + Shift + V” (on Mac), it will open the preview pane in a new window as oppose to side by side. -->

[Markdown help](https://www.inflectra.com/Support/KnowledgeBase/KB725.aspx)

**<ins>Git command</ins>**

history - display all the past code entered

1. Git status  //always check using Git status>

2. Git init  //Prep local folder for Git Repo, impt -> init once only

3. Git commit -am or -a -m "comment" //shortcut for git add + git commit

3a. 
Git add file1 file2   //add file for commit <br>
Or<br>
Git add .  //add all files for commit<br>
3b.<br>
Git commit -m "Message" //commit to repo<br>
  * &nbsp;&nbsp;&nbsp;&nbsp;Git commit //commit long text
Forgotten to add files
  * &nbsp;&nbsp;&nbsp;&nbsp;Git add forgotten file //add the missing file//
  * &nbsp;&nbsp;&nbsp;&nbsp;Git commit --amend //correction to previous commit

4. Git log //view commit logging
   * &nbsp;&nbsp;&nbsp;&nbsp;Git log --oneline // See comment; see one line comment

5. touch .gitignore //create file and input filenames for git to ignore, no tracking, no add during git add .

6. Git branch  //display all branch
  * &nbsp;&nbsp;&nbsp;&nbsp;Git branch <NewBranchName> //create a new branch
  * &nbsp;&nbsp;&nbsp;&nbsp;Git switch or Git checkout <NewBranchName> //switch to new branch
  * &nbsp;&nbsp;&nbsp;&nbsp;Git branch -m <Rename Branch> //Checkout or switch to branch and input new name
  * &nbsp;&nbsp;&nbsp;&nbsp;Git branch -D <branch to Del> //Del branch
  * &nbsp;&nbsp;&nbsp;&nbsp;Git branch -c //create a branch
  * &nbsp;&nbsp;&nbsp;&nbsp;git branch -r // view all remote branches

7. Git merge <branch to merge> // replace repo with branch to merge
  * &nbsp;&nbsp;&nbsp;&nbsp;Git commit -am "Merge conflict resolved" //after resolving Git merge conflict

8. Git diff //compare the difference between the 2 files (-file1, +file2) (staging Area and working directory)<br>
@@ -19,3 +19,14 @@ => (-)file1 line 19, 3 lines compare with (+)file2 line 19, 14 lines
  * &nbsp;&nbsp;&nbsp;&nbsp;Git diff head or Git diff head file1
  * &nbsp;&nbsp;&nbsp;&nbsp;Git diff --staged 
  * &nbsp;&nbsp;&nbsp;&nbsp;Git diff --cached
  * &nbsp;&nbsp;&nbsp;&nbsp;Git diff branch1..branch2 //compare 2 branches
  * &nbsp;&nbsp;&nbsp;&nbsp;Git diff commit1..commit2 //compare 2 commit

9. Go back previous commit 
  * &nbsp;&nbsp;&nbsp;&nbsp;Git checkout <log Hash> //goback and amend, git log --oneline
  * &nbsp;&nbsp;&nbsp;&nbsp;Git checkout HEAD~4 //go back 4 commit
  * &nbsp;&nbsp;&nbsp;&nbsp;Git checkout HEAD <FileName> or Git restore <FileName> //return to last commit, progress unsave
  * &nbsp;&nbsp;&nbsp;&nbsp;Git restore --staged <FileName.txt> //to remove a secret file after performing git add ., file will be untracked

10. Git reset <log Hash> //remove commit
  * &nbsp;&nbsp;&nbsp;&nbsp;Git reset --hard head~2 //remove commit + restore 2 commit prior

11. Git revert <log hash> //"Hide" or "delink" the head to the log hash point, create a new commit ignoring the "hidden" commit. The commit will still be present in Git log

12. git checkout 
  * &nbsp;&nbsp;&nbsp;&nbsp;git checkout origin/main // check the diff bet main repo and local commit, see the file for the difference

13. git switch <remote-branch-name> // git switch puppies, switch to remote branch both github and git local

**<ins>GitHub (http)</ins>**

Remote Branch<br>
⬇️Git Fetch ⬆️<br><br>
Remote Tracking Branch <br>
(Local Cache of remote branch's content)<br>
⬇️Git merge ⬆️git push<br>
Local Tracking Branch (Remote Repo Name,Origin)

1. Git Clone <url>  //Clone Git hub repo to local repo

2. Git remote  // check the current repo name
  * &nbsp;&nbsp;&nbsp;&nbsp;Git remote -v //check the path to push and fetch
  * &nbsp;&nbsp;&nbsp;&nbsp;Git remote rename <old> <new>  //rename
  * &nbsp;&nbsp;&nbsp;&nbsp;Git remote remove <name>  //remove git remote
  * &nbsp;&nbsp;&nbsp;&nbsp;Git remote add <name> <url>  //add name to github url and ready to push

3. git remote get-url --all origin // Check https or SSH clone

4. Git push <remote> <branch> // origin(Github) master(Local)
  * &nbsp;&nbsp;&nbsp;&nbsp;git push <remote> <local-branch>:<remote-branch> // origin(Github) cats(branch):master

5. Git Branch -r // View remote branch, local repository knows
  

6. git fetch <remote> <branch> // fetch a branch from a remote to local repo #not working dir
  * &nbsp;&nbsp;&nbsp;&nbsp;git fetch origin master // fetch latest from master on ori remote repo
  * &nbsp;&nbsp;&nbsp;&nbsp;git fetch origin // fetch all changes from the ori remote repo

7. git pull <remote> <branch> // fetch a branch from a remote to  working dir => git fetch + git merge
  * &nbsp;&nbsp;&nbsp;&nbsp;git pull origin movies // merge working dir with remote repo
