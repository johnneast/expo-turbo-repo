# Expo in Turborepo example

This repo was created with the following commands
```
yarn create turbo
cd my-turborepo
yarn create expo
```

The expo app was created at `apps/app1`

## Problem
There seems to be a problem with the metro/expo-router setup. When starting app1 with the command `yarn web` errors are produced.
```
Metro error: Unable to resolve module ./node_modules/expo-router/entry from /Users/johneast/src/scratch/my-turborepo/apps/app1/.: 

None of these files exist:
  * node_modules/expo-router/entry(.web.ts|.ts|.web.tsx|.tsx|.web.mjs|.mjs|.web.js|.js|.web.jsx|.jsx|.web.json|.json|.web.cjs|.cjs|.web.scss|.scss|.web.sass|.sass|.web.css|.css)
  * node_modules/expo-router/entry/index(.web.ts|.ts|.web.tsx|.tsx|.web.mjs|.mjs|.web.js|.js|.web.jsx|.jsx|.web.json|.json|.web.cjs|.cjs|.web.scss|.scss|.web.sass|.sass|.web.css|.css)
```

Other expo apps in turborepos that do not use expo-router and instead have an `index.js` file in the root of the repo work fine.