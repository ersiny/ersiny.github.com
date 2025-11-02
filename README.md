## Running Locally

1. **Install Quarto**:
   ```bash
   brew install quarto
   ```
   Or download from [quarto.org](https://quarto.org/docs/get-started/)

2. **Preview the site**:
   ```bash
   quarto preview
   ```
   Opens at `http://localhost:4200` with live reload.

## Creating a New Blog Post

1. **Create a new folder** in `posts/` with your post name:
   ```bash
   mkdir -p posts/my-new-post
   ```

2. **Create `index.qmd`** in that folder with frontmatter:
   ```yaml
   ---
   title: "Your Post Title"
   author: "Ersin Yilmaz"
   date: "2025-11-01"
   categories: ["category1", "category2"]
   tags: ["tag1", "tag2"]
   description: "Brief description of your post"
   ---

   Your content here...
   ```

3. **Render the site**:
   ```bash
   quarto render
   ```

4. **Publish**:
   ```bash
   git add .
   git commit -m "New post: your post title"
   git push
   ```

The site will update automatically via GitHub Pages.

## How Publishing Works

GitHub Pages serves your blog from the `docs/` folder:

1. `quarto render` generates static HTML files from your `.qmd` posts into `docs/`
2. You commit and push the `docs/` folder to GitHub
3. GitHub Pages serves the static files at ersin-yilmaz.com

**GitHub Pages is configured to:**
- Deploy from: `master` branch
- Folder: `/docs`

No server-side rendering happens on GitHub - that's why you must run `quarto render` locally before pushing.

## Quarto Features

See `posts/quarto-features-demo/` for examples of callouts, code execution, diagrams, math equations, and more.
