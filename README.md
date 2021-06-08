# Working with Git on VS Code
This project documents how to work with Git on VS Code.

## Table of Contents
1. [Setup a Git repository in VS Code](#setup-a-git-repository-in-vs-code)  
2. [How to use Git on VS Code](#how-to-use-git-on-vs-code)
    - [Commit and Push Changes](#commit-and-push-changes)  
    - [Pull Changes](#pull-changes)  
    - [Timeline View or Git History](#timeline-view-or-git-history)  
    - [Branches](#branches)  
3. [Useful Resources](#useful-resources)  
4. [Author's Note](#authors-note)  

## Setup a Git repository in VS Code
1.  Check that `.git` is auto-created in the project folder by VS Code (view in File Explorer).  
If `.git` is not found, you can initialize Git for the project in 2 ways:  
    - To get VS Code to automatically initialize Git in all projects, enable Git in VS Code settings. For VS Code 2019 and above, this should already be done (unless the user changed it).  
    To enable Git in VS Code: Go to File > Preferences > Settings. Type "Git: Enabled" in the search bar. Make sure that the box is ticked.  
    - If you don't want to automatically initialize Git in all projects, and only for one project, do the following:  
        - Type in terminal (within the project folder) `git --version` to check if Git is installed.  
If there is an output `git version ...`, it's already installed. If not, [download Git](https://git-scm.com/downloads/).  
        - Next, update Git config with name and email (skip if already done) by typing in the Terminal: 
            ```
            git config --global user.name "Your Name"
            git config --global user.email "Your Email"
            ``` 
        
        - To initialize the Git repository, go to the Source Control tab (`Ctrl+Shift+G`) and click `Initialize Repository` or type `git init {project-name}` in the Terminal.
2. With this Git repository, you can use the Git features on VS Code (such as branching, commiting changes). On VS Code, this is called Version/Source Control.

## How to use Git on VS Code
To see details of your current repository changes, select the Source Control icon in the Activity Bar on the left or press `Ctrl+Shift+G`.  

### Commit and Push Changes
1. After saving the file, stage changes by hovering over the file in the panel and click the `+` symbol 
    - It is possible to skip this step and commit unstaged changes, but VS Code will show a warning popup.
2. To commit changes, click the tick symbol at the top of the panel or press `Ctrl+Enter`.  
3. To push local changes to remote repository (on GitHub), type `git push` in the Terminal (in your project folder).

To undo your last commit, use the command `Git: Undo Last Commit` in the Command Palette (`Ctrl+Shift+P`)  
or click the 3 dot menu > Commit > Undo Last Commit.  

### Pull Changes
1. To pull changes from remote (on GitHub server) and update the local repository, go to the Source Control tab > three dot menu > Pull.  
Alternatively, type `git pull` in the Terminal (in your project folder).

### Timeline View or Git History
To visualise Git History (seeing the details of each commit and history of a file), there are 2 methods:  
- Go to the File Explorer in VS Code (select the Explorer icon in the Activity Bar on the left or press `Ctrl+Shift+E`).  
At the bottom of the panel, click the Timeline tab.  
- use the [Git History Extension](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory) from Don Jayamanne 

### Branches
To create branches, these are 2 methods:  
- In the Command Palette (`Ctrl+Shift+P`), use the command `Git: Create Branch`  
- Click the 3 dot menu > Branch > Create New Branch 

## Useful Resources
- [Video Tutorial by VS Code](https://code.visualstudio.com/docs/introvideos/versioncontrol)
- [Documentation by VS Code](https://code.visualstudio.com/docs/editor/versioncontrol)
- [Video Tuturial by Ihatetomatoes](https://www.youtube.com/watch?v=F2DBSH2VoHQ&ab_channel=Ihatetomatoes)

## Author's Note
This content was initially contributed by me ([mandychew](https://github.com/mandychew)) to [chewern/react-vscode-git](https://github.com/chewern/react-vscode-git).
