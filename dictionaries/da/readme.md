# dictionary-da

Danish spelling dictionary in UTF-8.

Useful with [hunspell][], [`nodehun`][nodehun], [`nspell`][nspell],
Open Office, LibreOffice, FireFox and Thunderbird, or [macOS][].

Generated by [`dictionaries`][dictionaries], from
[`stavekontrolden.dk`][source].

## Installation

[npm][]:

```bash
npm install dictionary-da
```

## Usage

```js
var da = require('dictionary-da')

da(function (err, result) {
  console.log(err || result)
});
```

Yields:

```js
{ dic: <Buffer>,
  aff: <Buffer> }
```

Where `dic` is a buffer for the dictionary file at `index.dic` (in UTF-8), and
`aff` is a buffer for the affix file at `index.aff` (in UTF-8).

Or directly load the files, using something like:

```js
var path = require('path')
var base = require.resolve('dictionary-da')

fs.readFileSync(path.join(base, 'index.dic'), 'utf-8')
fs.readFileSync(path.join(base, 'index.aff'), 'utf-8')
```

## License

Dictionary and affix file: [(GPL-2.0 OR LGPL-2.1 OR MPL-1.1)](https://github.com/wooorm/dictionaries/blob/master/dictionaries/da/license).
Rest: [MIT][] © [Titus Wormer][home].

[hunspell]: https://hunspell.github.io

[nodehun]: https://github.com/nathanjsweet/nodehun

[nspell]: https://github.com/wooorm/nspell

[macos]: https://github.com/wooorm/dictionaries#macos

[source]: http://www.stavekontrolden.dk

[npm]: https://docs.npmjs.com/cli/install

[dictionaries]: https://github.com/wooorm/dictionaries

[mit]: https://github.com/wooorm/dictionaries/blob/master/LICENSE

[home]: https://wooorm.com
