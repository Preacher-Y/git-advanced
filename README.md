# **_GIT-ADVANCED EXERCISES_**

## **EXERCiSE 1**:

## _Getting Started_ 

```bash
PREACHER@Preacher MINGW64 ~
$ cd E:\The Gym
bash: cd: too many arguments

PREACHER@Preacher MINGW64 ~
$ cd 'E:\The Gym'

PREACHER@Preacher MINGW64 /e/The Gym
$ git clone https://github.com/Preacher-Y/git-advanced.git
Cloning into 'git-advanced'...
warning: You appear to have cloned an empty repository.

PREACHER@Preacher MINGW64 /e/The Gym
$ cd git-advanced

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ touch test{1..4}.md
git add test1.md && git commit -m "chore: Create initial file"
git add test2.md && git commit -m "chore: Create another file"
git add test3.md && git commit -m "chore: Create third and fourth files"
[main (root-commit) 3983942] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
[main facf88e] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
[main edb7ebc] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
```

## _Missing File Fix_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit edb7ebc7af916715fa242e71ef15821668bc2128 (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit facf88ee1e0d1fd11f71cb4c150b63df314787f8
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:57 2025 +0200

    chore: Create another file

commit 3983942aa3c09f70d2d002510e7994707f5ecd0c
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git add test4.md

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit 973cde6050df1428b5ccde145b4460d7d6208250 (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:23:33 2025 +0200

    chore: Create third and fourth files

commit eb81f6bb69e567d839936111a4cd8cacf05ad1d5
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit b308da46a8e6d55edac6cacc2ff823e63d46e9c9
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:57 2025 +0200

    chore: Create another file

commit 3983942aa3c09f70d2d002510e7994707f5ecd0c
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file
```

## _Editing commit message_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit 973cde6050df1428b5ccde145b4460d7d6208250 (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:23:33 2025 +0200

    chore: Create third and fourth files

commit eb81f6bb69e567d839936111a4cd8cacf05ad1d5
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit b308da46a8e6d55edac6cacc2ff823e63d46e9c9
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:57 2025 +0200

    chore: Create second file

commit 3983942aa3c09f70d2d002510e7994707f5ecd0c
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file

```

## _combining Two commit into one_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

[detached HEAD c55b4ba] chore: Create initial file
 Date: Mon Mar 3 10:14:55 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit 2798da81fdc4f24973f47900677e3675ff7329ca (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:23:33 2025 +0200

    chore: Create third and fourth files

commit 2747a1409ebcbc4776abd1df5da205777be3b4f5
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit c55b4bacdc671fc21c0c8e011b08a5507ffba922
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file
```

##  _Splitting a commits_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit 2798da81fdc4f24973f47900677e3675ff7329ca (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:23:33 2025 +0200

    chore: Create fourth file

commit 2747a1409ebcbc4776abd1df5da205777be3b4f5
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third file

commit c55b4bacdc671fc21c0c8e011b08a5507ffba922
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file
```

## _Advanced Squashing_
```bash
``bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

[detached HEAD c55b4ba] chore: Create third and fourth files
 Date: Mon Mar 3 10:14:58 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit d19badc76e43a783566cc837e21382bbcb345264 (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit c55b4bacdc671fc21c0c8e011b08a5507ffba922
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file
```

##  _Dropping a Commit_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ touch unwanted.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        unwanted.txt

nothing added to commit but untracked files present (use "git add" to track)

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git add .

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git commit -m "Unwanted commit"
[main 60324fa] Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git rebase -i --root

Successfully rebased and updated refs/heads/main.
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log
commit d19badc76e43a783566cc837e21382bbcb345264 (HEAD -> main)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:58 2025 +0200

    chore: Create third and fourth files

commit c55b4bacdc671fc21c0c8e011b08a5507ffba922
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 10:14:55 2025 +0200

    chore: Create initial file

```

## _Re-ordering Commit_

Mine are already in  so i didn't do anything but i learnt through the video how to do it

## _Cherry-Picking Commits_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git switch "ft/branch"
fatal: invalid reference: ft/branch

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git switch -C "ft/branch"
Switched to a new branch 'ft/branch'

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ touch test5.md

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ git status
On branch ft/branch
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test5.md

nothing added to commit but untracked files present (use "git add" to track)

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ git add .

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch 4e7fa07] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ git log
commit 4e7fa07b12342a23378e7f2036e40bc31d2d66a8 (HEAD -> ft/branch)
Author: Preacher-Y <ysheja@gmail.com>
Date:   Mon Mar 3 13:20:04 2025 +0200

    Implemented test 5

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/branch)
$ git log --oneline
4e7fa07 (HEAD -> ft/branch) Implemented test 5

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git cherry-pick 4e7fa07
[main adee061] Implemented test 5
 Date: Mon Mar 3 13:20:04 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
```

## _Visualizing commit history_

``` bash

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log --graph
* commit adee061e34ca94698884b467271c787ba57c1be0 (HEAD -> main)
| Author: Preacher-Y <ysheja@gmail.com>
| Date:   Mon Mar 3 13:20:04 2025 +0200
|
|     Implemented test 5
|
* commit d19badc76e43a783566cc837e21382bbcb345264
  Author: Preacher-Y <ysheja@gmail.com>
  Date:   Mon Mar 3 10:14:58 2025 +0200

      chore: Create third and fourth files
```

## _Understanding Reflogs_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git reflog
adee061 (HEAD -> main) HEAD@{0}: cherry-pick: Implemented test 5
d19badc HEAD@{1}: checkout: moving from ft/branch to main
4e7fa07 (ft/branch) HEAD@{2}: commit: Implemented test 5
d19badc HEAD@{3}: checkout: moving from main to ft/branch
d19badc HEAD@{4}: rebase (finish): returning to refs/heads/main
d19badc HEAD@{5}: rebase: fast-forward
b01c39d HEAD@{6}: rebase (start): checkout b01c39d402ebee3e78a88a79785cf91b50ad9
e3f
d19badc HEAD@{7}: rebase (finish): returning to refs/heads/main
d19badc HEAD@{8}: rebase: fast-forward
a000c93 HEAD@{9}: rebase (start): checkout a000c93511f759baae4e3111bcd778d761b27
f0c
```

## **Exerices 2**:

## _Feture Branch Creation_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git switch -C ft/new-feature
Switched to a new branch 'ft/new-feature'
```

## _Working on the Feature Branch_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ touch feature.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ echo "adding new content onthe feature file" > feature.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ cat feature.txt
adding new content onthe feature file

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ git status
On branch ft/new-feature
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        feature.txt

nothing added to commit but untracked files present (use "git add" to track)

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ git add .
warning: in the working copy of 'feature.txt', LF will be replaced by CRLF the n
ext time Git touches it

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ git status
On branch ft/new-feature
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   feature.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ git commit -m "Implemented core functionality for new feature"
[ft/new-feature 89e3a0c] Implemented core functionality for new feature
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt

```

## _Switching Back and Making More Changes_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-feature)
$ git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 2 and 1 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ touch readme.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ echo "Holla, I'm Yves and i am doing introductions" > readme.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ cat readme.txt
Holla, I'm Yves and i am doing introductions

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git add readme.txt
warning: in the working copy of 'readme.txt', LF will be replaced by CRLF the ne
xt time Git touches it

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 1 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   readme.txt


PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git commit -m "Updated project readme"
[main 679c24f] Updated project readme
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt

```

## _Local vd Remote Branches_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git push origin ft/new-feature
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 7 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (9/9), 828 bytes | 207.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'ft/new-feature' on GitHub by visiting:
remote:      https://github.com/Preacher-Y/git-advanced/pull/new/ft/new-feature
remote:
To https://github.com/Preacher-Y/git-advanced.git
 * [new branch]      ft/new-feature -> ft/new-feature

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch -r
  origin/ft/new-feature
  origin/main

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git pull origin main
From https://github.com/Preacher-Y/git-advanced
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories

```

## _Branch Deletion_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git merge -m "merging ft/new-feature => main " ft/new-feature
Merge made by the 'ort' strategy.
 feature.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch -D ft/new-feature
Deleted branch ft/new-feature (was 89e3a0c).

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch
  ft/branch
* main

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git remote prune origin
Pruning origin
URL: https://github.com/Preacher-Y/git-advanced.git
 * [pruned] origin/ft/new-feature

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch -r
  origin/main

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git pull
Already up to date.

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git push origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 7 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 881 bytes | 440.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/Preacher-Y/git-advanced.git
   c359cfe..5e5fcee  main -> main

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git pull
Already up to date.
```

## _Creating a Branch from a Commit_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git log --oneline
5e5fcee (HEAD -> main, origin/main) Merge branch 'main' of https://github.com/Preache
r-Y/git-advanced "the merge successfull"
ec0a805 merging ft/new-feature => main
679c24f Updated project readme
89e3a0c Implemented core functionality for new feature
c359cfe Create README.md
adee061 Implemented test 5
d19badc chore: Create third and fourth files

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git checkout -b ft/new-branch-from-commit 679c24f
Switched to a new branch 'ft/new-branch-from-commit'

```

## _Branch Merging_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-branch-from-commit)
$ touch from-commit.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-branch-from-commit)
$ echo "I love messing around, and as you know the more you mess around the more you found out '-)" > from-commit.txt

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-branch-from-commit)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git merge -m "merging ft/new-branch-from-commit => main " ft/new-branch-from-commit
Merge made by the 'ort' strategy.
 from-commit.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 from-commit.txt

```

## _Branch Rebase_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git checkout ft/new-branch-from-commit
Switched to branch 'ft/new-branch-from-commit'

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/new-branch-from-commit)
$ git rebase main
Successfully rebased and updated refs/heads/ft/new-branch-from-commit

```

## _Branch Renaming_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch -m ft/new-branch-from-commit ft/improved-branch-name

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (main)
$ git branch
  ft/branch
  ft/improved-branch-name
* main

```

## _Checking Out Detached HEAD_

```bash
PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/improved-branch-name)
$ git log --oneline
5e5fcee (HEAD -> ft/improved-branch-name, origin/main, main) Merge branch 'main' of h
ttps://github.com/Preacher-Y/git-advanced "the merge successfull"
ec0a805 merging ft/new-feature => main
679c24f Updated project readme
89e3a0c Implemented core functionality for new feature
c359cfe Create README.md
adee061 Implemented test 5
d19badc chore: Create third and fourth files

PREACHER@Preacher MINGW64 /e/The Gym/git-advanced (ft/improved-branch-name)
$ git checkout ec0a805
A       from-commit.txt
Note: switching to 'ec0a805'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ec0a805 merging ft/new-feature => main

```
