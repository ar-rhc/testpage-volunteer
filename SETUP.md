# Quick Setup Guide

## Step 1: Create GitHub Repository

1. Go to https://github.com and sign in (or create an account)
2. Click the **"+"** icon in the top right → **"New repository"**
3. Repository name: `testpage-volunteer`
4. Make it **Public** (required for free GitHub Pages)
5. **DO NOT** check "Initialize with README"
6. Click **"Create repository"**

## Step 2: Push Your Code

Run these commands in your terminal (you're already in the right directory):

```bash
# Make sure you're in the testpage-volunteer directory
cd /Volumes/Nvme/ARfiles/Cursor/testpage-volunteer

# Commit your files
git commit -m "Initial commit - Volunteer page"

# Rename branch to main (GitHub standard)
git branch -M main

# Add your GitHub repository (replace YOUR_USERNAME with your actual GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/testpage-volunteer.git

# Push to GitHub
git push -u origin main
```

**Important:** Replace `YOUR_USERNAME` with your actual GitHub username!

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/YOUR_USERNAME/testpage-volunteer`
2. Click **"Settings"** tab
3. Click **"Pages"** in the left sidebar
4. Under **"Source"**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **"Save"**

## Step 4: View Your Site

Your site will be live at:
**https://YOUR_USERNAME.github.io/testpage-volunteer/**

⏱️ It may take 1-5 minutes for the site to be available after enabling Pages.

## Troubleshooting

- If you get authentication errors, you may need to set up a GitHub Personal Access Token
- Make sure the repository is **Public** (not Private) for free GitHub Pages
- Check the "Actions" tab in your repository to see if the site is being built
