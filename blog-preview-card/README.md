# Frontend Mentor - Blog Preview Card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS), part of learning path [Getting started on Frontend Mentor](https://www.frontendmentor.io/learning-paths/getting-started-on-frontend-mentor-XJhRWRREZd).

## Table of contents

- [Overview](#overview)
  - [Learning goals](#learning-goals)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
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

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![Blog preview card desktop screenshot](./screenshots/desktop-screenshot.png)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/blog-preview-card-sDpAD9byf0](https://www.frontendmentor.io/solutions/blog-preview-card-sDpAD9byf0)

- Live Site URL: [https://amansgz.github.io/getting-started-on-frontend-mentor/blog-preview-card/index.html](https://amansgz.github.io/getting-started-on-frontend-mentor/blog-preview-card/index.html)

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
blog-preview-card/
|
|--- .gitignore
|--- README.md
|--- index.html
|--- css/
|    |--- base.css
|    |--- main.css
|    |--- tokens.css
|    |--- layout.css
|    |--- components/
|         |--- author.css
|         |--- card.css
|         |--- attribution.css
|--- assets/
|    |---fonts/
|    |---images/
|--- screenshots/ (screenshots for mobile, tablet and desktop views)
```

### Front-end Style Guide

#### Colors

```
- Yellow: hsl(47, 88%, 63%)
- White: hsl(0, 0%, 100%)
- Gray 500: hsl(0, 0%, 42%)
- Gray 950: hsl(0, 0%, 7%)
```

#### Font

- Font size (paragraph): 16px
- Family: `Figtree`
- Weights: `500`, `800` (medium, extrabold)

#### Layout

- **Mobile**: 320px - 768px
- **Tablet/Desktop**: 768px - 1440px
- **Desktop XL**: 1440px+

### What I learned

#### Semantic HTML Structure

The component uses a single-component architecture with the `article` element, which represents a self-contained, independent composition.

The card `<header>` contains introductory content (image in this case).

The `<div>` groups related content (post metadata, title, description).

The `<time>` tag represents a specific period in time. It's perfect for dates, times, or both.

The `<footer>` contains author information.

```html
<!-- Card blog -->
<article>
  <!-- Card header -->
  <header>
    <img
      src="./assets/images/illustration-article.svg"
      alt=""
      aria-hidden="true"
    />
  </header>

  <!-- Card content -->
  <div>
    <span> Learning </span>

    <div>
      <span>Published</span>
      <time datetime="2023-12-21"> 21 Dec 2023 </time>
    </div>

    <h2>
      <a href="#"> HTML & CSS foundations </a>
    </h2>

    <p>
      These languages are the backbone of every website, defining structure,
      content, and presentation.
    </p>
  </div>

  <!-- Card footer  -->
  <footer>
    <div>
      <img
        src="./assets/images/image-avatar.webp"
        alt="Avatar of Greg Hooper"
      />
      <p>Greg Hooper</p>
    </div>
  </footer>
</article>
```

#### CSS Structure

- Main stylesheet path in `index.html`

```html
<link rel="stylesheet" href="./css/main.css" />
```

`main.css` import stylesheets:

```css
/* 1. TOKENS - Variables */
@import "tokens.css";

/* 2. BASE - Global styles, reset, typography */
@import "base.css";

/* 3. LAYOUT - Page structure*/
@import "layout.css";

/* 4. COMPONENTS */
@import "components/card.css"; /* imports author */
@import "components/attribution.css";
```

#### CSS styles

Implemented a design system based on the Figma design and style guide, featuring:

- **CSS custom properties** for colors, font styles and elements spacing
- **Logical properties** for improved layout flexibility
- **rem units** for consistent and responsive scaling
- **prefers-reduced-motion media query** for accessibility

**Adaptive image cropping**: Using image container `height` and blog image `object-fit: cover` to show different image sections - a cropped portion on mobile vs. the complete image on desktop.

```css
.card__header {
  inline-size: 100%;
  block-size: 12.5rem;
}

.card__img {
  inline-size: 100%;
  block-size: 100%;
  object-fit: cover;
}
```

How to apply **stylish borders** to the card using `border` and `box-shadow`

```css
.card {
  border: 0.0625rem solid var(--clr-border);
  box-shadow: 0.5rem 0.5rem 0 0 var(--clr-gray-950);
}
```

## Author

- Frontend Mentor - [@amansgz](https://www.frontendmentor.io/profile/amansgz)
- Github - [@amansgz](https://github.com/amansgz)
