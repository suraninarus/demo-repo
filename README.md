Időpont: 
Probléma: AZ ssh-add -K ~/.ssh/id_rsa paranc egy enter PIN-t dobott ki. Milyen ponre gondolhat, a videoban nem volt róla szó. 


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

5. zsolt@galvatron:~/Desktop/GitHub/demo-repo$ ssh-keygen -t rsa -b 4096 -C "suraninarus@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/zsolt/.ssh/id_rsa): gitHubKey
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in gitHubKey
Your public key has been saved in gitHubKey.pub
The key fingerprint is:
SHA256:t5wBJVwjMCtFIrwrZrJYJ4XnE7h2j4Lbj36wbYAxssU suraninarus@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
| .. ..=oo.+      |
|  .. o o.+ .     |
| . +. . .        |
|+ E +.   .       |
|.* * .  S o      |
|=oO =    o +     |
|=* O +    +      |
|+.o.= .          |
|.o+=.            |
+----[SHA256]-----+
zsolt@galvatron:~/Desktop/GitHub/demo-repo$ 

6. zsolt@galvatron:~/Desktop/GitHub/demo-repo$  git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.08 KiB | 554.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To https://github.com/suraninarus/demo-repo.git
   afd153a..8898f8b  main -> main


7. To copy private key: 
