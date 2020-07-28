# Learning React by Making a MovieList Application
## Description
This project was made from scratch using `npm`, `babel`, and `webpack`. It will
be a place for us to learn about some of the things `npx create-react-app` does
behind the scenes and will host notes from the various topics along the way.
This project was a step by step project created from the book "React Projects"
by Roy Derks.

## Webpack
### Commands ran
```npm i --save-dev webpack webpack-cli```
Installs webpack and webpack CLI as dev dependencies in our project.
```webpack --mode-production```
Minimizes code to decrease the size of the bundle. Useful when getting code
prod ready
```webpack --mode-development```
```node dist/main.js```
Runs the bundled version of our application and allows us to run JavaScript
code from the command line.
```npm i --save-dev html-webpack-plugin```
Extends webpack to add the minified bundled code to the `<body>` tags as
`<script>` when running.
```npm i --save-dev webpack-dev-server```
Create a webpack server that reloads when changes are made to the project
files. Also manages the files in memory instead of building the `dist`
directory.

### Configuration
`webpack.config.js`

## Babel
Allows React and ES2015+ to be ran in any browser. Compiles JavaScript code
into a readable format for every browser.
### Commands
```npm i --save-dev @babel/core @babel/preset-env @babel/preset-react babel-loader```
Install babel and its related packages as dev dependencies in our application
`babel-loader` is a helper so that Babel can run with `webpack` and two preset
packages. `@babel-preset-env` determines which plugins will be used to compile
our JavaScript code into a readable format for the browser.
`@babel/preset-react` compiles react specific code
### Configuration
`.babelrc`
The contents of this file can be injected directly into the `webpack.config.js`
file, but for better readability, we extracted the config into its own file.