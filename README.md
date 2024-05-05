# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

Small-Screen Design        |  Large-Screen Design
:-------------------------:|:-------------------------:
![](./implementation%20result/small%20screen.png)  |  ![](./implementation%20result/large%20screen.png)

### Links

- Solution URL: [Github Repo](https://github.com/Twixii99/FEM-Testimonials-grid)
- Live Site URL: [Live website](https://twixii99.github.io/FEM-Testimonials-grid/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow

### What I learned

1. using grid-template-areas and adjust areas depending on screen size.
2. using of grid-auto-column: 1fr; to decide the default size of grid column. (specifying the size of the grid columns that were created without having an explicit size)
```css
.testimonial-grid {
  max-width: 100%;

  display: grid;
  grid-auto-columns: 1fr;
  gap: var(--vertical-spacing) var(--horizontal-spacing);

  grid-template-areas: "one" "two" "three" "four" "five";
}

/* meduim screens */
@media screen and (min-width: 768px) {
  .testimonial-grid {
    grid-template-areas: "one one" "two three" "four three" "five five" ;
  }
}

/* large screens */
@media screen and (min-width: 992px) {
  .testimonial-grid {
    grid-template-areas: "one one two" "three three three" "four five five" ;
  }
}

/* larger screens */
@media screen and (min-width: 1200px) {
  .testimonial-grid {
    grid-template-areas: "one one two three" "four five five three" ;
  }
}
```

### Continued development

- using SASS preprocessor instead of pure CSS.

## Author

- Website - [Mahmoud Kamal](https://www.linkedin.com/in/mahmoud-kamal-120176169/)
- Frontend Mentor - [@Twixii99](https://www.frontendmentor.io/profile/Twixii99)
- Twitter - [@MkBayumi](https://twitter.com/MkBayumi)