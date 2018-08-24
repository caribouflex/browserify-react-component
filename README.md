- Install webpack

`npm install --save-dev webpack`

- Install babel

`npm install babel-cli babel-preset-react babel-preset-es2015 babel-plugin-add-module-exports -D`

- Install browserify

`npm install browserify browserify-global-shim -D`

- Install uglify-js

`npm install uglify-js -D`


-----------------------


1) The component should be distributed in a non-JSX version.
2) The entry point should be ES5 compatible.
3) It contains the whole React library. We want to bundle the component but not React.


No webpack, just Babel. It gets everything from the src directory, converts the JSX to pure JavaScript calls and ES6 to ES5.
We will use browserify to get a global access to the component, `browserify-global-shim` plugin will exclude React but imports the widget.
The component will be used as a script, so we will uglify it.
