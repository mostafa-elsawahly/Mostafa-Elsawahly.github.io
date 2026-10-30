# Mostafa Elsawahly | Data Analyst Portfolio

Personal portfolio website of **Mostafa Elsawahly**, a Junior Data Analyst and Banking & Investment Sciences undergraduate focused on Data Analytics and Business Intelligence.

The site presents my background, skills, services, experience, featured projects, and certifications in a single, fast, dependency-free page.

> **Positioning:** Banking & Investment knowledge + Data Analytics + Business Intelligence, turning financial and business data into actionable insights.

---

## Sections

| # | Section | What it covers |
|---|---------|----------------|
| 01 | **About** | Short bio, "Why Me" positioning, live GitHub stats, LinkedIn card |
| 02 | **Education** | B.Sc. Finance, Banking & Investment Sciences (Minor in Data Analytics) |
| 03 | **Technical Arsenal** | Skills grouped by area: Data Analytics, BI, Data & Querying, Power BI, Cloud, AI & Automation |
| 04 | **Services** | Data Analysis, Power BI & BI, SQL & Data Warehousing, Python Analysis, Dashboard & Reporting |
| 05 | **Experience** | Internships and training in an animated timeline |
| 06 | **Projects** | Featured projects with thumbnails, screenshot galleries, and links to their GitHub repositories |
| 07 | **Certifications** | Licenses and certificates |
| 08 | **Contact** | Email, LinkedIn, GitHub, WhatsApp, plus a freelance call to action |

Between the hero and About sits an interactive **pyramid mini-game** (see Features).

## Featured Projects

- **Advanced SQL Data Warehouse & Business Analytics**: Star Schema warehouse (Bronze/Silver/Gold layers), CTEs, window functions, views, stored procedures, indexing. *(11-screenshot gallery)*
- **Superstore Retail Analytics & Automated Reporting**: Python pipeline covering cleaning, feature engineering, RFM segmentation, geospatial analysis, Parquet export. *(14-screenshot gallery)*
- **Salla Call Center Performance**: Power BI dashboard with KPI measures built using DAX. *(5-screenshot gallery)*
- **Dynamic Data Dashboard**: Dashboard that turns raw CSV/Excel files into insights. *(5-screenshot gallery)*
- **Electronics Retail Executive Dashboard**: End-to-end Power BI dashboard using a Star Schema. *(4-screenshot gallery)*
- **Maven Toys Challenge Dashboard**: Power BI dashboard for the Maven Toys challenge. *(1 screenshot)*
- **Workflow Automation (Digitera)**: No-code workflow built with Zapier using the SCQA framework.

## Tech Stack

Built with plain **HTML, CSS, and vanilla JavaScript**. No frameworks, no build step, no npm dependencies.

- Google Fonts: Syne, JetBrains Mono, Cormorant Garamond
- GitHub public REST API for live repo/star counts
- Google Analytics tag (consent denied by default)

## Features

- Animated preloader (SVG ankh that assembles itself) with a 2-second intro
- **Pyramid mini-game:** build the Great Pyramid stone by stone. The layers form the DIKW pyramid (Data, Information, Knowledge, Insight, Decision). Completing the golden capstone triggers a spark burst, a rising sun, and a word-by-word reveal of the heritage quote. The **Skip** button calls a crew of ants that carry the stones up and build it for you
- **Project galleries:** every project card has a thumbnail and a "View Gallery" button that opens a lightbox with large images, thumbnails strip, arrow buttons, keyboard arrows, `Esc` to close, and swipe on mobile
- **Pyramid-shaped custom cursor** with a trailing outline pyramid that grows over interactive elements (desktop with a fine pointer only)
- Dark and light themes, auto-detected from the visitor's system and remembered in `localStorage`
- Scroll-triggered reveal animations that replay when sections re-enter the viewport
- Experience timeline with a scroll-linked progress line
- Typing effect on the hero description and a live Alexandria clock
- Live GitHub stats (repos and total stars) fetched client-side
- Sticky "Contact Me" button that fades while scrolling
- Email buttons that open the mail client and also copy the address as a fallback
- Fully responsive layout with a mobile menu
- SEO: meta description, Open Graph and Twitter cards, JSON-LD `Person` schema
- Accessibility: skip link, visible focus states, focus trap in the mobile menu, ARIA labels, keyboard-operable game and gallery, `prefers-reduced-motion` handling (the game skips animations and builds instantly)

## Project Structure

