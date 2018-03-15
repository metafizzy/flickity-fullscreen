# Flickity fullscreen

_Enable fullscreen view for Flickity carousels_

## Install

### Manual

+ Add `fullscreen.js` to your scripts
+ Add `fullscreen.css` to your stylesheets

### Package managers

npm: `npm install flickity-fullscreen`

Bower: `bower install flickity-fullscreen`

## Initialize

Enable fullscreen behavior by setting `fullscreen: true` in Flickity options.

``` js
// jQuery
var $carousel = $('.carousel').flickity({
  fullscreen: true,
});
```

``` js
// vanilla JS
var flkty = $('.carousel').flickity({
  fullscreen: true,
});
```

``` html
<!-- HTML -->
<div class="carousel" data-flickity='{ "fullscreen": true }'>
  ...
</div>
```

## Style

`.is-fullscreen` is added to the carousel when fullscreen.

Size cells to take up full height with CSS.

```css
/* normal */
.carousel-cell {
  height: 200px;
}

/* fullscreen */
.carousel.is-fullscreen .carousel-cell {
  height: 100%;
}
```

## Methods

### viewFullscreen

Expand carousel to fullscreen.

``` js
// jQuery
$carousel.flickity('viewFullscreen');

// vanilla JS
flkty.viewFullscreen();
```

### exitFullscreen

Collapse carousel from fullscreen back to normal size & position.

``` js
// jQuery
$carousel.flickity('exitFullscreen');

// vanilla JS
flkty.exitFullscreen();
```

### toggleFullscreen

Expand or collapse carousel fullscreen view.

``` js
// jQuery
$carousel.flickity('toggleFullscreen');

// vanilla JS
flkty.toggleFullscreen();
```

---

By [Metafizzy](https://metafizzy.co) 🌈🐻
