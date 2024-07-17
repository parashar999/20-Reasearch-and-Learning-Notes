# Git and GitHub Overview

## Git and GitHub Basics

| **Concept**               | **Description**                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| **Git**                   | Version control system to track changes to files. Free and open-source, available for Windows, macOS, and Linux. |
| **GitHub**                | Web-based hosting service for Git repositories. Popular for collaboration and code sharing.         |
| **Difference**            | **Git:** Software for version control on your computer. <br> **GitHub:** Online platform to store and share Git repositories. |
| **Version Control**       | Manages the history of code, tracking changes and enabling collaboration. Essential for software development. |
| **Analogy**               | Version control is like game checkpoints; move to any point in history and return to previous checkpoints. |
| **History**               | Before Git, SCCS (Source Code Control System) was used, proprietary and expensive. Git replaced SCCS, making version control accessible and user-friendly. |
| **Other VCS**             | Common version control systems include Subversion (SVN), CVS, and Perforce.                        |

## Learning Path

1. Get the basics
2. Use it daily
3. Face the problems
4. Solve them
5. Learn more

# Git Basic Commands Overview

| **Command**                             | **Description**                                                                                              |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git --version`                         | Check the version of Git installed on your system.                                                           |
| `git status`                            | Show the current state of your repository.                                                                   |
| `git config --global user.email`        | Set the global email configuration for Git commits.                                                          |
| `git config --global user.name`         | Set the global username configuration for Git commits.                                                       |
| `git config --list`                     | List all Git configuration settings.                                                                         |
| `git init`                              | Initialize a new Git repository.                                                                             |
| `git add <file> <file2>`                | Add files to the staging area.                                                                               |
| `git commit -m "commit message"`        | Commit changes with a message.                                                                               |
| `git log`                               | Show the commit history of the repository.                                                                   |
| `git log --oneline`                     | Show a compact view of the commit history.                                                                   |
| `git config --global core.editor`       | Change the default code editor for Git.                                                                      |
| `.gitignore`                            | File to specify which files and directories to ignore in the repository.                                      |

# Terminology

| **Term**           | **Description**                                                                                              |
|--------------------|--------------------------------------------------------------------------------------------------------------|
| **Repository**     | A collection of files and directories stored together, tracked by Git.                                       |
| **Branch**         | An alternative timeline of commits within a repository.                                                      |
| **Commit**         | A snapshot of your code at a particular point in time.                                                       |
| **Stage**          | A way to tell Git to track a particular file or folder before committing.                                    |
| **Config Settings**| Settings for Git, such as username, email, and default editor.                                               |
| **Logs**           | The history of commits in the repository.                                                                    |
| **Gitignore**      | A file specifying which files and directories Git should ignore.                                             |

# Git Behind the Scenes

## Git Snapshots
A git snapshot is a point in time in the history of your code. It represents a specific version of your code, including all the files and folders that were present at that time. Each snapshot is identified by a unique hash code, which is a string of characters that represents the contents of the snapshot. Snapshot is a loose term that is used when git stores information about the code in a locally stored key-value based database. Everything is stored as an object and each object is identified by a unique hash code.

## 3 Musketeers of Git

| **Object**        | **Description**                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| **Commit Object** | Contains information about a commit, including tree object, parent commit object, author, committer, and commit message. |
| **Tree Object**   | A container for all files and folders in the project, storing file mode, file name, file hash, and parent tree object. |
| **Blob Object**   | Contains the actual file content within the tree object.                                                     |

## Helpful Commands

| **Command**                                    | **Description**                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git show -s --pretty=raw <commit-hash>`       | Display the raw commit object for a specific commit hash.                                                    |
| `git ls-tree <tree-id>`                        | List the contents of a tree object using the tree ID.                                                        |
| `git show <blob-id>`                           | Display the content of a blob object using the blob ID.                                                      |
| `git cat-file -p <commit-id>`                  | Display the content of a commit object using the commit ID.                                                  |
# Branches in Git

Branches are a way to work on different versions of a project at the same time. They allow you to create a separate line of development that can be worked on independently of the main branch. This can be useful when you want to make changes to a project without affecting the main branch or when you want to work on a new feature or bug fix.

## Branching Concepts

| **Concept**              | **Description**                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------|
| **HEAD**                 | The HEAD is a pointer to the current branch that you are working on. It points to the latest commit in the current branch. |
| **Default Branch**       | The default branch used to be called master, but it is now called main. There is nothing special about main; it is just a convention. |

## Branching Commands

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git branch`                             | Lists all the branches in the current repository.                                                            |
| `git branch bug-fix`                     | Creates a new branch called bug-fix.                                                                         |
| `git switch bug-fix`                     | Switches to the bug-fix branch.                                                                              |
| `git log`                                | Shows the commit history for the current branch.                                                             |
| `git switch main`                        | Switches to the main branch.                                                                                 |
| `git switch -c dark-mode`                | Creates and switches to a new branch called dark-mode.                                                       |
| `git checkout orange-mode`               | Switches to the orange-mode branch.                                                                          |

## Merging Branches

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git checkout main`                      | Switches to the main branch.                                                                                 |
| `git merge bug-fix`                      | Merges the bug-fix branch into the main branch.                                                              |

