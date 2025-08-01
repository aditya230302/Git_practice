# **🚀 Git & Linux Basics (Quick Guide)**

---

## **1. What is Git?**

> **Git** is a **distributed version control system (DVCS)** used to manage source code history efficiently.

* **Free & Open-source**: Available for everyone.
* **Collaboration**: Multiple developers can work on the same project.
* **Tracks Changes**: Maintains history of changes to files.
* **Offline Support**: Work even without internet (unlike centralized systems).

---

## **2. Types of Version Control Systems (VCS)**

### **2.1 Local Version Control System (LVCS)**

* Stores changes **only on your machine**.
* **No collaboration** support.
* Example: `RCS (Revision Control System)`

---

### **2.2 Centralized Version Control System (CVCS)**

* All files stored in a **central server**.
* Requires **active internet connection**.
* **Single point of failure** (if server is down → work stops).
* Example: `SVN (Apache Subversion)`

```
[ Developer 1 ]  ↘  
[ Developer 2 ]  →  [ Central Server ]  
[ Developer 3 ]  ↗  
```

---

### **2.3 Distributed Version Control System (DVCS)**

* **Every developer has a full copy** of the repository.
* **Work offline** and sync later.
* **Better backup & reliability**.
* Examples: `Git`, `Mercurial`.

```
[ Dev 1 Repo ]    [ Dev 2 Repo ]    [ Dev 3 Repo ]
        \              |               /
                  [ Remote Repo ]
```

---

## **3. Key Features of Git**

* **Fast & Lightweight** – Very quick operations.
* **Branching & Merging** – Create multiple branches & merge them easily.
* **Data Integrity** – Ensures secure & consistent data storage.

---

# **Linux Basics for Git Users**

| **Command**          | **Description**             | **Example**                   |
| -------------------- | --------------------------- | ----------------------------- |
| `ls`                 | List files & directories    | `ls -l`                       |
| `cd <dir>`           | Change directory            | `cd projects`                 |
| `mkdir <dir>`        | Create a new directory      | `mkdir git_project`           |
| `touch <file>`       | Create an empty file        | `touch readme.md`             |
| `nano <file>`        | Open a file in Nano editor  | `nano readme.md`              |
| `vi <file>`          | Open a file in Vi editor    | `vi readme.md`                |
| `cat <file>`         | Display file contents       | `cat readme.md`               |
| `pwd`                | Show current directory path | `pwd`                         |
| `echo "text" > file` | Create/edit file with text  | `echo "Hello Git" > note.txt` |

**Nano Shortcuts:**

* **Ctrl + S** → Save
* **Ctrl + X** → Exit

**Vi Shortcuts:**

* Press **i** → Insert mode
* Press **Esc** → Exit insert mode
* Type **:wq** → Save & quit

---

# **Git Commands with Examples**

## **Initializing a Repo**

```bash
git init
```

Creates a **new Git repository** in your project folder.

---

## **Tracking Changes**

```bash
git status
```

Shows current status (**tracked / untracked** files).

```bash
git add filename.txt
```

Moves file to **staging area**.

```bash
git rm --cached filename.txt
```

Removes file from staging (back to untracked).

---

## **Committing Changes**

```bash
git commit -m "Added new feature"
```

Saves changes permanently in Git history.

---

## **Configuring User**

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## **Branching & Switching**

```bash
git branch          # List branches
git branch feature  # Create new branch
git checkout feature # Switch to branch
git checkout -b new_feature # Create + switch
git branch -m old new # Rename branch
```

---

## **Working with Remote Repos**

```bash
git remote add origin https://github.com/user/repo.git
git pull origin main     # Pull latest changes
git fetch                # Download changes (don’t merge)
git clone <RepoURL>      # Clone repo
```

---

## **Stashing (Temporary Hide Changes)**

```bash
git stash -u       # Stash untracked files
git stash pop      # Retrieve stashed changes
```

---

## **Merging Branches**

```bash
git merge feature
```

Merges **feature branch** into current branch.

---

## **Viewing Commit History**

```bash
git log
git log --oneline
git log --graph
```

---

## **Forking**

> **Forking** means creating a **copy** of someone else’s repository on your GitHub account to experiment or contribute.

---

# **Visual Flow of Git Workflow**

```
Untracked  →  Staged  →  Committed  →  Pushed to Remote
```

**Commands Sequence:**

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo-url>
git push -u origin main
```

---

# **Mini Hands-on Example**

```bash
mkdir myproject
cd myproject
git init
echo "Hello Git" > readme.md
git add readme.md
git commit -m "Initial commit"
git remote add origin https://github.com/username/myproject.git
git push -u origin main
```

---
