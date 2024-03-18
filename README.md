# AWS-course-git-demo
A comprehensive understanding of Git basics


# Set global user name
git config --global user.name "Your Name"

# Set global email
git config --global user.email "Your Email"

# Set default text editor
git config --global core.editor "nano"

# Set up an alias
git config --global alias.st status

# Git Commands
Initializing a Repository:
git init: # Initializes a new Git repository in the current directory.

Cloning a Repository:
git clone <repository_url>: # Clones a remote repository to your local machine.

Basic Snapshotting:
git add <file>: # Adds changes in <file> to the staging area.
git add .: # Adds all changes to the staging area.
git rm <file>: # Removes <file> from both the working directory and the index.
git mv <file_old> <file_new>: # Moves or renames <file_old> to <file_new>.

Committing Changes:
git commit -m "Commit message": # Commits staged changes with the given message.
git commit -a: # Stages modified and deleted files, and commits all changes.

Inspecting Changes:
git status: # Displays the status of the working directory and staging area.
git diff: # Shows changes between the working directory and the staging area.
git diff --staged: # Shows changes between the staging area and the last commit.

Branching and Merging:
git branch: # Lists all branches in the repository.
git branch <branch_name>: # Creates a new branch with <branch_name>.
git checkout <branch_name>: # Switches to the specified branch.
git checkout -b <branch_name>: # Creates a new branch and switches to it.
git merge <branch_name>: # Merges <branch_name> into the current branch.
Viewing Commit History:

git log: # Displays commit history.
git log --oneline: # Condenses each commit to a single line.
git log --graph: # Displays commit history as a graph.

Remote Operations:
git remote add <name> <url>: # Adds a remote repository with the specified name and URL.
git remote -v: # Lists all remote repositories.
git fetch <remote>: # Fetches changes from the remote repository.
git pull <remote> <branch>: # Fetches changes and merges them into the current branch.
git push <remote> <branch>: # Pushes local commits to the remote repository.

Stashing Changes:
git stash: # Stashes changes in the working directory.
git stash pop: # Applies the most recently stashed changes and removes them from the stash.

Reverting Changes:
git reset --hard HEAD: # Resets the working directory and staging area to the last commit.
git revert <commit>: # Creates a new commit that undoes the changes introduced by <commit>.

Tagging Releases:
git tag <tag_name>: # Creates a lightweight tag at the current commit.
git tag -a <tag_name> -m "Tag message": # Creates an annotated tag with a message.
git tag -l: # Lists all tags in the repository.
git push --tags: # Pushes tags to the remote repository.
These are some of the most commonly used Git operations. Understanding and mastering these operations will help you effectively manage your Git repositories and collaborate with others

 Setting Up Multiple Profiles:
# Global Configuration:
# Set up your global configuration with your default profile.

git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"


Work Profile:
Create a work profile for your work-related projects.

git config --global --replace-all user.name "Your Work Name"
git config --global --replace-all user.email "your_work_email@example.com"

Creating Multiple Local Git Repositories:
Let's create two local repositories, one for personal projects and another for work-related projects.

Personal Project Repository:
mkdir personal_project
cd personal_project
git init


Work Project Repository:
mkdir work_project
cd work_project
git init

Using Different Profiles in Each Repository:
Now, we'll configure each repository to use the appropriate profile.

Personal Project Repository:
git config user.name "Your Name"
git config user.email "your_email@example.com"

Work Project Repository:
git config user.name "Your Work Name"
git config user.email "your_work_email@example.com"

Verifying Configurations:
You can verify the configurations for each repository:

Personal Project Repository:
git config --list

Work Project Repository:
git config --list

Summary:
Now you have set up two profiles, one for personal projects and another for work-related projects, and configured each repository to use the appropriate profile. This allows you to maintain separate identities for your personal and work projects.

