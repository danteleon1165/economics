# Investment Education Hub

A professional GitHub Pages landing page for teaching people about investing through PDF guides and YouTube video tutorials.

## 🌐 Live Site

Visit the live site at: `https://danteleon1165.github.io/economics/`

## 📋 Features

- **Clean, Professional Design**: Modern and responsive layout that works on all devices
- **PDF Guides Section**: Display and provide download links for your investment guides
- **Video Tutorials Section**: Embed YouTube videos directly on the page
- **Easy to Customize**: Simple HTML/CSS structure for quick updates

## 🚀 Getting Started

### Enabling GitHub Pages

1. Go to your repository settings on GitHub
2. Navigate to "Pages" in the sidebar
3. Under "Source", select the branch you want to deploy (usually `main` or `copilot/add-github-pages-landing`)
4. Save the settings
5. Your site will be published at `https://danteleon1165.github.io/economics/`

### Adding Your PDF Guides

1. Place your PDF files in the `pdfs/` directory
2. Open `index.html` and update the PDF links:
   ```html
   <a href="pdfs/your-pdf-name.pdf" class="download-btn" target="_blank">Download PDF</a>
   ```
3. Update the titles and descriptions to match your content

### Adding YouTube Videos

1. Get the video ID from your YouTube video URL
   - Example: `https://www.youtube.com/watch?v=dQw4w9WgXcQ` → Video ID is `dQw4w9WgXcQ`
2. Open `index.html` and replace `VIDEO_ID_1`, `VIDEO_ID_2`, etc. with your actual video IDs:
   ```html
   <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" ...></iframe>
   ```
3. Update the video titles and descriptions

## 📁 Project Structure

```
economics/
├── index.html          # Main landing page
├── styles.css          # Styling for the page
├── pdfs/              # Directory for PDF guides
│   └── README.md      # Instructions for adding PDFs
├── README.md          # This file
└── LICENSE            # License information
```

## 🎨 Customization

### Changing Colors

Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #2c3e50;      /* Main dark color */
    --secondary-color: #3498db;    /* Blue accent */
    --accent-color: #e74c3c;       /* Call-to-action buttons */
}
```

### Adding More Content

You can add more guide cards or video cards by copying the existing card structure in `index.html`.

### Modifying Layout

The site uses CSS Grid for responsive layouts. Adjust the grid settings in `styles.css` to change how cards are displayed.

## 📱 Responsive Design

The site is fully responsive and optimized for:
- Desktop computers
- Tablets
- Mobile phones

## 📄 License

This project is released under the Unlicense - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Feel free to fork this project and customize it for your own investment education needs!

## ⚠️ Disclaimer

This content is for educational purposes only and does not constitute financial advice. Always consult with a qualified financial advisor before making investment decisions.