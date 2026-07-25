# Marie Marley – Author & Alzheimer’s Caregiver Advocate website  

A simple, responsive static site that showcases **Marie Marley, PhD** – her biography, books, upcoming releases, and contact information. The page is built with plain HTML + CSS (no framework) and includes SEO‑friendly meta tags, Open Graph/Twitter cards, and structured data (Schema.org JSON‑LD).

---  

## 📖 Overview  

| Feature | Description |
|--------|-------------|
| **Hero header** – Kansas‑city skyline with author name | Sets a visual tone and gives immediate branding. |
| **Book‑shelf carousel** | Displays covers of the four books (three published, one “Coming Soon”). |
| **Sticky navigation** | Home · About · Books · Contact – stays visible while scrolling. |
| **About / Bio section** | Portrait, credential line, and a concise narrative of Marie’s caregiving journey and career. |
| **Books section** | Card layout for each title, with cover image, description, Amazon purchase button, and “Read more” link. |
| **Upcoming book teaser** | Synopsis of the mystery novel *Silent Witness to Murder* (expected 2027) and a “Notify Me” email CTA. |
| **Contact form** | Simple mailto link for speaking‑engagements, media requests, or reader notes. |
| **Footer** | Quick navigation, copyright auto‑year script, and contact e‑mail. |
| **SEO & Social** | Title, meta description, keywords, canonical URL, Open Graph, Twitter Card. |
| **Schema.org JSON‑LD** | Person, Website, and Book entities for rich‑search results. |
| **Responsive typography** – Playfair Display & Lato via Google Fonts. |  

---  

## 🚀 Live demo  

- **URL:** https://www.mariemarley.com/  
- (If you clone the repo, just open `index.html` in a browser.)

---  

## 🛠️ Tech stack  

| Technology | Purpose |
|------------|----------|
| **HTML5** | Semantic markup (`<header>`, `<nav>`, `<section>`, `<article>`, etc.). |
| **CSS3** (`style.css`) | Layout, hero image, book‑shelf, responsive grid. |
| **Google Fonts** | Playfair Display & Lato for elegant typography. |
| **JSON‑LD** | Structured data for Person, Website, and Book entities. |
| **Meta tags** | SEO, Open Graph, Twitter Card. |
| **JavaScript** (tiny snippet) | Inserts current year in the footer. |

---  

## 📂 Repository structure  
/
│
├─ index.html            # Home page (the HTML you provided)
├─ style.css             # All styling for layout, typography & responsiveness
├─ README.md             # ← you are reading it!
│
├─ assets/               # (optional) place images here if you prefer a sub‑folder
│   ├─ kc-skyline-upscaled.png
│   ├─ Marie.jpg
│   ├─ cbet-cover.jpg
│   ├─ fjia-cover.jpg
│   └─ concerto-cover.png
│
└─ books/                # Individual book pages (already linked from index.html)
    ├─ come-back-early-today.html
    ├─ finding-joy-in-alzheimers.html
    └─ the-concerto.html


> **Tip:** If you move images into an `assets/` folder, update the `src` attributes accordingly.

---  

## ⚙️ Getting started (local preview)  

1. **Clone the repo**  
bash
   git clone https://github.com/your-username/marie-marley-site.git
   cd marie-marley-site

bash
   # With Python 3
   python -m http.server 8000
   # Then visit http://localhost:8000 in your browser


3. **Edit content**  

   - Update meta tags, book URLs, or copy text directly in `index.html`.  
   - For styling changes, edit `style.css`.  
   - New book cards can be added by copying an existing `<article class="book-card">` block and updating the fields.

---  

## 📦 Deployment  

Because it’s a static site, you can host it on any static‑file provider:

| Provider | Quick steps |
|----------|--------------|
| **GitHub Pages** | Push the repo to `gh-pages` (or set the repo’s default branch as the source). |
| **Netlify** | Connect the repo, Netlify will auto‑detect the `index.html`. |
| **Vercel** | Same as Netlify – just import the repo. |
| **Amazon S3 + CloudFront** | Upload the files to an S3 bucket, enable static‑website hosting. |

No build step is required – just serve the files as‑is.

---  

## 📝 Adding a new book  

1. **Create a new HTML file** under `books/` (e.g., `new-title.html`).  

2. **Add a card** in the “Books” section of `index.html`:

html
   <article class="book-card" itemscope itemtype="https://schema.org/Book">
     <div class="book-card-cover">
       <img src="NEW-COVER.jpg" alt="New Title book cover"
            itemprop="image" width="160" height="240" />
     </div>
     <div class="book-card-body">
       <h3 class="book-card-title" itemprop="name">New Title (202X)</h3>
       <p class="book-card-subtitle" itemprop="author"
          content="Marie Marley, PhD">Available in paperback and Kindle</p>
       <p class="book-card-desc" itemprop="description">
         <!-- short description -->
       </p>
       <div class="book-card-links">
         <a href="https://a.co/your-amazon-link"
            class="btn btn-primary" target="_blank" rel="noopener noreferrer">
           Buy on Amazon
         </a>
         <a href="books/new-title.html"
            class="btn btn-outline">Read more</a>
       </div>
     </div>
   </article>
   `
3. Add the book to the JSON‑LD block (inside <script type="application/ld+json">) so search engines can surface it.

🤝 Contributing
1. Fork the repository.  
2. Create a feature branch (git checkout -b feature/your‑feature).  
3. Make your changes, commit (git commit -m "Your message"), and push (git push origin feature/your‑feature).  
4. Open a Pull Request describing the changes.  

Please keep the HTML structure and class names consistent so the existing CSS continues to work.

📧
Contact  

• Email: contact@mariemarley.com  
• Speaking / Media inquiries: same address; the team will respond promptly.

