# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

---

## Day 2 — Dynamic Footer Date

The website footer displays the current date in DD Mon YYYY format.

JavaScript generates the date automatically using the `Date` object. The date is displayed in the `deployDate` HTML element.

The copyright year is also updated automatically.

Example: `14 Oct 2026`

```javascript
const now = new Date();
const day = String(now.getDate()).padStart(2, "0");

document.getElementById("deployDate").textContent =
  day + " " + months[now.getMonth()] + " " + now.getFullYear();
```

Note: The date represents the current date when the page is viewed, not necessarily the last deployment date.