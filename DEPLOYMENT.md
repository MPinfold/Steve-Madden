# GitHub Deployment Guide

This guide will help you deploy the Steve Madden AW25 Showcase to GitHub Pages.

## 🚀 Quick Deployment Steps

### 1. Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right → "New repository"
3. Name your repository (e.g., `steve-madden-aw25-showcase`)
4. Make it **Public** (required for free GitHub Pages)
5. Don't initialize with README (we already have one)
6. Click "Create repository"

### 2. Upload Your Files

**Option A: Using GitHub Web Interface**
1. On your new repository page, click "uploading an existing file"
2. Drag and drop all files from your `Steve Madden HTML5` folder
3. Write a commit message: "Initial upload of Steve Madden showcase"
4. Click "Commit changes"

**Option B: Using Git Commands**
```bash
# Navigate to your project folder
cd "/Users/michaelpinfold/Desktop/Steve Madden HTML5"

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial upload of Steve Madden showcase"

# Add remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/steve-madden-aw25-showcase.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section in the left sidebar
4. Under "Source", select **Deploy from a branch**
5. Choose **main** branch
6. Choose **/ (root)** folder
7. Click **Save**

### 4. Access Your Live Site

- Your site will be available at: `https://YOUR_USERNAME.github.io/REPOSITORY_NAME/`
- Example: `https://johndoe.github.io/steve-madden-aw25-showcase/`
- It may take 5-10 minutes for the site to be available

## 🔧 Configuration Details

### Files Created for Deployment:
- `README.md` - Project documentation
- `.gitignore` - Excludes unnecessary files
- `package.json` - Project metadata
- `index.html` - Entry point that redirects to mockup.html
- `.github/workflows/deploy.yml` - Automatic deployment workflow

### Repository Settings:
- **Visibility**: Must be Public for free GitHub Pages
- **Pages Source**: Deploy from main branch
- **Custom Domain**: Optional (can be configured later)

## 🌐 Custom Domain (Optional)

If you want to use a custom domain:

1. In repository Settings → Pages
2. Add your custom domain in the "Custom domain" field
3. Create a `CNAME` file in your repository root with your domain
4. Configure your domain's DNS to point to GitHub Pages

## 🔄 Updating Your Site

To update your site after making changes:

**Using GitHub Web Interface:**
1. Navigate to the file you want to edit
2. Click the pencil icon to edit
3. Make your changes
4. Commit the changes

**Using Git:**
```bash
# Make your changes to files
# Then add and commit
git add .
git commit -m "Description of your changes"
git push origin main
```

## 📊 Monitoring Deployment

- Check the **Actions** tab in your repository to see deployment status
- Green checkmark = successful deployment
- Red X = failed deployment (check logs for details)

## 🛠 Troubleshooting

### Common Issues:

1. **Images not loading**: Ensure all image paths are relative and files are uploaded
2. **404 errors**: Check that `index.html` exists and redirects properly
3. **Deployment failed**: Check the Actions tab for error details
4. **Site not updating**: Wait 5-10 minutes, then try hard refresh (Ctrl+F5)

### File Path Issues:
- Use forward slashes `/` in all paths
- Ensure all referenced files exist in the repository
- Check that image file names match exactly (case-sensitive)

## 📱 Testing

After deployment, test your site on:
- Desktop browsers (Chrome, Firefox, Safari, Edge)
- Mobile devices
- Different screen sizes

## 🔒 Security Notes

- Never commit sensitive information (API keys, passwords)
- All files in public repositories are visible to everyone
- Use the provided `.gitignore` to exclude sensitive files

## 📞 Support

If you encounter issues:
1. Check the GitHub Pages documentation
2. Review the Actions tab for deployment logs
3. Ensure all file paths are correct and case-sensitive
4. Verify that all referenced images and assets are uploaded

---

**Your Steve Madden showcase will be live and accessible worldwide once deployed!**
