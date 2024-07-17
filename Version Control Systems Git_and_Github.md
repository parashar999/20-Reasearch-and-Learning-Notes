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

