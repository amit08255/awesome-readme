<div align="center">

# Project Title
<br>
<h4>Project title tracking app built on top of <a href="https://reactjs.org/" target="_blank">ReactJS</a></h4>
</div>

<div align="center">
  <h3>
    <a href="#key-features">
      Website
    </a>
    <span> | </span>
    <a href="#key-features">
      Handbook
    </a>
    <span> | </span>
    <a href="#key-features">
      Ecosystem
    </a>
    <span> | </span>
    <a href="#key-features">
      Contributing
    </a>
    <span> | </span>
    <a href="#key-features">
      Reddit
    </a>
    <span> | </span>
    <a href="#key-features">
      Chat
    </a>
  </h3>
</div>

> ThisMyPC provides a neat web interface that can be used for browsing your desktop drives from any device in your browser itself. With the help of NodeJs, the file details are displayed in JSON format that can then we easily displayed in web browsers.

> The source code is open so that you can download the source code and set it up with ease if you would like to have your own exclusive environment.

<details>
<summary>📖 <b>Table of Contents</b></summary>
<br />

[![-----------------------------------------------------][colored-line]](#table-of-contents)

## ➤ Table of Contents

* [➤ Installation](#-installation)
* [➤ Getting Started (quick)](#-getting-started-quick)
* [➤ Getting Started (slower)](#-getting-started-slower)
	* [Blueprint](#blueprint)
	* [Usage](#usage)
	* [Configuration](#configuration)
* [➤ Templates](#-templates)
	* [Title](#title)
	* [Logo](#logo)
	* [Badges](#badges)
	* [Description](#description)
	* [Table of Contents](#table-of-contents)
	* [Contributors](#contributors)
* [➤ Contributors](#-contributors)
	* [License](#license)
* [➤ License](#-license)
* [➤ Load markdown files](#-load-markdown-files)
* [➤ Automatic documentation](#-automatic-documentation)
	* [my-button](#my-button)
		* [Properties](#properties)
		* [Slots](#slots)
* [➤ A bit about this readme](#-a-bit-about-this-readme)
* [➤ Custom templates](#-custom-templates)
* [➤ Advanced!](#-advanced)
	* [Check broken links](#check-broken-links)
	* [New template syntax](#new-template-syntax)
	* [Variables](#variables)
		* [Objects](#objects)
		* [1D Arrays](#1d-arrays)
		* [2D Arrays](#2d-arrays)
	* [Different colored lines](#different-colored-lines)
	* [Different formatted headings](#different-formatted-headings)
* [➤ Featured README's](#-featured-readmes)
* [➤ Future work](#-future-work)
* [➤ FAQ](#-faq)
	* [Can I see how my README file is going to look before I commit it?](#can-i-see-how-my-readme-file-is-going-to-look-before-i-commit-it)
	* [How can I get involved?](#how-can-i-get-involved)
	* [I already have a large README file - I don't have time to rewrite everything!](#i-already-have-a-large-readme-file---i-dont-have-time-to-rewrite-everything)
	* [How can I support you?](#how-can-i-support-you)
* [➤ Contributors](#-contributors-1)
* [➤ License](#-license-1)
</details>

[![-----------------------------------------------------][colored-line]](#installation)

## ➤ Walkthrough


### Built With

- [Node JS](https://nodejs.org/en/)
- [GraphQL](http://graphql.org)
- [Express JS](https://expressjs.com/)
- [Socket IO](https://socket.io/)
- [Angular](https://angularjs.org/)
- [Electron JS](https://electronjs.org/)
- [Mongodb](https://www.mongodb.com/)
- [React Native](https://facebook.github.io/react-native/)


### Build System
NG6 uses NPM scripts, Gulp, and Webpack together for its build system. Yes, you don't need Gulp if you're using Webpack. This is true if your build system is only responsible for file manipulation. However, ours is not.

`Webpack` handles all file-related concerns:
* Transpiling from ES6 to ES5 with `Babel`
* Loading HTML files as modules
* Transpiling stylesheets and appending them to the DOM
* Refreshing the browser and rebuilding on file changes
* Hot module replacement for transpiled stylesheets
* Bundling the app
* Loading all modules
* Doing all of the above for `*.spec.js` files as well

`Gulp` is the orchestrator:
* Starting and calling Webpack
* Starting a development server (yes, Webpack can do this too)
* Generating boilerplate for the Angular app

**Check out the [JSPM version](https://github.com/angularclass/NG6-starter/tree/jspm)--an alternative to Webpack as an ES6 build system.**

### File Structure

```
src/
 ├──app/                   * WebApp: folder, our source files that will be compiled to javascript
 │   │--shared/            * Do put all shared files within a component feature in a shared folder.
 |   |   |-- exception.service.ts
 |   |   |-- exception.service.spec.ts
 |   |   |-- shared.module.ts * shared module with all shared declarations and providers
 |   |   |-- index.ts             * barrel file
 │   |--app.module.ts      * angular module
 │   |--app.component.ts   * root component
 │   │──app.spec.ts        * a simple test of components in app.ts
 │   │──index.ts           * barrel file
 │   │
 │──assets/                * static assets are served here
 │   ├──icon/              * our list of icons from www.favicon-generator.org
 │   ├──images/            * our custom app images
 │   ├──service-worker.js  * ignore this. Web App service worker that's not complete yet
 │   ├──robots.txt         * for search engines to crawl your website
 │   └──human.txt          * for humans to know who the developers are
 |──main.ts        * our entry file for our browser environment
 │
 |──index.html     * Index.html: where we generate our index page
 │
 |──polyfills.ts   * our polyfills file
 │
 |──vendor.ts      * our vendor file
 |
 └──globals.d.ts   * our custom global type definitions
```

### Testing Setup
All tests are also written in ES6. We use Webpack to take care of the logistics of getting those files to run in the various browsers, just like with our client files. This is our testing stack:
* Karma
* Webpack + Babel
* Mocha
* Chai

To run tests, type `npm test` in the terminal. Read more about testing [below](#testing).


[![-----------------------------------------------------][colored-line]](#installation)

## ➤ Getting Started

### Dependencies
Tools needed to run this app:
* `node` and `npm`

#### Install Node.js

Node.js is an environment that can run JavaScript code outside of a web browser and is used to write and run server-side JavaScript apps. Node.js installation includes `npm`, the package manager that allows you to install NPM modules from your terminal. 
You can download an installer from the [Node.js homepage](https://nodejs.org/en/).

##### Check your Node.js installation

Check that you have the minimum required version installed by running the following command:

```sh
node -v
```

You should see a version larger than Node 10.

```sh
node -v
v12.14.0
```

> Project name' minimum supported Node.js version is Node 10, but more recent versions will work as well.


### Installing
* `fork` this repo
* `clone` your fork
* `npm install` to install dependencies

### Running the App
NG6 uses Gulp to build and launch the development environment. After you have installed all dependencies, you may run the app. Running `npm start` will bundle the app with `webpack`, launch a development server, and watch all files. The port will be displayed in the terminal.
 
#### Tasks
Here's a list of available tasks:
* `npm run build`
  * runs Webpack, which will transpile, concatenate, and compress (collectively, "bundle") all assets and modules into `dist/bundle.js`. It also prepares `index.html` to be used as application entry point, links assets and created dist version of our application.
* `npm run serve`
  * starts a dev server via `webpack-dev-server`, serving the client folder.
* `npm run watch`
  * alias of `serve`
* `npm start` (which is the default task that runs when typing `gulp` without providing an argument)
  * runs `serve`.
* `npm run component`
  * scaffolds a new Angular component. [Read below](#generating-components) for usage details.
  
### Testing
To run the tests, run `npm test`.

`Karma` combined with Webpack runs all files matching `*.spec.js` inside the `app` folder. This allows us to keep test files local to the component--which keeps us in good faith with continuing to build our app modularly. The file `spec.bundle.js` is the bundle file for **all** our spec files that Karma will run.

Be sure to define your `*.spec.js` files within their corresponding component directory. You must name the spec file like so, `[name].spec.js`. If you don't want to use the `.spec.js` suffix, you must change the `regex` in `spec.bundle.js` to look for whatever file(s) you want.
`Mocha` is the testing suite and `Chai` is the assertion library. If you would like to change this, see `karma.conf.js`.

#### Examples

It's always easier to learn something if you have an examples. Here is a list of repos which based on this starter:

 - [TodoMVC Example App](https://github.com/AngularClass/NG6-todomvc-starter)

### Usage

Run the `node_modules/.bin/readme generate` command and a README file will be generated for you. If you want to go into depth with the readme command, check out the following options or write `node_modules/.bin/readme generate -h` in your terminal if that's your cup of tea.


| Option                | Type                                             | Description                                      |
|-----------------------|--------------------------------------------------|--------------------------------------------------|
| -c, --config          | string                                           | Path of the configuration file. Defaults to 'blueprint.json |
| -p, --package         | string                                           | Path of the 'package.json' file. Defaults to 'package.json'. |
| --pkg.name            | string                                           | Name of the project. Used for the 'title' template. |
| --pkg.contributors    | {name: string; email: string; url: string; img: string; info: string[];}[] | Contributors of the project. Used for the 'contributors' template. |
| --pkg.license         | string                                           | License kind. Used for the 'license' template.   |
| -o, --output          | string                                           | Path of the generated README file. Defaults to 'README.md'. |
| -h, --help            |                                                  | Display this help message.                       |
| -i, --input           | string                                           | The blueprint. Defaults to 'blueprint.md'.       |
| --badges              | {alt: string, url: string, img: string}[]        | Badges. Used for the 'badges' template.          |
| --text                | string                                           | Text describing your project. Used for the 'description' template. |
| --demo                | string                                           | Demo url for your project. Used for the 'description' template. |
| --lineBreak           | string                                           | The linebreak used in the generation of the README file. Defaults to 'rn' |
| --tab                 | string                                           | The tab used in the generation of the README file. Defaults to 't' |
| --placeholder         | [string, string]                                 | The placeholder syntax used when looking for templates in the blueprint. Defaults to '["{{", "}}"]. |
| --line                | string                                           | The line style of the titles. Can also be an URL. Defaults to 'colored'. |
| --templates           | {name: string, template: string}[]               | User created templates.                          |
| -s, --silent          | boolean                                          | Whether the console output from the command should be silent. |
| -d, --dry             | boolean                                          | Whether the command should run as dry. If dry, the output file is notgenerated but outputted to the console instead. |
| --headingPrefix       | {[key: number]: string}                          | The prefix of the header tags. Defaults to '{1: "➤ ", 2: "➤ "}' |
| --logo                | {src: string; alt?: string; width?: number; height?: number;} | The logo information. Used for the 'logo' template. |
| --contributorsPerRow  | number                                           | The amount of contributors pr row when using the 'contributors' template. Defaults to '6' |
| --documentationConfig | object                                           | Configuration object for automatic documentation template. |
| --extend              | string                                           | Path to another configuration object that should be extended. |
| --checkLinks          | boolean                                          | Checks all links for aliveness after the README file has been generated. |


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[colored-line]: ./.docs/lines/colored.png