# @xdanangelxoqenpm/laborum-corporis-explicabo <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES spec-compliant `Object.hasOwn` shim. Invoke its "shim" method to shim `Object.hasOwn` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the [spec](https://tc39.es/proposal-accessible-object-hasownproperty/).

Most common usage:
```js
var assert = require('assert');
var hasOwn = require('@xdanangelxoqenpm/laborum-corporis-explicabo');

var obj = { a: 1, b: 2 };

assert(hasOwn(obj, 'a'));
assert(hasOwn(obj, 'b'));
assert('toString' in obj && !hasOwn(obj, 'toString'));

if (!Object.hasOwn) {
	hasOwn.shim();
}

assert.deepEqual(Object.hasOwn(obj, 'a'), hasOwn(obj, 'a'));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@xdanangelxoqenpm/laborum-corporis-explicabo
[npm-version-svg]: https://versionbadg.es/xdanangelxoqenpm/laborum-corporis-explicabo.svg
[deps-svg]: https://david-dm.org/xdanangelxoqenpm/laborum-corporis-explicabo.svg
[deps-url]: https://david-dm.org/xdanangelxoqenpm/laborum-corporis-explicabo
[dev-deps-svg]: https://david-dm.org/xdanangelxoqenpm/laborum-corporis-explicabo/dev-status.svg
[dev-deps-url]: https://david-dm.org/xdanangelxoqenpm/laborum-corporis-explicabo#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@xdanangelxoqenpm/laborum-corporis-explicabo.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@xdanangelxoqenpm/laborum-corporis-explicabo.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@xdanangelxoqenpm/laborum-corporis-explicabo.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@xdanangelxoqenpm/laborum-corporis-explicabo
[codecov-image]: https://codecov.io/gh/xdanangelxoqenpm/laborum-corporis-explicabo/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/xdanangelxoqenpm/laborum-corporis-explicabo/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/xdanangelxoqenpm/laborum-corporis-explicabo
[actions-url]: https://github.com/xdanangelxoqenpm/laborum-corporis-explicabo/actions
