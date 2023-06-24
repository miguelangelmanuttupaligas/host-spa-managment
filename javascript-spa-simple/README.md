# Vanilla SPA
A simple example of a Single Page Application using Javascript, HTML, and CSS.

Tools used in this example are:
* Webpack
* Sass

# Installation

First install dependencies
```shell
npm install
```

Execute in Development Mode
```shell
npm start # to execute in development mode
```

Execute in Build mode
```js
// Edit package.json. change the value "dev" to "prod" in "start"

// Before
"scripts": {
    "start": "webpack serve --config ./webpack/webpack.config.js --env env=dev --open",
    ..
  },

// After
"scripts": {
    "start": "webpack serve --config ./webpack/webpack.config.js --env env=prod --open",
    ..
  },
```
```shell
npm run build # to compile project to production
npm start
```

View this projects in "localhost:8080"
