# CVEN-5833: AI in Earth System Science Course Website

This is the course website for CVEN-5833: AI in Earth System Science at the University of Colorado Boulder.

## Website Structure

- `index.html` - Main course website page with syllabus information
- `styles.css` - Stylesheet for modern, responsive design
- `README.md` - This file

## Deployment to GitHub Pages

### Option 1: Deploy from Main Branch

1. **Create a GitHub Repository**
   - Go to GitHub and create a new repository (e.g., `cven5833-course-website`)
   - Don't initialize with README, .gitignore, or license (since we already have files)

2. **Push Your Files to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Course website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click on **Settings** tab
   - Scroll down to **Pages** section (in the left sidebar)
   - Under **Source**, select **Deploy from a branch**
   - Choose **main** branch and **/ (root)** folder
   - Click **Save**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Option 2: Deploy from gh-pages Branch

If you prefer to keep your website on a separate branch:

```bash
git checkout -b gh-pages
git push origin gh-pages
```

Then in GitHub Settings > Pages, select the `gh-pages` branch as the source.

### Option 3: Using GitHub Actions (Optional)

For automated deployments, you can create a GitHub Actions workflow. This is more advanced and not necessary for simple static sites.

## Customizing the Website

### Update Course Information

1. **Edit `index.html`** and replace placeholder text:
   - `[Term/Year]` - Current term and year
   - `[Days of week]` - Class meeting days
   - `[Time]` - Class meeting time
   - `[Room/Building]` - Classroom location
   - `[Instructor Name]` - Instructor's name
   - `[email]` - Contact email addresses
   - `[Office Location]` - Office location
   - `[Office Hours]` - Office hours

2. **Update Course Content**:
   - Course description
   - Learning objectives
   - Prerequisites
   - Weekly schedule
   - Assignments and due dates
   - Grading breakdown
   - Required resources

### Styling

- Edit `styles.css` to customize colors, fonts, and layout
- The color scheme uses CSS variables defined at the top of `styles.css`
- Modify these variables to change the theme:
  ```css
  :root {
      --primary-color: #1a5490;  /* Main color */
      --secondary-color: #ffc107; /* Accent color */
      /* ... */
  }
  ```

## Local Development

To view the website locally before deploying:

1. **Simple HTTP Server (Python 3)**
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser

2. **Simple HTTP Server (Python 2)**
   ```bash
   python -m SimpleHTTPServer 8000
   ```

3. **Using Node.js (if you have it installed)**
   ```bash
   npx http-server
   ```

4. **Using VS Code**
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

## Adding More Pages

To add additional pages (e.g., assignments page, resources page):

1. Create new HTML files (e.g., `assignments.html`)
2. Link to them from the navigation in `index.html`
3. Use the same `styles.css` for consistent styling

## Notes

- The website is fully responsive and works on mobile, tablet, and desktop devices
- All sections are easily customizable
- The design follows modern web standards and accessibility best practices
- No JavaScript is required - the site is pure HTML/CSS

## License

This course website template is provided for educational use. Modify as needed for your course.
