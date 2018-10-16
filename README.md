# Typescript Course

# Course outline and slides
 * [View course outline here](https://mike.works/course/typescript-fundamentals-7832c19)
 * [View slides here](https://docs.mike.works/typescript-slides)

# What's in this project?

* [Webpack 3](https://webpack.js.org)
* [TypeScript](https://www.typescriptlang.org) 2.5, setup for experimental decorator support
* [TSLint](https://github.com/palantir/tslint) for linting, setup with a strict JSX-friendly set of rules
* [sass-loader](https://github.com/webpack-contrib/sass-loader) for traditional management of styles
* [React](https://facebook.github.io/react/) v16 for building components
* [Hot Loader v3](https://github.com/gaearon/react-hot-loader) so styles and JS are updated in place as you save source code
* [extract-text-webpack-plugin](https://github.com/webpack-contrib/extract-text-webpack-plugin) so compiled styles are external stylesheets instead of inline style blocks
* [Jest](http://facebook.github.io/jest/) as a testing platform


## General Packages

Please make sure you have the following general software installed

| Required | Library | Version Range | Notes |
| ------------- | ------------- | ---| --- |
| ✔ | [Node.js](http://nodejs.org/)  | >= 8.0 | [nvm](https://github.com/creationix/nvm) is highly recommended for managing multiple node versions on a single machine |
| ✔ | [Visual Studio Code](https://code.visualstudio.com/)  | >= 1.14 | We'll be using several specific features of the VS Code editor. We can't force you to use it, but you'll miss out if you don't! |
| ✔ | [Yarn](https://yarnpkg.com/)  | >= 0.24 | An alternative to [npm](https://github.com/npm/npm) (if you are using nvm: `brew install yarn --without-node`, else use `brew install yarn`) |

## VS Code Extensions

Additionally, to take advantage of syntax hilighting, static code analysis and other editor features, you'll want to install the latest version of the following VS Code extensions

| Required | Extension | Notes |
| ------------- | ------------- | --- |
| ✔ | [sass-indented](https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented) | Syntax highlighting and code completion support for [Sass](http://sass-lang.com) stylesheets |
| ✔ | [tslint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint) | Static code analysis for JavaScript and TypeScript files |
| ✔ | [jest](https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest) | Syntax highlighting for [Jest snapshot testing](https://facebook.github.io/jest/docs/snapshot-testing.html) and in-editor test pass/fail statuses |
| ✔ | [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome) | Allows us to attach to Chrome for debugging |
|   | [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons) | Better file and folder icons |


## Global Node.js Packages

Make sure you have these npm packages installed globally. This can be done by running

```
npm install -g <package-name>
```

| Required | Library | Version Range |
| ------------- | ------------- | ---|
| ✔ | [typescript](https://github.com/microsoft/typescript)  | ^2.5.0 |
| ✔ | [tslint](https://github.com/palantir/tslint) | ^5.7.0 |
| ✔ | [ts-node](https://github.com/TypeStrong/ts-node) | ^3.3.0 |

## Project setup

First, clone this project from Github

```
git clone https://github.com/mike-works/typescript-fundamentals tscript
cd tscript
```

Finally, while in the top-level folder of this project, download the and install this project's dependencies by running

```
yarn
```

To start the app, run

```
npm test accounts 
```

and you should see some failing tests waiting for you

### How to use it

##### Start the Development Server
`npm start <exercise-name>`

##### Build Development Assets in the `/dist` folder
This will be an un-minified version of an exercise, and will include some webpack-specific tooling, intended only for development use

`npm run build:dev <exercise-name>`

##### Build Production Assets in the `/dist` folder
This will be an an optimized version of the exercise

`npm run build:dist <exercise-name>`

# The Exercise Folder
Exercises are standalone mini-projects with the following folder structure.
```sh
index.html   # HTML served for exercise
./src        # Scripts (ts, js, tsx and jsx)
./styles     # Styles
   ⌙ app.scss       #  (optional) Entry point for styles
./tests      # Tests
   ⌙ myfile.test.ts # Tests must have *.test.js or *.test.ts
```