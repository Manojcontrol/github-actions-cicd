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
