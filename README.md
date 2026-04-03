# Sakhile Bhayi Website

This repository contains a single-page personal website for Sakhile Bhayi, an industrial intelligence architect focused on mining technology, fleet management systems, operational analytics, and AI-assisted decision support.

The site is built as a lightweight static webpage with no build step. It uses Tailwind CSS through the CDN, Google-hosted fonts, Material Symbols, and a hosted Web3Forms endpoint for contact form delivery.

## Overview

The website presents a professional profile and service offering for industrial and mining-focused digital consulting. It combines a strong editorial narrative with a high-contrast visual style and includes sections for:

- Hero introduction and positioning
- Operational capabilities and expertise
- Metrics and biography timeline
- Full professional profile
- Portfolio links and public presence
- Contact and project inquiry form

## Live Site Purpose

This website is designed to:

- Present Sakhile Bhayi's professional identity and domain focus
- Showcase expertise in mining systems, analytics, integration, and AI
- Provide a structured professional profile and portfolio summary
- Give visitors a direct way to submit project inquiries
- Support personal branding, credibility, and lead generation

## Tech Stack

- HTML5
- Tailwind CSS via CDN
- Vanilla JavaScript
- Google Fonts: Epilogue and Inter
- Google Material Symbols
- Web3Forms for contact form submission

## Project Structure

```text
.
├── index.html
├── logo.png
├── LICENSE
└── README.md
```

## How The Site Works

The entire website is contained in `index.html`.

### Styling

- Tailwind is loaded from the CDN rather than compiled locally
- A custom `tailwind.config` block extends colors, fonts, and border radii
- Additional inline CSS handles icon rendering, glow effects, smooth scrolling, and select styling

### Layout

The page is structured as a single scrolling experience with anchor-based navigation. It includes:

- A fixed top navigation bar for small and medium screens
- A mobile drawer menu for smaller devices
- A fixed left sidebar navigation on extra-large screens
- Multiple content sections with bold typography and dark industrial styling

### Interactivity

Vanilla JavaScript at the bottom of the page handles:

- Opening and closing the mobile navigation drawer
- Updating the active sidebar state using `IntersectionObserver`
- Submitting the contact form asynchronously to Web3Forms
- Basic client-side validation and status message display

## Page Sections

### 1. Home

The landing section introduces the brand positioning: industrial intelligence, mining systems, and architecture leadership.

### 2. Operational Logic Units

This section highlights service and capability categories such as:

- Fleet intelligence platforms
- Performance analytics
- AI decision support
- Industrial system integration

### 3. Metrics Of Momentum

Provides high-level experience signals such as years in industry, number of initiatives delivered, operating mindset, and regional base.

### 4. Biography

Presents a narrative timeline covering:

- Operational grounding
- Systems delivery
- Intelligence leadership

It also includes a short philosophy section around technical rigor and embedded intelligence.

### 5. Expertise

Describes technical and strategic capability areas in more detail, including operational platforms, analytics, AI, system integration, and technical infrastructure concepts.

### 6. Profile

This is the most detailed section of the site and includes:

- Contact details
- Professional summary
- Skills and proficiencies
- Certifications and interests
- Employment history
- Academic record
- Portfolio assets
- Public presence and external profiles
- Future actions and reference links

### 7. Contact

Contains:

- Availability and operating schedule
- Direct LinkedIn access
- A project inquiry form for visitors

### 8. Call To Action And Footer

Closes the experience with a collaboration prompt and minimal footer navigation.

## Contact Form Integration

The site uses Web3Forms for form submission.

### Current Behavior

- Form submission is sent to `https://api.web3forms.com/submit`
- Submission is performed with JavaScript using `fetch`
- Required fields are validated in the browser before submission
- Success and error panels are displayed inline
- A honeypot field is included to reduce bot spam

### Configured Hidden Fields

- `access_key`
- `subject`
- `from_name`
- `botcheck`

### Important Note

The current form configuration includes a live access key directly in `index.html`. For a static site this is common with third-party form services, but it should still be managed carefully. If the site is published publicly, monitor the form service dashboard for abuse and rotate the key if necessary.

## Running Locally

Because this is a static website, there is no installation step.

### Option 1: Open Directly

Open `index.html` in a browser.

### Option 2: Serve With A Local HTTP Server

Using a local server is preferable when testing assets, navigation behavior, and form integration.

If Python is available:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

This project can be deployed to any static hosting provider, including:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Amazon S3 with static website hosting

### Deployment Requirements

- `index.html` must remain at the site root
- `logo.png` must remain available at the root path
- External CDN access must be allowed for fonts, icons, and Tailwind
- The Web3Forms endpoint must remain reachable from the client browser

## External Dependencies

The website depends on external services loaded at runtime:

- Tailwind CDN
- Google Fonts
- Google Material Symbols
- Web3Forms API

If any of these services are unavailable, parts of the website may render incorrectly or lose functionality.

## Customization Guide

Common edits can be made directly in `index.html`.

### Update Branding

- Change the page title and meta tags in the `<head>`
- Replace `logo.png` with a new brand asset if needed
- Update hero copy, labels, and footer text

### Update Colors And Typography

- Edit the `tailwind.config` block in the `<script id="tailwind-config">` section
- Adjust the extended color tokens and font families
- Update inline CSS rules only when utility classes are not sufficient

### Update Content

Edit the relevant sections directly in the HTML for:

- Biography
- Experience
- Certifications
- Links
- Portfolio entries
- Contact details

### Update Contact Form Destination

If the form destination changes:

- Replace the Web3Forms `access_key`
- Update the hidden subject and sender fields if required
- Test success and failure states after the change

## Accessibility And UX Notes

The current site includes several strong UX choices:

- Responsive layouts for mobile, tablet, and desktop
- Fixed navigation patterns for different breakpoints
- High visual hierarchy with strong headings and section segmentation
- Inline status feedback for form submission
- Smooth scrolling for section navigation

Areas that can still be improved over time:

- Add a visible skip link for keyboard users
- Add stronger focus-visible states for all interactive elements
- Review heading hierarchy for assistive technology flow
- Test color contrast across all surface and text combinations
- Add reduced-motion handling for users who prefer less animation

## SEO Notes

The page already includes:

- A descriptive title
- Meta description
- Meta keywords
- Open Graph title and description
- Favicon

Possible future improvements:

- Add Open Graph image metadata
- Add canonical URL metadata
- Add structured data using JSON-LD
- Add Twitter card metadata
- Split repeated profile data into more search-friendly structured content if the site grows

## Maintenance Recommendations

To keep the site current:

- Review profile content monthly
- Keep links to projects and external profiles up to date
- Rotate or replace form keys if spam appears
- Periodically verify that external CDN dependencies still resolve correctly
- Recheck contact details and employment timeline as roles evolve

## Known Characteristics

- The site is intentionally implemented as a single static HTML document
- There is no package manager, bundler, or component framework in this repository
- Styling and behavior are centralized in one file for simplicity and portability
- The site requires internet access for external assets and hosted form submission

## License

This repository includes the MIT License. See `LICENSE` for details.

## Author

Sakhile Bhayi

- Website: https://sakhilebhayi.com
- GitHub: https://github.com/sakhileb
- ORCID: https://orcid.org/my-orcid?orcid=0009-0004-7055-0427
- LinkedIn: https://za.linkedin.com/in/sakhilebayi