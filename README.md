# Pedestal Docs [![Build Status](https://travis-ci.com/pedestal/pedestal-docs.svg?branch=master)](https://travis-ci.com/pedestal/pedestal-docs)

This is an open-source repository of documentation for the
[Pedestal](https://github.com/pedestal/pedestal) libraries.

## Get Started with Pedestal

[Read Pedestal Docs](http://pedestal.io)

##  Contributing

If you wish to point out an issue in the site or propose a new page,
you can do so by filing a GitHub issue at
https://github.com/pedestal/pedestal-docs/issues

If you wish to make a contribution (typo, modification, or new
content), see [CONTRIBUTING.md](./CONTRIBUTING.md).

## Building the Site

The site is built using [JBake](http://jbake.org/).

See the JBake [download](https://jbake.org/download.html) site for installation instructions.

You'll need a recent version of JBake; if you are on an M1 Mac, you'll need 2.7.0 (currently pre-release).

To build the site, you need side-by-side checkouts of Pedestal and Pedestal Docs.

Retrieve Pedestal and switch to a publicly-available version:

    git clone https://github.com/pedestal/pedestal.git pedestal
    cd pedestal
    git checkout 0.5.8
    cd .. # back out to the parent directory

To build the site:

Retrieve the content:

* `git clone https://github.com/pedestal/docs.git pedestal-docs` (or your own fork)
* `cd pedestal-docs`

Generate the pages:

* `jbake -b -s` - this will create the static site in the output
  directory, start a web server and watch for changes. The local site
  is available at http://localhost:8820/index.

### Pedestal API Documentation

Pedestal API documentation should be updated after each Pedestal release; this is accomplished via
the `script/gen-api-doc.sh` script.

This generates API documentation into the `api` directory.  When deploying, the contents of
the `api` directory are merged with the generated content in `output`.

License
-------
Copyright 2014-2023 Cognitect, Inc.

The use and distribution terms for this software are covered by the
[Eclipse Public License 1.0](http://opensource.org/licenses/eclipse-1.0)
which can be found in the file [epl-v10.html](epl-v10.html) at the root of this
distribution.

By using this software in any fashion, you are agreeing to be bound by
the terms of this license.

You must not remove this notice, or any other, from this software.
