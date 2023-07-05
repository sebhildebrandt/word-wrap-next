# word-wrap-next

[![NPM version](https://img.shields.io/npm/v/sebhildebrandt/word-wrap-next.svg?style=flat)](https://www.npmjs.com/package/sebhildebrandt/word-wrap-next)
[![NPM monthly downloads](https://img.shields.io/npm/dm/sebhildebrandt/word-wrap-next.svg?style=flat)](https://npmjs.org/package/sebhildebrandt/word-wrap-next)
[![NPM total downloads](https://img.shields.io/npm/dt/sebhildebrandt/word-wrap-next.svg?style=flat)](https://npmjs.org/package/sebhildebrandt/word-wrap-next)

> Wrap words to a specified length.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save word-wrap-next
```

## Usage

```js
var wrap = require('word-wrap-next');

wrap('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.');
```

Results in:

```
  Lorem ipsum dolor sit amet, consectetur adipiscing
  elit, sed do eiusmod tempor incididunt ut labore
  et dolore magna aliqua. Ut enim ad minim veniam,
  quis nostrud exercitation ullamco laboris nisi ut
  aliquip ex ea commodo consequat.
```

## Options

![image](https://cloud.githubusercontent.com/assets/383994/6543728/7a381c08-c4f6-11e4-8b7d-b6ba197569c9.png)

### options.width

Type: `Number`

Default: `50`

The width of the text before wrapping to a new line.

**Example:**

```js
wrap(str, {width: 60});
```

### options.indent

Type: `String`

Default: `` (none)

The string to use at the beginning of each line.

**Example:**

```js
wrap(str, {indent: '      '});
```

### options.newline

Type: `String`

Default: `\n`

The string to use at the end of each line.

**Example:**

```js
wrap(str, {newline: '\n\n'});
```

### options.escape

Type: `function`

Default: `function(str){return str;}`

An escape function to run on each line after splitting them.

**Example:**

```js
var xmlescape = require('xml-escape');
wrap(str, {
  escape: function(string){
    return xmlescape(string);
  }
});
```

### options.trim

Type: `Boolean`

Default: `false`

Trim trailing whitespace from the returned string. This option is included since `.trim()` would also strip the leading indentation from the first line.

**Example:**

```js
wrap(str, {trim: true});
```

### options.cut

Type: `Boolean`

Default: `false`

Break a word between any two letters when the word is longer than the specified width.

**Example:**

```js
wrap(str, {cut: true});
```

## About

### Related projects

* [common-words](https://www.npmjs.com/package/common-words): Updated list (JSON) of the 100 most common words in the English language. Useful for… [more](https://github.com/jonschlinkert/common-words) | [homepage](https://github.com/jonschlinkert/common-words "Updated list (JSON) of the 100 most common words in the English language. Useful for excluding these words from arrays.")
* [shuffle-words](https://www.npmjs.com/package/shuffle-words): Shuffle the words in a string and optionally the letters in each word using the… [more](https://github.com/jonschlinkert/shuffle-words) | [homepage](https://github.com/jonschlinkert/shuffle-words "Shuffle the words in a string and optionally the letters in each word using the Fisher-Yates algorithm. Useful for creating test fixtures, benchmarking samples, etc.")
* [unique-words](https://www.npmjs.com/package/unique-words): Return the unique words in a string or array. | [homepage](https://github.com/jonschlinkert/unique-words "Return the unique words in a string or array.")
* [wordcount](https://www.npmjs.com/package/wordcount): Count the words in a string. Support for english, CJK and Cyrillic. | [homepage](https://github.com/jonschlinkert/wordcount "Count the words in a string. Support for english, CJK and Cyrillic.")

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Contributors

| **Commits** | **Contributor**                                     |
| ----------- | --------------------------------------------------- |
| 1           | [sebhildebrandt](https://github.com/sebhildebrandt) |
| 43          | [jonschlinkert](https://github.com/jonschlinkert)   |
| 2           | [lordvlad](https://github.com/lordvlad)             |
| 2           | [hildjj](https://github.com/hildjj)                 |
| 1           | [danilosampaio](https://github.com/danilosampaio)   |
| 1           | [2fd](https://github.com/2fd)                       |
| 1           | [toddself](https://github.com/toddself)             |
| 1           | [wolfgang42](https://github.com/wolfgang42)         |
| 1           | [zachhale](https://github.com/zachhale)             |

### Running tests

Running and reviewing unit tests is a great way to get familiarized with a library and its API. You can install dependencies and run tests with the following command:

```sh
$ npm install && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](https://twitter.com/jonschlinkert)

**Maintainer `word-wrap-next`**

* [github/sebhildebrandt](https://github.com/sebhildebrandt)

### License

Copyright © 2014-2023, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT License](LICENSE).
