---
title: 'Polyfilling'
order: 9
---

Because we used the `@babel/polyfills` package, which is now obsolete, it is necessary to manually import the polyfills if needed.
For this case, we have prepared package `react-union-polyfills`.

##Usage

To use stable polyfills, just import `importPolyfills` function from `react-union-polyfills` in root package

```js
import { importPolyfills } from 'react-union-polyfills';
```

###Internet Explorer

If you need to support Internet Explorer 11, run function `importPolyfills.ie11()` within `ready` function of root package

```js
ready(() => {
	importPolyfills.ie11();
	justRender(<Root />);
});
```

To support Internet Explorer 9, run function `importPolyfills.ie9()` instead of `importPolyfills.ie11()` as mentioned above. Support for IE11 will be added automaticaly.
