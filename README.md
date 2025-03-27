# git-setup-notes-CLI
Personal reference guide for Git and GitHub basics

# 🚀 Getting Started with GitHub Using CLI (Windows)

This is a complete beginner-friendly guide to help you use GitHub entirely from the command line (CLI) on Windows. It includes:
- Installing GitHub CLI
- Creating a GitHub account
- Creating and pushing code to a GitHub repository

---

## 🧑‍💻 1. Create a GitHub Account
If you don’t have a GitHub account yet:
1. Go to https://github.com
2. Click **Sign up**
3. Fill in your email, password, and username
4. Verify your email

✅ Done! You now have a GitHub account.

---

## 🛠️ 2. Install GitHub CLI (Command Line Interface)

### Option A: Easy Installer
1. Visit: https://cli.github.com
2. Click **Download for Windows (.msi)**
3. Run the installer
4. ✅ Make sure the option "Add to PATH" is checked

After installing, restart your terminal (like PowerShell or Command Prompt), then test:

> 💡 **Note:** Bash is just a type of command-line interface. On Windows, you can use **PowerShell**, **Command Prompt**, or **Git Bash**.  
> They all let you talk to your computer using text commands—just pick whichever you're most comfortable with!

```bash
gh --version
```
You should see a version number.

---

## 🔐 3. Login to GitHub from Terminal
In your terminal:
```bash
gh auth login
```
Then:
- Choose: **GitHub.com**
- Choose: **HTTPS**
- It will open a browser → Click **Authorize**

✅ You're now connected to your GitHub account!

---

## 📁 4. Create a Local Project
```bash
mkdir git-setup-notes
cd git-setup-notes
echo "# Git Setup Notes" > README.md
git init
git add .
git commit -m "Initial commit"
```

---

## 🌍 5. Create and Push a Repo Using GitHub CLI
```bash
gh repo create git-setup-notes --public --source=. --remote=origin --push
```

Breakdown:
- `--public`: Makes the repo public (or use `--private`)
- `--source=.`: Uses the current folder
- `--remote=origin`: Connects local to GitHub
- `--push`: Pushes the code to GitHub

✅ Your project is now online!

---

## 🌐 6. View Your Repo in a Browser
```bash
gh repo view --web
```

---

## 🧼 7. (Optional) Set Your Git Identity
Only needed once:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

## 🧪 Example Full Workflow
```bash
mkdir hello-cli
cd hello-cli
echo "# Hello from CLI!" > README.md
git init
git add .
git commit -m "first commit"
gh repo create hello-cli --public --source=. --remote=origin --push
gh repo view --web
```

---

## ✅ You're Ready!
You’ve now:
- Created a GitHub account
- Installed GitHub CLI
- Made a repo and pushed code — all from terminal!

Keep this as your quick-start guide for future projects. 🧠💪
