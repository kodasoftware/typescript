# Koda Software Typescript Styling Guide

This styling guide provide configuration and rules for `typescript`, `eslint` and `prettier` that can be used in Koda Software projects to ensure they meet these recommended stylistic choices. It does not inform code quality, merely the look of how code should be written to ensure it is consistent and easy to interpret for developers.

## Using this style guide in your project

In order to use this guide you should first install the following dependencies in your project

```bash
npm add -D eslint prettier prettier-eslint typescript eslint-config-prettier eslint-plugin-node eslint-plugin-prettier eslint-plugin-simple-import-sort @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

Then install this package to your project

```bash
npm add -D @kodasoftware/typescript
```

Then you can add the following files to your Typescript project

`.eslintrc.json`

```json
{
  "extends": "./node_modules/@kodasoftware/typescript/.eslintrc.json"
  // Add any overrides/extensions here...
}

```

`.prettierrc.js`

```javascript
module.exports = {
  ...require('@kodasoftware/typescript/.prettierrc.json')
  // And any overrides/extensions here...
}

```

We also recommend adding the following

`.eslintignore`

```
dist/
```

`tsconfig.json`

This is an example of a typescript configuration you can put into your project that extends the typescript configuration of this library.

```json
{
  "extends": "./node_modules/@kodasoftware/typescript/tsconfig.json",
  "compilerOptions": {
    "baseUrl": "./",
    "outDir": "dist",
    "paths": {
      "@/*": ["src/*"]
    }
    // Add any overrides/extensions here...
  }
}

```

Enjoy!
