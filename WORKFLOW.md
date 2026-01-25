# Monthly Website Update Workflow

A simple checklist for updating prof-savva.github.io, primarily for new opinion pieces and articles.

---

## How to Run This Update

### Option 1: Using Claude Code (Recommended)

Open a terminal in this repository and run:

```bash
claude
```

Then ask:

> "Run the monthly website update. Check for new articles I've published and update the website."

Claude will:
1. Search Think @ LBS and Forbes for new articles
2. Add any new articles to both `index.html` and `opinion-pieces.html`
3. Commit and push the changes

### Option 2: Manual Update

Follow the checklist below to update manually.

---

## Manual Checklist

### 1. Check for New Articles

Search for new articles published in the past month:

- [ ] **Think @ LBS**: Check https://www.london.edu/think/articletopics#q=savva
- [ ] **Forbes**: Search "Nicos Savva" on forbes.com/sites/lbsbusinessstrategyreview
- [ ] **Other outlets**: HBR, Management Science Review, etc.

### 2. Update the Website

#### Adding a New Opinion Piece

**On the main page (`index.html`):**

Find the "Recent (2025-2026)" section and add the new article at the top:

```html
<li><a href="URL_HERE">Article Title Here</a> <em>(Publication Name, Month Year)</em></li>
```

**On the full list (`opinion-pieces.html`):**

Add the article under the appropriate year section:

```html
<li>
    <a href="URL_HERE">Article Title Here</a>
    <em>(Publication Name, Month Year)</em>
</li>
```

#### Adding a New Publication (if applicable)

For journal publications, add to `index.html` in the publications section:

```html
<li><a href="JOURNAL_URL"><strong>Paper Title</strong></a> with Co-authors, <em>Journal Name</em>, (Year) Volume(Issue), Pages, (<a href="manuscript.pdf">Manuscript.pdf</a>)</li>
```

### 3. Test Locally (Optional)

Open `index.html` in a browser to verify changes look correct.

### 4. Commit and Push

```bash
git add .
git commit -m "Add [article title] to opinion pieces"
git push origin main
```

### 5. Verify Live Site

After pushing, wait 2-3 minutes and check https://prof-savva.github.io to confirm changes are live.

---

## Quick Reference: File Locations

| Content | File |
|---------|------|
| Main homepage | `index.html` |
| Full opinion pieces list | `opinion-pieces.html` |
| Styles | `styles.css` |
| CV | `SavvaCV.pdf` |
| Paper manuscripts | `*.pdf` files in root |

---

## Common Tasks

### Update CV
1. Replace `SavvaCV.pdf` with the new version
2. Commit and push

### Add a New PDF Manuscript
1. Upload the PDF file to the repository
2. Add a link in `index.html`: `<a href="filename.pdf">Manuscript.pdf</a>`
3. Commit and push

### Update Contact Information
1. Edit the `.contact-info` section in `index.html`
2. Commit and push

---

## Article Format Examples

### Think @ LBS
```html
<li><a href="https://www.london.edu/think/ARTICLE-SLUG">Article Title</a> <em>(Think @ London Business School, 2026)</em></li>
```

### Forbes
```html
<li><a href="https://www.forbes.com/sites/lbsbusinessstrategyreview/YYYY/MM/DD/article-slug/">Article Title</a> <em>(Forbes, Month Year)</em></li>
```

### Harvard Business Review
```html
<li><a href="https://hbr.org/YYYY/MM/article-slug">Article Title</a> <em>(Harvard Business Review, Year)</em></li>
```

---

## Year-End Tasks

At the start of each year:

1. Update footer copyright year in `index.html`:
   ```html
   <p>&copy; 2026 Nicos Savva. All rights reserved.</p>
   ```

2. Add new year section to `opinion-pieces.html` if needed:
   ```html
   <section class="section">
       <h3>2027</h3>
       <ul class="publication-list">
           <!-- New articles go here -->
       </ul>
   </section>
   ```

3. Consider moving older articles from "Recent" to "Selected Earlier Work" on main page

---

## Troubleshooting

**Changes not appearing on live site?**
- Wait 2-5 minutes for GitHub Pages to rebuild
- Hard refresh browser (Ctrl+Shift+R or Cmd+Shift+R)
- Check https://github.com/prof-savva/prof-savva.github.io/actions for build status

**Broken link?**
- Verify URL is correct and accessible
- Check for typos in href attribute
- Ensure URL uses https:// prefix

---

*Last updated: January 2026*
