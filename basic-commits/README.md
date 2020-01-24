2. What does the git log look like?

tsaelinh:basic-commits tsaelinh$ git log
commit b33b9848572d312e3261924f35bc489855455dac (HEAD -> master, origin/master, origin/HEAD)
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:38:11 2020 -0800

    Adding 3-way-merge exercise

commit fe4ffde0f877a7009b24a9ea8f707bc35a6c257d (greeting)
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:31:19 2020 -0800

    Adding README

commit 87b5ecc7772643330c4113159e8e3f5e1e3c8131
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:30:13 2020 -0800

    3-way adding greeting.txt

commit bd6084affe17dbc2da06ae33aa044f594fa9a512
Author: Tiffany Saelinh <tiffany@templarbit.com>
Date:   Thu Jan 23 23:21:40 2020 -0800

    Initial commit

4. What does the output from git status look like now?

tsaelinh:basic-commits tsaelinh$ vi test.txt
tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	test.txt

nothing added to commit but untracked files present (use "git add" to track)

6. How does git status look like now?

tsaelinh:basic-commits tsaelinh$ git add --all
tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   README.md
	new file:   test.txt

8. How does git status look like now?

tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

10. What does git status look like now?

tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md
	modified:   test.txt

no changes added to commit (use "git add" and/or "git commit -a")

12. after adding the file change, waht does the git status look like now?

tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   README.md
	modified:   test.txt

15. What does status look like now? the log? 

tsaelinh:basic-commits tsaelinh$ vi test.txt
tsaelinh:basic-commits tsaelinh$ git commit -m "Step 14 of basic-commits"
[master a6055b2] Step 14 of basic-commits
 2 files changed, 26 insertions(+), 1 deletion(-)
tsaelinh:basic-commits tsaelinh$ git status
On branch master
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md
	modified:   test.txt

no changes added to commit (use "git add" and/or "git commit -a")
tsaelinh:basic-commits tsaelinh$ git log
commit a6055b24980ffc687815ccde3c0a484ffa161a34 (HEAD -> master)
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:47:37 2020 -0800

    Step 14 of basic-commits

commit 7e7ed4a784361477ac783741966e6717bac5cefb
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:43:46 2020 -0800

    adding README.md

commit daca16dfc24a2de221c14813328457aab3c20129
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:43:07 2020 -0800

    Step 7 of basic-commits to commit files

commit c29ee65605cd41ce6483ec3cd3a23908e3f59e5a (origin/master, origin/HEAD)
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:40:18 2020 -0800

    Adding basic-commit README.md

commit b33b9848572d312e3261924f35bc489855455dac
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:38:11 2020 -0800

    Adding 3-way-merge exercise

commit fe4ffde0f877a7009b24a9ea8f707bc35a6c257d (greeting)
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:31:19 2020 -0800

    Adding README

commit 87b5ecc7772643330c4113159e8e3f5e1e3c8131
Author: Tiffany Saelinh <saelinht@gmail.com>
Date:   Thu Jan 23 23:30:13 2020 -0800

    3-way adding greeting.txt

commit bd6084affe17dbc2da06ae33aa044f594fa9a512
Author: Tiffany Saelinh <tiffany@templarbit.com>
Date:   Thu Jan 23 23:21:40 2020 -0800

    Initial commit
