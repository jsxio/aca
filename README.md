# aca

> The Aho–Corasick algorithm (aca) is a string searching algorithm.

```javascript
$ npm i aca
```

```javascript
const aca = require("aca");
```

## aca.find(keywords: array, text: string, [charset: string])

> Search for keywords in text strings.

**charset**  (optional, Unicode or ASCII, defaults to Unicode)

```js
aca.find(keywords, text) // => { matches, positions, count }
```

**Example**

```js
var keywords = ["h", "he", "she", "hers", "his"];
var text = "ahishers";

var result = aca.find(keywords, text, 'ASCII');

result.matches //keyword:positions
=> {"h":[1,4],"his":[1],"she":[3],"he":[4],"hers":[4]} 
result.positions //position:keywords
=> [[1,["h","his"]],[3,["she"]],[4,["h","he","hers"]]]
result.count //keyword:count
=> {"h":2,"his":1,"he":1,"she":1,"hers":1}
```

## aca.dict(keywords: string|buffer, text: string|buffer, [charset: string])

> Coming soon.

**keywords.txt** one keyword per single line.
```js
h
his
she
he
hers
```
**text.txt**
```js
ahishers
```

## Command line

> Coming soon.

```js
$ aca -v
```


Aho–Corasick algorithm [wiki](https://en.wikipedia.org/wiki/Aho%E2%80%93Corasick_algorithm)!
