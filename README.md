# Nicos Savva - Personal Academic Website

Personal academic website for Professor Nicos Savva, hosted on GitHub Pages.

**Live site:** [https://prof-savva.github.io](https://prof-savva.github.io)

## About

This website serves as an academic portfolio showcasing:

- Professional biography and research interests
- Journal publications and working papers
- Non-technical research briefs and opinion pieces
- Contact information and external profiles

## Structure

```
prof-savva.github.io/
|-- index.html          # Main website page
|-- opinion-pieces.html # Full opinion pieces archive
|-- styles.css          # Stylesheet
|-- DSC_5800.jpg        # Profile photo
|-- SavvaCV.pdf         # Academic CV
|-- *.pdf               # Research papers and manuscripts
|-- README.md           # This file
|-- LICENSE             # License information
`-- .gitignore          # Git ignore rules
```

## Updating the Website

### Adding a New Publication

1. Upload the PDF file to the repository
2. Edit `index.html` and add a new `<li>` entry in the publications section:

```html
<li><strong>Paper Title</strong> with Co-authors, <em>Journal Name</em>, (Year) Volume(Issue), Pages, (<a href="filename.pdf">Manuscript.pdf</a>)</li>
```

### Updating Contact Information

Edit the `.contact-info` section in `index.html`.

### Updating the CV

Replace `SavvaCV.pdf` with the updated version.

## Technologies

- HTML5
- CSS3 (responsive design)
- GitHub Pages (hosting)
- Statcounter (analytics)

## License

See [LICENSE](LICENSE) for details.
