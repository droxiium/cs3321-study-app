# Push to GitHub - Step by Step

This guide walks you through creating a GitHub repo and pushing your study app code.

## Prerequisites
- GitHub account (free at github.com)
- Git installed on your computer (https://git-scm.com)

## Step 1: Create GitHub Repository

1. Go to **github.com** and log in
2. Click the **+** icon in top right → **New repository**
3. Fill in:
   - **Repository name**: `cs3321-study-app`
   - **Description**: `Interactive study application for CS 3321 with spaced repetition and mock exams`
   - **Public** (so recruiters can see it)
   - **Add .gitignore**: Python (we already have one, but this doesn't hurt)
   - **Add a README**: NO (we already have README.md)
4. Click **Create repository**

You'll see a page with instructions. Copy the commands shown—we'll use them below.

## Step 2: Open Terminal/Command Prompt

Navigate to your study app folder:

```bash
cd "path/to/CS3321 - Software Engineering/Study App"
```

For example, if on Mac/Linux:
```bash
cd ~/Spring\ 2026/CS3321\ -\ Software\ Engineering/Study\ App
```

Or on Windows:
```bash
cd "C:\Users\YourName\Spring 2026\CS3321 - Software Engineering\Study App"
```

## Step 3: Initialize Git & Make First Commit

Run these commands in order:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: CS 3321 Study App with spaced repetition and mock exams"

# Rename branch to main (GitHub's default)
git branch -M main
```

## Step 4: Connect to GitHub

Replace `YOUR_USERNAME` with your GitHub username:

```bash
git remote add origin https://github.com/YOUR_USERNAME/cs3321-study-app.git
```

Example:
```bash
git remote add origin https://github.com/aimalorakzai/cs3321-study-app.git
```

## Step 5: Push to GitHub

```bash
git push -u origin main
```

It will ask for your GitHub credentials. Use:
- **Username**: Your GitHub username
- **Password**: A personal access token (see note below)

### Note: Personal Access Token (instead of password)

GitHub now requires a personal access token instead of your password:

1. Go to GitHub → Settings → Developer settings → Personal access tokens
2. Click **Generate new token**
3. Check `repo` (under "Full control of private repositories")
4. Click **Generate token**
5. Copy the token (you'll only see it once!)
6. Paste it when Git asks for your password

## Step 6: Verify on GitHub

1. Go to **github.com/YOUR_USERNAME/cs3321-study-app**
2. You should see your README.md, index.html, and other files
3. The README should be displayed beautifully below the file list

## Done! 🎉

Your code is now on GitHub. You can:
- Share the link with recruiters/interviewers
- Add a demo GIF to your README
- Continue updating with `git commit` and `git push`

## Common Commands Going Forward

```bash
# Make changes, then commit
git add .
git commit -m "Describe your changes"
git push

# View your repository
git log  # See all commits
git status  # See what changed
```

## Troubleshooting

**"fatal: not a git repository"**
- Make sure you're in the right folder (the one with index.html)
- Run `git init` again

**"Repository not found"**
- Check your username in the URL
- Make sure the repository exists on GitHub

**Authentication failed**
- Make sure you're using a personal access token, not your password
- Check that the token has the `repo` permission

**Can't push (branch conflicts)**
- Run: `git pull origin main` first
- Then `git push`

---

**Questions?** Check out GitHub's guides: https://guides.github.com
