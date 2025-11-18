# GitHub Upload Guide

## What's Been Created

Your website project is ready! Here's what you have:

### Files Created:
- **index.html** - Your main website with a professional layout
- **README.md** - Project documentation
- **.gitignore** - Git configuration to exclude unnecessary files
- **Local Git Repository** - Already initialized and committed

## Next Steps to Upload to GitHub

### Step 1: Create a GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Sign in to your account (or create one if you don't have one)
3. Click the **+** icon in the top-right corner
4. Select **New repository**
5. Fill in the repository details:
   - **Repository name**: `my-cloud-deployment` (or any name you prefer)
   - **Description**: "My First Cloud Deployment - A personal website"
   - **Visibility**: Public (so others can see your work)
   - **Do NOT initialize** with README, .gitignore, or license
6. Click **Create repository**

### Step 2: Connect Local Repository to GitHub

After creating the repository, GitHub will show you commands to run. Execute these in PowerShell:

```powershell
cd c:\xampp\htdocs\DevOps
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/my-cloud-deployment.git
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username**

### Step 3: Verify Upload

1. Go to your GitHub repository URL: `https://github.com/YOUR_USERNAME/my-cloud-deployment`
2. You should see all your files (index.html, README.md, .gitignore)
3. Your README.md will display nicely on the repository homepage

## Customization Before Uploading

**Before uploading to GitHub, customize your website:**

1. Open `index.html` in a text editor
2. Replace `"Your Name"` with your actual name
3. Add a `profile.jpg` image file to the same directory as `index.html`
4. Commit your changes:
   ```powershell
   cd c:\xampp\htdocs\DevOps
   git add .
   git commit -m "Add profile picture and personal details"
   git push
   ```

## Deploy Your Website

### Option 1: GitHub Pages (FREE & EASY)

1. Go to your GitHub repository
2. Click **Settings** (gear icon)
3. Scroll to **Pages** section (left menu)
4. Under "Source", select **main** branch
5. Click **Save**
6. Your site will be live at: `https://YOUR_USERNAME.github.io/my-cloud-deployment`

### Option 2: Local Web Server (XAMPP)

Your files are already in `c:\xampp\htdocs\DevOps`, so you can:

1. Start XAMPP
2. Open your browser and go to: `http://localhost/DevOps/`

### Option 3: Other Cloud Platforms

- **AWS S3**: Upload HTML and image to an S3 bucket with static website hosting
- **Azure Static Web Apps**: Connect your GitHub repo directly
- **Netlify**: Connect to GitHub repo for automatic deployment
- **Vercel**: Similar to Netlify, automatic deployment from GitHub

## Troubleshooting

### Git Error: "Please tell me who you are"
Run:
```powershell
git config --global user.email "your.email@example.com"
git config --global user.name "Your Name"
```

### Authentication Error when pushing
GitHub now requires personal access tokens (not passwords). 
1. Go to GitHub Settings → Developer settings → Personal access tokens
2. Generate a new token with "repo" permissions
3. Use the token as your password when pushing

## Important Customizations Needed

Replace these in `index.html`:
- Line with `"Your Name"` → Your actual name
- `"profile.jpg"` → Your actual profile image filename

## Project Structure

```
DevOps/
├── index.html          # Your website
├── README.md           # Documentation
├── .gitignore          # Git settings
└── profile.jpg         # (Add your image here)
```

Good luck with your cloud deployment! 🚀
