### Getting Started
Create an account on https://github.com/.  [Send me an email](mailto:archon68@gmail.com) with your username, so I can add you as a collaborator on our GitHub repository.

Our repository is located at:  https://github.com/benrbray/AdamBots-FIRST-2013-Robot-Code

### Terminology

* _Repository_:  Where your project (including all files across all branches) is stored.
* _Commit_:  Saves the changes you have made to the files in the repository since the last time you committed.  Remember that commits are local until you push them to the repository.  When you commit, you are essentially “staging” the changes you make to be later pushed to the remote branches of the repository for other users to see publicly.
* _Branch_:  By creating a new Branch, you make a new copy of the repository in its current state, allowing you to develop and modify features without changing other branches/versions.  When a branch is completed or when it reaches a desired checkpoint, it can be merged with other branches.
* _Push_:  Saves local commits to the remote repository.  
* _Pull_:  Retrieve the most recent versions of the files in the repository and merge .  Branches that you pull will be merged into the current local branch, so make sure that you only pull from the remote branch that corresponds to the branch you are currently working in.
* _Fetch_:  Retrieve the most recent version of the files in remote branches without merging them into your local branches.  You can do a git fetch at any time to update your local copy of a remote branch. This operation never changes any of your own branches and is safe to do without changing your working copy. 
* _Checkout Revision_:  Copies a remote branch to your local repository (or switches to a different local branch).  

### Cloning the Robot Code Repository in NetBeans
In NetBeans, navigate to Team > Clone (or Team > Git > Clone).  Copy and paste the Repository URL (found on the GitHub page) into the text field that appears.  Enter your login information and click Next.

On the next screen, you will see a list of “Remote Branches”.  Select all of the branches and hit Next.

Enter the local directory in which you want to store local copies of the repository.  Keep the clone name the same, and use the settings below.

Click “Finish”, and NetBeans should prompt you to open any projects found in the repository.

### Configuring Your NetBeans Workspace
The Git Repository Browser in NetBeans will make working with Git much easier.  To show the Repository Browser, navigate to Team > Git > Repository Browser.

### Creating a New Branch
When you’re developing a new feature for the robot, create a new branch.  You should not work directly out of the master branch.  To create a new branch, right click on a remote branch in the repository browser and choose “Checkout Revision”.  The current working branch will appear in bold in the repository browser.

### Committing Changes
Before pushing modified code to a remote branch, you must first locally commit the changes you have made.  To commit your changes, right click on your NetBeans project or a file in your project and select Git > Commit.  

Before committing, be sure to enter a commit message.

### Pushing
When you want to update the remote repository with changes you have made locally, you must Push your changes.  You can only push after you’ve Committed or Merged Branches.  To push, right click on your project and select Git > Remote > Push.  Ensure that the Git repository URL is correct and hit Next.  Select the local branches you’d like to push to the remote repository and hit Next.  Hit Finish again.  

### Merging Branches
When you’re done working on a particular feature in a branch other than “master”, you should merge your changes with the master branch.  To do this, right click on the master branch in the repository browser and select Checkout Revision.  Click Checkout, then right click on the branch you’d like to merge with the master branch and select Merge Revision.  Click through the prompts and then Push to make your changes public.