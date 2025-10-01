# Modern GitHub Pages Portfolio

A sleek, modern portfolio site with dark gradient theme, scroll animations, and glass morphism effects. Built with HTML, CSS (Tailwind), and JavaScript. No build tools required - perfect for GitHub Pages deployment.

## 🚀 Features

- **Modern Dark Theme**: Gradient black-gray background with animated elements
- **Scroll Animations**: Elements appear smoothly as you scroll down the page
- **Glass Morphism**: Beautiful frosted glass effects on cards and navigation
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Dynamic Content**: Loads profile and project data from JSON files
- **Smooth Scrolling**: Elegant navigation between sections
- **CORS-Free**: Works when opened directly in browser (includes fallback data)
- **GitHub Integration**: Direct links to your GitHub repositories
- **Easy Customization**: Just update JSON files to add/modify content
- **Lightweight**: No build process, uses Tailwind CDN

## 📁 File Structure

```
/
├── index.html          # Main HTML file with modern dark theme
├── script.js          # JavaScript with scroll animations and fallback data
├── profile.json       # Your profile information
├── projects.json      # Your projects data
├── server.py          # Local development server (fixes CORS issues)
├── start-server.bat   # Quick server startup script
├── assets/
│   ├── profile.svg    # Placeholder profile picture (replace with your photo)
│   └── profile.jpg    # Alternative profile picture format
└── README.md          # This file
```

## 🖥️ Local Development

To avoid CORS issues when developing locally, use the included server:

### Option 1: Python Server (Recommended)
```bash
python server.py
```

### Option 2: Batch File (Windows)
```bash
start-server.bat
```

The server will automatically open your browser to `http://localhost:8000`

## 🛠️ Customization

### 1. Update Your Profile

Edit `profile.json`:

```json
{
  "name": "Your Name",
  "bio": "Your bio description here...",
  "profile_picture": "assets/profile.jpg"
}
```

### 2. Add Your Projects

Edit `projects.json`:

```json
[
  {
    "title": "Project Name",
    "description": "Brief description of your project...",
    "link": "https://github.com/yourusername/your-repo"
  }
]
```

### 3. Replace Profile Picture

- Replace `assets/profile.svg` or `assets/profile.jpg` with your actual photo
- Update the `profile_picture` path in `profile.json` if needed
- Recommended size: 200x200px or larger (will be automatically resized)

### 4. Customize Styling (Optional)

The site uses Tailwind CSS via CDN. To customize:

1. **Colors**: Modify the color classes in `index.html` (e.g., `bg-blue-600` to `bg-green-600`)
2. **Layout**: Adjust grid classes (`md:grid-cols-2` to `md:grid-cols-3`)
3. **Spacing**: Modify padding/margin classes (`p-8` to `p-6`)

## 🌐 GitHub Pages Deployment

1. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

2. **Your site will be available at**:
   `https://yourusername.github.io/repository-name`

3. **Custom Domain (Optional)**:
   - Add a `CNAME` file with your domain name
   - Configure DNS settings with your domain provider

## 🔧 Development

### Local Testing

Since this is a static site, you can:

1. **Simple**: Open `index.html` directly in your browser
2. **With Server**: Use any local server (Python, Node.js, etc.)

```bash
# Python 3
python -m http.server 8000

# Node.js (with http-server)
npx http-server

# PHP
php -S localhost:8000
```

### Adding New Projects

1. Open `projects.json`
2. Add a new project object to the array:

```json
{
  "title": "New Project",
  "description": "Description of the new project...",
  "link": "https://github.com/yourusername/new-project"
}
```

3. Save the file - changes will appear immediately!

## 🎨 Customization Examples

### Change Color Scheme

Replace `bg-blue-600` and `hover:bg-blue-700` in `index.html` with:
- Green: `bg-green-600` and `hover:bg-green-700`
- Purple: `bg-purple-600` and `hover:bg-purple-700`
- Red: `bg-red-600` and `hover:bg-red-700`

### Modify Grid Layout

In `index.html`, find the projects grid:
```html
<div id="projects-grid" class="hidden grid gap-6 md:grid-cols-2 lg:grid-cols-3">
```

Change to:
- 2 columns max: `md:grid-cols-2`
- 4 columns on large screens: `lg:grid-cols-4`
- Single column: Remove `md:grid-cols-2 lg:grid-cols-3`

## 🐛 Troubleshooting

### Projects Not Loading
- Check that `projects.json` is valid JSON (use a JSON validator)
- Ensure all required fields are present: `title`, `description`, `link`
- Check browser console for error messages

### Profile Picture Not Showing
- Verify the image file exists in the `assets/` folder
- Check the path in `profile.json` matches the actual file location
- Ensure image format is supported (JPG, PNG, SVG, WebP)

### Styling Issues
- Clear browser cache and refresh
- Check that Tailwind CDN is loading (check browser network tab)
- Verify HTML class names are correct

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to fork this project and customize it for your own portfolio! If you make improvements that could benefit others, pull requests are welcome.

---

**Happy coding!** 🚀