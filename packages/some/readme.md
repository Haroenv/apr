<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## some

<a id="some"></a>
Returns true if at least one element in the `coll` satisfies an async test.

[![](https://img.shields.io/npm/v/apr-some.svg?style=flat-square)](https://www.npmjs.com/package/apr-some) [![](https://img.shields.io/npm/l/apr-some.svg?style=flat-square)](https://www.npmjs.com/package/apr-some)

**Parameters**

-   `input` **([Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Iterable)** 
-   `iteratee` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

**Examples**

```javascript
import awaitify from 'apr-awaitify';
import some from 'apr-some';

const access = awaitify(fs.access);
const files = [
  'file1',
  'file2',
  'file3'
];

const oneExist = await some(files, async (file) =>
  await access(file)
);
```

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 

### series

**Parameters**

-   `input` **([Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Iterable)** 
-   `iteratee` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 

### limit

**Parameters**

-   `input` **([Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) \| [Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) | Iterable)** 
-   `limit` **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `iteratee` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 
