# Team Collaboration Guide

This guide explains how to give access to teammates to edit code in this repository.

## For Repository Owner: How to Add Teammates

### Method 1: Add Collaborators (Recommended for Small Teams)

1. **Go to Repository Settings**
   - Navigate to https://github.com/ddevMetal/k-shortest-path-csci323
   - Click on **Settings** tab (top right)

2. **Add Collaborators**
   - In the left sidebar, click **Collaborators** (or **Collaborators and teams**)
   - Click the **Add people** button
   - Enter your teammate's GitHub username or email
   - Click **Add [username] to this repository**

3. **Set Permission Level**
   - **Write**: Allows push access to the repository (recommended for team members)
   - **Maintain**: Write access plus manage issues and pull requests
   - **Admin**: Full access including repository settings

4. **Teammate Accepts Invitation**
   - Your teammate will receive an email invitation
   - They must accept the invitation to gain access
   - Or they can go to https://github.com/ddevMetal/k-shortest-path-csci323 and accept the invitation there

### Method 2: Create an Organization (For Larger Teams)

1. Create a GitHub Organization
2. Transfer the repository to the organization
3. Add team members to the organization
4. Manage access through teams

## For Teammates: How to Start Contributing

### Step 1: Accept the Invitation

1. Check your email for the collaboration invitation
2. Click the link in the email or visit the repository URL
3. Click **Accept invitation**

### Step 2: Clone the Repository

```bash
# Clone the repository to your local machine
git clone https://github.com/ddevMetal/k-shortest-path-csci323.git

# Navigate into the repository
cd k-shortest-path-csci323
```

### Step 3: Configure Git (First Time Only)

```bash
# Set your name and email (use your GitHub email)
git config user.name "Your Name"
git config user.email "your.email@example.com"
```

### Step 4: Work on the Code

```bash
# Create a new branch for your work
git checkout -b feature/your-feature-name

# Make your changes to the code
# Edit files using your preferred editor

# Check what files you've changed
git status

# Add your changes
git add .

# Commit your changes with a descriptive message
git commit -m "Description of your changes"

# Push your changes to GitHub
git push origin feature/your-feature-name
```

### Step 5: Create a Pull Request (Optional but Recommended)

1. Go to the repository on GitHub
2. Click **Pull requests** tab
3. Click **New pull request**
4. Select your branch
5. Add a description of your changes
6. Click **Create pull request**
7. Wait for team review and approval

## Team Workflow Best Practices

### 1. Communication
- Discuss who is working on what to avoid conflicts
- Use GitHub Issues to track tasks
- Comment on pull requests for code review

### 2. Branching Strategy

```bash
# Always create a new branch for your work
git checkout -b feature/algorithm-improvement
git checkout -b fix/bug-description
git checkout -b docs/update-readme
```

### 3. Sync Before Starting Work

```bash
# Always get the latest changes before starting work
git checkout main
git pull origin main

# Then create your feature branch
git checkout -b feature/your-feature
```

### 4. Handling Conflicts

If you get a merge conflict:

```bash
# Update your branch with latest main
git checkout main
git pull origin main
git checkout your-branch
git merge main

# Resolve conflicts in your editor
# Then commit the merge
git add .
git commit -m "Resolve merge conflicts"
git push origin your-branch
```

### 5. Code Review Process

- Always create pull requests instead of pushing directly to main
- Have at least one teammate review your changes
- Address review comments before merging
- Use meaningful commit messages

## Working with Google Colab

Since this project uses Jupyter notebooks and Google Colab:

### Option 1: Direct Git Integration
1. In Colab, go to **File** → **Save a copy in GitHub**
2. Select the repository and branch
3. Add a commit message
4. Click **OK**

### Option 2: Download and Upload
1. Download the notebook from Colab (**File** → **Download** → **Download .ipynb**)
2. Save it to your local clone of the repository
3. Commit and push using git commands above

### Option 3: GitHub Integration in Colab
1. Open Colab notebook
2. Click **File** → **Open notebook**
3. Select **GitHub** tab
4. Enter repository URL
5. Select the notebook to open
6. Make changes and save back to GitHub

## Quick Reference Commands

```bash
# Clone repository
git clone https://github.com/ddevMetal/k-shortest-path-csci323.git

# Check status
git status

# Create new branch
git checkout -b branch-name

# Add all changes
git add .

# Commit changes
git commit -m "Your message"

# Push to GitHub
git push origin branch-name

# Pull latest changes
git pull origin main

# Switch branches
git checkout branch-name

# List all branches
git branch -a
```

## Common Issues and Solutions

### Issue: "Permission denied"
**Solution**: Make sure you've accepted the collaboration invitation and are using the correct GitHub credentials.

### Issue: "Merge conflict"
**Solution**: Follow the conflict resolution steps above, or ask a teammate for help.

### Issue: "Cannot push to main"
**Solution**: Create a new branch instead of working directly on main. The main branch might be protected.

### Issue: "Already up to date but changes not showing"
**Solution**: Make sure you're on the correct branch and have pulled the latest changes.

## Need Help?

- Check the [GitHub Docs on Collaboration](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)
- Ask your teammates for assistance
- Create an issue in the repository to discuss problems

---

**Group**: FT14  
**Course**: CSCI323 - Modern Artificial Intelligence  
**Project**: Comparative Analysis on K Shortest Simple Path Problem