```
.
├── index.html                       # The entire site (HTML, CSS, JS)
├── Mostafa_Elsawahly_CV.pdf         # CV linked from the "Download CV" button
├── README.md
└── pic/
    ├── photo.jpg                    # Profile photo shown in the hero
    ├── Certifications pic/
    │   ├── Data-Fundamentals.jpg
    │   ├── powerbi-dashboard-certificate.jpg
    │   ├── datacamp-sql.jpg
    │   ├── huawei.jpg
    │   ├── ibm-ai.jpg
    │   ├── digitera.jpg
    │   ├── google-data-analytics.jpg
    │   └── coursera-l1.jpg
    └── project pic/
        ├── Depi-Mini-Project-2-Advanced-SQL-Data-Warehouse-Business-Analytics/
        ├── Dynamic Dashboard/
        ├── Electronics Store Performance & Customer Insights/
        ├── Maven Toys Challenge Dashboard/
        ├── Retail Analytics & Automated Reporting/
        └── sall call center/        # screenshots for each project gallery
```

> Keep these folder and file names exactly as listed, including capitalization. `index.html` references them with relative paths, and GitHub Pages is case-sensitive, so a mismatch shows as a broken image.

## Run Locally

No installation needed. Either:

1. Open `index.html` directly in your browser, or
2. Serve the folder with any static server, for example:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

Then visit `http://localhost:8000`.

> The GitHub stats widget and Google Fonts need an internet connection. Offline, the stats show a dash and fonts fall back to system defaults.

## Deploy to GitHub Pages

1. Push all files to a repository (for example `mostafa-elsawahly.github.io` or `portfolio`):

   ```bash
   git add -A
   git commit -m "Update portfolio"
   git push origin main
   ```

2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After a minute your site is live at `https://<username>.github.io/<repo>/`. Use `Ctrl+F5` to bypass the cache when checking an update.

**After deploying**, update the share-preview image so LinkedIn, WhatsApp, and X can find it. In `index.html`, change these tags to an absolute URL:

```html
<meta property="og:image" content="https://<your-domain>/pic/photo.jpg" />
<meta name="twitter:image" content="https://<your-domain>/pic/photo.jpg" />
```

## Customization

| What | Where to change it |
|------|--------------------|
| Name, headline, bio | Hero and About sections in `index.html` |
| Colors | CSS variables in `:root` (`--primary`, `--bg`, `--fg`, ...) at the top of the `<style>` block |
| Light theme colors | `:root[data-theme="light"]` block |
| Email address | `mailto:` links and the `copyEmail` / `fallbackCopyEmail` functions |
| WhatsApp number | `https://wa.me/...` links |
| GitHub username for live stats | `username` variable in the "Live GitHub stats" script |
| Preloader duration | The `setTimeout(...,2000)` in the preloader script and the `ankh*` animation delays in CSS |
| Analytics ID | The `G-XXXXXXXXXX` value in the Google tag snippet in `<head>` |
| Project gallery images | The `G` object in the "Project galleries" script (folder name plus file names per project) |
| Add a gallery to a card | Add a `<span class="gallery-btn" data-gallery="key">` button, a `.project-thumb` block with `data-gallery="key"` and `data-start="N"` (the image index opened first), and a matching entry in `G` |
| Image base folders | `BASE` in the "Project galleries" script, and the `src` paths of thumbnails and certificates |
| Pyramid layers and quote | `NAMES` and `SEG` in the "Pyramid mini-game" script |
| Cursor shape | `#custom-cursor-dot` / `#custom-cursor-ring` SVGs in the body and the "Pyramid cursor" CSS block |

## Browser Support

Works in current versions of Chrome, Edge, Firefox, and Safari. Uses modern CSS (custom properties, grid, `clamp()`, `backdrop-filter`, `clip-path`), the Web Animations API, and `IntersectionObserver`.

> `.jfif` screenshots (Dynamic Dashboard) may not display in Safari. Renaming them to `.jpg` and updating their names in `G` fixes that.

## Contact

- **Email:** mostafasamerwork@gmail.com
- **LinkedIn:** [linkedin.com/in/mostafa-elsawahly](https://www.linkedin.com/in/mostafa-elsawahly)
- **GitHub:** [github.com/mostafa-elsawahly](https://github.com/mostafa-elsawahly)
- **Location:** Alexandria, Egypt

## License

© Mostafa Elsawahly. All rights reserved.

The code structure may be used as inspiration, but please do not copy the personal content, photo, or certificates. If you would like to reuse the layout, reach out first.
