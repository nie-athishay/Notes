The module mainly covers **VCS, Git, Git commands, Git process, branching, and Gitflow**. 

# Module 2 – Important 15-Mark Answers

## Important Questions

### 1. Explain Version Control System (VCS) and its types.

### 2. Explain Git and its important terminology.

### 3. Explain important Git commands with examples.

### 4. Explain the Git process/workflow with a suitable example.

### 5. Explain branching and Gitflow strategy in detail.

### 6. Explain centralized and distributed version control systems. Compare them.

### 7. Explain Git branching strategy and different branches used in Gitflow.

---

# 1. Explain Version Control System (VCS) and its Types

## Introduction

When developers work together on a project, they face many problems:

* How to share code with team members?
* How to maintain different versions of code?
* How to track changes?
* How to get an old version of the code?

These problems are solved using a **Version Control System (VCS)**. 

## Definition

A **Version Control System** is software that tracks changes made to files over time.

It allows developers to:

1. Collaborate on code
2. Retrieve code
3. Maintain different versions
4. Track changes
5. Restore earlier versions

### Examples

* Git
* Subversion (SVN)
* Mercurial

---

# Types of VCS

There are mainly two types:

1. **Centralized Version Control System**
2. **Distributed Version Control System**

---

## 1. Centralized Version Control System

In a centralized system, there is **one central server** containing the project code.

Developers connect to this server to:

* Upload code
* Download code
* Retrieve previous versions

### Examples

* SVN
* CVS
* TFVC
* VSS

### Diagram

```text
        CENTRAL SERVER
              |
      ┌───────┼───────┐
      ↓       ↓       ↓
   Dev 1    Dev 2    Dev 3
```

### Advantages

* Central location for code
* Easy collaboration
* Central backup

### Disadvantages

1. Internet/network connection may be required.
2. If the central server fails, developers cannot retrieve or archive code.
3. Code history may be lost if the server is lost. 

---

# 2. Distributed Version Control System

In a distributed system, every developer has a **local copy of the repository**.

There is also a remote repository.

### Diagram

```text
             REMOTE
           REPOSITORY
          /     |     \
         /      |      \
      Dev 1   Dev 2   Dev 3
       Local   Local   Local
       Repo    Repo    Repo
```

Each developer has:

* Code
* History
* Local repository

Therefore, developers can continue working even if the remote repository is temporarily unavailable.

When the connection is available again, repositories can be synchronized. 

### Example

**Git** is a distributed version control system.

---

## Advantages of Distributed VCS

1. Work can continue without internet.
2. Every developer has a copy of the code.
3. Every local repository contains history.
4. Changes can later be synchronized with the remote repository.

---

## Conclusion

VCS is very important in software development because it helps developers **collaborate, track changes, maintain versions and restore old code**.

### Easy memory:

> **VCS = Share + Version + Track + Retrieve**

---

# 2. Explain Git and Important Git Terminology

## Introduction

**Git** is a distributed version control system.

It allows multiple developers to work on the same project while maintaining the history of changes.

Git stores changes as **commits**, which can later be tracked and retrieved. 

---

# Important Git Terms

## 1. Repository

A **repository** is the storage area where source code is tracked and versioned.

There are two important repositories:

* Local repository
* Remote repository

---

## 2. Clone

**Clone** means creating a local copy of a remote repository.

Example:

```bash
git clone <url>
```

### Easy meaning:

**Clone = Remote → Local**

---

## 3. Commit

A **commit** represents a saved change.

The changes are stored in the local repository.

Each commit has a unique identifier called **SHA-1**.

Example:

```bash
git commit -m "Add login feature"
```

### Easy meaning:

**Commit = Save changes**

---

## 4. Branch

A **branch** is a separate line of development.

Developers can work on a branch without directly affecting the main branch.

For example:

```text
main
  |
  ├── feature-login
  └── feature-payment
```

After completing the work, branches can be merged.

---

## 5. Merge

**Merge** combines changes from one branch into another.

Example:

```bash
git merge feature-login
```

### Easy meaning:

**Merge = Combine branches**

---

## 6. Checkout / Switch

It allows developers to move from one branch to another.

Example:

```bash
git switch feature-login
```

---

## 7. Fetch

Fetch downloads changes from the remote repository **without merging them** into the local branch.

```bash
git fetch
```

### Easy meaning:

**Fetch = Download, but don't merge**

---

## 8. Pull

Pull updates the local repository with changes from the remote repository.

A pull is equivalent to:

**Fetch + Merge**

```bash
git pull
```

---

## 9. Push

Push uploads local commits to the remote repository.

```bash
git push
```

### Easy memory:

**Pull = Remote → Local**

**Push = Local → Remote**

---

## 10. Pull Request

A **Pull Request (PR)** is used to propose and discuss changes before they are integrated into the main branch.

It provides a web/GUI interface for discussing proposed changes with team members. 

---

## Quick Revision Table

