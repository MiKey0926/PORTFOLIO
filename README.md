# Llana Pacis Personal Portfolio

A responsive single-page portfolio website for **Llana Pacis**, an aspiring artist and UI/UX designer studying Information Technology. The site presents an introduction, skills, school projects, hobbies, education and work experience, and a simple contact form.

## Features

- Responsive layout for mobile, tablet, and desktop screens
- Sticky navigation with a mobile menu
- Hero and introduction sections with personal highlights
- Skills cards with visual proficiency indicators
- Project cards with technology tags and external project links
- Hobby cards using local image assets
- Education and experience timeline
- Accessible labels, descriptive image alt text, and live regions for dynamically loaded content
- Client-side contact form feedback

## Built with

- HTML5
- CSS3, including CSS Grid, custom properties, media queries, and transitions
- Vanilla JavaScript
- JSON for editable portfolio content
- Google Fonts: DM Sans, DM Mono, and Playfair Display

## Project structure

```text
PORTFOLIO/
|-- index.html          # Page markup and site sections
|-- README.md           # Project documentation
|-- css/
|   `-- style.css       # Responsive styles and component states
|-- js/
|   `-- script.js       # Data loading, rendering, menu, and form behavior
|-- data/
|   `-- data.json       # Skills, projects, hobbies, and timeline content
`-- assets/
    |-- sheva.jpg       # Hero portrait
    |-- art.jpg         # Hobby image
    |-- garden.jpg      # Hobby image
    |-- cookies.jpg     # Hobby image
    `-- logo.png        # Portfolio logo asset
```

## Customize the portfolio

### Update content

Edit [data/data.json](data/data.json) to update the sections rendered by JavaScript:

- `skills`: name, icon text, and level from `0` to `100`
- `projects`: title, description, display text, card color, technology tags, and optional link
- `hobbies`: name, image path, and description
- `timeline`: type, title, subtitle, and date

Example project entry:

```json
{
  "title": "My Project",
  "description": "A short description of the project.",
  "display": "Project slogan.",
  "color": "#7a1f2b",
  "tags": ["HTML", "CSS", "JavaScript"],
  "link": "https://example.com"
}
```

### Update personal details

Edit [index.html](index.html) for content that is written directly in the page, including:

- Name, role, and introduction text
- Navigation labels
- Hero portrait path and alt text
- Contact-section copy
- Footer copyright year and location

### Replace images

Add replacement images to `assets/`, then update the matching paths in `index.html` or `data/data.json`. Keep image files reasonably optimized so the portfolio remains quick to load.

### Adjust the design

The main design colors are defined as CSS variables near the top of [css/style.css](css/style.css):

```css
--bg: #f7f3eb;
--wine: #7a1f2b;
--sage: #6c7a57;
--terracotta: #c46a3a;
--ink: #2b2b2b;
```

Change these values to quickly adapt the overall visual theme. The same stylesheet contains the responsive breakpoints at `768px` and `1200px`.

## How it works

When the page loads, `js/script.js` fetches `data/data.json` and creates the skills, project, hobby, and timeline cards dynamically. This keeps portfolio content separate from the page structure and makes regular updates easier.

The script also:

- Opens and closes the mobile navigation menu
- Closes the mobile menu after a navigation link is selected
- Shows a fallback message if portfolio data cannot be loaded
- Validates required contact-form fields in the browser
- Displays a confirmation message after the contact form is submitted

## Contact form note

The contact form is currently a **front-end demo**. It clears the form and shows a success message, but it does not send email or save submissions. To make it functional, connect it to a form provider or a back-end endpoint.

## Deployment

This is a static website and can be deployed to services such as GitHub Pages, Netlify, or Vercel. Upload the complete project folder while preserving the `css`, `js`, `data`, and `assets` paths. Since the app uses relative paths, no build step is required.

## License

This project is intended as a personal portfolio. Add a license file if you plan to share, reuse, or distribute it publicly.
