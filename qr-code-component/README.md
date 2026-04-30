# Frontend Mentor | QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H), part of learning path [Getting started on Frontend Mentor](https://www.frontendmentor.io/learning-paths/getting-started-on-frontend-mentor-XJhRWRREZd).

## Table of contents

- [Overview](#overview)
  - [Learning goals](#learning-goals)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Project Structure](#project-structure)
  - [Front-end style guide](#front-end-style-guide)
    - [Colors](#colors)
    - [Font](#font)
    - [Layout](#layout)
  - [What I learned](#what-i-learned)
    - [Semantic HTML Structure](#semantic-html-structure)
    - [CSS structure](#css-structure)
    - [CSS styles](#css-styles)
- [Author](#author)

## Overview

### Learning Goals

- Master semantic HTML structure
- Improve CSS layout techniques (Flexbox)
- Build responsive components that work on all devices

### The challenge

The challenge was to build out this QR code component and get it as close as possible to the original design.

### Screenshot

![Desktop screenshot for the QR code component solution](./screenshots/desktop-screenshot.png)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/card-component-built-with-css-custom-properties-krZg583OIP](https://www.frontendmentor.io/solutions/card-component-built-with-css-custom-properties-krZg583OIP)

- Live Site URL: [https://amansgz.github.io/getting-started-on-frontend-mentor/qr-code-component/index.html](https://amansgz.github.io/getting-started-on-frontend-mentor/qr-code-component/index.html)

## My process

### Built with

- Semantic HTML5 markup
- BEM Methodology
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Figma design

### Project Structure

```
qr-code-component/
|
|--- .gitignore
|--- README.md
|--- index.html
|--- CSS/
|    |--- base.css
|    |--- main.css
|    |--- tokens.css
|    |--- layout.css
|    |--- components/
|         |--- card.css
|         |--- attribution.css
|--- IMAGES/
|--- SCREENSHOTS/ (screenshots for mobile, tablet and desktop versions)
|--- DESIGN
```

### Front-end Style Guide

#### Colors

```
- White: hsl(0, 0%, 100%)
- Slate 300: hsl(212, 45%, 89%)
- Slate 500: hsl(216, 15%, 48%)
- Slate 900: hsl(218, 44%, 22%)
```

#### Font

- Font size (paragraph): 15px
- Family: `Outfit`
- Weights: `400, 700` (regular, bold)

```html
<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;700&display=swap"
  rel="stylesheet"
/>
```

#### Layout

- **Mobile**: 320px - 768px
- **Tablet/Desktop**: 768px - 1440px
- **Desktop XL**: 1440px+

### What I learned

#### Semantic HTML Structure

The component uses a single-component architecture with the `article` element, which represents a self-contained, independent composition.

```html
<article>
  <img
    src="./images/image-qr-code.png"
    alt="Scan this QR code to visit the Frontend Mentor website"
  />
  <h2>Improve your front-end skills by building projects</h2>
  <p>
    Scan the QR code to visit Frontend Mentor and take your coding skills to the
    next level
  </p>
</article>
```

#### CSS Structure

- Main stylesheet path in `index.html`

```html
<link rel="stylesheet" href="./css/main.css" />
```

`main.css` imports stylesheets:

```css
/* 1. TOKENS - Variables */
@import "tokens.css";

/* 2. BASE - Global styles, reset, typography */
@import "base.css";

/* 3. LAYOUT - Page structure*/
@import "layout.css";

/* 4. COMPONENTS */
@import "components/card.css";
@import "components/attribution.css";
```

#### CSS styles

Implemented a design system based on the Figma design and style guide, featuring:

- **CSS custom properties** for colors, font styles and elements spacing
- **Logical properties** for improved layout flexibility
- **rem units** for consistent and responsive scaling

## Author

- Frontend Mentor - [@amansgz](https://www.frontendmentor.io/profile/amansgz)
- Github - [@amansgz](https://github.com/amansgz)
