this part of the repo is about 3 way merges for 191A

tsaelinh:3-way-merge tsaelinh$ git checkout -b greeting
Switched to a new branch 'greeting'
tsaelinh:3-way-merge tsaelinh$ vi greeting.txt
tsaelinh:3-way-merge tsaelinh$ git status
On branch greeting
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	./

nothing added to commit but untracked files present (use "git add" to track)
tsaelinh:3-way-merge tsaelinh$ git add greeting.txt
tsaelinh:3-way-merge tsaelinh$ git status
On branch greeting
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   greeting.txt

tsaelinh:3-way-merge tsaelinh$ git commit -m "3-way adding greeting.txt"
[greeting 87b5ecc] 3-way adding greeting.txt
 1 file changed, 1 insertion(+)
 create mode 100644 3-way-merge/greeting.txt
tsaelinh:3-way-merge tsaelinh$ vi README.md
tsaelinh:3-way-merge tsaelinh$ git status
On branch greeting
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

nothing added to commit but untracked files present (use "git add" to track)
tsaelinh:3-way-merge tsaelinh$ git add README.md
tsaelinh:3-way-merge tsaelinh$ ls
README.md	greeting.txt
tsaelinh:3-way-merge tsaelinh$ git status
On branch greeting
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   README.md

tsaelinh:3-way-merge tsaelinh$ git commit -m "Adding README"
[greeting fe4ffde] Adding README
 1 file changed, 1 insertion(+)
 create mode 100644 3-way-merge/README.md
tsaelinh:3-way-merge tsaelinh$ git log --oneline --graph --all
* fe4ffde (HEAD -> greeting) Adding README
* 87b5ecc 3-way adding greeting.txt
* bd6084a (origin/master, origin/HEAD, master) Initial commit
tsaelinh:3-way-merge tsaelinh$ git diff greeting master
diff --git a/3-way-merge/README.md b/3-way-merge/README.md
deleted file mode 100644
index 5c397e8..0000000
--- a/3-way-merge/README.md
+++ /dev/null
@@ -1 +0,0 @@
-this part of the repo is about 3 way merges for 191A
diff --git a/3-way-merge/greeting.txt b/3-way-merge/greeting.txt
deleted file mode 100644
index 0ff4fb4..0000000
--- a/3-way-merge/greeting.txt
+++ /dev/null
@@ -1 +0,0 @@
-howdy
tsaelinh:3-way-merge tsaelinh$ git merge greeting master
Already up to date.
tsaelinh:3-way-merge tsaelinh$ git merge master greeting
Already up to date.
tsaelinh:3-way-merge tsaelinh$ git diff master greeting
diff --git a/3-way-merge/README.md b/3-way-merge/README.md
new file mode 100644
index 0000000..5c397e8
--- /dev/null
+++ b/3-way-merge/README.md
@@ -0,0 +1 @@
+this part of the repo is about 3 way merges for 191A
diff --git a/3-way-merge/greeting.txt b/3-way-merge/greeting.txt
new file mode 100644
index 0000000..0ff4fb4
--- /dev/null
+++ b/3-way-merge/greeting.txt
@@ -0,0 +1 @@
+howdy
tsaelinh:3-way-merge tsaelinh$ git status
On branch greeting
nothing to commit, working tree clean
tsaelinh:3-way-merge tsaelinh$ git branch
* greeting
  master
tsaelinh:3-way-merge tsaelinh$ git branch master
fatal: A branch named 'master' already exists.
tsaelinh:3-way-merge tsaelinh$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
tsaelinh:3-way-merge tsaelinh$ git status
fatal: Unable to read current working directory: No such file or directory
tsaelinh:3-way-merge tsaelinh$ cd ..
tsaelinh:191-tiffanywong tsaelinh$ ls
README.md
tsaelinh:191-tiffanywong tsaelinh$ git checkout greeting
Switched to branch 'greeting'
tsaelinh:191-tiffanywong tsaelinh$ ls
3-way-merge	README.md
tsaelinh:191-tiffanywong tsaelinh$ git merge master greeting
Already up to date.
tsaelinh:191-tiffanywong tsaelinh$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
tsaelinh:191-tiffanywong tsaelinh$ git merge greeting
Updating bd6084a..fe4ffde
Fast-forward
 3-way-merge/README.md    | 1 +
 3-way-merge/greeting.txt | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 3-way-merge/README.md
 create mode 100644 3-way-merge/greeting.txt
tsaelinh:191-tiffanywong tsaelinh$
