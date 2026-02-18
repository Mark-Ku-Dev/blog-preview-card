# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./preview.jpg)

Add a screenshot of your solution when you have one (e.g. take a full-page or cropped screenshot in Firefox, or use a tool like [FireShot](https://getfireshot.com/)). Save it as `screenshot.jpg` or `preview.jpg` and update the path above if needed.

### Links

- Solution URL: [Add solution URL here](https://www.frontendmentor.io/solutions)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox for layout
- Plain CSS (no frameworks)

### What I learned

This challenge helped me build a clear **mental workflow for using Flexbox to create cards**: think of the card as a flex container with `flex-direction: column` and `gap` to stack sections, then use nested flex containers for any row (e.g. the author row). That “container → direction → alignment → gap” mindset made the layout much easier to reason about.

Two highlights:

**1. Vertically aligning the text next to the user’s avatar**

The author block (avatar + name) is a row of items that need to sit on the same baseline. I made the author section a flex container and used `align-items: center` so the image and text align vertically:

```css
.card_info {
  display: flex;
  align-items: center;
  gap: 10px;
}
```

**2. Creating the “Learning” badge**

I wanted a small pill-style label that didn’t stretch full width. Using `display: inline-block` on the badge let it size to its content, and padding + border-radius gave it the badge look:

```css
.card_about .badge {
  background-color: hsl(47, 88%, 63%);
  padding: 6px 12px;
  border-radius: 4px;
  font-weight: 800;
  font-size: 16px;
  display: inline-block;
  margin-bottom: 10px;
}
```

### Continued development

- Practicing focus states for accessibility (keyboard navigation).
- Refining the Flexbox workflow on more card-style layouts.
- Experimenting with responsive spacing (e.g. relative units) for different screen sizes.

### Useful resources

- [MDN: Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) – Clear explanation of flex containers and alignment.
- [CSS-Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) – Visual reference for Flexbox properties.
