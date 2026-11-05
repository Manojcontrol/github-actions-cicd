# Automate Code Deployment Using CI/CD Pipeline (GitHub Actions)

## 1. Project Overview

This project demonstrates how to automate application deployment using a Continuous Integration and Continuous Deployment (CI/CD) pipeline with GitHub Actions.

The main objective is to automatically deploy application code to an AWS EC2 server whenever new code is pushed to the GitHub repository.

### Project Objectives

- Understand Git and GitHub.
- Create and manage a GitHub repository.
- Understand Continuous Integration and Continuous Deployment.
- Configure GitHub Actions workflows.
- Connect GitHub Actions securely to AWS EC2.
- Automate application deployment.
- Verify successful deployment.

## 2. Technologies Used

| Technology | Purpose |
|---|---|
| Git | Version control system |
| GitHub | Online code repository |
| GitHub Actions | CI/CD automation |
| AWS EC2 | Application hosting server |
| Linux | Server operating system |
| SSH | Secure server connection |
| YAML | GitHub Actions workflow configuration |
| HTML | Sample web application |

## 3. Understanding CI/CD

### What is CI?

CI stands for Continuous Integration.

It is the practice of frequently integrating code changes into a shared repository and automatically performing checks such as building and testing.

### What is CD?

CD stands for Continuous Delivery or Continuous Deployment.

It automates the process of preparing or deploying application code after successful integration and testing.

### Our CI/CD Workflow

1. Developer creates or modifies application code.
2. Developer pushes code to GitHub.
3. GitHub Actions detects the code changes.
4. The workflow starts automatically.
5. The application is checked and tested.
6. GitHub Actions securely connects to AWS EC2.
7. The latest application files are deployed.
8. The updated application becomes accessible.

## 4. Project Implementation – Step by Step

### Step 1: Create a GitHub Account

**Purpose:** GitHub provides an online platform to store, manage, and collaborate on source code.

### Step 2: Install Git

**Purpose:** Git is a version control tool that tracks changes in project files.

**Verification command:**

```bash
git --version
```

**Expected result:** Displays the installed Git version.

### Step 3: Create a Project Directory

**Command:**

```bash
mkdir github-actions-cicd
```

**Explanation:** Creates a new directory for the project.

**Enter the directory:**

```bash
cd github-actions-cicd
```

**Explanation:** Changes the current working directory to the project folder.

### Step 4: Create a Sample Website

**Command:**

```bash
echo "<h1>Hello! CI/CD Pipeline is Working!</h1>" > index.html
```

**Explanation:** Creates an HTML file containing a sample heading.

**Verify the file:**

```bash
cat index.html
```

### Step 5: Initialize Git

**Command:**

```bash
git init
```

**Explanation:** Initializes a local Git repository inside the project directory so Git can track project changes.

### Step 6: Configure Git Identity

**Commands:**

```bash
git config --global user.name "Manoj Kumar Sahu"
git config --global user.email "manojkumar.sahu1100@gmail.com"
```

**Explanation:** Configures the username and email used to identify commits made from this computer.

**Verify configuration:**

```bash
git config --global --list
```

### Step 7: Check Project Status

**Command:**

```bash
git status
```

**Explanation:** Displays the current status of files in the Git repository.

An untracked file means Git has detected the file but is not yet tracking it.

### Step 8: Add Files to Git

**Command:**

```bash
git add index.html
```

**Explanation:** Adds the HTML file to the staging area. The staging area contains changes selected for the next commit.

### Step 9: Commit the Changes

**Command:**

```bash
git commit -m "Initial commit - Create website"
```

**Explanation:** Creates a snapshot of the staged changes in the local Git repository.

### Step 10: View Commit History

**Command:**

```bash
git log --oneline
```

**Explanation:** Displays the commit history in a short format.

## 5. Upcoming Implementation Steps

The following tasks will be completed during the project:

