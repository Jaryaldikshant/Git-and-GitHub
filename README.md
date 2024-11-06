## **Version Control System (VCS)**

### **Definition:**
- Also known as **source control**
- Tracks and manages software code changes over time.

### **Famous VCS Examples:**
1. **Git**
2. **Apache Subversion**
3. **Piper** (used by Google)

---

## **Using Git**

- **Git** is a free and open-source distributed VCS, efficient for managing projects of any size.

### **Installation:**
- Download Git: [https://git-scm.com/downloads](https://git-scm.com/downloads)

### **Git CLI (Command Line Interface)**

#### **Global Configuration:**
1. Set global username: `git config --global user.name`
2. Set global email: `git config --global user.email`

---

## **Version Control using Git**

### **Creating a Git Project:**
1. **Initialize Git:**  
   - `git init`  
   - Initializes an empty Git repo in the current directory and creates a hidden `.git` folder containing project tracking data.

2. **View Hidden Folders:**  
   - `ls -force`  
   - Shows hidden folders/files in the current directory.

### **Tracking Project Files:**

1. **Add Files to Git:**  
   - Track specific files: `git add <file_name>`
   - Track files by path: `git add <file_path>`
   - Track all files: `git add .`

2. **Remove Files from Git:**  
   - `git rm <file_path>`

### **Tracking Code Changes Over Time**

- **Adding Files to Track Changes:**  
  - Use `git add <file_name>` for tracking updates.

- **Identifying Code Changes:**  
  - Green line: indicates added code.
  - Blue line: shows deleted or modified code.

3. **Check Changes:**  
   - View line-by-line changes: `git diff`

4. **Add All Changes:**  
   - `git add .`  
   - Adds all files at once, simplifying the tracking process.

---

## **Introduction to Commit**

- **Commit**: Saves code changes as a snapshot in Git.

### **Commit Commands:**
1. **Make a Commit:**  
   - `git commit -m "Message describing changes"`

2. **View Commit History:**  
   - `git log`

3. **View Code Changes in a Commit:**  
   - `git show`

4. **See Changes Made by Each Author:**  
   - `git blame <file_name>`

5. **Check Current State:**  
   - `git status`

---

## **Reverting Changes (Undoing Mistakes)**

- **Reverting** allows undoing mistakes.
- **Head**: Points to the latest commit.

### **Reset and Revert Commands:**
1. **Reset Head to Previous Commit:**  
   - `git reset --hard <commit_id>`  
   - Deletes commits after the specified commit.

2. **Revert Specific Changes in a File:**  
   - `git revert <commit_id>`

---

## **Git Collaboration**

- **Scenario**: Working on a project with teammates using Git as the VCS.
  
### **Using a Single Source of Truth:**
- A **Remote Server** is used to store the main project copy.
- Process:
  1. Each collaborator makes changes on their local machine.
  2. Changes are pushed to the remote server.
  3. The remote server ensures all collaborators have the latest code copy.

### **Git Servers:**
- **GitHub** (publicly available)
- **Other Git servers:** GitLab, Bitbucket

#### **Summary:**
1. Use Git locally to track changes.
2. Use a remote server (e.g., GitHub) for the central code version.
3. Push changes to the remote server, and teammates pull them to sync.

---

## **Introduction to GitHub**

### **Getting Started:**
1. **Sign Up** on GitHub.
2. **Create a Repository** and copy its URL.

### **Adding a Remote:**
- Link your local repo to the GitHub repo (name it "origin"):  
  - `git remote add origin <repo_URL>`

### **Push Changes to Main Branch:**
- `git push -u origin main`

### **SSH (Secure Shell):**  
- A secure protocol used for authentication when interacting with GitHub.

---

## **Branching in Git**

### **Why Use Branching?**
- Branches allow separate work areas in the project to avoid cluttering the main branch with every collaborator’s changes.
- Example: Use a **main branch** for the stable version of the code.

### **How Branches Work:**
- **Collaborators create new branches** from the latest commit (Head).
- Changes are pushed to the new branch.
- Once complete, changes are **merged** into the main branch, creating a single, summarized commit.

### **Branch Commands:**
1. **Create a New Branch:**  
   - `git branch <branch_name>`

2. **Switch Between Branches:**  
   - `git checkout <branch_name>`

3. **Push a Branch to Remote:**  
   - `git push --set-upstream origin <branch_name>`

4. **Merge Branches:**  
   - `git merge origin/<branch_name>`

---

