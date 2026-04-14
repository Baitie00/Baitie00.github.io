# Academic Homepage

Static HTML/CSS academic homepage. No build step, no dependencies.

## File Structure

```
academic-homepage/
├── index.html          # Main page
├── style.css           # Global styles
├── assets/
│   ├── avatar.jpg      # Your profile photo (148×148 or larger, square)
│   ├── cv.pdf          # Your CV
│   ├── pub1-thumb.png  # Paper thumbnail images (120×80 recommended)
│   └── pub2-thumb.png
└── blog/
    ├── post.css        # Blog post styles
    ├── post-template.html  # Copy this to create a new post
    └── your-post.html
```

## How to Fill In Content

### index.html — find and replace these placeholders:

| Placeholder | Replace with |
|---|---|
| `[Your Name]` | Your full name |
| `[Your University]` | Your institution |
| `[Advisor Name]` | Your advisor's name |
| `[Your Research Area]` | e.g., Scientific Machine Learning |
| `you@university.edu` | Your email |
| GitHub / Scholar / Twitter links | Your actual profile URLs |
| `[Paper Title N]` | Paper titles and authors |
| `[Conference / Journal]` | Venue name and year |

### Adding a new blog post

1. Copy `blog/post-template.html` → `blog/your-post-slug.html`
2. Fill in the title, date, and body content
3. Add a link in `index.html` under the Blog section:
```html
<li class="blog-item">
  <a href="blog/your-post-slug.html">
    <span class="blog-title">Your Post Title</span>
    <span class="blog-meta">Apr 2025 · Research</span>
  </a>
</li>
```

### Enabling math in blog posts

Uncomment the KaTeX block at the bottom of your post HTML.
Then use `$...$` for inline math and `$$...$$` for display math.

## Deployment

**GitHub Pages (free):**
1. Push this folder to a GitHub repo named `yourusername.github.io`
2. Go to Settings → Pages → Source: main branch / root
3. Your site will be live at `https://yourusername.github.io`

**Netlify (free, custom domain support):**
1. Drag and drop this folder at netlify.com/drop
2. Done — you get a live URL instantly
