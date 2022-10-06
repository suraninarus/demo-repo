
1. git clone https://github.com/suraninarus/demo-repo.git


2. git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

3. a/ zsolt@galvatron:~/Desktop/GitHub/demo-repo$ touch index.html
   b/ zsolt@galvatron:~/Desktop/GitHub/demo-repo$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

no changes added to commit (use "git add" and/or "git commit -a")
zsolt@galvatron:~/Desktop/GitHub/demo-repo$ 

4. zsolt@galvatron:~/Desktop/GitHub/demo-repo$ git add index.html README.md 
zsolt@galvatron:~/Desktop/GitHub/demo-repo$ git add .     
zsolt@galvatron:~/Desktop/GitHub/demo-repo$ git commit -m "I have created an HTML file and changed the READ.mdto commands" -m "This is for the descrition box" 

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'zsolt@galvatron.(none)')
zsolt@galvatron:~/Desktop/GitHub/demo-repo$ 