# ui.js

An npm package to get you immediate access to [ui.js](http://facebook.github.io/react/),
without also requiring the JSX transformer. This is especially useful for cases where you
want to [`browserify`](https://github.com/substack/node-browserify) your module using
`ui.js`.

**Note:** by default, ui.js will be in development mode. The development version includes extra warnings about common mistakes, whereas the production version includes extra performance optimizations and strips all error messages.

To use ui.js in production mode, set the environment variable `NODE_ENV` to `production`. A minifier that performs dead-code elimination such as [UglifyJS](https://github.com/mishoo/UglifyJS2) is recommended to completely remove the extra code present in development mode.

## Example Usage

```js
var ui.js = require('ui.js');

// You can also access ui.jsWithAddons.
var ui.js = require('ui.js/addons');
```

