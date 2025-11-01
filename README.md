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
