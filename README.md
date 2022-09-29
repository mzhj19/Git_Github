
# Git Commands

### Some of the most useful & used  git commands are here.

## Check version: 
    
        git –version

## Help Commands:
    git help
    git help config

## Configuration Commands:
	git config --global setting value

    Global:  
        git config --global user.name "Zahid Hasan Jamil"
		git config --global user.email "mzhj19@gmail.com"
	Local:
        git config  user.name "Zahid Hasan Jamil"	// local means one folder or like this
		git config  user.email "zahid@usoz.com"
 
    Show configuration:
			git config –list
			git config –global --list
    Change configuration:
			git config –global user.name “new name” // same for others


## Initialize:
	git init

## Check status:  // staged or unstaged, tracked or untracked
	git status


## Working directory to stagging area:
	git add day1.txt // single file 
	git add .  // all files in directory but not subdirectories
	git add -A // A for all,  all of directory and subdirectories
	git add *.js // all files of .js extention ,not subdirectories
	git add **/*.js //  all of directory and subdirectories

## Unstaged from staged:
	git rm –cached day2.txt	// rm for remove

## Check difference of previous staged and current unstaged file:
	git diff

## Restore previous: 
	git restore day1.txt

## Commit: Moving staging to local repository
	git commit -m “Commit massage”
	********
	Stagging and commit at a same time directly:
		git commit -am “message”
		    Or 
        git add . && git commit -m “message”
	********

## Uncommit: Local repository to  staging area
	git reset --soft HEAD^	// local repository to staging area , HEAD means latest commit
	git reset HEAD^		    // local repository to working directory
	git reset –hard HEAD^	// reseting everything to previous commit
    git reset –soft HEAD-2	// HEAD~2   //  first 2 head commit

## Undo/discard: Staging area to working directory
	git checkout day2.txt
	git checkout 3edde3f // id of going to which commit, id’s after that the commits will be discard
	git checkout master // to recent commit
	git checkout -- file-name	// back out any changes to specified file to last commit


## Show the commit:
	git log	//details
	git log --oneline	// in one line
	git log –oneline –graph –decorate –color 
	git show 2e232da // id from online command


## .gitignore:
	.env	// .env 
	*.txt 	// all of .txt
	!story.txt	
	Folder_name/		// folder ignore

## Check remote connection:
	git remote -v	// shows the remote along with the url




## Connect with remote repository/  Local repository to remote repository connection:
	git remote add origin https://github.com/mzhj19/gitGithub.git

		/// origin =any name=the url,, like c++ define


## Clone git repository:
	git clone https://github.com/mzhj19/gitGithub.git 



## Push /local to remote repository:
	git push -u origin main




	**** solution of not pushing into remote repo ****

    git remote add origin https://github.com/mzhj19/XXXXXXXX.git
    git branch -M main
    git push -u origin main


    locar branch and remote branch must be same.Otherwise errors occure.
	If push into main not working ,push into master will be working.
    

	git pull origin main –allow-unrelated-histories
    git push origin main –force


    Run git push -u origin master instead of git push -u origin main
    	Or 
	if you want to name the branch main
    Run-
		git checkout -B main 
	before 
		git push -u origin main


	************




## Branch:
	git branch myBranch	// create branch
	git checkout myBranch	// move to myBranch branch
	git chechout master	// move to master branch
	git merge myBranch 	// merge with master
	git branch -d myBranch	// delete branch

## Show branch:
	git branch

## SSH Authentication Commands:
	
    cd ~    // for root  user directory , exmple: /c/Users/JAMIL
    cd .ssh	// if have .ssh
    mkdir .ssh	// if not have .ssh
    cd .ssh
    pwd
    ssh-keygen -t rsa -C "zahid@usoz.com"	// generate ssh key
    ls -list	// show the list
    mate id_rsa.pub	// open id_rsa.pub , windows user can use notepad id_rsa.pub
    ssh -T git@github.com	// connect github over ssh protocol.



	********* By default commands provided by github ********
		create a new repository on the command line
		echo "# LiveChat" >> README.md
		git init
	git add README.md
	git commit -m "first commit"
	git branch -M main
	git remote add origin https://github.com/mzhj19/LiveChat.git
	git push -u origin main
	or push an existing repository from the command line
	git remote add origin https://github.com/mzhj19/LiveChat.git
	git branch -M main
	git push -u origin main

	*****************************************************

# Some commands for file or directory
    	cd .. // previous folder
    	cd filename/ forderName  // specific file or forlder
    	pwd // present directory
    	mkdir // make directory/folder
    	touch day1.txt // make file
    	open day1.txt // open file
    	notepad filename.extention // file create if have not,otherwise open in notepad

    	ls // only visible file
    	ls -a // all files ,with hidden
	    	Version control possible from local repository ,Not from working
	    	Directory or stagging area
	
		Mkdir // make directory
		rm -rf test.txt	// remove/ delete a folder ////// rm =remove directory,rf=remove file

		Show the file system:
			ls
			ls -1 // one item per line
			ls -l // one per line details
	
		Go back directory:
			cd .. 		// one down
			cd ../.. 	// two down and so on ..
			cd ~		// root directory
	
		Go to target directory:
			cd /dir
			cd fileName

		Rename/move dirctory:
			mv test docker		// test tot docker

		Create file:
			touch fileName	// one file
			touch fil1 file2 file3	// multiple file

		Remove file:
			rm fileName	// one file
			rm file*	// file start with file like file1,file2,file3
		
		Remove directory:
			rm -r dir/	// here -r for recursively

		See documents of a file:
			cat filename

		Transfer file documents to another file:
			cat file1.txt > file2.txt	// document transfer to file2 from file1



    *****************************************************
 
## What should we do to work in a team?
	
    git checkout master			// move to master
    git pull				// pull from master
    git checkout -b newBranch		// create new branch
    git push origin newBranch		// push to new branch
    

6.9.22
