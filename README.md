<div align="center">
  <img width="1200" height="475" alt="Tanya Garg B.Arch Portfolio" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Tanya Garg — B.Arch Portfolio Website

This repository contains the interactive portfolio website for **Tanya Garg**, Bachelor of Architecture (B.Arch) graduate (June 2026). The site is built with a premium, architect-aligned aesthetic—featuring blueprint grid-paper layouts, sharp corners, geometric typography, CAD outline overlays, and a dynamic drawing gallery.

---

## 🚀 Key Features

* **Cyclic Image Carousels**: Projects containing multiple drawings (such as site plans, sections, and perspectives) display interactive left/right chevrons on hover to browse drawings in a cyclic loop.
* **Auto-Hiding Navigation Controls**: Single-image projects dynamically detect their image count and hide the navigation arrows on page load to keep the interface clean.
* **Fullscreen Lightbox Viewer**: 
  * Hovering over a project modal drawing displays a `zoom-in` cursor overlay.
  * Clicking the image expands it into a blurred-backdrop fullscreen overlay displaying the drawing in high resolution.
  * Chevrons are anchored on the sides of the screen to browse drawings inside fullscreen mode.
  * Clicking the fullscreen image displays a `zoom-out` cursor; clicking it exits fullscreen mode.
* **Two-Way State Synchronization**: Browsing drawings in fullscreen automatically updates the parent detail modal and the project card in the grid, maintaining navigation order across views.
* **Tab-Based Hash Routing**: Bookmarkable URL hash-links (`#hero`, `#about`, `#experience`, `#works`, `#competitions`, `#contact`) scroll and switch sections instantly without page reloads.
* **Works Catalog Filters**: Interactive category filtering (e.g. *Thesis*, *Internship*, *Studio*) with nested sub-category filtering (e.g. *Revit*, *Structural*, *Electrical*).

---

## 📁 Asset Directory Structure

All drawing assets must be placed inside the `public/assets/` directory under their respective folders. Ensure filenames match exactly (case-sensitive) to prevent deployment issues on Linux servers (like Render):

* 🎓 **Thesis (Mixed Use IT Park)**: `public/assets/thesis/` (`01.png`, `02.png`, `03.jpeg`, `04.png`)
* 💼 **MEP Revit Portfolio**: `public/assets/internship/revit/` (`01.jpeg`, `02.jpeg`, `03.png`)
* 🏘️ **Studio Township**: `public/assets/studio_township/` (`01.jpeg`, `02.png`)
* 🏨 **Zostel (The Wayfarer)**: `public/assets/visualizations/zostel/` (`Zostel 01.png`)
* 🏛️ **ARCHON Academy**: `public/assets/visualizations/architectural_institute/` (`01.png`, `02.png`)
* 🏗️ **Structural Drawings**: `public/assets/internship/structural/` (`01.png`, `02.png`, `03.png`)
* ⚡ **Electrical Design**: `public/assets/internship/electrical/` (`1.jpeg`)
* 🕌 **Bhakt Niwas (Competitions)**: `public/assets/competition/` (`Picture0.png` to `Picture3.png`)

---

## 💻 Local Development

**Prerequisites:** Node.js (v18+)

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Run the Development Server**:
   ```bash
   npm run dev
   ```

> [!TIP]
> **Windows PowerShell Execution Policy Security Error**: If you run into script execution errors when starting `npm run dev` in PowerShell, run it via the Command Prompt (`cmd`), or bypass the policy using:
> ```powershell
> powershell -ExecutionPolicy Bypass -Command "npm run dev"
> ```

---

## 🌐 Deploying to Render.com

To deploy this project to Render.com as a **Static Site** (direct CDN delivery):

1. Link your GitHub repository to a new **Static Site** on Render.
2. In the deployment settings, configure the build settings as follows:
   * **Build Command**: `npm run build`
   * **Publish Directory**: `dist`
3. Trigger a manual deploy. Vite will build the static pages and bundle your drawing assets into the `dist/` directory, which Render will serve at the root level.
