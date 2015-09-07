# grunt-import-js

> Copy JS files from src to dest, replacing @import instructions for other JS files by their contents.

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-import-js --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-import-js');
```

## The "import_js" task

Add @import instruction to your JS files and let them be replaced bei the content of the files.

```js
// @import "vendor/js/jquery/jquery.min.js";
// @import "vendor/js/bootstrap/bootstrap.min.js";
// @import "base.js";
```

### Overview
In your project's Gruntfile, add a section named `import_js` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  import_js: {
    files: {
      // file list options go here.
    },
  },
});
```

### Options

none


### Usage Examples

In this example, import-js is used to read all javascript files from `app/Resources/js/` and scan them for @import instructions. The content of the @import files then replaces the @import instruction.

```js
grunt.initConfig({
  import_js: {
    files: {
      expand: true,
      cwd: 'app/Resources/js/',
      src: ['**/*.js'],
      dest: 'assets/js/',
      ext: '.js'
    }
  },
});
```


## Release History
_(Nothing yet)_