
# AcademiaConnect App – Git Collaboration Workflow

Welcome to the **AcademiaConnect** repository. This document outlines the **branching strategy**, **workflow**, and **commands** each developer (Arijit, Abir, and Raheta) should follow to collaborate efficiently.

---

## 🚀 Overview

- `main`: Production-ready stable branch.
- `arijit`: Development branch for Arijit.
- `abir`: Development branch for Abir.
- `raheta`: Development branch for Raheta.

Each team member develops features or fixes in **their own branch** and submits **Pull Requests (PRs)** to merge into `main` after review.

---

## 🛠️ Initial Setup (Once per Member)

### ✅ Step 1: Clone the Repository
```bash
git clone https://github.com/aroyy007/AcademiaConnectApp.git
cd AcademiaConnectApp
```
✅ Step 2: Checkout Your Branch

For Arijit:
```bash
git checkout -b arijit origin/arijit
```
For Abir:
```bash
git checkout -b abir origin/abir
```
For Raheta:
```bash
git checkout -b raheta origin/raheta
```

---

🔁 Daily Workflow

✅ 1. Pull Latest main and Sync Your Branch

Arijit:
```bash
git checkout main
git pull origin main

git checkout arijit
git merge main
```
Abir:
```bash
git checkout main
git pull origin main

git checkout abir
git merge main
```
Raheta:
```bash
git checkout main
git pull origin main

git checkout raheta
git merge main
```
🧠 Tip: You can use git rebase main instead of merge for cleaner history.


---

✅ 2. Make Changes and Push

Arijit:
```bash
git add .
git commit -m "Arijit: Implemented login UI"
git push origin arijit
```
Abir:
```bash
git add .
git commit -m "Abir: Added course list screen"
git push origin abir
```
Raheta:
```bash
git add .
git commit -m "Raheta: Fixed schedule bug"
git push origin raheta
```

---

✅ 3. Create a Pull Request to main

Go to the GitHub repo.

Click "Compare & pull request".

Select base: main, compare: your branch (e.g., abir).

Add a meaningful title and description.

Assign reviewers (e.g., team lead).

After approval and conflict resolution, merge to main.



---

🔄 Staying Updated

Run this daily to avoid conflicts:
```bash
git checkout main
git pull origin main

git checkout your-branch
git merge main   # OR git rebase main
```

---

🔐 Protecting the main Branch (Maintainer)

Enable the following in GitHub:

Go to Settings > Branches > Branch protection rules.

Add rule for main:

✅ Require pull request before merging.

✅ Require review from at least one team member.

✅ Prevent force pushes and deletions.




---

📁 .gitignore (Example)

Make sure your .gitignore includes:
```bash
node_modules/
.env
.DS_Store
*.log
```

---

🙋 Questions / Help

If you’re stuck, ask in the group chat or open a GitHub issue.


---

✅ Final Notes

Don’t push directly to main.

Pull frequently to reduce merge conflicts.

Write clean, meaningful commit messages.

Use branches responsibly.

Review PRs with care.


