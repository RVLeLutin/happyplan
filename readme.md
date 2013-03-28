# Happy Plan! [![Build Status](https://travis-ci.org/kud/happy-plan.png)](https://travis-ci.org/kud/happy-plan)

> When Grunt.js uses Jekyll as a peon.

Happy plan is bundle of amazing tools to be used as a static website generator. It's all about fun and so easy to publish on [gh-pages](http://pages.github.com/).

### What in it?

* A static website generator from html or markdown: [Jekyll](https://github.com/mojombo/jekyll).
* A task-based command line build tool: [Grunt.js](http://gruntjs.com/) & some pre-defined tasks (scripts, styles & images automatic minification & compression).
* An amazing CSS pre-processor, [Sass](http://sass-lang.com/) directly served with [Compass](http://compass-style.org/).
* A quick way to provide scalable icons as font thanks to [Fontcustom](http://fontcustom.com/) & a Grunt task.
* A [Livereload](http://livereload.com/) server ([tiny-lr](https://github.com/mklabs/tiny-lr) provided by the [grunt-contrib-livereload](https://github.com/gruntjs/grunt-contrib-livereload) task) to make development as fast as hell.
* A package manager for the web called [Bower](https://github.com/twitter/bower) to handle web components.

Oh, by the way, why "happy plan" ? [Here is not the answer](http://www.youtube.com/watch?v=5zVVKXT8Vi0).

## Requirements

The easy way is on **OS X** (but it shouldn't be so hard to make this working on any unix like system. Make a PR :)).

### Jekyll [[+](https://github.com/mojombo/jekyll/wiki/install)]

    $ (sudo) gem install jekyll

### Node.js [[+](https://github.com/joyent/node/wiki/Installation)]

    $ brew install node

#### Npm [[+](https://github.com/isaacs/npm)]

    $ curl http://npmjs.org/install.sh | sh

### Grunt.js (>0.4) [[+](http://gruntjs.com/getting-started)]

    $ npm install -g grunt-cli

### Compass [[+](http://compass-style.org/install/)]

    $ (sudo) gem install compass

### Optionals

#### Fontcustom [[+](http://fontcustom.com/#installation)]

    $ brew install fontforge eot-utils ttfautohint
    $ (sudo) gem install fontcustom

##### More for [grunt-webfont](https://github.com/sapegin/grunt-webfont) task

    $ brew install ttf2eot
    $ brew install https://raw.github.com/sapegin/grunt-webfont/master/Formula/sfnt2woff.rb

#### Bower [[+](https://github.com/twitter/bower#installing-bower)]

    $ npm install bower -g

---

## Installation

When everything above is okay, just run:

    $ npm install

That's it. Now you can start your website bro'.

## Build

To build the website

    $ grunt dist

## Development

Using `watch` will allow you to test & dev your posts with livereload included (it needs a [livereload browser extension](http://go.livereload.com/extensions))

    $ grunt

## Server

You certainly need an http server to display your website. No problem, just use this command:

    $ node server.js

and connect you to `http://localhost:8080`.

---

## Publish on gh-pages (github)

If you want to publish your build on the gh-pages:

    $ bin/publish.sh

This script just build the website (grunt dist) & commit + push on gh-pages branch.

### Please, read it

You absolutely must create one branche: a source branch `src` for your devevelopment branch, and `gh-pages` or `master` to publish your static files. The script will push it for you.

#### Warning for username.github.com

`username.github.com` is a bit special. It's act already like a `gh-pages` branch, so builded files should be on `master` branch. So use a `src` branch for the source.

You have to modify yourself the `publish.sh` file for now. An option will come to not change the file, it'll be easier.

## Create a new post

Want to create a new post quickly? No problem.

    $ node bin/newpost.js

This create a new post in `src/_posts`.

For more informations about posts, just read [Jekyll's doc](https://github.com/mojombo/jekyll/wiki)

---

# Migrations

[Jekyll already have a migration doc](https://github.com/mojombo/jekyll/wiki/blog-migrations)

Note: For Wordpress, [wordpress-to-jekyll-exporter](https://github.com/benbalter/wordpress-to-jekyll-exporter) seems a quick & good choice (+ keep disqus thread id !)

---

# Support

Come up and say hello on [IRC](http://webchat.freenode.net/?channels=happyplan)! We'll be glad to answer you if you have any questions.

    #happyplan @ irc.freenode.net

