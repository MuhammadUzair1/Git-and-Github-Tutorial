# Git and GitHub Setup and Tutorial

This tutorial will guide you through the basics of setting up Git and GitHub, connecting the two, and managing your version control workflow effectively. By the end, you'll be able to make commits, push and pull changes, handle branching, and create merge requests.

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installing Git](#installing-git)
3. [Setting Up Git](#setting-up-git)
4. [Creating a GitHub Account](#creating-a-github-account)
5. [Connecting Git with GitHub](#connecting-git-with-github)
6. [Basic Git and GitHub Workflow](#basic-git-and-github-workflow)
    - Cloning a Repository
    - Making Commits
    - Pushing Changes
    - Pulling Changes
    - Generating Pull Requests
7. [Branching in Git](#branching-in-git)
    - Creating a Branch
    - Switching Branches
    - Merging Branches
8. [Managing Merge Requests](#managing-merge-requests)
9. [Common Git Commands](#common-git-commands)
10. [Best Practices](#best-practices)

---

## Prerequisites

- A computer with Windows, macOS, or Linux
- Basic command-line knowledge

---

## Installing Git

1. **Windows**  
   Download and install Git for Windows from [git-scm.com](https://git-scm.com/). During installation, select default options unless you have specific preferences.

2. **macOS**  
   Open a terminal and run:
   ```bash
   brew install git
   ```

3. **Linux**  
   Use your distribution’s package manager:
   ```bash
   sudo apt update
   sudo apt install git
   ```

---

## Setting Up Git

1. **Verify Installation**  
   Run the following command:
   ```bash
   git --version
   ```

2. **Configure User Details**  
   Set your name and email for commits:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "youremail@example.com"
   ```

3. **Check Configuration**  
   Confirm your settings:
   ```bash
   git config --list
   ```

---

## Creating a GitHub Account

1. Go to [GitHub](https://github.com/) and sign up for a free account.
2. Once signed in, create a new repository by clicking the `+` icon and selecting **New repository**.

---

## Connecting Git with GitHub

1. **Generate SSH Key**  
   Run the following commands to create an SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "youremail@example.com"
   ```

2. **Add SSH Key to GitHub**  
   - Copy the generated key:
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
   - Go to GitHub **Settings > SSH and GPG keys**, click **New SSH Key**, and paste the copied key.

3. **Test Connection**  
   Verify the connection:
   ```bash
   ssh -T git@github.com
   ```

---

## Basic Git and GitHub Workflow

### Cloning a Repository
Clone an existing repository from GitHub:
```bash
git clone git@github.com:username/repository-name.git
cd repository-name
```

### Making Commits
1. Make changes to files.
2. Stage changes:
   ```bash
   git add .
   ```
3. Commit changes:
   ```bash
   git commit -m "Describe your changes"
   ```

### Pushing Changes
Push your commits to GitHub:
```bash
git push origin branch-name
```

### Pulling Changes
Fetch and merge changes from GitHub:
```bash
git pull origin branch-name
```

### Generating Pull Requests
1. Push your branch to GitHub.
2. On GitHub, navigate to your repository.
3. Click **Compare & pull request**.
4. Add a description and submit the request.

---

## Branching in Git

### Creating a Branch
```bash
git branch branch-name
```

### Switching Branches
```bash
git checkout branch-name
```

### Merging Branches
1. Switch to the target branch (e.g., `main`):
   ```bash
   git checkout main
   ```
2. Merge the branch:
   ```bash
   git merge branch-name
   ```

---

## Managing Merge Requests

1. Review the pull request on GitHub.
2. Approve or request changes.
3. Merge the request using the **Merge** button.

### Handling Merge Conflicts
If conflicts arise:
1. Open the conflicting file and resolve issues manually.
2. Stage the resolved file:
   ```bash
   git add file-name
   ```
3. Complete the merge:
   ```bash
   git commit
   ```

---

## Common Git Commands

| Command                             | Description                                    |
|-------------------------------------|------------------------------------------------|
| `git init`                          | Initialize a new Git repository.              |
| `git status`                        | Check the status of your working directory.   |
| `git log`                           | View commit history.                          |
| `git remote -v`                     | Show connected remote repositories.           |
| `git branch`                        | List branches in the repository.              |
| `git checkout -b branch-name`       | Create and switch to a new branch.            |

---

## Best Practices

- Write clear commit messages.
- Use branches for new features or bug fixes.
- Regularly pull changes to avoid merge conflicts.
- Always test before merging into the main branch.

---

With this guide, you’re well-equipped to manage your projects using Git and GitHub effectively.