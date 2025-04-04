# Git Exercise Solutions

## Bundle 1

### Exercise 1
```bash
bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon
$ git init
Initialized empty Git repository in C:/Users/bobsh/Desktop/Studies/amalitech-training/git-learning/moon/.git/

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (master)
$ echo "Hello world!" >> file1.txt

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (master)
$ echo "It's me" >> file2.txt

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (master)
$ git branch -M main

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (main)
$ git add .
warning: in the working copy of 'file1.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'file2.txt', LF will be replaced by CRLF the next time Git touches it

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (main)
$ git commit -m 'Initialised git and added two text files'
[main (root-commit) f1907e2] Initialised git and added two text files
 2 files changed, 2 insertions(+)
 create mode 100644 file1.txt
 create mode 100644 file2.txt

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (main)
$ git remote add origin https://github.com/Bob-Karemera-Shema/git-playground.git

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 294 bytes | 58.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Bob-Karemera-Shema/git-playground.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (main)
$ git checkout -b dev
Switched to a new branch 'dev'

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git checkout -b test
Switched to a new branch 'test'

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (test)
$ git checkout dev
Switched to branch 'dev'

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Bob-Karemera-Shema/git-playground/pull/new/dev
remote:
To https://github.com/Bob-Karemera-Shema/git-playground.git
 * [new branch]      dev -> dev

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git checkout test
Switched to branch 'test'

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Bob-Karemera-Shema/git-playground/pull/new/test
remote:
To https://github.com/Bob-Karemera-Shema/git-playground.git
 * [new branch]      test -> test

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (test)
$ git checkout dev
Switched to branch 'dev'

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git branch -D test
Deleted branch test (was f1907e2).

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git push origin --delete test
To https://github.com/Bob-Karemera-Shema/git-playground.git
 - [deleted]         test
```

### Exercise 2
```bash
bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ touch home.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git add home.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html


bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash
Saved working directory and index state WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash list
stash@{0}: WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ touch about.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git add about.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash
Saved working directory and index state WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ touch team.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git add team.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash
Saved working directory and index state WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash list
stash@{0}: WIP on dev: f1907e2 Initialised git and added two text files
stash@{1}: WIP on dev: f1907e2 Initialised git and added two text files
stash@{2}: WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ ^C

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (5118324c951615a6f8785c69dabf694d6e130861)

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash list
stash@{0}: WIP on dev: f1907e2 Initialised git and added two text files
stash@{1}: WIP on dev: f1907e2 Initialised git and added two text files

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (a1351955105c21a94334c139fea2341a1f63190a)

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git add .

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git commit -m 'added stashed changes'
[dev b93eaee] added stashed changes
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git push -u origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 571 bytes | 285.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Bob-Karemera-Shema/git-playground.git
   f1907e2..b93eaee  dev -> dev
branch 'dev' set up to track 'origin/dev'.

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (c6d14e6478900574634d9080b9ca61dbcc375c79)

bobsh@LAPTOP-LCN44KK0 MINGW64 ~/Desktop/Studies/amalitech-training/git-learning/moon (dev)
$ git reset --hard
HEAD is now at b93eaee added stashed changes
```