| Term         | Easy Meaning              |
| ------------ | ------------------------- |
| Repository   | Storage of code           |
| Clone        | Remote → Local copy       |
| Commit       | Save changes              |
| Branch       | Separate development line |
| Merge        | Combine branches          |
| Switch       | Change branch             |
| Fetch        | Download remote changes   |
| Pull         | Fetch + Merge             |
| Push         | Local → Remote            |
| Pull Request | Discuss/propose changes   |

---

# 3. Explain Important Git Commands with Examples

This is a **very important practical 15-mark question**.

## 1. `git init`

Creates a new Git repository.

```bash
git init
```

### Meaning:

**Initialize Git in the current folder.**

---

## 2. `git clone`

Copies an existing remote repository.

```bash
git clone <url>
```

Example:

```bash
git clone https://github.com/user/repo.git
```

---

## 3. `git status`

Shows the current status of files.

```bash
git status
```

It shows:

* Changed files
* Staged files
* Untracked files

---

## 4. `git add`

Stages a file for the next commit.

```bash
git add file.txt
```

To stage all files:

```bash
git add .
```

---

## 5. `git commit`

Saves staged changes.

```bash
git commit -m "First Commit"
```

---

## 6. `git log`

Displays commit history.

```bash
git log
```

---

## 7. `git branch`

Lists branches.

```bash
git branch
```

---

## 8. `git switch`

Switches to another branch.

```bash
git switch main
```

To create and switch to a new branch:

```bash
git switch -c feature-login
```

---

## 9. `git merge`

Merges another branch into the current branch.

```bash
git merge feature-login
```

---

## 10. `git pull`

Fetches and merges changes from the remote repository.

```bash
git pull
```

---

## 11. `git fetch`

Downloads remote changes without merging them.

```bash
git fetch
```

---

## 12. `git push`

Uploads local commits to the remote repository.

```bash
git push
```

---

## 13. `git remote -v`

Displays remote repository URLs.

```bash
git remote -v
```

---

## 14. `git stash`

Temporarily saves uncommitted work.

```bash
git stash
```

---

## 15. `git restore`

Discards local changes in a file.

```bash
git restore file.txt
```

These commands and their purposes are listed in the module PPT. 

---

# Complete Basic Git Workflow

Remember this sequence:

```text
git init
   ↓
git add .
   ↓
git commit -m "message"
   ↓
git push
```

For an existing repository:

```text
git clone
   ↓
git switch -c feature
   ↓
git add .
   ↓
git commit
   ↓
git push
```

The PPT's example follows this basic workflow. 

---

# 4. Explain the Git Process / Git Workflow

## Introduction

Git allows multiple developers to work on the same project.

The basic process involves:

**Local Repository ↔ Remote Repository**

The module describes a workflow where one developer pushes code, another developer retrieves and modifies it, and the updated version is pushed back. 

---

## Step 1: First Developer Commits Code

The first developer writes code and saves the changes as a commit in the local repository.

```text
Developer 1
     ↓
   Code
     ↓
  Commit
     ↓
Local Repository
```

---

## Step 2: Push to Remote Repository

The developer pushes the code to the remote repository.

```text
Local Repository
       ↓
     push
       ↓
Remote Repository
```

---

## Step 3: Second Developer Gets the Code

The second developer retrieves the code from the remote repository.

```text
Remote Repository
       ↓
     pull
       ↓
Developer 2
```

---

## Step 4: Second Developer Updates Code

The second developer makes changes and creates a new commit.

```text
Developer 2
     ↓
Modify Code
     ↓
 Commit
```

---

## Step 5: Push Updated Code

The second developer pushes the new version to the remote repository.

```text
Developer 2
     ↓
   Push
     ↓
Remote Repository
```

---

## Step 6: First Developer Retrieves Latest Version

The first developer pulls the latest version.

```text
Remote Repository
       ↓
      Pull
       ↓
Developer 1
```

---

## Complete Diagram

```text
       DEVELOPER 1
           |
        Commit
           |
        Push ↓
    ┌──────────────┐
    │    REMOTE    │
    │  REPOSITORY  │
    └──────────────┘
        ↓       ↑
      Pull     Push
        ↓       ↑
   DEVELOPER 2
        |
     Modify
        |
     Commit
```

---

## Why Git Workflow is Useful

1. Multiple developers can work together.
2. Changes are tracked.
3. Previous versions can be retrieved.
4. Developers can work independently.
5. Changes can be synchronized through remote repositories.

---

# 5. Explain Branching and Gitflow Strategy

## Introduction

A **branch** is a separate line of development.

Branches allow developers to work on features without directly affecting the main production code.

Gitflow is a branching strategy that organizes development using different branches.

---

# Gitflow Branches

The important branches are:

1. **Master/Main**
2. **Develop**
3. **Feature**
4. **Release**
5. **Hotfix**

---

# 1. Master Branch

The **master branch** contains the code currently in production.

According to the PPT:

* It contains production code.
* Developers do not directly work on it. 

```text
MASTER
Production Code
```

---

# 2. Develop Branch

The develop branch contains changes that are planned for the **next delivery**.

