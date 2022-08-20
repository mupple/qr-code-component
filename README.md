# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Overview

### Screenshot

![](./1440x1024_screenshot.png)

### Links

- [Solution](https://github.com/mupple/qr-code-component)

## My process

I don't (yet) have a Pro subscription to Frontend Mentor; dimensions and spacing are therefore determined by inspection, trial and error. To facilitate this, I set the design file (e.g. '`desktop-design.jpg`') from the downloadable materials as the `background-image` on the `body` and setting the `opacity` of the component to `.3` or `.4`. At times, instead of making the qr component partially transparent, I set the `mix-blend-mode` on the component to `difference`.

```css
body {
  background-image: url('./design/desktop-design.jpg');

  ...
}

.qr {
  opacity: .3;

  /* or */

  mix-blend-mode: difference;

  ...
}
```

From there, various aspects of the design can be determined by trial and error much more efficiently.

Turning to the design itself, the three blocks (image, header and body text) in a column lend themselves to a flexbox column layout.

Colours, and font information are specified in custom properties on the `:root`, named with a `qr-` prefix to show that they relate to the qr component.

A very modest reset (`margin`, `padding` and `box-sizing`) is set on the `.qr` wrapper, in case they are not set on the page in which the component is to be used.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What's still bugging me

The challenge material specifies the body copy font size as 15px. I established this by setting font sizes for the component (in rem), assuming the default root font size of 16px. But should I have set the font size explicitly in px on the component (and perhaps in em for the header)? This would avoid changes in the root font size affecting the component. But you might want them to affect the component.

I think I'm happy with my decision on this, but would be interested in views as to best practice on this sort of thing when designing/implementing components.


## Author

- Frontend Mentor - [@mupple](https://www.frontendmentor.io/profile/mupple)
- Twitter - [@mupple](https://www.twitter.com/mupple)

## Acknowledgments

Huge thanks to Kevin Powell for everything he puts out, particularly on [YouTube](https://www.youtube.com/kepowob/). I hope you're proud, Kevin. You've done a huge amount to help an enormous number of people.
