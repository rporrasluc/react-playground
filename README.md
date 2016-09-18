# react-playground
A project for tracking my progress learning React.

## Getting started
First place to go when learning React is [React official page](https://facebook.github.io/react/docs/getting-started.html). 

Based in their recommendations we have downloaded the starter pack and created our helloworld. A 2 minutes example which shows us how easy is to render our first view using React.

Thanks to this small piece of code I have learnt a bit about the [JSX syntax](https://facebook.github.io/react/docs/jsx-in-depth.html) and included Babel to perform the transformation in the browser.

In the first chapter we will see how React can be used together with package managers.

## Package Management with Browserify
What was supposed to be react playground is going to be a new (for me) JS tools playground. As Rails developer, I am more used to Sprockets as tool for bundling the application files up in only one file. The great advantage I can find is that defining modules you care only about what the module requires rather than having to deal with the order in which all your files are loaded to accomplish the dependencies.

We have replaced the three files we were fetching from the server side for only one file called bundle.js. For doing this first we got the package manager browserify using `npm install -g browserify`. Browserify allows you to use your npm managed libraries inside your application, so we have move forward and downloaded the required npm packages.

```
npm install --save react react-dom babelify babel-preset-react
```

Finally, we have used `browserify -t [ babelify ] src/helloworld.js -o src/bundle.js` for creating the file bundle.js from the file helloworld.js. The file helloworld is in charge of specify its dependencies.

```javascript
var React = require('react');
var ReactDOM = require('react-dom');

ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('example')
);
```

## React Tutorial
Following React next steps recommendations, we are going to follow the React Tutorial. React Tutorial code already provides a set of web servers written in different programming languages so you are free to choose your favourite one. In our case, we have chosen the Ruby one. We have removed all unused servers and, as stated by the tutorial, the script file that contains what will be the result of your learning work.

Don't be cheater and write, not only read! :)

Our tutorial folder structure is the following:

```
|-- tutorial
    |-- comments.json
    |-- server.rb
    |-- public
        |-- index.html
        |-- css
            |-- base.css
```