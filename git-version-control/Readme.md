
#  Git 
This is my personal journey of learning Git — making mistakes, and fixing them.

💻 What is Git?

Git is a version control system — it helps you track changes in your code or project over time.

Think of Git as a time machine for your code:

It remembers every version.

You can go back to any point.

You can work on features without breaking the main code.

It’s especially useful when working with teams.



## 📍 Step 1: Start Tracking the Project

```bash
git init
````

This creates a hidden `.git/` folder. Now Git will track all changes in this project folder.

---

## 📂 Step 2: Add Files to Staging Area

### Concept:

Your changes live in the **Working Directory**. You use `git add` to send them to the **Staging Area**.

```bash
git add file2.txt file3.txt
```

Or to add everything:

```bash
git add .
```

---

## 📝 Step 3: Commit Changes to Repository

### Concept:

Now files in staging area are ready to be saved permanently in Git (repository).

```bash
git commit -m "initial project setup done"
```

This creates the first version (commit) of the project.

---

## 🔄 Step 4: Making Changes and Recommitting

If you edit `file.txt` or `file3.txt`, it’s again in the **Working Directory**. Git knows it changed:

```bash
git status
```

To update the changes:

```bash
git add .
git commit -m "updated file.txt and file3.txt"
```

This creates the next version of the project.

---

## 📜 Step 5: View Commit History

```bash
git log
```

To view shorter version with commit IDs:

```bash
git log --oneline
```

Sample output:

```
effe1e6 done
71f62f6 initial project setup done
```

These commit IDs help you go back to any version later.

---

## 🗑️ Step 6: Delete a File (and Track It)

If you delete `file2.txt` manually, Git sees that as a change in the Working Directory.

To stage that deletion:

```bash
git add file2.txt
```

Then commit:

```bash
git commit -m "file2 has been deleted"
```

Now this deletion is part of Git history — just like adding.

---

##  Step 7: Ignore Unwanted Files with `.gitignore`

Some files (like `__pycache__/`, virtualenv folders, `.log`, etc.) shouldn't be pushed to GitHub.

So I created a `.gitignore` file and added:

```
tasks_env/
__pycache__/
*.log
db.sqlite3
```

> ⚠️ Important: `.gitignore` must be set **before** adding files.
> If already added, untrack using:

```bash
git rm --cached filename
```

---

## 🚀 Final Step: Push to GitHub

### Setup GitHub Remote

Rename the default branch if needed:

```bash
git branch -M main
```

Add GitHub repo:

```bash
git remote add origin https://github.com/nosratee-jahan-naba/task-management.git
```

Push the code:

```bash
git push -u origin main
```

Everything uploads!

---


## 💡 Git Concept Recap 

Git is a version control system that tracks changes in your code/project over time.

It helps you save versions, go back, and collaborate with others.

Mostly used with GitHub for sharing code online.

🔧 Common Git Commands:

git init → Start tracking a project.
git add . → Stage all changes.
git commit -m "msg" → Save a version (commit).
git status → Show current file changes.
git log → View commit history.
git branch -M main → Rename branch to main.
git remote add origin <url> → Connect to GitHub repo.
git push -u origin main → Push project to GitHub.

⏳ Git = Time Machine for Code

Git saves every version of your project.

You can go back to any previous version anytime.

It’s like creating checkpoints while coding.

If something breaks, just rewind to a working state.

👉 That’s why developers say:

"Git is a time machine for your code."



## Git Branching
To see bracnh list
```bash
git branch
```

output:
* main
feature-x
develop


*main-> we are in main branch 

To create a new branch
```bash
git branch branch_name
```

ex:git branch feature-xyz

branch switch
```bash
git checkout branch_name
```

## Git merging

1.git checkout des-branch
```bash
git checkout main
```

2.git merge src-branch
```bash
git merge feature-xyz
```

## Git clone
remote repo clone
```bash
git clone <repository_url>
```

## Going back to a specific commit

git checkout commit_id

```bash
   $ git log --oneline
```
8935cc7 (HEAD -> main, origin/main) done
e9ee65a git version control

```bash
git checkout 8935cc7
```

## Git restore

```bash
git restore --source=main .
```

