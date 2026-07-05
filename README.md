# The Admin Dashboard

This is the solution to the final project in [Intermediate HTML and CSS](https://www.theodinproject.com/lessons/node-path-intermediate-html-and-css-admin-dashboard) from [The Odin Project](https://www.theodinproject.com/).

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### Screenshot

![Desktop Screenshot](./desktop_screenshot.png)

### Links

- Solution URL: [Github Repository](https://github.com/jacobtitong/TOP-admin-dashboard)
- Live Site URL: [Github Live Pages](https://jacobtitong.github.io/TOP-admin-dashboard)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Grid
- [Josh Comeau's Modern CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/)

### What I learned

I learned that CSS Grid works very well for fixed, two-dimensional layouts, while Flexbox works well for layouts that are based on the content.

In this example, I used Grid for the main page structure and Flexbox for aligning items within smaller containers.

```css
body {
  display: grid;
  grid-template: 150px 1fr / 1fr 5fr;
  grid-template-areas: "sidebar header" "sidebar main";
}

.dashboard {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
```

I learned the importance of semantics. Though my implementation is not perfect, I still managed to make use of it by using tags like `<header>` and `<main>` to give the document better meaning.

Documentation is also very important. Using comments allowed me to separate my CSS into well-defined parts, making my code much easier to read and maintain.

Initially, setting the body's width to `100vw` added an unwanted horizontal scrollbar to my webpage. I learned that to fix this, I should set it to its default `100%` instead to cleanly remove it.

```css
body {
  width: 100%; /* Prevents the horizontal scrollbar */
  height: 100vh;
  margin: 0;
}
```

I realized that the contents of an element can actually go past a grid track if not handled properly. Being mindful of how content sizes affect defined grid areas is crucial to prevent the layout from breaking.

Instead of relying strictly on image files, I learned that you can download SVGs online and embed them directly into your HTML document. This makes it incredibly easy to style them with CSS later.

```html
<svg
  xmlns="[http://www.w3.org/2000/svg](http://www.w3.org/2000/svg)"
  viewBox="0 0 24 24"
>
  <path
    d="M10 21H14C14 22.1 13.1 23 12 23S10 22.1 10 21M21 19V20H3V19L5 17V11C5 7.9 7 5.2 10 4.3V4C10 2.9 10.9 2 12 2S14 2.9 14 4V4.3C17 5.2 19 7.9 19 11V17L21 19M17 11C17 8.2 14.8 6 12 6S7 8.2 7 11V18H17V11Z"
  />
</svg>
```

```css
/* Styling the embedded SVGs */
.dashboard svg {
  width: 45px;
  height: 45px;
  fill: white;
}
```

Using the repeat() function along with auto-fit or auto-fill allows for great responsive design. It automatically wraps my grid items without needing to write multiple media queries.

```css
/* Automatically sizing and wrapping grid items */
.project-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
```

[!NOTE]I also learned that git repositories CAN get CORRUPTED. Unfortunately, it happened to this project which made me lose all of old commits. Lesson learned: always push your commits once your done working at a certain point!

### Continued development

In the future, I'd like to get into CSS custom properties or variables and how to properly use them because I believe it will help me in the long run for collaborating with other developers and for future developments of older projects.

### Useful resources

- [Josh Comeau's Modern CSS Reset](https://www.joshwcomeau.com/css/custom-css-reset/) - This helped me stop overthinking of default styles from web browsers.
- [Material Icon Assets](https://pictogrammers.com/library/mdi/) - This is an amazing library of free-to-use SVGs which made my website look interesting.

## Author

- Github - [jacobtitong](https://github.com/jacobtitong)
- Linkedin - [Jacob Titong](https://www.linkedin.com/in/jacobtitong/)

## Acknowledgments

I'd like to give my gratitude to the Odin Project's community for being very supportive and helpful with feedbacks, especially in their [Discord server](https://discord.com/invite/fbFCkYabZB) which gave me a boost of motivation to keep learning through their curriculum.
