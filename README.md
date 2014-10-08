# Starterkit

We use this repository as a starting point for our web apps.
It provides a prepared development environment based on [gulp](https://github.com/gulpjs/gulp), [stylus](https://github.com/LearnBoost/stylus) and [webpack](https://github.com/webpack/webpack).

## Installation

Install all dependencies. 

```
$ npm install
```

### Imports Loader

If you want to use plugins for a certain library, that does not require dependencies you can use the [imports loader](http://webpack.github.io/docs/shimming-modules.html#imports-loader). Here the file 'awesome-plugin.js' expects a global variable called jQuery. We can just import that variable via ```jQuery=path/to/jQuery```.

Install the imports loader via:

```
npm install --save imports-loader
```
You can use it in your code like:

```
var $ = require('../bower_components/jquery/dist/jquery');
require("imports?jQuery=../bower_components/jquery/dist/jquery!./awesome-plugin.js");
```


## Development

Builds the application and starts a webserver with livereload. By default the webserver starts at port 1337.
You can define a port with ```$ gulp --port 3333```.

```
$ gulp
```

## Build

Builds a minified version of the application in the dist folder.

```
$ gulp build --type production
```


###Requirements
* node
* npm
* bower
* gulp
