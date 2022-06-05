# Full Notes

```
PowerShell 7.2.4
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\Users\Bruce\Programming> cd .\git-fetch--git-merge--example\
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
* main
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        the_empty_file.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git add .
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git commit -m "Added empty 'the_empty_file.md'."
[main b7eb35d] Added empty 'the_empty_file.md'.
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 the_empty_file.md
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 323 bytes | 323.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/brucestull/git-fetch--git-merge--example.git
   ad82f15..b7eb35d  main -> main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -r
  origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
* main
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git fetch
remote: Enumerating objects: 2, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 1.26 KiB | 322.00 KiB/s, done.
From https://github.com/brucestull/git-fetch--git-merge--example
 * [new branch]      branch-with-line-number-one -> origin/branch-with-line-number-one
 * [new branch]      branch-with-line-number-two -> origin/branch-with-line-number-two
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
* main
  remotes/origin/branch-with-line-number-one
  remotes/origin/branch-with-line-number-two
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -r
  origin/branch-with-line-number-one
  origin/branch-with-line-number-two
  origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git fetch --dry-run
remote: Enumerating objects: 8, done.
remote: Counting objects: 100% (8/8), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), 1.36 KiB | 116.00 KiB/s, done.
From https://github.com/brucestull/git-fetch--git-merge--example
   776d64e..5deadfb  branch-with-line-number-one -> origin/branch-with-line-number-one
   3e3f823..e0f3947  branch-with-line-number-two -> origin/branch-with-line-number-two
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -4
commit d260c907d2776d90c12c82bce6d88839c30336d9 (HEAD -> main, origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.

commit b7eb35d6d44251f12c92b9dbc26e39f5af28223c
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 03:58:42 2022 -0400

    Added empty 'the_empty_file.md'.

commit ad82f15b59219f16337d69f794dd02bac78b54c3
Author: Bruce Stull <bruce.stull@gmail.com>
Date:   Sun Jun 5 03:34:10 2022 -0400

    first commit
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git fetch
From https://github.com/brucestull/git-fetch--git-merge--example
   776d64e..5deadfb  branch-with-line-number-one -> origin/branch-with-line-number-one
   3e3f823..e0f3947  branch-with-line-number-two -> origin/branch-with-line-number-two
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -6
commit d260c907d2776d90c12c82bce6d88839c30336d9 (HEAD -> main, origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.

commit b7eb35d6d44251f12c92b9dbc26e39f5af28223c
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 03:58:42 2022 -0400

    Added empty 'the_empty_file.md'.

commit ad82f15b59219f16337d69f794dd02bac78b54c3
Author: Bruce Stull <bruce.stull@gmail.com>
Date:   Sun Jun 5 03:34:10 2022 -0400

    first commit
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
* main
  remotes/origin/branch-with-line-number-one
  remotes/origin/branch-with-line-number-two
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-one
Switched to a new branch 'branch-with-line-number-one'
branch 'branch-with-line-number-one' set up to track 'origin/branch-with-line-number-one'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch branch-with-line-number-one
Your branch is up to date with 'origin/branch-with-line-number-one'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-two
Switched to a new branch 'branch-with-line-number-two'
branch 'branch-with-line-number-two' set up to track 'origin/branch-with-line-number-two'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch branch-with-line-number-two
Your branch is up to date with 'origin/branch-with-line-number-two'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
  branch-with-line-number-one
* branch-with-line-number-two
  main
  remotes/origin/branch-with-line-number-one
  remotes/origin/branch-with-line-number-two
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git diff branch-with-line-number-one remotes/origin/branch-with-line-number-one
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git diff main remotes/origin/branch-with-line-number-two
diff --git a/the_empty_file.md b/the_empty_file.md
index 54f96c2..3c3fa2c 100644
--- a/the_empty_file.md
+++ b/the_empty_file.md
@@ -1,7 +1,7 @@

+Line number 2




-
-The last line!
\ No newline at end of file
+The last line!
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -6
commit d260c907d2776d90c12c82bce6d88839c30336d9 (HEAD -> main, origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.

commit b7eb35d6d44251f12c92b9dbc26e39f5af28223c
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 03:58:42 2022 -0400

    Added empty 'the_empty_file.md'.

commit ad82f15b59219f16337d69f794dd02bac78b54c3
Author: Bruce Stull <bruce.stull@gmail.com>
Date:   Sun Jun 5 03:34:10 2022 -0400

    first commit
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch
  branch-with-line-number-one
  branch-with-line-number-two
* main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-one
Switched to branch 'branch-with-line-number-one'
Your branch is up to date with 'origin/branch-with-line-number-one'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -6
commit 5deadfb4101365cbafeea7b72f2d52a50cc54aef (HEAD -> branch-with-line-number-one, origin/branch-with-line-number-one)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:31 2022 -0400

    Update the_empty_file.md

commit 776d64e5f80c4efb5468839853abb31aae348018
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:18:05 2022 -0400

    Merge pull request #2 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit d260c907d2776d90c12c82bce6d88839c30336d9 (origin/main, main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.

commit b7eb35d6d44251f12c92b9dbc26e39f5af28223c
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 03:58:42 2022 -0400

    Added empty 'the_empty_file.md'.

commit ad82f15b59219f16337d69f794dd02bac78b54c3
Author: Bruce Stull <bruce.stull@gmail.com>
Date:   Sun Jun 5 03:34:10 2022 -0400

    first commit
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-two
Switched to branch 'branch-with-line-number-two'
Your branch is up to date with 'origin/branch-with-line-number-two'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -6
commit e0f3947733e1ecd448a75263c3e7589c6be2e9a4 (HEAD -> branch-with-line-number-two, origin/branch-with-line-number-two)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:57 2022 -0400

    Update the_empty_file.md

commit 3e3f8237f8ca54f927366a93db6f2a03e563f980
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:19:26 2022 -0400

    Merge pull request #3 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit d260c907d2776d90c12c82bce6d88839c30336d9 (origin/main, main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.

commit b7eb35d6d44251f12c92b9dbc26e39f5af28223c
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 03:58:42 2022 -0400

    Added empty 'the_empty_file.md'.

commit ad82f15b59219f16337d69f794dd02bac78b54c3
Author: Bruce Stull <bruce.stull@gmail.com>
Date:   Sun Jun 5 03:34:10 2022 -0400

    first commit
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch
  branch-with-line-number-one
* branch-with-line-number-two
  main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch -a
  branch-with-line-number-one
  branch-with-line-number-two
* main
  remotes/origin/branch-with-line-number-one
  remotes/origin/branch-with-line-number-two
  remotes/origin/main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git merge -v --no-ff branch-with-line-number-one
Merge made by the 'ort' strategy.
 the_empty_file.md | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -4
commit 6f68280b2a3ea94b18687302c8a88cb5e7a3fa84 (HEAD -> main)
Merge: d260c90 5deadfb
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:01:42 2022 -0400

    Merge branch 'branch-with-line-number-one'

commit 5deadfb4101365cbafeea7b72f2d52a50cc54aef (origin/branch-with-line-number-one, branch-with-line-number-one)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:31 2022 -0400

    Update the_empty_file.md

commit 776d64e5f80c4efb5468839853abb31aae348018
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:18:05 2022 -0400

    Merge pull request #2 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit d260c907d2776d90c12c82bce6d88839c30336d9 (origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git merge -v --no-ff branch-with-line-number-two
Auto-merging the_empty_file.md
CONFLICT (content): Merge conflict in the_empty_file.md
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git merge -v branch-with-line-number-two
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git diff main branch-with-line-number-two
diff --git a/the_empty_file.md b/the_empty_file.md
index 65dc7c9..3c3fa2c 100644
--- a/the_empty_file.md
+++ b/the_empty_file.md
@@ -1,5 +1,5 @@
-Line number 1

+Line number 2



PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch
  branch-with-line-number-one
  branch-with-line-number-two
* main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git merge -v --no-ff branch-with-line-number-two
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   the_empty_file.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git add .
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   the_empty_file.md

PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git commit -m "Atttempted to resolve conflicts."
[main 7e87f46] Atttempted to resolve conflicts.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -6
commit 7e87f4626d11a6e9f0a81b6aac2e51f65bfc2737 (HEAD -> main)
Merge: 6f68280 e0f3947
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:07:02 2022 -0400

    Atttempted to resolve conflicts.

commit 6f68280b2a3ea94b18687302c8a88cb5e7a3fa84
Merge: d260c90 5deadfb
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:01:42 2022 -0400

    Merge branch 'branch-with-line-number-one'

commit e0f3947733e1ecd448a75263c3e7589c6be2e9a4 (origin/branch-with-line-number-two, branch-with-line-number-two)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:57 2022 -0400

    Update the_empty_file.md

commit 5deadfb4101365cbafeea7b72f2d52a50cc54aef (origin/branch-with-line-number-one, branch-with-line-number-one)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:31 2022 -0400

    Update the_empty_file.md

commit 3e3f8237f8ca54f927366a93db6f2a03e563f980
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:19:26 2022 -0400

    Merge pull request #3 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit 776d64e5f80c4efb5468839853abb31aae348018
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:18:05 2022 -0400

    Merge pull request #2 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git branch
  branch-with-line-number-one
  branch-with-line-number-two
* main
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -3
commit 7e87f4626d11a6e9f0a81b6aac2e51f65bfc2737 (HEAD -> main)
Merge: 6f68280 e0f3947
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:07:02 2022 -0400

    Atttempted to resolve conflicts.

commit 6f68280b2a3ea94b18687302c8a88cb5e7a3fa84
Merge: d260c90 5deadfb
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:01:42 2022 -0400

    Merge branch 'branch-with-line-number-one'

commit e0f3947733e1ecd448a75263c3e7589c6be2e9a4 (origin/branch-with-line-number-two, branch-with-line-number-two)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:57 2022 -0400

    Update the_empty_file.md
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-one
Switched to branch 'branch-with-line-number-one'
Your branch is up to date with 'origin/branch-with-line-number-one'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -3
commit 5deadfb4101365cbafeea7b72f2d52a50cc54aef (HEAD -> branch-with-line-number-one, origin/branch-with-line-number-one)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:31 2022 -0400

    Update the_empty_file.md

commit 776d64e5f80c4efb5468839853abb31aae348018
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:18:05 2022 -0400

    Merge pull request #2 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit d260c907d2776d90c12c82bce6d88839c30336d9 (origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout branch-with-line-number-two
Switched to branch 'branch-with-line-number-two'
Your branch is up to date with 'origin/branch-with-line-number-two'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -3
commit e0f3947733e1ecd448a75263c3e7589c6be2e9a4 (HEAD -> branch-with-line-number-two, origin/branch-with-line-number-two)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:57 2022 -0400

    Update the_empty_file.md

commit 3e3f8237f8ca54f927366a93db6f2a03e563f980
Merge: b7eb35d d260c90
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:19:26 2022 -0400

    Merge pull request #3 from brucestull/main

    Added some empty lines to 'the_empty_file.md'.

commit d260c907d2776d90c12c82bce6d88839c30336d9 (origin/main)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:14:10 2022 -0400

    Added some empty lines to 'the_empty_file.md'.
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)
PS C:\Users\Bruce\Programming\git-fetch--git-merge--example> git log -3
commit 7e87f4626d11a6e9f0a81b6aac2e51f65bfc2737 (HEAD -> main)
Merge: 6f68280 e0f3947
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:07:02 2022 -0400

    Atttempted to resolve conflicts.

commit 6f68280b2a3ea94b18687302c8a88cb5e7a3fa84
Merge: d260c90 5deadfb
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 05:01:42 2022 -0400

    Merge branch 'branch-with-line-number-one'

commit e0f3947733e1ecd448a75263c3e7589c6be2e9a4 (origin/branch-with-line-number-two, branch-with-line-number-two)
Author: Bruce Stull <47562501+brucestull@users.noreply.github.com>
Date:   Sun Jun 5 04:35:57 2022 -0400

    Update the_empty_file.md
```

[README.md](../README.md)