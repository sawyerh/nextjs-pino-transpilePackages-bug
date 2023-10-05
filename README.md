To reproduce the bug, run the application in dev mode:

```
npm run dev
```

You will see the following error:

```
 ⨯ ./node_modules/pino/browser.js
Module parse failed: Cannot use 'import.meta' outside a module (437:16)
|                 // still a Refresh Boundary later.
|                 // @ts-ignore importMeta is replaced in the loader
>                 import.meta.webpackHot.accept();
|                 // This field is set when the previous version of this module was a
|                 // Refresh Boundary, letting us know we need to check for invalidation or
```

To resolve the issue, remove `transpilePackages` from `next.config.js` and restart the server.
