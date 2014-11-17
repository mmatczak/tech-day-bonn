Getting Started
=============

To get started you simply need to clone this repository and install the dependencies.
### 1. Install prerequisites
You need a Git client to clone the repository and the Node.js platform (including its package manager - npm) which allows Grunt and Bower to install the dependencies and build the application.     
### 2. Clone the Git repository
Clone this repository and switch to the 'from_scratch' branch repository using Git (e.g. to the `from_scratch` directory):

```
git clone https://github.com/mmatczak/tech-day-bonn.git -b from_scratch from_scratch
cd from_scratch
```
### 3. Install the dependencies
The application template has two kinds of dependencies: tools used to develop, test and build the application and JavaScript libraries the application uses.

Both kinds of dependencies can be installed via:

```
npm install
```

The tools are installed in the `from_scratch/node_modules` directory, while the JavaScript libraries in the `from_scratch/app/bower_components` directory (as configured in `from_scratch/.bowerrc`). Please note that the latter was actually done by Bower's `bower install` which was called as the npm's post install step (as configured in `from_scratch/package.json`).       

### 4. Enjoy

#### Developing

Start the application using Grunt:

```
grunt serve-minimal
```

The above Grunt's task opens the application in your default browser and watches for any HTML/JavaScript/CSS changes. Once you do one, the page is reloaded automatically! 

#### Testing

Run application's Jasmine tests:

```
grunt test
```

This Grunt's task uses the Karma test runner to execute Jasmine tests (against the PhantomJS) and watches for any change in your JavaScript files (both sources and specs).  Test Driven Development has never been easier :)

If you would like to run the tests against a real browser (rather than against the PhantomJS) or use it to debug a test, call: 

```
grunt test:debug
```