### Types of Merges

| **Type**                  | **Description**                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------|
| **Fast-Forward Merge**    | The branch being merged is ahead, with no conflicts.                                                         |
| **Not Fast-Forward Merge**| The master branch also has commits not in the bug-fix branch, leading to conflicts that need manual resolution. |

## Managing Conflicts

| **Tool**                  | **Description**                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------|
| **VSCode Merge Tool**     | A built-in merge tool in VSCode to help resolve conflicts.                                                   |
| **Github Merge Tool**     | Github also has a merge tool for resolving conflicts.                                                        |

## Additional Branch Management

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git branch -m <old-branch-name> <new-branch-name>` | Renames a branch from old-branch-name to new-branch-name.                                                      |
| `git branch -d <branch-name>`            | Deletes a branch called branch-name.                                                                          |
| `git checkout <branch-name>`             | Switches to the branch called branch-name.                                                                    |
| `git branch`                             | Lists all branches in the repository.                                                                         |

# Git Diff, Stash, and Tags

## Git Diff

The `git diff` command is used to show the differences between two commits. It compares the changes made in one commit with another, identifying the differences between file versions.

### Diff Concepts

| **Concept**  | **Description**                                                                                              |
|--------------|--------------------------------------------------------------------------------------------------------------|
| **a -> file A and b -> file B** | Indicates the two different versions of the same file.                                      |
| **----**     | Indicates file A.                                                                                             |
| **+++**      | Indicates file B.                                                                                             |
| **@@**       | Indicates the line number.                                                                                    |

### Diff Commands

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git diff`                               | Shows the unstaged changes in your working directory compared to the staging area.                           |
| `git diff --staged`                      | Shows the changes between your last commit and the staging area (changes that are staged and ready to be committed). |
| `git diff <branch-name-one> <branch-name-two>` | Compares the difference between two branches.                                                                 |
| `git diff branch-name-one..branch-name-two` | Another way to compare the difference between two branches.                                                    |
| `git diff <commit-hash-one> <commit-hash-two>` | Compares the difference between two commits.                                                                  |

## Git Stash

Stash is a way to save your changes in a temporary location, allowing you to switch branches or perform other actions without committing changes.

### Stash Commands

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git stash`                              | Saves your changes in a temporary location.                                                                  |
| `git stash save "work in progress on X feature"` | Saves your changes with a specific name.                                                                     |
| `git stash list`                         | Views the list of stashes.                                                                                   |
| `git stash apply`                        | Applies the stash.                                                                                           |
| `git stash apply stash@{0}`              | Applies a specific stash.                                                                                    |
| `git stash pop`                          | Applies the stash and drops it from the stash list.                                                          |
| `git stash drop`                         | Drops the stash.                                                                                             |
| `git stash apply stash@{0} <branch-name>` | Applies the stash to a specific branch.                                                                      |
| `git stash clear`                        | Clears all stashes.                                                                                          |

## Git Tags

Tags are used to mark specific points in your repository, such as releases or important commits.

### Tag Commands

| **Command**                              | **Description**                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| `git tag <tag-name>`                     | Creates a new tag with the specified name, attached to the current commit.                                    |
| `git tag -a <tag-name> -m "Release 1.0"` | Creates an annotated tag with the specified name and message.                                                 |
| `git tag`                                | Lists all the tags in your repository.                                                                        |
| `git tag <tag-name> <commit-hash>`       | Tags a specific commit.                                                                                       |
| `git push origin <tag-name>`             | Pushes tags to a remote repository.                                                                           |
| `git tag -d <tag-name>`                  | Deletes a tag.                                                                                               |
| `git push origin :<tag-name>`            | Deletes a tag on a remote repository.                                                                         |

## Git Rebase

Rebase in Git allows you to move a branch to a new starting point by replaying commits from the original base onto the new base. It helps maintain a cleaner, linear project history.

### Rebase Commands

| Command                                 | Description                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------|
| `git rebase main`                       | Replays commits from the current branch (`feature-branch`) onto the main branch.                     |
| `git add <resolved-files>`              | Resolves conflicts during rebase by adding resolved files.                                            |
| `git rebase --continue`                 | Continues the rebase process after resolving conflicts.                                               |
| `git rebase --abort`                    | Cancels the rebase operation and resets the branch to its original state before rebase started.      |
| `git rebase -i <commit-hash>`           | Initiates an interactive rebase allowing you to squash, edit, or reorder commits interactively.       |

## Git Reflog

Git reflog is a command that shows a history of commits, useful for debugging and understanding changes in project history over time.

### Reflog Commands

| Command                                 | Description                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------|
| `git reflog`                            | Displays a log of all commits, including those no longer referenced by any branch or tag.             |
| `git reflog <commit-hash>`              | Shows the history of changes associated with a specific commit hash.                                   |
| `git reset --hard <commit-hash>`        | Resets the current branch to the specified commit, useful for recovering lost commits or changes.     |
| `git reset --hard HEAD@{1}`             | Resets the current branch to the commit one step before the current HEAD, based on reflog entries.    |
