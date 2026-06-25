# Git & GitHub Practice Repository

## Overview

This repository documents my hands-on learning journey with Git and GitHub. The purpose of this project is to understand version control concepts, repository management, branching strategies, and collaboration workflows that are commonly used in DevOps and software development.

The exercises in this repository focus on practical Git commands and GitHub operations that every DevOps Engineer should know.

---

# What is Git?

Git is a distributed version control system (DVCS) used to track changes in source code and other files over time.

It helps developers:

* Track file modifications
* Maintain version history
* Collaborate with team members
* Create and manage branches
* Merge changes safely
* Recover previous versions when needed

## Why Use Git?

Without Git:

* Changes can be lost
* Collaboration becomes difficult
* No history of modifications
* Recovery from mistakes is challenging

With Git:

* Every change is tracked
* History is preserved
* Collaboration becomes easier
* Rollbacks are simple
* Development workflows become organized

---

# What is GitHub?

GitHub is a cloud-based platform that hosts Git repositories.

GitHub provides:

* Remote repository hosting
* Collaboration features
* Pull Requests
* Code Reviews
* Issue Tracking
* CI/CD Integrations
* Project Management Tools

## Git vs GitHub

| Git                    | GitHub                      |
| ---------------------- | --------------------------- |
| Version Control System | Repository Hosting Platform |
| Works locally          | Works in the cloud          |
| Tracks changes         | Stores repositories         |
| Command-line tool      | Web platform                |

---

# How Git Works

Git follows a simple workflow:

```text
Working Directory
        ↓
   Staging Area
        ↓
      Commit
        ↓
 Local Repository
        ↓
 Remote Repository (GitHub)
```

### Working Directory

The area where files are created and modified.

Example:

```bash
vim main.py
```

### Staging Area

Changes are prepared before committing.

```bash
git add main.py
```

### Commit

A snapshot of changes is saved.

```bash
git commit -m "added python file"
```

### Remote Repository

Changes are uploaded to GitHub.

```bash
git push origin main
```

---

# Git Configuration

Configure Git username:

```bash
git config --global user.name "your-username"
```

Configure Git email:

```bash
git config --global user.email "your-email@example.com"
```

Verify configuration:

```bash
git config --list
```

---

# Repository Initialization

Create project directory:

```bash
mkdir git-practice
cd git-practice
```

Initialize Git repository:

```bash
git init
```

Check repository status:

```bash
git status
```

---

# Working with Files

## Creating a File

```bash
touch hello.txt
```

Add content:

```bash
echo "hello" > hello.txt
```

Check status:

```bash
git status
```

Stage file:

```bash
git add hello.txt
```

Commit file:

```bash
git commit -m "added file"
```

---

# Working with Python Files

Create file:

```bash
vim main.py
```

Stage changes:

```bash
git add main.py
```

Commit:

```bash
git commit -m "added python file"
```

Modify file and create another commit:

```bash
git commit -m "modified python file"
```

---

# Git Restore Commands

## Restore Modified File

Discard local changes:

```bash
git restore main.py
```

Purpose:

* Removes uncommitted changes
* Restores file from latest commit

---

## Unstage File

Remove file from staging area:

```bash
git restore --staged main.py
```

Purpose:

* Keeps file changes
* Removes file from staging area

---

## Restore Deleted File

Delete file:

```bash
rm main.py
```

Restore file:

```bash
git restore main.py
```

Purpose:

* Recovers deleted tracked files

---

# Working with Shell Scripts

Create script:

```bash
vim hello.sh
```

Make executable:

```bash
chmod 764 hello.sh
```

Execute script:

```bash
./hello.sh
```

Commit script:

```bash
git add hello.sh
git commit -m "added script"
```

---

# SSH Authentication

Generate SSH key:

```bash
ssh-keygen
```

View public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Benefits of SSH:

* Secure authentication
* No repeated password entry
* Recommended for GitHub operations

---

# Connecting Local Repository to GitHub

Add remote repository:

```bash
git remote add origin <repository-url>
```

Verify remote:

```bash
git remote -v
```

Push code:

```bash
git push -u origin main
```

---

# Cloning Repositories

Clone an existing repository:

```bash
git clone <repository-url>
```

Benefits:

* Downloads complete repository
* Includes commit history
* Includes branches

---

# Branching in Git

Branches allow developers to work on features independently without affecting the main codebase.

## Create New Branch

```bash
git checkout -b devops
```

Verify:

```bash
git branch
```

---

## Switch Between Branches

Move to main branch:

```bash
git checkout main
```

Move to devops branch:

```bash
git checkout devops
```

---

# Branch-Based Development Practice

Created files:

```text
install_nginx.sh
index.html
```

Example Nginx installation script:

```bash
#!/bin/bash

sudo apt update
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```

Commit changes:

```bash
git add .
git commit -m "added nginx installation script"
```

Push branch:

```bash
git push origin devops
```

---

# Frequently Used Git Commands

| Command       | Description              |
| ------------- | ------------------------ |
| git init      | Initialize repository    |
| git status    | View repository status   |
| git add       | Stage files              |
| git commit    | Save changes             |
| git log       | View commit history      |
| git restore   | Restore files            |
| git branch    | View branches            |
| git checkout  | Switch branches          |
| git clone     | Clone repository         |
| git remote -v | View remote repositories |
| git push      | Upload changes           |
| git pull      | Download updates         |
| git config    | Configure Git            |

---

# DevOps Use Cases of Git

## Infrastructure as Code (IaC)

Store and manage:

* Terraform configurations
* Kubernetes manifests
* CloudFormation templates

## CI/CD Pipelines

Version control for:

* GitHub Actions
* Jenkins Pipelines
* GitLab CI/CD

## Configuration Management

Track:

* Ansible Playbooks
* Shell Scripts
* Dockerfiles

## Team Collaboration

Enable:

* Feature Branches
* Pull Requests
* Code Reviews
* Release Management

---

# Key Concepts Learned

During this practice, I learned:

* Git repository initialization
* File tracking and staging
* Creating commits
* Modifying and restoring files
* Branch creation and switching
* Remote repository management
* SSH authentication
* GitHub integration
* Repository cloning
* Shell script version control
* Basic DevOps Git workflows

---

# Learning Outcome

Git and GitHub are foundational tools for DevOps Engineers. Understanding version control is essential for managing infrastructure code, CI/CD pipelines, automation scripts, and collaborative software projects.

This repository represents my practical learning and experimentation with Git and GitHub concepts through hands-on exercises and real-world DevOps scenarios.

---