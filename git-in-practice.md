# What is Git?

Git is a version control system that is widely used for software development and other version control tasks. It allows multiple developers to work on the same project concurrently, and it tracks changes to the project over time, so that developers can recall specific versions later if needed. Git also makes it easy to collaborate with other developers, since it allows you to share your changes and merge the changes of others into your own project.

Git is a distributed version control system, which means that each developer's copy of the project includes the complete project history, so they can work offline and commit their changes at a later time. This also makes it easy to recover from mistakes, since you can always revert to a previous version of the project if needed.

# What is GitHub?

GitHub is a web-based platform that provides hosting for Git repositories. It is a subsidiary of Microsoft and is widely used by software developers and other professionals to store and manage their code repositories.

GitHub provides a user interface for working with Git repositories, which makes it easier for developers to collaborate on projects.

In addition to hosting code repositories, GitHub also provides tools for CI/CD, which allow developers to automate the process of building, testing, and deploying their code.

# Git vs GitHub

Most of the time biginur folks think that Git and GitHub are the same thing, but they are not. **Git** is a free and open-source version control system (VCS), while **GitHub** is a company that provides hosting for Git repositories online.

Git is a command-line tool that you can use to manage and track changes to your code and collaborate with other developers.

GitHub, on the other hand, is a web-based platform that provides a user interface for working with Git repositories. Also provides additional features and tools for working with Git repositories, such as a web-based code editor, project management tools, and team collaboration features.

**In order to use Git, you have to install it on your computer. To do this, you can download the latest version on the [official website](https://git-scm.com/downloads). You can download for your operating system from the options given.**

# Configure Git

I will assume that at this point you have installed Git. To verify this, you can run this command on the command line: `git --version`. This shows you the current version installed on you PC.

The next thing you'll need to do is to set your `username` and `email`. Git will use this information to identify who made specific changes to files.

To set your username, type and execute these commands: `git config --global user.name <YOUR_USERNAME>` and `git config --global user.email <YOUR_EMAIL>`. Just make sure to replace `<YOUR_USERNAME>` and `<YOUR_EMAIL>` with yours.

## Here are some common Git commands that you may find useful:

`git init` - This command is used to initialize a new Git repository on your local machine. It creates a new folder called "`.git`" in the current directory, which stores all the information about the repository, including the commit history and any configured branches.

`git clone <repository>` - This command is used to create a copy of an existing Git repository on your local machine. You can clone a repository from a remote server, such as GitHub, by specifying the `URL` of the repository. This is a useful command when you want to work on an existing project or contribute to an open-source project.

`git add <file>` - This command is used to stage a file for commit. When you stage a file, you are telling Git that you want to include it in the next commit. You can stage multiple files at once by specifying multiple file names, or you can use the `git add .` command to stage all modified and untracked files.

`git commit` - This command is used to save your changes to the repository. When you commit, you are creating a new snapshot of the repository that includes all the staged changes. _You should always include a commit message with each commit, which is a brief description of the changes you have made._

`git push` - This command is used to send your local commits to a remote repository, such as GitHub. When you push, you are updating the remote repository with your local commits, so that other developers can access your changes.

`git pull` - This command is used to retrieve updates from a remote repository and merge them into your local repository. When you pull, you are fetching any new commits from the remote repository and merging them into your local repository.

## Git Branches

In Git, a branch is a separate line of development within a repository. By default, every Git repository has a main branch called "`master`", which is the main line of development for the project. However, you can create additional branches to work on separate features or changes without affecting the `main` branch.

For example, suppose you are working on a software project and you want to add a new feature to the project. Instead of adding the feature directly to the `master` branch, you can create a new branch called `feature-x` and develop the feature in that branch. This allows you to work on the feature separately from the main development of the project, and it makes it easy to test and review the feature before integrating it into the master branch.

When you are ready to merge the feature into the master branch, you can use Git's merge or rebase commands to integrate the changes from the feature branch into the master branch. This allows you to keep the master branch clean and stable, while still being able to work on new features and changes in separate branches.

Branching is a powerful feature of Git that allows developers to work on multiple features or changes concurrently, and it makes it easy to review and test code before integrating it into the main development of the project.

Here is an example of using Git branches in a command-line workflow:

```Bash
# Create a new branch called "feature-x" and switch to it
git checkout -b feature-x

# Make some changes to the code and stage them for commit
git add file1.py file2.py

# Commit the changes with a commit message
git commit -m "Implemented feature x"

# Push the feature branch to the remote repository
git push -u origin feature-x

# Switch back to the master branch
git checkout master

# Fetch the latest changes from the remote repository
git pull

# Merge the feature-x branch into the master branch
git merge feature-x

# Push the updated master branch to the remote repository
git push
```

This example shows how to create a new branch called "feature-x", make some changes to the code, commit the changes, and push the branch to the remote repository. It also shows how to switch back to the master branch, fetch the latest changes from the remote repository, and merge the feature-x branch into the master branch.
