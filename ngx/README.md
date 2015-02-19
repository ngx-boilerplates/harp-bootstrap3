![AngularJS Express](http://i.imgur.com/nTj9QgN.png)

## Bootstrap 3 boilerplate for AngularJS Express

**Zero configuration required!**

This boilerplate combines all best practices of:

- customizing [Bootstrap 3](http://getbootstrap.com) to keep CSS file size down as much as possible
- the lovely [HarpJS](http://harpjs.com) web server

Component based approach:

- add/remove features by adding/removing components
- add/remove components by adding/removing files
- each components has its own styles, scripts and templates

## Installation

Install the latest dependencies:

```sh
$ npm install
$ bower install
```

Run gulp to assemble the concatenated AngularJS library:

```sh
$ gulp
```

Start the harp server from your project directory:

```sh
$ harp server
```

And navigate to `http://localhost:9000` in your browser.


## How it works

All action happens in the `public` directory, so let's have a look at its structure:

```sh
public
├── 200.jade
├── _build                          # main _build directory for global app stuff
│   ├── _bootstrap.less             # Enable/disable Bootstrap 3 modules you need
│   ├── _mixins.less                # Place to put your custom mixins
│   ├── _variables.less             # Customize the Bootstrap 3 variables
│   ├── app.js                      # Global JavaScript (empty by default)
│   ├── app.less                    # Global app styles that you want Gulp to add to /public/build/css/app.css
├── build                           # Build directory where files built by Gulp are saved
│   ├── css
│   │   ├── app.css                 # All .less files from _build directories are concatenated here
│   │   └── app.min.css             # Minified version for production
│   └── js
│       ├── app.js                  # All .js files from _build directories are concatenated here
│       └── app.min.js              # Minified version for production
└── components
    ├── footer                      # Example footer component
    │   ├── _build                  # Component _build directory with files that you want Gulp to build
    │   │   └── footer.less         # Styles that you want to add to /public/build/css/app.css
    │   └── footer.jade             # Jade file will be compiled to HTML automatically
    ├── header                      # Example header component
    │   ├── _build                  # Component _build directory with files that you want Gulp to build
    │   │   └── header.less         # Styles that you want to add to /public/build/css/app.css
    │   └── header.jade             # Jade file will be compiled to HTML automatically
    └── homepage                    # Example homepage component
        ├── _build                  # Component _build directory with files that you want Gulp to build
        │   └── homepage.routes.js  # JavaScript code that you want to add to /public/build/js/app.js
        └── homepage.jade           # Jade file will be compiled to HTML automatically
```

## Gulp

Gulp is used to:

- selectively copy specific files from the Bower components to the `public/vendor` directory
- build individual components from all `_build` directories into the `public/build` directory

## Changelog

### v0.1.0

- Initial boilerplate
