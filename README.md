# npm_responsive-media-queries


## Usage:

`The Breakpoint Mixin`
> `rmq_breakpoint()` mixin makes it easy to write media queries. You can use the named breakpoints, or a custom pixel, rem, or em value.
To use the mixin, call it with `@include`, and then include the CSS content you want inside the curly braces.
The behavior of the media query can be changed by adding the keyword `up`, `down` or `only` after the breakpoint value, separated by a space.
It's also possible to pass in `custom values`. You can enter a pixel, rem, or em value—all values are converted to em at the end.
Lastly, there are three special media queries that are not width-based: `portrait`, `landscape`, and `retina`. Using these keywords with the rmq_breakpoint() mixin will output a media query for device orientation or pixel density, rather than screen width.

```
.element {
  // Only affects medium screens and larger
  @include rmq_breakpoint(medium) {
    // All CSS in here goes inside the media query
  }
}
```

```
.element {
  // Only affects medium screens and smaller
  @include rmq_breakpoint(medium down) { }
  // Only affects medium screens, not small or large
  @include rmq_breakpoint(medium only) { }
}
```

```
.element {
  // Converted to 20em
  @include rmq_breakpoint(320px) { }
  // Unitless values are assumed to be pixels
  @include rmq_breakpoint(320) { }
  // Converted to 40em
  @include rmq_breakpoint(40rem) { }
}
```

```
.element {
  @include rmq_breakpoint(landscape) {
    // CSS for landscape-oriented devices only
  }
  @include rmq_breakpoint(retina) {
    // CSS for high-resolution displays only
  }
}
```

## Mixins:
```
@mixin rmq_aspect-ratio-iphone5-up()
@mixin rmq_aspect-ratio-iphone5()
@mixin rmq_aspect-ratio-iphone6()
@mixin rmq_aspect-ratio-iphone6plus()
@mixin rmq_aspect-ratio-ipad()
@mixin rmq_tv-down()
@mixin rmq_desktop-down()
@mixin rmq_tablet-down()
@mixin rmq_mobile-down()
@mixin rmq_ipad($pageOrientation)
@mixin rmq_ipad3($pageOrientation)
@mixin rmq_iphone4($pageOrientation)
@mixin rmq_iphone5($pageOrientation)
@mixin rmq_iphone6($pageOrientation)
@mixin rmq_iphone6plus($pageOrientation)
@mixin rmq_iphone6plus_only($pageOrientation)
@mixin rmq_samsung_galaxy_s3($pageOrientation)
@mixin rmq_samsung_galaxy_s4($pageOrientation)
@mixin rmq_samsung_galaxy_s5($pageOrientation)
```

## HTML Classes:
```
.rmq_samsung_galaxy_s5
.rmq_samsung_galaxy_s5-landscape
.rmq_samsung_galaxy_s5-portrait
.rmq_samsung_galaxy_s4
.rmq_samsung_galaxy_s4-landscape
.rmq_samsung_galaxy_s4-portrait
.rmq_samsung_galaxy_s3
.rmq_samsung_galaxy_s3-landscape
.rmq_samsung_galaxy_s3-portrait
.rmq_iphone6
.rmq_iphone6-landscape
.rmq_iphone6-portrait
.rmq_iphone6plus
.rmq_iphone6plus-landscape
.rmq_iphone6plus-portrait
.rmq_iphone5
.rmq_iphone5-landscape
.rmq_iphone5-portrait
.rmq_iphone4
.rmq_iphone4-landscape
.rmq_iphone4-portrait
.rmq_iphone3
.rmq_iphone3-landscape
.rmq_iphone3-portrait
.rmq_ipad
.rmq_ipad-landscape
.rmq_ipad-portrait
.rmq_hidden-xs-below
.rmq_hidden-xs-above
.rmq_hidden-sm-below
.rmq_hidden-sm-above
.rmq_hidden-md-below
.rmq_hidden-md-above
.rmq_hidden-lg-below
.rmq_hidden-lg-above
.rmq_hidden-xl-below
.rmq_hidden-xl-above
.rmq_hidden-xxl-below
.rmq_hidden-xxl-above
```

## Note:
> That the iPhone 5 does not have a 16:9 aspect ratio. It is in fact 40:71.

## Resources:
https://www.adobe.com/products/edge-inspect.html
http://caniuse.com/#feat=css-mediaqueries
https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
https://www.w3.org/TR/2002/CR-css3-mediaqueries-20020708/
http://andrew.hedges.name/experiments/aspect_ratio/
https://www.apple.com/iphone/compare/
