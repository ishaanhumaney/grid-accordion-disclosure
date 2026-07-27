# Grid Accordion Disclosure

A simple pattern demonstrating smooth accordion collapse animations using native HTML structure and modern grid styling techniques.

---

## Overview

Animating height transitions on collapsible components has historically required either fixed pixel heights or custom JavaScript script calculations to compute target heights dynamically.

This project shows how to achieve height transitions down to `0fr` using CSS Grid on native `<details>` and `<summary>` elements. By pairing this with exclusive selection via the HTML `name` attribute, state management stays entirely within the browser's standard rendering tree.

---

## How It Works

1. **State Isolation**: Using the `name="faq-group"` attribute on HTML `<details>` elements creates exclusive toggle groups natively across modern browsers.
2. **Grid Interpolation**: The inner collapsible container uses `display: grid` with `grid-template-rows: 0fr`.
3. **Smooth Expansion**: When the open attribute changes (`details[open]`), the property transitions to `grid-template-rows: 1fr`.
4. **Child Overflow Guard**: The immediate inner container sets `min-height: 0` so child margins don't break grid sizing calculations.

---

## Key Features

* Zero layout shifts during height expansion or collapse.
* Built-in browser keyboard interaction and screen reader structure out of the box.
* Automatic exclusive toggle grouping via native HTML attributes.
* Configurable color and structural variables defined at root level.

---

## Tech Stack Breakdown

* **HTML5**: Leverages semantic disclosure widgets (`<details>`, `<summary>`).
* **CSS3**: Uses CSS Custom Properties alongside structural grid definitions.

---

## Prerequisites & Web-Based Quick Start

You can inspect, preview, and modify this repository directly inside your browser without installing local dependencies.

### Option A: Edit Directly on GitHub Web
1. Press `.` on your keyboard while viewing this repository to launch Visual Studio Code for the Web.
2. Edit `index.html` or `style.css` directly.
3. Use the Source Control sidebar tab to stage and commit changes.

### Option B: Run in GitHub Codespaces
1. Click the **Code** button at the top of the main repository page.
2. Select the **Codespaces** tab and click **Create codespace on main**.
3. Use the built-in live server extension or preview tool to view updates in real time.

### Option C: Local Execution
Clone the repository and open `index.html` in any browser:
```bash
git clone [https://github.com/your-username/grid-accordion-disclosure.git](https://github.com/your-username/grid-accordion-disclosure.git)
cd grid-accordion-disclosure
open index.html
```

## Repository Structure

```text
grid-accordion-disclosure/
├── .github/
│   └── workflows/
│       └── static-analysis.yml # HTML & CSS syntax validation workflow
├── .gitignore                  # Standard web ignore definitions
├── LICENSE                     # MIT open-source license text
├── README.md                   # Repository overview & instructions
├── index.html                  # Core markup structure
└── style.css                   # Grid animation rules and variables
```

## Roadmap

[ ] Add reduced-motion media query support to disable grid transitions gracefully.

[ ] Extend root token architecture for automated light and dark theme switching.

[ ] Add nested disclosure group examples.
