# grunt-angular-i18n-finder

> Find key name for Angular i18n

This plugin will read all given template files and look for `'_key_name' | i18n` and try to compare with list of key names from given JSON blob file to look for unused key names.

## Getting Started
This plugin requires Grunt `~0.4.2`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-angular-i18n-finder --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-angular-i18n-finder');
```

## The "angular_i18n_finder" task

### Overview
In your project's Gruntfile, add a section named `angular_i18n_finder` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
    angular_i18n_finder: {
      files: [ "views/*.html", "views/**/*.html" ],
      options: {
        pathToJSON: [ "locale/en_US/*.json" ],
        ignoreKeys: [ "Blah", "just a var key name", "what does the fox say" ],
      },
    },
});
```

### Options

#### options.pathToJSON
Type: `Array`

An array of path to JSON blob file(s).

#### options.ignoreKeys
Type: `Array`

An array of strings value that is used to ignore any keys that you don't want it to complain about.

### options.filter
Type: `String` (default: _i18n_)

A filter name used to perform translation. If you are using an other filter than `i18n` to print
translated strings (ex: `{{ '_key_name' | translate }}` ), set `filter: "translate"`.

#Support:

Currently we support both `.html` and `.ejs`.
