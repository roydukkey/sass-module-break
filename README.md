# sass-break

[![Release Version](https://img.shields.io/npm/v/sass-break.svg)](https://www.npmjs.com/package/sass-break)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

This Sass module provides mixins, functions, and variables for working with breakpoints and aids in responsive development.

**Important:** [sass-break v1](//github.com/roydukkey/sass-module-break/tree/1.x.x) will continue to provide an API similar to Bootstrap v5.

## Install

* Dart Sass: `>=1.33.0`

Install the package:

```bash
npm install sass-break
```

Use the package like any other Sass module:

```scss
@use 'sass-break';
```

Depending on your setup, you may need to configure `node_modules` as include path:

```js
const sass = require('sass');

sass.render({
  file: scss_filename,
  includePaths: ['node_modules']
});
```

## Public API

### Horizontal Breakpoints

#### Variables

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_horizontal-sizes.sass"><code>$horizontal-sizes !default</code></a></dt>
  <dd>A configurable map defining the dimensions at which layout will change, adapting to different screen widths, according to media queries.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_horizontal-sizes.sass"><code>$horizontal-names</code></a></dt>
  <dd>A list of sorted horizontal breakpoint names.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_horizontal-sizes.sass"><code>$horizontal-values</code></a></dt>
  <dd>A list of sorted horizontal breakpoint values.</dd>

</dl>

#### Mixins / Functions

Mixins apply a media query rule to the provided content. Functions generate a media query rule for the as a string.

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_out.sass"><code>out ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given horizontal breakpoint and wider.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_in.sass"><code>in ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given horizontal breakpoint and narrower.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_in-between.sass"><code>in-between ( $first-breakpoint, $second-breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given horizontal breakpoints which is equal and wider than the smaller, and equal and narrower than the larger.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_in-only.sass"><code>in-only ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given horizontal breakpoint.</dd>

</dl>

### Vertical Breakpoints

#### Variables

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_vertical-sizes.sass"><code>$vertical-sizes !default</code></a></dt>
  <dd>A configurable map defining the dimensions at which layout will change, adapting to different screen heights, according to media queries.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_vertical-sizes.sass"><code>$vertical-names</code></a></dt>
  <dd>A list of sorted vertical breakpoint names.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_vertical-sizes.sass"><code>$vertical-values</code></a></dt>
  <dd>A list of sorted vertical breakpoint values.</dd>

</dl>

#### Mixins / Functions

Mixins apply a media query rule to the provided content. Functions generate a media query rule for the as a string.

<dl>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_up.sass"><code>up ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given vertical breakpoint and taller.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_down.sass"><code>down ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given vertical breakpoint and shorter.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_down-between.sass"><code>down-between ( $first-breakpoint, $second-breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given vertical breakpoints which is equal and taller than the smaller, and equal and shorter than the larger.</dd>

  <dt><a href="//github.com/roydukkey/sass-module-break/tree/master/src/break/_down-only.sass"><code>down-only ( $breakpoint )</code></a></dt>
  <dd>Produces a media query rule for the given vertical breakpoint.</dd>

</dl>

Don't see the function you're looking for? Request a [new feature](//github.com/roydukkey/sass-module-break/issues/new) describing a use case.
