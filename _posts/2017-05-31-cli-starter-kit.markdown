# Build Tools Example

Example of build tools using NPM scripts.

## Dependencies

Node.js

## Instructions

<a href="https://github.com/evelynmaire/cli-starter-kit/archive/master.zip">Download required files</a>.

`cd` into your directory

`open package.json`

### Install dependencies

run: `npm install`

### Run one of the following build scripts.

* Compile CSS

run: `npm run build:css`

Compile Sass to CSS and watches the 'src/sass' directory for changes.

* Lint and Browserify JavaScript

run: `npm run build:js`

Lint and Browserify JavaScript and watch the 'src/js' directory for changes.

* Compile CSS, Lint and Browserify JavaScript

run: `npm run build watch`

Compile Sass to CSS, Lint and Browserify JavaScript and watch the 'src' directory for changes.

* Browsersync

While watch tasks are running open a new Terminal window to run Browsersync.

run: `npm run browser-sync`

Sync browser when all HTML files and all files in the 'public' directory change.

## Licence

Licensed under the MIT Licence
