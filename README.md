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
