# Deployment Guide

## Overview
This guide assumes minimal technical knowledge. Follow step-by-step to deploy the trafficking research database.

## Option 1: GitHub Pages (Recommended)

### Prerequisites
- GitHub account (free)
- Basic familiarity with uploading files

### Steps

1. **Create Repository**
   - Go to github.com
   - Click "New repository"
   - Name: `trafficking-research-db`
   - Set to Public
   - Initialize with README

2. **Upload Files**
   - Click "Add file" > "Upload files"
   - Upload:
     - `index.html`
     - `resources.csv`
     - `style.css` (if separate)
     - `script.js` (if separate)

3. **Enable GitHub Pages**
   - Go to Settings > Pages
   - Source: Deploy from branch
   - Branch: main, folder: / (root)
   - Click Save

4. **Access Your Site**
   - URL will be: `https://[your-username].github.io/trafficking-research-db`
   - Takes 5-10 minutes first time

### Updating Data
1. Download latest CSV from Zotero
2. Rename to `resources.csv`
3. Go to repository
4. Click on `resources.csv`
5. Click pencil icon (Edit)
6. Delete contents
7. Paste new CSV data
8. Commit changes
9. Site updates automatically (2-5 minutes)

## Option 2: Google Drive Hosting

### Note
Google Drive hosting is more limited and requires workarounds.

### Steps
1. **Prepare Files**
   - Ensure all assets are embedded in index.html
   - CSV data must be embedded as JavaScript variable

2. **Upload to Drive**
   - Upload index.html
   - Right-click > Share > Anyone with link
   - Copy link

3. **Create Hosting URL**
   - Take the file ID from share link
   - Use: `https://drive.google.com/uc?export=view&id=[FILE_ID]`

### Limitations
- No separate files (everything embedded)
- Harder to update
- Less reliable

## Maintenance Tasks

### Monthly
1. Export fresh CSV from Zotero
2. Check for broken links (optional)
3. Update resources.csv in GitHub

### Quarterly
1. Review tag consistency
2. Check browser compatibility
3. Backup repository

### Annually
1. Audit all resources for relevance
2. Update any deprecated CDN links
3. Consider feature additions

## Troubleshooting

### Site not loading
- Check GitHub Pages is enabled
- Verify index.html exists
- Wait 10 minutes for propagation

### CSV not updating
- Clear browser cache (Ctrl+Shift+R)
- Check CSV format hasn't changed
- Verify file is named exactly `resources.csv`

### Search not working
- Check browser console for errors
- Verify JavaScript is enabled
- Test with smaller CSV subset

## Getting Help

### Resources
- GitHub Pages docs: https://pages.github.com/
- GAHTS workgroup meeting (monthly)
- Project lead: Jarrett Davis

### Common Issues
1. **"404 Not Found"** - Check repository name and Pages settings
2. **"Search returns nothing"** - CSV encoding issue, re-save as UTF-8
3. **"Site looks broken"** - CDN might be down, wait and retry

## Sharing Access

### For Workgroup Members
1. Add as collaborators in GitHub
2. Settings > Manage access > Add people
3. They can update CSV directly

### For Public
- Just share the GitHub Pages URL
- No login needed for viewing
- Read-only access automatic
