This is a **JavaScript** version of the original cb2promise library. All coffeescript files have been transpiled and replaced by their JS counterparts.

This repo was created in a repsonse to an [issue about using this library with webpack](https://github.com/jviotti/electron-json-storage/issues/50).

To replace the original coffeescript library with this JS one simply run:

```
npm install --save git+https://github.com/Maddoc42/cb2promise.git
```


# cb2promise

![Last version](https://img.shields.io/github/tag/Kikobeats/cb2promise.svg?style=flat-square)
[![Dependency status](http://img.shields.io/david/Kikobeats/cb2promise.svg?style=flat-square)](https://david-dm.org/Kikobeats/cb2promise)
[![Dev Dependencies Status](http://img.shields.io/david/dev/Kikobeats/cb2promise.svg?style=flat-square)](https://david-dm.org/Kikobeats/cb2promise#info=devDependencies)
[![NPM Status](http://img.shields.io/npm/dm/cb2promise.svg?style=flat-square)](https://www.npmjs.org/package/cb2promise)
[![Donate](https://img.shields.io/badge/donate-paypal-blue.svg?style=flat-square)](https://paypal.me/kikobeats)

> Converts whatever standard NodeJS callback function into ES6 standard promise.

## Install

```bash
npm install cb2promise --save
```

If you want to use in the browser (powered by [Browserify](http://browserify.org/)):

```bash
bower install cb2promise --save
```

and later link in your HTML:

```html
<script src="bower_components/cb2promise/dist/cb2promise.js"></script>
```

## Usage

```js
var cb2promise = require('cb2promise');

var sampleFunction = function(done) {
  return done(null, 'hello world');
};

var promise = cb2promise(sampleFunction)

promise().then(console.log);
// => hello world

```

## License

MIT © [Kiko Beats](http://www.kikobeats.com)
