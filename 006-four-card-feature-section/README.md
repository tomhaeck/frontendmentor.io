# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you to improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

### Links

- [Solution URL](https://your-solution-url.com)
- [Live Site URL](https://your-live-site-url.com)

## My process

### Built with

- HTML
- CSS custom properties
- CSS Flexbox

### What I learned

Although the layout of the cards is 2D-ish for larger viewports, I chose to use CSS Flexbox instead of CSS Grid.  I wanted to use tools that are as basic as possible.  CSS Flexbox is used to horizontally center the content in the page, and to layout the four cards.  The 2D card layout is mimicked using nested flex containers.

CSS variables are declared with a global scope in a `:root` pseudo-class.

A very basic CSS reset is done as follows
```css
*, *::before, *::after {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}
```

CSS properties are declared 'as high as possible as much as possible', e.g. the body contains properties that are inherited by all elements.

The very limited responsive behavior is implemented using a `max-width: 500px` media query:
```css
@media all and (max-width: 500px) {
    header {
        width: 311px;
    }
}
```
Note that this behavior is limited in the sense that the implementation mimics
as good as possible both the mobile viewport design at 375px wide and the desktop viewport design at 1440px, but the page does not provide a good user experience for widths that are in between.  
This implementation is what Andy Bell describes in [his talk](https://www.youtube.com/watch?v=5uhIiI9Ld5M) as 'pixel-pushing': it resembles as good as possible the Figma design at only 
two discrete viewpoints, ignoring all other viewports.  

The font sizes are not fluid and do not follow
a scale either.  The implementation also does not follow Andy Bell's CubeCSS, where the CSS is conceptually separated into Global CSS, Compositions, Utilities, Blocks and Exceptions.  

I hope this is the last 'pixel-pushing' solution I have implemented, and will provide a real responsive
solution soon.

## Author

- Website - [Tom Haeck](https://github.com/tomhaeck)
- Frontend Mentor - [@tomhaeck](https://www.frontendmentor.io/profile/tomhaeck)
