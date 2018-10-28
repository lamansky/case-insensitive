# case-insensitive

Wraps around an array or string and transforms certain methods into case-insensitive versions.

## Installation

Requires [Node.js](https://nodejs.org/) 6.0.0 or above.

```bash
npm i case-insensitive
```

## API

The module exports a single function.

### Parameter

`thing` (string or array)

### Return Value

An object of methods that operate on the underlying `thing` in a case-insensitive way. The methods returned depend on the type of input:

| Method      | Arrays | Strings |
| ----------: | :----: | :-----: |
| endsWith    |        |    ✔    |
| equals      |   ✔    |    ✔    |
| includes    |   ✔    |    ✔    |
| indexOf     |   ✔    |    ✔    |
| lastIndexOf |   ✔    |    ✔    |
| startsWith  |        |    ✔    |

## Example

```javascript
const ci = require('case-insensitive')

ci('String').equals('STRING') // true
ci('String').startsWith('s') // true
ci('String').endsWith('nG') // true
ci('STRING').indexOf('t') // 1

ci(['Test']).equals(['test']) // true
ci(['A', 'B']).includes('a') // true
ci(['A', 'B']).indexOf('b') // 1
```
