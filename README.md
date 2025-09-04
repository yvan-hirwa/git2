# GIT ADVANCED EXERCISES

## PART 1: Refining Git History

1. Missing File Fix:

```bash
    #using git amend to add a missing file to a recent commit.

    #Initial commit
    echo "test">test1.md #First file
    echo "test">test2.md #Second file
    echo "test">test3.md #Third file
    git add test1.md test2.md #Added only two file
    git commit -m "Create two files"

    #Using git amend to add the third file to the recent commit
    git add test3.md
    git commit --amend -m"Create three files"
```

2. Editing an Older Commit with Interactive Rebase

```bash
    #git log --oneline to check the commit History
    cb2a83e (HEAD -> main, origin/main, origin/HEAD) Done: Exercise 1
    70914cc Create three files #<-- commit to change
    fb5bd2c Initial commit

    #Initializing interactive rebase with the last 2 commits
     git rebase -i HEAD~2

#    After Change:
#     git rebase -i HEAD~2
# [detached HEAD d7d80ae] Create all files
#  Date: Wed Sep 3 15:41:39 2025 +0200
#  3 files changed, 0 insertions(+), 0 deletions(-)
#  create mode 100644 test1.md
#  create mode 100644 test2.md
#  create mode 100644 test3.md
# Successfully rebased and updated refs/heads/main.
```
