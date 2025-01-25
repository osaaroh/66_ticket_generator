# Conference ticket generator solution | Frontend Mentor

This is a solution to the [Conference ticket generator challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/conference-ticket-generator-oq5gFIU12w). 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- Complete the form with their details
- Receive form validation messages if:
  - Any field is missed
  - The email address is not formatted correctly
  - The avatar upload is too big or the wrong image format
- Complete the form only using their keyboard
- Have inputs, form field hints, and error messages announced on their screen reader
- See the generated conference ticket when they successfully submit the form
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

### Links

- Live Site URL: [live site URL](https://ticket-generator-o.netlify.app/)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

- Multiple css backgrounds:
- Dragover and drop background with js

```css
body {
  background-image: url("../images/pattern-squiggly-line-top.svg"), url("../images/pattern-circle.svg"), url("../images/pattern-lines.svg"), url("../images/pattern-squiggly-line-bottom-desktop.svg"), url("../images/pattern-circle.svg"), url("../images/background-mobile.png");
  background-repeat: no-repeat;
  background-position: right 55px, -17px -95px, center, left bottom, 70% 54%, right bottom;
  background-size: 300px, 190px, auto, 250px, 190px, cover;
  padding-bottom: 60px;
  min-height: 100vh;
}
```
```js
    // listening to the dragover event
    uploadContainer.addEventListener('dragover', function (e) {
        e.preventDefault();
    });

     // Dropping image
    uploadContainer.addEventListener('drop', function (e) {
        e.preventDefault();
        if (e.dataTransfer.files && e.dataTransfer.files.length > 0) {
            const file = e.dataTransfer.files[0];
            console.log(e.dataTransfer.files);
        }})
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

## Author

- Website - [Osaaroh](https://osaaroh.vercel.app/)
- Frontend Mentor - [@Osaaroh](https://www.frontendmentor.io/profile/osaaroh)
