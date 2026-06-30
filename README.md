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
