# new-project

## 📌 Purpose

This repository was created as part of Jira ticket **PROM-42164**.

The purpose of this project is to demonstrate how to:
- create a new Git repository
- work with branches using Git
- use a development branch for changes
- commit changes using Smart Commit format
- merge changes into the main branch

This README contains **step-by-step instructions** so that anyone can reproduce the same setup independently.

---

## 🛠️ Step-by-Step Instructions

### 1. Create a new project directory

```bash
mkdir new-project
cd new-project
```
This command creates a new folder for the project and navigates into it.

### 2. Initialize a Git repository
```bash
git init
```
This initializes an empty Git repository in the new-project directory.

### 3. Set the main branch name
```bash
git branch -M main
```

This ensures that the default branch is named main, which is the current Git best practice.

### 4. Create the README.md file
```bash
echo "# new-project" > README.md
```
This creates the README.md file, which is required for project documentation.

### 5. Stage and commit initial changes
```bash
git add README.md
git commit -m "init"
```

git add stages the file

git commit saves the changes to the repository history

## Development Branch Workflow
### 6. Create and switch to the development branch
```bash
git checkout -b development
```

### 7. Update README.md with instructions

Edit the README.md file and add detailed instructions (this document).

After editing, stage and commit the changes using Smart Commit format:
```bash
git add README.md
git commit -m "PROM-42164 #comment Add step-by-step instructions to README"
```

This commit message follows Jira Smart Commit rules and links the commit to the Jira ticket.


Merge Changes into Main
### 8. Switch back to the main branch
```bash
git checkout main
```
### 9. Merge development branch into main
```bash
git merge development
```
This merges all completed changes from the development branch into the main branch.

Verification
### 10. Verify repository status
```bash
git status
```
Expected output:
nothing to commit, working tree clean

This confirms that all changes have been committed successfully.

Push Repository to GitHub
### 11. Add remote repository
```bash
git remote add origin https://github.com/RusMar/new-project.git
```
### 12. Push branches to GitHub
```bash
git push -u origin main
git push origin development
```
This publishes both the main and development branches to GitHub.  

