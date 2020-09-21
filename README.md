# tiny-version-compare

> Compare two software versions, with any number of points (<1KB)

Supports most version types, from `r12.3` to `1.03.4.234567-RC4`. Development versions are sorted as: `dev`, `alpha`, `beta`, `rc`, `pre`.

Also [used by Refined GitHub](https://github.com/sindresorhus/refined-github/pull/1218).

## Install

```
$ npm install tiny-version-compare
```


## Usage

```js
const compareVersions = require('tiny-version-compare');

switch (compareVersions('1.2.3', '2.3.4')) {
	case -1: console.log('Second one is greater'); break
	case 1:  console.log('Second one is lower'); break
	case 0:  console.log('Versions are equal'); break
}

['v2.0-beta', '1.0', 'v2.0', '1.0.1'].sort(compareVersions);
// ['1.0', '1.0.1', 'v2.0-beta', 'v2.0']
```


## API
### compareVersions(versionA, versionB)

It follows the standard JavaScript [comparison function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#Description) for Arrays.

Returns `-1` if `versionB` is greater, `1` if `versionA` is greater, `0` if the versions are equivalent.

#### versionA, versionB

Type: `string`

The versions to compare.

## License

MIT © [Federico Brigante](https://bfred.it)

