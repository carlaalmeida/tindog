# TinDog

This repository contains the code for the landing page promoting the fictional TinDog mobile app.

## Overview

### The project

This project is featured in [The Complete 2023 Web Development Bootcamp](https://www.udemy.com/course/the-complete-web-development-bootcamp/) as an introduction to Bootstrap 4. So it may be the case you've seen other similar repos around.

I took this course in 2020, and since then I was able to improve my Web Development skills (at least, I like to believe I did).

I decided to revisit this project and apply some best practices such as using semantic HTML and a mobile-first approach.

### Links

- Live Site URL: [TinDog](https://carlaalmeida.github.io/tindog/)

## My process

### Built with

- Semantic HTML5 Markup
- Bootstrap 4.4
- Mobile-first workflow

### What I Learned

As stated before, the skeleton for this project was built in 2019 as part of the then-called [The Complete 2020 Web Development Bootcamp](https://www.udemy.com/course/the-complete-web-development-bootcamp/) and it used Bootstrap and plain CSS.

When I first worked on this project I was just starting to learn Bootstrap and my CSS skills were not so strong. Back then, this project really helped me to get familiar with **Bootstrap** and using **media queries**.

In the course, we used some of Bootstrap's classes to help with the page's layout, such as `container-fluid`, `row`, `col` `navbar`, or `carousel`. Later, when browsing the documentation myself, I found many others that I could use. For example, the `d-flex` or the spacing utilities to standardize the spacing on the page:

```html
<div class="container-fluid colored-section pt-lg-5 pb-lg-0">...</div>
```

In this second revision, I tried to apply the knowledge that I've been collecting for the last few years but kept the original idea and design. This allowed me to look at my code from a different perspective. As it has been over two years, it was like I was looking at someone else's code, which is always fun!

I changed the `styles.css` to comply with a mobile-first approach, instead of the original desktop-first. This also implied a revision of the media queries breakpoints.

Take a look at the code I had before for the `.title-image`:

```css
.title-image {
  -ms-transform: rotate(20deg);
  /* IE 9 */
  transform: rotate(20deg);
  width: 60%;
  position: absolute;
  right: 30%;
}

@media (max-width: 991px) {
  .title-image {
    position: static;
    -ms-transform: rotate(0);
    /* IE 9 */
    transform: rotate(0);
  }
}
```

Now I have this:

```css
.title-image {
  width: 60%;
}

@media (min-width: 992px) {
  .title-image {
    -ms-transform: rotate(20deg);
    /* IE 9 */
    transform: rotate(20deg);
    position: absolute;
    right: 30%;
  }
}
```

This is a good example of why mobile-first makes more sense in projects like this. We don't need to override the `transform` and `position` properties for mobile.

### Useful resources

- [Bootstrap 4.4](https://getbootstrap.com/docs/4.4/getting-started/introduction/)
- [Font Awesome](https://fontawesome.com/)

## Acknowledgments

- [Dr. Angela Yu](https://github.com/angelabauer) for creating the [The Complete Web Development Bootcamp](https://www.udemy.com/course/the-complete-web-development-bootcamp/) and all the challenges throughout the course, including this one.
