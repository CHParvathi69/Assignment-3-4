#### Git Assignment 3 ----- ----- 4

## 📘 Assignment 3: 
Branching Strategies & Merge Conflicts

# # ### 🛠️ Steps followed:

1. **Initialized a GitHub repository with an HTML project.**
```bash
git init
echo "<!DOCTYPE html>
<html>
<head>
 <title> Merge Conflict </title>
</head>
<body>
 <h1>Hello Minfy</h1>
 <p>Welcome to Hyderabad</p>
</body>
</html>" > Basic.html
git add.
git commit -m "Basic HTML"
git remote add origin https://github.com/CHParvathi69/Assignment-3-4.git
git branch -M main
git push -u origin main
```

2. **Created two feature branches from `main`:**
   - `short-hyd`: Modified the paragraph.
   - `add-sec`: Added new info to the same paragraph line.
```bash
git checkout -b short-hyd
# (Make edits to Basic.html)
git add.
git commit -m "changed to short-hyd"
git push origin short-hyd

git checkout main
git checkout -b add-sec
# (Make edits to Basic.html)
git add.
git commit -m "Added secunderabad"
Git push origin add-sec
```

3. **Both branches changed the same line in `Basic.html` (`<p>` tag), resulting in a conflict.**
   - In `short-hyd`, the paragraph : `<p>Welcome to Hyd</p>`
   - In `add-sec`, the paragraph: `<p>Welcome to Hyderabad-Secunderabad</p>`

4. **Merged one branch successfully.**
   - Merged the `short-hyd` branch.

5. Got a merge conflict while merging the second branch.**
   - GitHub raised the merge conflict in `Basic.html`.

6. **Manually resolved the conflict by combining changes.**
```html
# Inside Basic.html after conflict markers
<<<<<<< HEAD
<p>Welcome to Hyd</p>
=======
<p>Welcome to Hyderabad-Secunderabad</p>
>>>>>>> add-sec

# Final resolution:
<p>Welcome to Hyderabd</p>
```

7. **Finalized the merge with both updates preserved.**
```bash
git add Basic.html
git commit -m "Resolved merge conflict in Basic.html"
git push origin main
```

### 📷 Screenshots

- Pull Request showing a merge conflict.
![Compare Changes]()
![Merge Conflict ]()

- Conflict resolution in progress.
![Resolved]()
![No Conflicts]()
- Final version after the merge.
![Merged]()
### 🔗 Repository Link

`https://github.com/CHParvathi69/Assignment-3-4.git`

---

# # ### 🧾 Final HTML Code

```html
<!DOCTYPE html>
<html>
<head>
  <title>Merge Conflict Demo</title>
</head>
<body>
  <h1>Hello Minfy</h1>
  <p>Welcome to Hyderabad</p>
</body>
</html>
```

---



# Assignment 4: Git Hooks & Automation

## Objective

This assignment helped me understand how automation can be integrated into the Git workflow to maintain code quality and consistency. It introduced tools like Husky, lint-staged, commitlint, and GitHub Actions, which are commonly used in real-world development setups.


### 🔹 Git Hooks & Husky
I learned that **Git hooks** are scripts that run automatically at different points in the Git lifecycle (like before committing or pushing code). **Husky** is a tool that makes it easier to manage these hooks directly from the project.

### 🔹 Linting & Formatting
Tools like **ESLint** (for JavaScript) help catch coding errors and enforce code standards. **Prettier** is used for consistent formatting. I learned that using these tools before committing code can prevent issues from reaching the main codebase.

### 🔹 lint-staged
**lint-staged** allows running linters only on files that are staged for commit. This saves time and makes pre-commit checks more efficient.

# # ### 🔹 Commit Message Validation
I explored **commitlint**, which ensures that commit messages follow a specific format (like the conventional commit style). This makes commit history easier to read and automate in CI/CD pipelines.

# # ### 🔹 GitHub Actions
**GitHub Actions** enables automation on GitHub. I learned how it can be used to run tests, linters, or any script automatically when code is pushed to a repository or a pull request is created.

## Thoughts on Automation

Automation brings a lot of benefits, especially in team projects:
- It helps catch mistakes early.
- Enforces coding standards consistently.
- Saves time by reducing manual checks.
- Makes collaboration smoother by improving code quality.
