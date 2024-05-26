# @taktikorg/dolore-blanditiis <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES spec-compliant shim for `Date`. Invoke its "shim" method to shim `Date` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) “multi” interface. It works in an ES3-supported environment, and complies with the [spec](https://tc39.es/proposal-promise-any/#sec-@taktikorg/dolore-blanditiis).

Most common usage:
```js
var assert = require('assert');

var shims = require('@taktikorg/dolore-blanditiis');

assert.deepEqual(shims, [
	'Date',
	'Date.prototype.getFullYear',
	'Date.prototype.getMonth',
	'Date.prototype.getDate',
	'Date.prototype.getUTCDate',
	'Date.prototype.getUTCFullYear',
	'Date.prototype.getUTCMonth',
	'Date.prototype.toUTCString',
	'Date.prototype.toDateString',
	'Date.prototype.toString',
	'Date.prototype.toISOString',
	'Date.prototype.toJSON',
	'Date.now',
	'Date.parse',
]);

require('@taktikorg/dolore-blanditiis/auto'); // will be a no-op if not needed

assert.ok(new Date() instanceof Date);
assert.equal(typeof Date.now(), 'number');

// etc, with all the Date methods you expect
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@taktikorg/dolore-blanditiis
[npm-version-svg]: https://versionbadg.es/taktikorg/dolore-blanditiis.svg
[deps-svg]: https://david-dm.org/taktikorg/dolore-blanditiis.svg
[deps-url]: https://david-dm.org/taktikorg/dolore-blanditiis
[dev-deps-svg]: https://david-dm.org/taktikorg/dolore-blanditiis/dev-status.svg
[dev-deps-url]: https://david-dm.org/taktikorg/dolore-blanditiis#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/dolore-blanditiis.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/dolore-blanditiis.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/dolore-blanditiis.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/dolore-blanditiis
[codecov-image]: https://codecov.io/gh/taktikorg/dolore-blanditiis/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/taktikorg/dolore-blanditiis/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/taktikorg/dolore-blanditiis
[actions-url]: https://github.com/taktikorg/dolore-blanditiis/actions
