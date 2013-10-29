# grunt-goserver

> Grunt task to spawn and reload a Go server

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-goserver --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-goserver');
```

## The "goserver" task

### Overview
In your project's Gruntfile, add a section named `goserver` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  goserver: {
    options: {
      // Task-specific options go here.
    },
    default: {
      srcPath: '/full/path/to/src/folder',
      srcFile: 'name_of_go_file_to_build',
      binPath: '/full/path/to/go/bin/folder'
    },
  },
})
```

### Options

#### options.srcPath
Type: `String`
Default value: `''`

Full path to Go source folder
Must be the full path, do not use ~/

#### options.srcFile
Type: `String`
Default value: `''`

Name of Go source file to build e.g. 'main'
Extension is not necessary

#### options.binPath
Type: `String`
Default value: `''`

Full path to Go binary folder
Must be the full path, do not use ~/
This is the path where your binary will be installed when doing 'go install'.

### Usage Examples

#### Default Options

```js
grunt.initConfig({
  goserver: {
    options: {},
    default: {
      srcPath: '/Users/John/Go/src/github.com/john/repo_name',
      srcFile: 'main',
      binPath: '/Users/John/Go/bin'
    },
  },
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
