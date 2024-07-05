# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

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

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

### Desktop website looks like this

![alt text](https://github.com/Gagana999/Create-Product-Card/blob/main/design/desktop-design.jpg)

### Mobile website looks like this

![alt text](https://github.com/Gagana999/Create-Product-Card/blob/main/design/mobile-design.jpg)

### Links

- Live Site URL: [Click me to go to live site](https://product-card-by-gagana.netlify.app/)

## My process

### Built with

- Make html structure
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Design desktop veiew

### What I learned

#### Creating a responsive perfume product card and uploading it to GitHub has been an enriching experience. Here are some key takeaways from the project:

- Responsive Design Principles: I gained a deeper understanding of responsive design, ensuring that the product card adapts seamlessly to different screen sizes and devices. This involved using CSS media queries and flexible 
  layouts to maintain usability and aesthetics across various platforms.

- HTML and CSS Proficiency: I honed my skills in HTML and CSS, learning how to structure the content and style it effectively. This project helped me understand the importance of semantic HTML for better accessibility and 
  search engine optimization.

- Flexbox and Grid Layouts: Implementing the layout using Flexbox and Grid significantly enhanced my ability to create complex and flexible designs. These CSS techniques allowed me to arrange elements dynamically and 
  responsively.

- Version Control with GitHub: Uploading the project to GitHub reinforced my knowledge of version control. I learned how to manage code versions, collaborate with others, and showcase my work through GitHub repositories.

### Here is the HTML Code that I created : 

```html
  <main>
    <article class="product">
      <picture>
        <source srcset="images\image-product-desktop.jpg" media="(min-width: 700px)">
        <img src="images/image-product-mobile.jpg" alt="perfume-product-icon">
      </picture>

      <div class="product-details">
        <p class="product-category">Perfume</p>
        <h1 class="product-title">Gabrielle Essence Eau De Parfum</h1>
        <p class="product-description">A floral, solar and voluptuous interpretation composed by Olivier Polge, 
          Perfumer-Creator for the House of CHANEL.</p>
        <div class="prices">
          <p class="product-price">$149.99</p>
          <p class="product-original-price">$169.99</p>
        </div>
        <button class="add-to-cart-button" data-icon="shopping-cart">Add to Cart</button>
      </div>
    </article>
  </main>
```

### Here is the css code that I created
```css
/* Custome Varibles */
:root{
     --primary-400: hsl(158, 36%, 37%);
     --primary-700: hsl(158, 36%, 17%);
     --secondary-200: hsl(30, 38%, 92%);

     --neutral-900: hsl(212, 21%, 14%);
     --neutral-400: hsl(228, 12%, 48%);
     --neutral-100: hsl(0, 0%, 100%);

     --fw-regular: 500;
     --fw-bold: 700;

     --ff-accent: 'Fraunces', serif;
     --ff-base: 'Montserrat', sans-serif;
}

/* CSS Reste */

*, *::before, *::after {
     box-sizing: border-box;
   }

* {
     margin: 0;
}

body {
     line-height: 1.7;
     -webkit-font-smoothing: antialiased;
}

img, picture, video, canvas, svg {
     display: block;
     max-width: 100%;
}

input, button, textarea, select {
     font: inherit;
}

p, h1, h2, h3, h4, h5, h6 {
     overflow-wrap: break-word;
}

#root, #__next {
     isolation: isolate;
}

/* General CSS */
body{
     font-family: var(--ff-base);
     font-weight: var(--fw-regular);
     font-size: 0.875rem;
     color: var(--neutral-400);
     background-color: var(--secondary-200);
}

main{
     width: 100%;
     min-height: 100vh;
     display: flex;
     align-items: center;
     justify-content: center;
}

.product{
     --gap: 1rem;
     margin: 1rem;
     background-color: var(--neutral-100);
     border-radius: .5rem;
     overflow: hidden;
     display: flex;
     flex-direction: column;
     max-width: 800px;
}

@media(min-width: 700px){
     .product{
          --gap: 2rem;
          width: 100%;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;
     }
     .product-details{
          width: 90%;
     }
}

.product-details{
     margin: 2rem;
     display: flex;
     flex-direction: column;
     gap: var(--gap);
}

.product-category{
     text-transform: uppercase;
     letter-spacing: 5px;
}

.product-title{
     font-size: 2rem;
     font-family: var(--ff-accent);
     color: var(--neutral-900);
     line-height: 1.1;
     font-weight: var(--fw-bold);
}

.product-description{
     font-size: .975rem;
}

.prices{
     display: flex;
     align-items: center;
     justify-content: start;
     gap: var(--gap);
}

.prices .product-price{
     color: var(--primary-400);
     font-size: 2rem;
     font-family: var(--ff-accent);
     font-weight: var(--fw-bold);
}

.prices .product-original-price{
     text-decoration: line-through;
}

.add-to-cart-button{
     background-color: var(--primary-400);
     color: var(--neutral-100);
     border-radius: .5rem;
     padding: 1rem 1.5rem;
     border: none;
     outline: none;
     font-size: .875rem;
     font-weight: var(--fw-bold);
     transition: background 1s linear;
     display: flex;
     align-items: center;
     justify-content: center;
     gap: 0.5rem;
}

.add-to-cart-button:is(:hover, :active){
     background-color: var(--primary-700);
}

.add-to-cart-button[data-icon="shopping-cart"]::before{
     content: "";
     width: 15px;
     height: 16px;
     background-image: url(images/icon-cart.svg);
}
```

### If you want to include fonts that I used to this project simply copy this code and paste inside your HTML file's Head tag :
<head>
  //Paste it here
</head>

```html
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght,SOFT,WONK@0,9..144,100..900,0..100,0..1;1,9..144,100..900,0..100,0..1&display=swap" rel="stylesheet">
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

## Author

- Name - NBG.Rantharu
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Linkdin - [@Gagana Rantharu]([https://www.twitter.com/yourusername](https://www.linkedin.com/in/gagana-rantharu-01a7092b5/overlay/about-this-profile/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3B9ueXI8LiSHKzK3XAJMD4qw%3D%3D))
