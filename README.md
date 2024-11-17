# **Git Cheat Sheet - Commands Detailed Explanations and Common Workflows**

---

## **Basic Commands**

### **1. `git init`**

**Usage**:

```bash
git init

```

- Initializes a new Git repository in the current directory.
- Creates a `.git` directory to store Git history and metadata.

---

### **2. `git clone`**

**Usage**:

```bash
git clone <repository-url>

```

- Copies an existing repository from a remote source (e.g., GitHub) to your local machine.

---

### **3. `git add`**

**Usage**:

```bash
git add <file>
git add .

```

- Stages changes to be included in the next commit.
- Use `git add .` to stage all changes in the current directory.

---

### **4. `git commit`**

**Usage**:

```bash
git commit -m "Your message here"

```

- Saves staged changes as a snapshot in the repository.
- The `m` option allows adding a commit message directly.

---

### **5. `git status`**

**Usage**:

```bash
git status

```

- Displays the current state of the working directory and staging area.
- Shows tracked, untracked, and staged files.

---

### **6. `git log`**

**Usage**:

```bash
git log
git log --oneline --graph --all

```

- Lists the commit history for the repository.
- Use flags like `-oneline`, `-graph`, and `-all` for a concise and visual history.

---

### **7. `git branch`**

**Usage**:

```bash
git branch
git branch <branch-name>

```

- Lists all branches (`git branch`).
- Creates a new branch (`git branch <branch-name>`).

---

### **8. `git checkout`** (or `git switch`)

**Usage**:

```bash
git checkout <branch-name>
git checkout -- <file>

```

- Switches to the specified branch.
- Reverts changes in a file to the last committed state with `- <file>`.

---

### **9. `git merge`**

**Usage**:

```bash
git merge <branch-name>

```

- Merges the specified branch into the current branch.
- Resolves any conflicts during the merge.

---

### **10. `git pull`**

**Usage**:

```bash
git pull
git pull origin main

```

- Fetches and integrates changes from the remote repository into the current branch.

---

### **11. `git push`**

**Usage**:

```bash
git push
git push origin <branch-name>

```

- Uploads local commits to the remote repository.

---

## **Undoing Changes**

### **12. `git reset`**

**Usage**:

```bash
git reset <file>
git reset --hard <commit>

```

- Unstages files or resets the repository to a previous state.
- Use `-hard` to discard all changes.

---

### **13. `git revert`**

**Usage**:

```bash
git revert <commit>

```

- Creates a new commit that undoes the changes made by a specific commit.

---

### **14. `git stash`**

**Usage**:

```bash
git stash
git stash apply

```

- Temporarily saves changes that are not ready to commit.
- Apply the stashed changes later.

---

## **Remote Repository Commands**

### **15. `git remote`**

**Usage**:

```bash
git remote add origin <url>

```

- Adds a remote repository.
- Use `git remote -v` to view remotes.

---

### **16. `git fetch`**

**Usage**:

```bash
git fetch

```

- Downloads updates from the remote repository but does not integrate them.

---

### **17. `git tag`**

**Usage**:

```bash
git tag <tag-name>
git tag

```

- Adds a tag to mark a specific commit.
- List all tags with `git tag`.

---

## **Advanced Commands**

### **18. `git rebase`**

**Usage**:

```bash
git rebase <branch-name>

```

- Reapplies commits on top of another base branch.
- Helps maintain a clean commit history.

---

### **19. `git cherry-pick`**

**Usage**:

```bash
git cherry-pick <commit>

```

- Applies changes from a specific commit to the current branch.

---

### **20. `git bisect`**

**Usage**:

```bash
git bisect start
git bisect bad
git bisect good <commit>

```

- Finds the commit that introduced a bug using binary search.

---

## **Common Workflows**

### **1. Basic Workflow**

```bash
# Initialize a repository
git init

# Add and commit changes
git add .
git commit -m "Initial commit"

# Push to a remote repository
git remote add origin <url>
git push -u origin main

```

---

### **2. Feature Branch Workflow**

```bash
# Create and switch to a feature branch
git checkout -b feature-branch

# Make changes and commit
git add .
git commit -m "Add new feature"

# Push feature branch
git push origin feature-branch

# Merge into main
git checkout main
git merge feature-branch

```

---

### **3. Undo Committed Changes**

```bash
# Reset to a previous commit (soft keeps changes, hard discards them)
git reset --soft <commit>
git reset --hard <commit>

```

---

### **4. Collaborating on a Project**

```bash
# Clone repository
git clone <url>

# Create a new branch for your work
git checkout -b my-branch

# Make changes, commit, and push
git add .
git commit -m "My changes"
git push origin my-branch

# Submit a pull request on GitHub

```

---

### **5. Resolving Merge Conflicts**

```bash
# Merge a branch with conflicts
git merge feature-branch

# Edit conflicting files to resolve conflicts

# Mark conflicts as resolved and commit
git add <resolved-files>
git commit

```

---

### **6. Squash Commits**

```bash
# Rebase to squash multiple commits into one
git rebase -i HEAD~<number-of-commits>

```

---
