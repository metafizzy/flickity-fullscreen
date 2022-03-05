# Flickity fullscreen

_Enable fullscreen view for Flickity carousels_

## Install

Add `fullscreen.css` to your stylesheets and `fullscreen.js` to your scripts.

### Download

+ [fullscreen.css](https://unpkg.com/flickity-fullscreen@2/fullscreen.css)
+ [fullscreen.js](https://unpkg.com/flickity-fullscreen@2/fullscreen.js)

### CDN

``` html
<link rel="stylesheet" href="https://unpkg.com/flickity-fullscreen@2/fullscreen.css">
```

``` html
<script src="https://unpkg.com/flickity-fullscreen@2/fullscreen.js"></script>
```

### Package managers

npm: `npm install flickity-fullscreen`

Yarn: `yarn add flickity-fullscreen`

## Usage

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

### Webpack

``` js
const Flickkty = require('flickity');
require('flickity-fullscreen');

var flkty = new Flickity( '.carousel', {
  fullscreen: true,
});
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

## Events

### fullscreenChange

Triggered after entering or exiting the fullscreen view.

``` js
// jQuery
$carousel.on( 'fullscreenChange.flickity', function( event, isFullscreen ) {...} );

// vanilla JS
flkty.on( 'fullscreenChange', function( isFullscreen ) {...} );
```

 - `event` · _Event_ · jQuery `event` object
 - `isFullscreen` · _Boolean_ · `true` if viewing fullscreen, `false` if exiting fullscreen

---

By [Metafizzy](https://metafizzy.co) 🌈🐻
