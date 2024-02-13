# Git & Github Tutorials

In this tutorial, you will:

- Create and use a repository
- Start and manage a new branch
- Make changes to a file and push them to GitHub as commits
- Open and merge a pull request

### What is Git?
Git is a distributed version control system used to track changes in source code during software development. It allows multiple people to collaborate on projects and keep track of changes made to the codebase.

### What is GitHub?
GitHub is a web-based hosting service for Git repositories. It provides a graphical interface and tools for collaboration and allows developers to host their Git repositories online.

## Setting Up Git and GitHub
1. **Install Git**: Go to [git-scm.com](https://git-scm.com/downloads) and download the appropriate version of Git for your operating system. Follow the installation instructions.

2. **Create a GitHub Account**: Go to [github.com](https://github.com/) and sign up for an account. It's free!

3. **Set Up Git Configuration**: Open a terminal or command prompt and configure Git with your username and email address:
    ```
    git config --global user.name "Your Name"
    git config --global user.email "youremail@example.com"
    ```

## Basic Git Commands

![Alt text](https://www.junosnotes.com/wp-content/uploads/2021/07/basic-git-commands.png)

1. Create a new directory called `git-exercise` and navigate into it:
   ```
   mkdir git-exercise
   cd git-exercise
   ```

2. Initialize a new Git repository:
   ```
   git init
   ```

3. Create a file named `README.md` and add some content to it.

4. Stage the file for commit:
   ```
   git add README.md
   ```

5. Commit the file to the repository:
   ```
   git commit -m "Initial commit"
   ```

6. View the status of your repository to see which files are staged or modified:
    ```
    git status
    ```

7. See a list of commits in your repository:
    ```
    git log
    ```

## Introduction to GitHub

**Creating a GitHub Repository**

1. Sign up or log in to [GitHub](https://github.com/).
2. Click on the "+" icon in the top right corner and select "New repository."

Notes: You have the choice to create a Public or Private repository, for the exercice you can create a Public repository.

3. Name your repository `git-exercise` and click "Create repository."

**Pushing Changes to GitHub**

1. Link your local repository to your GitHub repository:
   ```
   git remote add origin <repository-URL>
   ```
2. Push your commits to GitHub:
   ```
   git push -u origin master
   ```
3. Go to the original GitHub repository page, you'll see your changes.

## Collaboration with Github

Pair up with a classmate to practice a collaborative workflow using branching, pull requests, and merges.


**Adding a Collaborator:**
1. Go to the `git-exercise` repository on GitHub.
2. Navigate to "Settings" > "Collaborate" and add your classmate or colleague by their GitHub username as a collaborator. They will need to accept the invitation.

**Creating Feature Branches:**
1. Each collaborator clones the repository to their local system:
     ```
     mkdir collaboration-exercice
     cd collaboration-exercice
     git clone <repository-url>
     ```
2. Each collaborator creates a new branch named after their firstname. For example, if your name is Bob, you would create a branch `bob`:
     ```
     git checkout -b bob
     ```

**Adding Files:**
1. On your branch (`bob`), create a new file named after yourself with a `.txt` extension (e.g., `bob.txt`).
2. Add some content to your file, such as a brief introduction or a note.
3. Stage and commit your file to your branch:
     ```
     git add <filename>
     git commit -m "Add <filename>"
     ```

**Pushing Branches and Creating Pull Requests:**
1. Push your branch to GitHub:
     ```
     git push -u origin <branch-name>
     ```
2. Go to the GitHub page for your `git-exercise` repository. You should see a prompt to create a pull request for your branch. Click "Compare & pull request" and submit it.

**Reviewing and Merging:**
1. Each collaborator reviews the other's pull request by going to the "Pull Requests" tab on GitHub, selecting the pull request, and reviewing the changes.
2. Provide feedback if necessary. If everything looks good, the repository owner (or collaborator with merge permissions) merges the pull request into the main branch.
3. To update your local repository with changes from GitHub, use:
    ```
    git pull origin main
    ```

## Working with GitHub Issues

1. Go to your `git-exercise` repository on GitHub.
2. Navigate to the "Issues" tab and click "New issue".
3. Give your issue a title that summarizes the task or problem, such as "Add a contributors file".
4. In the description, provide more details about what needs to be done. For example, "Create a `CONTRIBUTORS.md` file to list all project contributors.".
5. Click "Submit new issue."
6. Assign the the issue to yourself: *Assignees* > "assign yourself".
6. Create a branch from the issue: Open the issue go to *Development* > "Create a branch".
