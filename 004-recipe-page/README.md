# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

### Screenshot

![](./screenshot.png)

### Links

- [Solution URL](#)
- [Live Site URL](https://tomhaeck.github.io/frontendmentor.io/004-recipe-page/)

## My process

### Built with

- HTML
- CSS custom properties
- CSS Flexbox

### What I learned

The way how the text is structured follows as close as possible how it is defined 
by the Figma file.  For instance, the `<h1>` element 'Simple Omelette Recipe'
is grouped together with the paragraph below ('An easy and quick dish [...]'),
because it is also grouped together in the Figma file.  This allows for easier
translation of the spacings from Figma to HTML/CSS.

The HTML5's semantic elements `<main>` and `<section>` were used.

Color variables like e.g. `--white: hsl(0, 0%, 100%)`, described in the style-guide
are declared in a `:root` element for global scoping.

Do not forget a CSS reset for e.g. `box-sizing`, `padding` and `margin`.

Define font properties that are mostly used in the document, like `font-weight`, `font-size`
and `letter-spacing` and `line-height`, as generally as possible, 
like e.g. in the body.  These can be overwritten for specific
paragraphs if needed.  This is the principle of *Cascaded* style sheets!

If the `.attribution` section is positioned absolutely (`position: absolute`) 
with respect to the body, the body needs to have the property  `position: relative` (or analogous).

Items in an `<ul>` or `<ol>` list can be spaced by declaring it a flex container.

The bullet point markers of an `<ul>` or `<ol>` list can be targeted e.g. as follows:
`ul li::marker`.  `::marker` is a pseudo-element, as compared to e.g. `:hover` which is 
a pseudo-class.

Do not shy away from using ad hoc's `margin-bottom` instead of declaring everything a flex container
to control spacing.

The margins defined by Figma sometimes do not correspond to the ones from the 
`{desktop|mobile}-design.jpg`.  E.g. Figma specifies a top margin of 128px between 
the top and the recipe-card, whereas I measure 122px from the design jpg.  Same goes 
for the space between the recipe image and title.

It is possible to drill down an HTML hierachy using CSS selectors as follows:
`.recipe-preparation-time ul li::marker`.

If a table has `border-collapse: collapse`, there are no gaps between cells.
Borders in a table are specified by declaring borders on the constituing `<th>` and `<td>` elements.
The first and last row's cells can be selected as follows.
```css
tr:first-child th, tr:first-child td {
    border-top: unset;
    padding-top: 0;

}

tr:last-child th, tr:last-child td {
    border-bottom: unset;
    padding-bottom: 0;
}
```

Use media queries to change the layout for mobile screens.  For the mobile design, 
the recipe image extends beyond its container by using negative margins.
Note also the use of the CSS built-in `calc()` function:
```css
@media all and (max-width: 500px) {
    h1 {
        font-size: 36px;
    }
    .recipe-image img {
          width: calc(100% + 2*32px);
          border-radius: 0px;
          /* Negative margins allow elements to go outside the
           bounds of the parent element */
          margin: -40px -32px 36px -32px;
      }
}
```

## Author

- Website - [Tom Haeck](https://github.com/tomhaeck)
- Frontend Mentor - [@tomhaeck](https://www.frontendmentor.io/profile/tomhaeck)
