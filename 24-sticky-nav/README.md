# Key Points

## Vertical offsets and scroll

* `element.offsetTop` represents how far down (in pixels) our element is from the top of the page.
* `window.scrollY` represents how far down (in pixels) we've scrolled from the top of the page.

## The `scroll` event

```js
window.addEventListener('scroll', cb);
```

## Animating the width of an element with CSS using transitions

You cannot animate the width of something using CSS. So instead of using:

```css
.logo {
  width: 0;
}

.fixed-nav .logo {
  width: auto;
}
```

you need to do:

```css
.logo {
  max-width: 0;
  overflow: hidden;
  transition: all 0.5s;
}

.fixed-nav .logo {
  max-width: 500px; /* just pick ANY width larger than the actual element */
}
