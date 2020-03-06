# USAJOBS Design System

This repository houses the design system for the next generation of USAJOBS. A design system describes the base visual language, using UI elements and style guidelines, upon which the site can be built. It will also include examples and usage guidelines of new components.

The USAJOBS design system starts with the The [U.S. Web Design System](https://designsystem.digital.gov/) and extends them to meet the needs of the USAJOBS next generation project. This repo allows the team working on USAJOBS to:

1. Document where we have intentionally deviated from an existing guildeline in the U.S. Web Design Standards and provide a platform for contributing back to those standards.

2. Document where we have unintentionally deviated from an existing guideline in the U.S. Web Design Standards and want to track getting back inline with the standards.

3. Design new components or elements that are not yet a part of the U.S. Web Design Standards. These components or elements may or may not be appropriate to contribute back to the standards given their potential for reuse elsewhere.

## Setup for your local environment

### Requirements

This repo uses [Jekyll](https://jekyllrb.com/) to serve and build the markup of the site. CSS and JS are managed by [Gulp](https://gulpjs.com/).

Thus you will need [Ruby](https://www.ruby-lang.org) ( > version 2.2.3 ) and [Node](https://nodejs.org/en/download/) ( > 4.1.2 ). The Node install will also provide npm, the Node package manager.

You may consider using a Ruby version manager such as
[rbenv](https://github.com/sstephenson/rbenv) or [rvm](https://rvm.io/) to
help ensure that Ruby version upgrades don't mean all your
[gems](https://rubygems.org/) will need to be rebuilt.

On OS X, you can also use [Homebrew](http://brew.sh/) to install Ruby in
`/usr/local/bin`, which may require you to update your `$PATH` environment
variable. Here are the commands to follow to install via homebrew:

```shell
$ brew update
$ brew install ruby
$ brew install node
```

If you do use rbenv it is important to set your global Ruby version to 2.2.3 or higher so that you can install gems properly:

```shell
$ rbenv global
```

### Installation

Now that you have verified that you have Ruby and Node installed, run the following commands to clone the USA Jobs repo and install the packages that the design system depends upon:

Note: some of the following npm commands may require ```sudo```

```shell
$ git clone https://github.com/USAJOBS/design-system.git
$ cd cd openopps-help
$ bundle install
$ npm install -g gulp
$ npm install -g gulp-cli
$ npm install
$ npm run build
```

The post-install step should run bundle install.

### Development

To view and work on the site run:

```shell
$ npm start
```

This will perform the necessary Jekyll build, generate concatenated CSS and JS files, serve the site, and watch for changes to Sass and JS files. You should now be able to visit `http://127.0.0.1:4001/` and view the design system locally.

Questions or need help with setup? Feel free to open an issue here [https://github.com/USAJOBS/design-system/issues](https://github.com/USAJOBS/design-system/issues).

### How to use this repo in projects

We will create a new repo for each project that will incrementally redesign a portion of the USAJOBS site. Those project repos will depend on the usajobs-design-system node module.

If you have node installed on your machine, you can use npm to install the design system. Add usajobs-design-system to your project's package.json as a dependency:

```shell
npm install usajobs-design-system --save
```

The package will be installed in `node_modules/usajobs-design-system`.

The main Sass (SCSS) source file is here:

```shell
_scss/all-usajobs.scss
```

## Feedback

Please create a [GitHub Issue](https://github.com/USAJOBS/design-system/issues).

## Contributing to the code base

See [CONTRIBUTING](CONTRIBUTING.md).

## Licenses and attribution

Please refer to the [LICENSE](LICENSE.md) page.
