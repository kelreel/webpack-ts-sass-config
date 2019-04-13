<h1 align="center"><img height="150" src="./docs/logo.png" /><br>Webpack 4 TypeScript config</h1>
<p align="center">
  <sub>TypeScript, Babel, SASS, PostCSS... <sub>
</p>

This is my personal Webpack 4 config for single page (index.html) without frameworks. It will be updated as needed.
  
## Installation

Clone this repository and install modules:

```bash
git clone https://github.com/kanitelk/webpack-ts-sass-config.git
cd webpack-ts-sass-config
npm install
```

![](./docs/split.png)

## Commands

Run development mode

```bash
npm run start
```

Run build mode

```bash
npm run build
```

## Features

* TypeScript
* Babel
* CSS/SASS + PostCSS (CSSnano, autoprefixer) + Normilize
* Hashing
* Assets folder for Production
* Minifying JS & CSS
* Two .js chunks - main.js and vendor.js (modules)

![](./docs/split.png)

## Entry point 

Webpack.config.js

```javascript
{
  entry: { main: "./src/index.ts" }, // Entry Point
  output: {
    path: path.resolve(__dirname, "docs"), // Output folder (Production)
    filename: "[name].[chunkhash].js",
    pathinfo: false
}
```

