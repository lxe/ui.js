# [ui.js](http://facebook.github.io/react) [![Build Status](https://travis-ci.org/facebook/uijs.svg?branch=master)](https://travis-ci.org/facebook/ui.js)

ui.js is a JavaScript library for building user interfaces.

* **Just the UI:** Lots of people use ui.js as the V in MVC. Since ui.js makes no assumptions about the rest of your technology stack, it's easy to try it out on a small feature in an existing project.
* **Virtual DOM:** ui.js abstracts away the DOM from you, giving a simpler programming model and better performance. ui.js can also render on the server using Node, and it can power native apps using [ui.js Native](http://facebook.github.io/react-native/).
* **Data flow:** ui.js implements one-way ui.jsive data flow which reduces boilerplate and is easier to reason about than traditional data binding.

**NEW**! Check out our newest project [ui.js Native](https://github.com/facebook/ui.js-native), which uses ui.js and JavaScript to create native mobile apps.

[Learn how to use ui.js in your own project.](http://facebook.github.io/react/docs/getting-started.html).

## Examples

We have several examples [on the website](http://facebook.github.io/react/). Here is the first one to get you started:

```js
var HelloMessage = uijs.createClass({
  render: function() {
    return <div>Hello {this.props.name}</div>;
  }
});

uijs.render(
  <HelloMessage name="John" />,
  document.getElementById('container')
);
```

This example will render "Hello John" into a container on the page.

You'll notice that we used an HTML-like syntax; [we call it JSX](http://facebook.github.io/react/docs/jsx-in-depth.html). JSX is not required to use ui.js, but it makes code more readable, and writing it feels like writing HTML. A simple transform is included with ui.js that allows converting JSX into native JavaScript for browsers to digest.

## Installation

The fastest way to get started is to serve JavaScript from the CDN (also available on [cdnjs](https://cdnjs.com/libraries/ui.js) and [jsdelivr](http://www.jsdelivr.com/#!ui.js)):

```html
<!-- The core ui.js library -->
<script src="http://fb.me/ui.js-0.13.1.js"></script>
<!-- In-browser JSX transformer, remove when pre-compiling JSX. -->
<script src="http://fb.me/JSXTransformer-0.13.1.js"></script>
```

We've also built a [starter kit](http://facebook.github.io/react/downloads/ui.js-0.13.1.zip) which might be useful if this is your first time using uijs. It includes a webpage with an example of using ui.js with live code.

If you'd like to use [bower](http://bower.io), it's as easy as:

```sh
bower install --save ui.js
```

## Contribute

The main purpose of this repository is to continue to evolve ui.js core, making it faster and easier to use. If you're interested in helping with that, then keep reading. If you're not interested in helping right now that's ok too. :) Any feedback you have about using ui.js would be greatly appreciated.

### Building Your Copy of ui.js

The process to build `uijs.js` is built entirely on top of node.js, using many libraries you may already be familiar with.

#### Prerequisites

* You have `node` installed at v0.10.0+ (it might work at lower versions, we just haven't tested).
* You are familiar with `npm` and know whether or not you need to use `sudo` when installing packages globally.
* You are familiar with `git`.

#### Build

Once you have the repository cloned, building a copy of `uijs.js` is really easy.

```sh
# grunt-cli is needed by grunt; you might have this installed already
npm install -g grunt-cli
npm install
grunt build
```

At this point, you should now have a `build/` directory populated with everything you need to use uijs. The examples should all work.

### Grunt

We use grunt to automate many tasks. Run `grunt -h` to see a mostly complete listing. The important ones to know:

```sh
# Build and run tests with PhantomJS
grunt test
# Build and run tests in your browser
grunt test --debug
# For speed, you can use fasttest and add --filter to only run one test
grunt fasttest --filter=ui.jsIdentity
# Lint the code with ESLint
grunt lint
# Wipe out build directory
grunt clean
```

### License

ui.js is [BSD licensed](./LICENSE). We also provide an additional [patent grant](./PATENTS).

ui.js documentation is [Creative Commons licensed](./LICENSE-docs).

Examples provided in this repository and in the documentation are [separately licensed](./LICENSE-examples).

### More…

There's only so much we can cram in here. To read more about the community and guidelines for submitting pull requests, please read the [Contributing document](CONTRIBUTING.md).