- [ ] Connect the local Git repository to GitHub.
- [ ] Push application code to GitHub.
- [ ] Verify the AWS EC2 server.
- [ ] Configure the web server on EC2.
- [ ] Configure secure SSH authentication.
- [ ] Add GitHub repository secrets.
- [ ] Create the GitHub Actions workflow file.
- [ ] Configure automatic deployment.
- [ ] Test the complete CI/CD pipeline.
- [ ] Verify the updated application in a web browser.

## 6. Expected Final Result

Whenever a developer pushes new code to the main branch of the GitHub repository, GitHub Actions will automatically execute the deployment workflow and update the application hosted on AWS EC2.

**Project Status:** In Progress

**Project:** Automate Code Deployment Using CI/CD Pipeline (GitHub Actions)

## Step 11: Rename the Default Git Branch to Main

**Command:**
```bash
git branch -M main
```

**What does this command do?**

- `git branch` is used to manage branches in Git.
- `-M` renames the current branch.
- `main` is the new branch name.

**Why is this required?**

Git repositories commonly use `main` as the default branch name. We renamed our local branch from `master` to `main` to match the GitHub repository.

**Result:**

The local Git branch was successfully renamed to `main`.

---

## Step 12: Connect the Local Repository to GitHub

**Command:**
```bash
git remote add origin https://github.com/Manojcontrol/github-actions-cicd.git
```

**What does this command do?**

- `git remote` manages connections to remote repositories.
- `add` adds a new remote repository.
- `origin` is the default name given to the remote repository.
- The URL specifies our GitHub repository.

**Why is this required?**

This connects our local project folder to the GitHub repository so that we can upload and download project files.

**Verify the connection:**
```bash
git remote -v
```

This command displays the remote repository URLs configured in Git.

**Result:**

The local repository was successfully connected to GitHub using the remote name `origin`.

---

## Step 13: Download and Merge Existing GitHub Files

**Command:**
```bash
git pull origin main --allow-unrelated-histories --no-rebase
```

**What does this command do?**

- `git pull` downloads and integrates changes from a remote repository.
- `origin` identifies our GitHub repository.
- `main` specifies the branch.
- `--allow-unrelated-histories` allows Git to merge two repositories that were initialized separately.
- `--no-rebase` instructs Git to use a merge instead of rebasing.

**Why is this required?**

We initially created the `README.md` file directly on GitHub, while our `index.html` file and initial commit were created locally. Since both repositories had separate histories, we needed to merge them.

**Additional step:**

Git opened the Vim editor to confirm the merge commit message.

To save and exit:
1. Press `Esc`.
2. Type `:wq`.
3. Press `Enter`.

**Result:**

The local repository and GitHub repository histories were successfully merged.

---

## Step 14: Upload the Local Project to GitHub

**Command:**
```bash
git push -u origin main
```

**What does this command do?**

- `git push` uploads local commits to GitHub.
- `-u` establishes an upstream tracking connection.
- `origin` specifies the remote repository.
- `main` specifies the destination branch.

**Why is this required?**

This uploads our local project files and commits to the GitHub repository, making them available online.

The upstream tracking connection also allows us to use `git push` and `git pull` more easily in future operations.

**Result:**

The local project is synchronized with the GitHub repository.

---

## Step 15: Verify the GitHub Repository

**Repository URL:**

https://github.com/Manojcontrol/github-actions-cicd

**Files expected in the repository:**

1. `README.md` – Project documentation.
2. `index.html` – Sample website.

**Verification:**

Open the GitHub repository in a browser and confirm that both files are visible.

**Result:**

The project files and documentation are available in the GitHub repository.

---

## Current Project Progress

- [x] Git installation and configuration
- [x] Local project folder creation
- [x] Sample HTML website creation
- [x] Git repository initialization
- [x] Initial commit
- [x] Rename branch to main
- [x] Connect local repository to GitHub
- [x] Merge local and remote repository histories
- [x] Upload project to GitHub
- [x] Verify repository files

**Next Phase:** Configure AWS EC2 and prepare the server for automated website deployment using GitHub Actions.
