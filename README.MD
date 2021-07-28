# Sass Compiler

It`s project compile SASS, SCCS style to CSS

**To set up a new project**
```
npm init
```

**Install webpack and all the additions for it**
```
npm i webpack webpack-cli webpack-dev-server -D
```

**Basic webpack settings**
```js
const path = require('path');

module.exports = {
    mode: "development",
    entry:  "index.js",
    output: {
        filename: "bundle.js",
        path: path.resolve(__dirname, 'dist'),
    },
}
```

**Install SASS additions**
```
npm i sass-loader sass style-loader css-loader -D
```

**Add SASS additions to config**
```js
module: {
    rules: [
        {
        test: /\.s[ac]ss$/i,
        use: [
            "style-loader",
            "css-loader",
            "sass-loader",
        ],
        },
    ],
},
```

____

**Settings package.json for start project**
```json
"scripts": {
    "start": "webpack --mode development",
    "watch": "webpack --watch",
    "build": "webpack --mode production"
},
```

:white_check_mark: npm run "script name" (without quotes)