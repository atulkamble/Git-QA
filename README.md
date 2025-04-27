Awesome! 🚀  **complete guide** — including **Scenario-Based Git Interview Questions** at the end!

---

# 🚀 Git Interview Q&A (Updated)

### 1. **What is Git?**
> Git is a **distributed version control system** used to track code changes and collaborate across developers.

---

### 2. **Difference between Git and GitHub?**
> Git → tool for version control.  
> GitHub → cloud-based hosting for Git repositories.

---

### 3. **Explain Git workflow.**
> Working Directory → Staging Area → Local Repository → Remote Repository

---

### 4. **What is a Git branch?**
> A branch is an independent line of development in your project.

---

### 5. **How do you resolve a merge conflict?**
> Identify conflicts → manually edit conflicting files → `git add` → `git commit`

---

### 6. **Difference: Git Merge vs Git Rebase?**
> - **Merge**: combines commits, maintains history (good for teamwork).  
> - **Rebase**: re-writes history, makes linear clean history (good for solo work).

---

### 7. **What are Git hooks?**
> Git hooks are **scripts** triggered before or after Git events (like commit, push).

---

### 8. **Explain Git stash.**
> Temporary storage for uncommitted work.

```bash
git stash
git stash pop
```

---

### 9. **How to undo the last Git commit?**
- Keep changes: `git reset --soft HEAD~1`
- Remove changes: `git reset --hard HEAD~1`

---

### 10. **What is .gitignore?**
> File to specify untracked files Git should ignore.

---

# 🛠️ Git Practical Codes / Commands

| Action | Command |
|:-------|:--------|
| Initialize Repo | `git init` |
| Stage Files | `git add .` |
| Commit | `git commit -m "message"` |
| Create Branch | `git branch feature-1` |
| Switch Branch | `git checkout feature-1` |
| Merge Branch | `git merge feature-1` |
| Clone Repo | `git clone <url>` |
| Push Branch | `git push origin feature-1` |
| Pull Changes | `git pull origin main` |
| View Log | `git log --oneline --graph --all` |
| Delete Branch | `git branch -d branch-name` |
| Set Remote URL | `git remote add origin <url>` |

---

# 📚 Git Tutorials (Free Resources)

| Resource | Link |
|:--------|:----|
| Git Official Docs | [git-scm.com/doc](https://git-scm.com/doc) |
| GitHub Git Guides | [github.com/git-guides](https://github.com/git-guides) |
| Git Crash Course (FreeCodeCamp Video) | [YouTube](https://www.youtube.com/watch?v=SWYqp7iY_Tc) |
| Atlassian Git Tutorials | [atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials) |
| Learn Git Branching (Interactive) | [learngitbranching.js.org](https://learngitbranching.js.org/) |

---

# 🎯 Scenario-Based Git Interview Questions

---

### 1. **You committed to the wrong branch. What will you do?**
> - Create a new branch: `git checkout -b correct-branch`  
> - Cherry-pick the commit: `git cherry-pick <commit-hash>`  
> - Or:  
>   - `git reset HEAD~1` (undo commit)
>   - Switch to correct branch
>   - Commit again

---

### 2. **You did `git pull` and now there are conflicts. What next?**
> - Run `git status` to see conflicted files.
> - Open conflicted files, manually resolve.
> - Stage them: `git add <file>`.
> - Commit the merge: `git commit`.

---

### 3. **You accidentally deleted a branch. How to recover it?**
> If you know the last commit ID:
```bash
git checkout -b branch-name <commit-id>
```
> Or use:
```bash
git reflog
```
> Find previous HEAD and restore it.

---

### 4. **Remote repository has commits missing locally. How will you sync?**
> Run:
```bash
git fetch
git rebase origin/main
```
> (or use `git pull --rebase` if needed)

---

### 5. **You pushed sensitive data (like passwords). What now?**
> - Immediately **delete** sensitive commits:
```bash
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch secret-file.txt" \
  --prune-empty --tag-name-filter cat -- --all
```
- Force push:
```bash
git push origin --force --all
```
- Rotate the compromised credentials.

---

### 6. **What happens if you push a merge conflict?**
> You *cannot* push if a merge conflict exists. Git will block the push until conflicts are resolved locally and committed.

---

### 7. **How to clean a messed-up working directory?**
```bash
git reset --hard
git clean -fd
```
> (Be careful: this will remove all untracked files and reset tracked files.)

---

### 8. **You made multiple local commits. Now you want to combine them.**
> Use **Interactive Rebase**:
```bash
git rebase -i HEAD~3
```
> Then mark previous commits as `squash` to combine them.

---

### 9. **How to switch to a specific commit (detached HEAD)?**
```bash
git checkout <commit-id>
```
> (You are now in detached state. Create a branch if you want to save changes.)

---

### 10. **Team member pushed directly to `main`. You want code reviews. What will you do?**
> - Create a protected branch rule on GitHub/GitLab.
> - Require Pull Requests (PRs) before merging to `main`.

---

# 🔥 Quick Mini Git Project Idea
- Make a **portfolio website**.
- Push it to GitHub.
- Deploy using **GitHub Pages**.

> I can also give you a sample GitHub repo structure if you want to **practice hands-on!** 🎯  

---

# ✅ Summary

| Section | Covered |
|:------|:--------|
| Core Git Interview Q&A | ✅ |
| Practical Git Codes/Commands | ✅ |
| Free Git Tutorials | ✅ |
| Scenario-Based Interview Questions | ✅ |
| Bonus Mini Project Idea | ✅ |

---
