 [![NPM version](https://badge.fury.io/js/setjs.png)](http://badge.fury.io/js/setjs) [![Dependency Status](https://gemnasium.com/bebraw/setjs.png)](https://gemnasium.com/bebraw/setjs) [![build status](https://secure.travis-ci.org/bebraw/setjs.png)](http://travis-ci.org/bebraw/setjs)

# setjs - Set data structure for JavaScript

`setjs` implements a a Set API inspired by [Python](http://docs.python.org/2/library/stdtypes.html#set). There are some differences, though. The biggest difference is that the API is immutable by design. There is a basic `set` structure and functions that operate upon it. Consider the API below:

```js
var a = set(4, 3, 4, 3); // set accepts arbitrary amount of items and may be empty
var b = set(4, 5);
var c = set(b, 6); // set accepts sets too. this results in {4, 5, 6}

set.count(a); // 2
set.contains(a, 3); // true
set.equals(a, a); // true
set.equals(a, set()); // false

set.union(a, b); // {3, 4, 5}
set.intersection(a, b); // {4}
set.difference(a, b); // {5}
set.symmetricDifference(a, b); // {3, 5}
```

## Contributors

* [David Ellis](https://github.com/dfellis) - Made library truly immutable.

## License

MIT.
