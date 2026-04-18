# Sakhile Bhayi Website

![Sakhile Bhayi Logo](./logo.png)

Personal single-page website for Sakhile Bhayi, focused on industrial intelligence, mining technology, operational analytics, and AI-assisted decision support.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Sections Included](#sections-included)
- [Contact Form Integration](#contact-form-integration)
- [Run Locally](#run-locally)
- [Deployment](#deployment)
- [Customization](#customization)
- [Accessibility and SEO](#accessibility-and-seo)
- [Maintenance Checklist](#maintenance-checklist)
- [License](#license)
- [Author](#author)

## Overview

This repository contains a lightweight static website built around a professional profile and consulting value proposition for mining and industrial systems.

The website is designed to:

- Present a clear professional identity and technical focus
- Showcase capabilities across operations, analytics, integration, and AI
- Provide a detailed profile section with experience and portfolio links
- Offer a direct inquiry channel through a hosted contact form

## Features

- Single-page responsive layout
- Fixed and mobile-aware navigation
- Structured sections for profile, expertise, and credentials
- Interactive contact form with inline success/error feedback
- Clean static deployment with no build step

## Tech Stack

- HTML5
- Tailwind CSS (CDN)
- Vanilla JavaScript
- Google Fonts
- Google Material Symbols
- Web3Forms API for contact submissions

## Project Structure

```text
.
├── index.html
├── logo.png
├── LICENSE
└── README.md
```

## How It Works

The full application is implemented in `index.html`.

- Styling: Tailwind CDN plus a custom in-page configuration and utility CSS
- Layout: section-based single page with anchor navigation
- Behavior: JavaScript handles mobile nav, active section tracking, and form submission

## Sections Included

The page includes:

- Home / hero introduction
- Operational logic units (services and capabilities)
- Metrics and impact highlights
- Biography and philosophy
- Expertise details
- Full profile (skills, history, education, links)
- Contact and project inquiry form
- Closing call-to-action and footer

## Contact Form Integration

Form requests are sent to:

`https://api.web3forms.com/submit`

Current implementation details:

- Uses browser `fetch` for asynchronous submission
- Performs basic required-field validation
- Displays inline success and error messages
- Includes a honeypot field to reduce spam

Configured hidden fields include:

- `access_key`
- `subject`
- `from_name`
- `botcheck`

Security note:

For static websites, exposing a third-party form access key in client code is common, but you should monitor submissions and rotate the key if abuse occurs.

## Run Locally

No installation is required.

Option 1: open `index.html` directly in a browser.

Option 2: serve locally for more realistic testing:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

This project can be hosted on any static platform, including:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Amazon S3 Static Website Hosting

Deployment requirements:

- Keep `index.html` at the site root
- Keep `logo.png` at the site root
- Allow runtime access to external CDNs and Web3Forms endpoint

## Customization

Most edits are made directly in `index.html`.

Common updates:

- Branding: title, hero copy, and logo asset
- Visuals: Tailwind config colors, fonts, spacing, and radius tokens
- Content: biography, profile data, links, and portfolio entries
- Form settings: access key, subject, and sender values

## Accessibility and SEO

Current strengths:

- Responsive layouts across breakpoints
- Clear visual hierarchy and segmented sections
- Inline status feedback for form interactions

Recommended improvements:

- Add a skip link for keyboard navigation
- Improve focus-visible styles for all interactive controls
- Review heading levels for assistive technologies
- Add OG image, canonical URL, and Twitter card metadata
- Consider JSON-LD structured data for profile content

## Maintenance Checklist

- Review profile and portfolio details monthly
- Verify outbound links and social profiles
- Monitor contact form submissions for spam
- Rotate form key if misuse is detected
- Recheck third-party dependency availability

## License

Released under the MIT License. See `LICENSE` for details.

## Author

Sakhile Bhayi

- Website: https://sakhilebhayi.com
- GitHub: https://github.com/sakhileb
- ORCID: https://orcid.org/my-orcid?orcid=0009-0004-7055-0427
- LinkedIn: https://za.linkedin.com/in/sakhilebayi