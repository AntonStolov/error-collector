Simple error bag collector
---

Usage

1. TypesScript example

```ts
import { ErrorBag } from 'error-collector';
const errorBag = new ErrorBag();

try {
    throw new Error('some error');
} catch (error) {
    errorBag.add(error);
}

errorBag.logErrors(); // just logging errors
errorBag.handleErrors(); // throw all errors in one error
```

2. JavaScript example

```js
const { ErrorBag } = require('error-collector');

const errorBag = new ErrorBag();

try {
    throw new Error('some error');
} catch (error) {
    errorBag.add(error);
}

errorBag.logErrors();
errorBag.handleErrors();
```
