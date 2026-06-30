# 🧩 Sticker Photomosaic Creator & Cheatsheet Generator

A premium web-based tool to convert any source image into a stunning photomosaic made entirely out of Panini 2026 World Cup stickers. 

The application generates a detailed, coordinate-based grid map and a checklist, allowing you to physically reconstruct the mosaic using real stickers.

---

## 🚀 Live Demo / Features

* **Interactive Live Preview**: Hover over any sticker in the generated mosaic to identify the player, their team, and grid coordinates.
* **Dithering & Variety Algorithms**: Built-in Floyd-Steinberg error diffusion and repetition avoidance ensuring high-detail and diverse player distribution.
* **Excel Cheatsheet Export**: Generates a spreadsheet containing:
  1. A **Visual Grid Map** where cells are color-coded based on the sticker color and labeled with sticker IDs (e.g. `ARG_17`).
  2. A **Shopping Checklist** aggregating counts of how many of each sticker are needed to complete the physical mural.
* **Social Video Export**: Generates a smooth, zoom-out animation showing the mural assemble from a central point, ready to share on social media.

---

## 📖 How It Works

### 1. Match Engine
The application downsamples your uploaded image and matches each pixel's color profile to the average color of a Panini sticker in the database. 

For example, a cyan-blue pixel might match the **Argentina** kit:

<div align="center">
  <img src="ARG_17.png" alt="ARG_17 - Lionel Messi" width="100">
  <p><i>ARG_17 - Lionel Messi (used as a matching color tile)</i></p>
</div>

### 2. Assembly Animation
When you load an image, the app renders a radial spiral animation showing the stickers appearing cell-by-cell and scaling/flipping into place:

<div align="center">
  <img src="sticker_mural_reveal.gif" alt="Sticker Mural Assembly Reveal" width="480">
  <p><i>Mural assembly reveal animation</i></p>
</div>

---

## 🛠️ How to Run

### Locally (Double-click)
For general usage, simply double-click `index.html` to open it in your browser. All core logic, mosaic rendering, interactive tooltips, and Excel cheatsheet generator will work out-of-the-box!

### Locally (With Web Server)
Due to browser security protocols (CORS restriction), **video exports require a local web server to function.** 
1. If you are using VS Code, install the **Live Server** extension.
2. Right-click `index.html` and select **Open with Live Server**.

### GitHub Pages (Hosting)
This repository is optimized for GitHub Pages:
1. Push this folder to a new GitHub repository.
2. In repository settings, navigate to **Pages**.
3. Choose the branch (e.g. `main`) and folder (e.g. `/root`), then click **Save**.
4. Your photomosaic creator will be live at `https://<your-username>.github.io/<repo-name>/`.
