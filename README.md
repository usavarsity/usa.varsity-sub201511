# USA.Varsity

<!-- MarkdownTOC -->
- [Getting Started](#getting-started)
  - [Dependencies](#dependencies)
  - [git](#git)
  - [SalesForce](#salesforce)
  - [Grunt](#grunt)
    - [Initialize (WIP)](#initialize-wip)
    - [Development](#development)
    - [Build](#build)
    - [Shortcuts](#shortcuts)
  - [Project Structure](#project-structure)
- [To Do](#to-do)
<!-- /MarkdownTOC -->

## Getting Started

### Dependencies

Install dependencies with:

```sh
$ npm install
```
---

Third-party dependencies are managed with [grunt-wiredep](https://github.com/stephenplusplus/grunt-wiredep). Add new dependencies using **Bower** and then run the **Grunt** task to load them:

```sh
$ bower install --save plugin_name
$ grunt wiredep
```

This works if the package author has followed the [Bower spec](https://github.com/bower/bower.json-spec). If the file is not automatically added to the grunt configuration

To manually add dependencies, `bower install --save depName` to get the files, then add a `script` or `style` tag to your `index.html` or another appropriate place.

The components are installed in the root of the project at `/bower_components`. To reference them from index.html, use `src="bower_components"` or `src="/bower_components"`. Treat the `bower_components` directory as if it was a sibling to `index.html`.

*Testing Note*: a project checked into source control and later checked out needs to have `bower install` run from the `test` folder as well as from the project root.

* [Node.js](http://nodejs.org/)
* [bower](https://github.com/bower/bower)
* [Grunt CLI](https://github.com/gruntjs/grunt-cli)
* [Sass](http://sass-lang.com/install)

### git

The project has been under git version control since it was initialized.

### Salesforce

### Grunt

The project is build and developed using the [Grunt Task Runner](http://gruntjs.com/).

`grunt`         To build the work environment, generating css from scss files, compiling js, etc..
`grunt serve`   Launch local host environment and launches live preview of web app.
`grunt deploy`  Build and upload `dist` as a `static resource` in [Force.com](https://developer.force.com)

### Project Structure

Quick overview of the file structure for development and maintenance

<pre>
$ ls -R | grep ":" | sed -e 's/://' -e 's/[^-][^\/]*\//--/g' -e 's/^/   /' -e 's/-/|/'
 |-app
 |---fonts
 |---images
 |---scripts
 |---styles
 |-bower_components
 |-node_modules
 |-test
 |---spec
</pre>

## To Do

* [ ]

## License
Copyright (c) Varsity Brands | GNU GENERAL PUBLIC LICENSE

>   LICENSE