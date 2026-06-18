# Rise & Invest

**The education your school never offered.**

The website for [Rise & Invest](https://riseandinvest.org) — personalized courses and 1:1 coaching on the skills schools skip: college admissions, careers, AI, and investing. Taught by Dylan Gutowski (Cornell Dyson '29).

> There's a gap between what most programs teach and what actually moves the needle. I teach the version I wish I'd had.

What started as a free financial literacy workshop series — 100+ students taught across 3+ countries — is now a full coaching practice with 12 active courses.

## What's offered

**Three booking tracks:**

| Track | Format |
|---|---|
| College Counseling | Full-service 1:1 |
| 1:1 Master Class | Private session on any topic |
| Group Master Class | Group session, 4–10 students |

**12 courses across three areas:**

- **College Prep** — College Apps 101, SAT 101, College Resume 101, The Insider's Playbook
- **Career & Finance** — Internships & Opportunities 101, Interview Prep 101, LinkedIn 101, Investing 101
- **AI & Tech** — AI for Real Life, AI for School, Claude Advanced, AI Website Builder

## The site

A static, multi-page site — no framework, no build step. Just hand-built HTML, CSS, and a touch of JavaScript.

```
index.html          # entry point (copy of home.html, required at Netlify root)
home.html           # landing page
master-classes.html # course catalog
about.html          # founder story & approach
book.html           # booking form
_redirects          # Netlify routes (/ → home, /services → master-classes, /booking → book)
og-image.jpg        # social preview (1200×630)
favicon.png, dylan.jpeg, cornell.png, teaching.jpg
```

### Design system

- **Type** — Cormorant Garamond (headings) + DM Sans (body)
- **Color** — dark forest hero gradient with `--green: #1A9E72` accent
- **Layout** — max-width 1400px, fluid `clamp()` typography
- **Motion** — `IntersectionObserver` fade-up reveals on scroll

## Running locally

It's static, so any local server works:

```bash
python3 -m http.server 8080
# http://localhost:8080
```

## Deploying

Hosted on **Netlify**. The booking form uses built-in [Netlify Forms](https://docs.netlify.com/forms/setup/) — submissions post via AJAX and show inline confirmation (no redirect), and are visible in the Netlify dashboard under **Forms**. Routing is handled by `_redirects`. Live at **riseandinvest.org**.

## Roadmap

- Real testimonials section
- Analytics (Plausible)
- Stripe payments + Calendly scheduling
- Per-course landing pages
