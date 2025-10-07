# Quick Setup Guide

This guide will help you get your GitHub Pages site live and customize it with your content.

## Step 1: Enable GitHub Pages

1. Go to your repository on GitHub: https://github.com/danteleon1165/economics
2. Click on **Settings** (gear icon in the top menu)
3. In the left sidebar, click on **Pages**
4. Under **Source**, select the branch: `copilot/add-github-pages-landing` (or `main` after merging)
5. Leave the folder as `/ (root)`
6. Click **Save**
7. Wait a few minutes for the site to deploy
8. Your site will be live at: **https://danteleon1165.github.io/economics/**

## Step 2: Add Your PDF Files

1. Create your PDF guides (e.g., using Microsoft Word, Google Docs, or any PDF creator)
2. Save them with descriptive filenames, for example:
   - `getting-started.pdf`
   - `portfolio-management.pdf`
   - `risk-management.pdf`
   - `investment-strategies.pdf`
3. Upload these files to the `pdfs/` directory in your repository
4. Commit and push the changes

**Via GitHub Web Interface:**
- Navigate to the `pdfs/` folder
- Click "Add file" → "Upload files"
- Drag and drop your PDFs
- Commit the changes

**Via Git Command Line:**
```bash
git add pdfs/*.pdf
git commit -m "Add investment guide PDFs"
git push
```

## Step 3: Add Your YouTube Videos

1. Upload your videos to YouTube
2. For each video, get the video ID from the URL:
   - Example URL: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
   - Video ID: `dQw4w9WgXcQ`
3. Open `index.html` in an editor
4. Find the video embed sections (search for `VIDEO_ID_1`, `VIDEO_ID_2`, etc.)
5. Replace each placeholder with your actual video ID:

**Before:**
```html
<iframe src="https://www.youtube.com/embed/VIDEO_ID_1" ...>
```

**After:**
```html
<iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" ...>
```

6. Update the video titles and descriptions to match your content
7. Commit and push the changes

## Step 4: Customize Content (Optional)

### Update Titles and Descriptions

Edit `index.html` to customize:
- Page title (line 7): `<title>Investment Education Hub</title>`
- Navigation logo (line 14): `<h1 class="logo">Investment Education Hub</h1>`
- Hero section heading and text (lines 25-27)
- Guide card titles and descriptions (lines 37-80)
- Video titles and descriptions (lines 90-155)
- About section text (lines 163-190)

### Change Colors

Edit `styles.css` (lines 10-15):
```css
:root {
    --primary-color: #2c3e50;      /* Dark blue-gray for header/footer */
    --secondary-color: #3498db;    /* Light blue for buttons */
    --accent-color: #e74c3c;       /* Red for call-to-action */
}
```

### Add More Guide Cards

Copy one of the existing guide card blocks (lines 37-46 in `index.html`) and modify:
```html
<div class="guide-card">
    <div class="guide-icon">🎓</div>
    <h3>Your New Guide Title</h3>
    <p>Description of your new guide...</p>
    <a href="pdfs/your-new-guide.pdf" class="download-btn" target="_blank">Download PDF</a>
</div>
```

### Add More Videos

Copy one of the existing video card blocks (lines 93-103 in `index.html`) and modify:
```html
<div class="video-card">
    <div class="video-container">
        <iframe 
            src="https://www.youtube.com/embed/YOUR_VIDEO_ID" 
            title="Your Video Title" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
        </iframe>
    </div>
    <div class="video-info">
        <h3>Your Video Title</h3>
        <p>Description of your video...</p>
    </div>
</div>
```

## Step 5: Test Your Site

After enabling GitHub Pages:
1. Wait 2-5 minutes for the first deployment
2. Visit: https://danteleon1165.github.io/economics/
3. Test all PDF download links
4. Verify YouTube videos play correctly
5. Check the site on mobile devices

## Troubleshooting

### Site Not Loading
- Ensure GitHub Pages is enabled in repository settings
- Check that you've selected the correct branch
- Wait a few minutes after making changes

### PDFs Not Downloading
- Verify PDF files are in the `pdfs/` directory
- Check that filenames in `index.html` match exactly (case-sensitive)
- Ensure PDFs are committed and pushed to the repository

### Videos Not Playing
- Verify you're using the correct video ID
- Make sure videos are set to "Public" or "Unlisted" on YouTube
- Check that the embed code is correct

## Need Help?

- Check the main [README.md](README.md) for more details
- Review the [GitHub Pages documentation](https://docs.github.com/en/pages)
- Open an issue in the repository if you encounter problems

---

**Remember:** After any changes to HTML, CSS, or adding new files, you need to commit and push them to GitHub for the changes to appear on your live site.
