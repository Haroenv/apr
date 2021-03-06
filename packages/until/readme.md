<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## until

<a id="until"></a>
Repeatedly call `fn` until `test` returns `true`.

[![](https://img.shields.io/npm/v/apr-until.svg?style=flat-square)](https://www.npmjs.com/package/apr-until) [![](https://img.shields.io/npm/l/apr-until.svg?style=flat-square)](https://www.npmjs.com/package/apr-until)

**Parameters**

-   `test` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 
-   `fn` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** 

**Examples**

```javascript
import until from 'apr-until';

const then = (v) => new Promise((resolve) => resolve(v));

const maxCalls = 10;
let calls = 0;


const output = await until(async () => {
  await then();
  return (calls += 1) >= maxCalls;
}, async () => (
  await then(calls)
);

// output = 10
```

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 