It is created from the master branch.

```text
Master
   ↓
Develop
```

---

# 3. Feature Branch

For each new functionality, a feature branch is created from the develop branch.

Example:

```text
develop
   |
   ├── feature/login
   ├── feature/payment
   └── feature/profile
```

Developers work on these branches independently.

After completing a feature, it is merged back into develop. 

---

# 4. Release Branch

When the latest features are ready for deployment, a **release branch** is created from develop.

```text
develop
   ↓
release
```

The release branch is deployed through different environments.

---

# 5. Hotfix Branch

If a bug is found in production, a **hotfix branch** is created.

Example:

```text
master
   ↓
hotfix/login-bug
```

After fixing the bug, the hotfix is merged into:

* Master
* Develop

This ensures that the fix is available in both production and future development. 

---

# Gitflow Diagram

Draw this in the exam:

```text
                    ┌───────────────┐
                    │     MASTER    │
                    │  Production  │
                    └───────┬───────┘
                            ↓
                       ┌─────────┐
                       │ DEVELOP │
                       └────┬────┘
                            ↓
              ┌─────────────┼─────────────┐
              ↓             ↓             ↓
        feature/login  feature/payment  feature/profile
              \             |             /
               \            |            /
                └──────→ DEVELOP ←──────┘
                            ↓
                         RELEASE
                            ↓
                         MASTER
                            ↓
                       PRODUCTION

Production Bug
      ↓
   HOTFIX
      ↓
MASTER + DEVELOP
```

---

# Gitflow Process

### Step 1

Master contains production code.

### Step 2

Create develop from master.

### Step 3

Create feature branches from develop.

### Step 4

Complete features and merge them into develop.

### Step 5

Create release branch from develop.

### Step 6

Deploy release through environments.

### Step 7

After production deployment, merge release into master.

### Step 8

If a production bug occurs, create a hotfix branch and merge the fix into master and develop.

This sequence is directly described in the PPT. 

---

# 6. Explain Centralized and Distributed VCS and Compare Them

## Centralized VCS

In centralized VCS, all developers depend on a **central server**.

```text
       CENTRAL SERVER
       /      |      \
     Dev1    Dev2    Dev3
```

Examples:

* SVN
* CVS
* TFVC
* VSS

### Advantages

* Central code storage
* Easy collaboration
* Central backup

### Disadvantages

* Network dependency
* Server failure can affect development
* Code/history may be unavailable if the server is lost. 

---

## Distributed VCS

In distributed VCS, each developer has a **complete local repository**.

```text
         REMOTE
        REPOSITORY
       /    |    \
     Dev1  Dev2  Dev3
     Local Local Local
     Repo  Repo  Repo
```

Git follows this model.

### Advantages

* Can work without remote connection.
* Local history is available.
* Changes can be synchronized later.
* Each developer has a copy of the repository. 

---

## Difference

| Centralized VCS                   | Distributed VCS                     |
| --------------------------------- | ----------------------------------- |
| Central server is important       | Each developer has local repository |
| Code mainly stored centrally      | Code and history available locally  |
| Network dependency is higher      | Can work offline                    |
| Server failure is a major problem | Local copy provides backup          |
| Example: SVN                      | Example: Git                        |

### Easy memory

**Centralized = One main server**

**Distributed = Everyone has a copy**

---

# ⭐ MOST IMPORTANT LAST-MINUTE REVISION

If you have very little time, concentrate on these **5 questions first**:

### ⭐ 1. VCS and Types

Remember:

> **VCS = Track + Version + Collaborate + Retrieve**

Types:

> **Centralized + Distributed**

---

### ⭐ 2. Git Terminology

Remember:

> **Repository → Clone → Add → Commit → Push → Pull**

And:

> **Branch → Merge → Fetch → Pull Request**

---

### ⭐ 3. Git Commands

Memorize this:

```bash
git init
git clone <url>
git status
git add .
git commit -m "message"
git log
git branch
git switch <branch>
git merge <branch>
git pull
git fetch
git push
git remote -v
git stash
git restore <file>
```

The PPT explicitly lists these commands and their functions. 

---

### ⭐ 4. Git Workflow

```text
Code
 ↓
Add
 ↓
Commit
 ↓
Push
 ↓
Remote Repository
 ↓
Pull
 ↓
Modify
 ↓
Commit
 ↓
Push
```

---

### ⭐ 5. Gitflow

Remember:

> **Master → Develop → Feature → Release → Master**

For production bugs:

> **Master → Hotfix → Master + Develop**

---

## 🧠 One-Minute Memory Map

```text
                    GIT
                     |
          ┌──────────┼──────────┐
          ↓          ↓          ↓
         VCS       COMMANDS    GITFLOW
          |          |          |
     Centralized    init       Master
     Distributed    add        Develop
                    commit     Feature
                    push       Release
                    pull       Hotfix
                    fetch
                    merge
```

If you can remember this **one map + the diagrams**, you can expand each point into a strong **15-mark answer** during the internal.
