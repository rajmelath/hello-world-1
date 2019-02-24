# TIP Bytes, Session #1 - Git
##### 24<sup>th</sup> February, 2018

### Creating a Git Repo
How to create a new local repository
```BASH
git init .  # In the directory of choice.
```
#### How to add files
```BASH
git add <filename>
git add *   # All files in current directory, except hidden files
git add .   # All changes in repo, except deletions
git add -u  # All changes including deletions in repo, but not new files
git add -A  # All changes - What you'll mostly use.
```

How to remove files and add to git (Not used all that much)
```BASH
git rm <filename>
```
Does exactly what `rm` does and stages the changes.

### A brief explanation of how Git works
In git every user can make changes and add them as a _commit_. A commit forms a part of a linkedlist in the repo.
If you modify a commit inside the linked list - the chain breaks and the entire repo breaks. So all your changes are always only at the top.

#### File modification states.
In git there are 4 states each file can be in.
State | Meaning
:--|:--
Untracked| This file is not a part of the repo - even though it's in the file system.
Unstaged| This is a part of the repo and changes were made, but the changes haven't been added.
Staged| These changes are ready to be saved (committed)
Committed| Saved!

### Checking the status

You can check the status of changes in a git repository by using `git status`

### Checking the logs

You can print the history of the git repo by using `git log`

### Staging Changes

Same as add

### Unstaging

```BASH
git reset HEAD              # to unstage staged work
git reset HEAD <filename>   # to unstage one file
```

### Committing

Creating a commit basically means that you are _committing to these changes_ and that you are making them permanent.

`git commit`
This opens the commit message dialog (`vi` or `nano` text editor opens.)

General commit message format:
```BASH
<One line short explanation (max 56 char) end with fullstop>.

<Multiline long explanantion of the cause, solution and effect of bug etc>

<Fixes: xyz Read: xyz>
```

Sample:
```nasm
commit cca7633739e433259b926224f659b9540e518e0a
Author: Anish <anishbhobe@hotmail.com>
Date:   Mon Apr 23 19:25:36 2018 +0530

    Replaces CTRL with CMD in TileMapEditor for MacOS.
    
    Replacing CTRL with CMD makes sense dure to consistency
    with MacOS and avoiding conflict with the accessibility
    hotkey (ctrl+lmb = rmb)
    
    Fixes: #18238
```

### Branching workflow

Time to go online!!!

##### Commands to review
```BASH
git branch
git branch <new branch>
git checkout <some branch>
git merge <from>
git rebase <from>
git reset <where>  #HEAD, HEAD^, HEAD~2, commit-hash
git revert
```
