Query string handler
====================

[![build status](https://img.shields.io/travis/cjssdk/query.svg?style=flat-square)](https://travis-ci.org/cjssdk/query)
[![npm version](https://img.shields.io/npm/v/cjs-query.svg?style=flat-square)](https://www.npmjs.com/package/cjs-query)
[![dependencies status](https://img.shields.io/david/cjssdk/query.svg?style=flat-square)](https://david-dm.org/cjssdk/query)
[![devDependencies status](https://img.shields.io/david/dev/cjssdk/query.svg?style=flat-square)](https://david-dm.org/cjssdk/query?type=dev)
[![Gitter](https://img.shields.io/badge/gitter-join%20chat-blue.svg?style=flat-square)](https://gitter.im/DarkPark/cjssdk)
[![RunKit](https://img.shields.io/badge/RunKit-try-yellow.svg?style=flat-square)](https://npm.runkit.com/cjs-query)


Module to parse query part of the location URL.


## Installation ##

```bash
npm install cjs-query
```


## Usage ##

Add to the scope:

```js
var query = require('cjs-query');
```

Parse some parameters:

```js
// gives {param: '5000', another_param: 'another_value'}
// note that the type of param value is string
console.log(query.parse('param=5000&another_param=another_value'));
```

Parse current document query string:

```js
console.log(query.parse(document.location.search.substring(1)));
```

Stringify query params:

```js
// gives 'param=128'
console.log(query.stringify({param: 128}));
```


## Contribution ##

If you have any problems or suggestions please open an [issue](https://github.com/cjssdk/query/issues)
according to the contribution [rules](.github/contributing.md).


## License ##

`cjs-query` is released under the [MIT License](license.md).
