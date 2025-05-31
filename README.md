# Git Workflow Example: Tom and Jerry

This project demonstrates a simple Git version control workflow using two developers, Tom and Jerry. The guide shows how to set up Git, create branches, make changes, and merge them using pull requests (PRs).

---

## 🛠 Initial Setup

1. Both Tom and Jerry have Git installed on their computers.
2. They clone the project repository from a central source (GitHub).
   ```bash
   git clone https://github.com/adaezeokoduwa/git-version-control.git
[Tom clone](./imgs/Tom%20clone.png)

[jerry clone](./imgs/Jerry%20clone1.png)

   ## Tom and Jerry Start Working

3. Both developers pull the latest version of the repository to ensure they have the current `index.html` file.

## 👨‍💻 Working on the Project

### 1. 📥 Pulling Latest Changes

Tom and Jerry begin by pulling the latest version of the project from the remote repository.  
This ensures they both have the most recent version of all files, especially `index.html`.

```bash
git pull origin main 

```

### 2. 🌿 Creating Feature Branches

To work independently without affecting the main codebase, each developer creates their own feature branch:

- **Tom's branch:** `update-navigation`  
- **Jerry's branch:** `add-contact-info` 

# Tom
git checkout -b update-navigation

# Jerry
git checkout -b add-contact-info
[tom new branch](./imgs/Tom%20new%20branch.png)
[jerry new branch](./imgs/jerry%20new%20branch.png)

### 3. ✏️ Making Changes

Each developer makes edits to the `index.html` file:

- **Tom** updates the **navigation bar**.
- **Jerry** adds **contact information** to the **footer**.

Once their changes are complete, they stage and commit the updates with clear, descriptive messages.
# Tom
git add index.html
git commit -m "added navigation bar"
[tom makes changes](./imgs/tom%20make%20changes.png)

# Jerry
git add index.html
git commit -m "Added contact info"
[jerry makes changes](./imgs/Jerry%20make%20changes.png)


## 🔀 Merging Changes

### Step 1: 🚀 Push Branches to Remote

After making and committing their changes locally, both Tom and Jerry push their feature branches to the remote repository:

```bash
git push origin update-navigation
git push origin add-contact-info

```
### Step 2: 📥 Creating Pull Requests

- **Tom** creates a **Pull Request (PR)** from the `update-navigation` branch to the `main` branch.
- The team reviews **Tom’s PR** and merges it into the `main` branch after approval.
[tom merged changes](./imgs/Tom%20merged.png)


### Step 3: 🔄 Sync Jerry's Branch

After Tom's changes have been merged into the `main` branch, **Jerry** updates his local branch to include the latest changes:

```bash
git checkout add-contact-info
git pull origin main

```
### Step 4: ✅ Final Merge

- **Jerry** pushes the updated branch to the remote:

```bash
git push origin add-contact-info

```
[jerry merged changes](./imgs/jerry%20%20merged.png)