# npmdoc-rsvp

#### api documentation for  [rsvp (v3.5.0)](https://github.com/tildeio/rsvp.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-rsvp.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-rsvp) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-rsvp.svg)](https://travis-ci.org/npmdoc/node-npmdoc-rsvp)

#### A lightweight library that provides tools for organizing asynchronous code

[![NPM](https://nodei.co/npm/rsvp.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/rsvp)

- [https://npmdoc.github.io/node-npmdoc-rsvp/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-rsvp/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-rsvp/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-rsvp/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-rsvp/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-rsvp/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tilde, Inc. & Stefan Penner"
    },
    "browser": {
        "vertx": false
    },
    "bugs": {
        "url": "https://github.com/tildeio/rsvp.js/issues"
    },
    "dependencies": {},
    "description": "A lightweight library that provides tools for organizing asynchronous code",
    "devDependencies": {
        "broccoli-babel-transpiler": "^5.6.1",
        "broccoli-concat": "^3.0.2",
        "broccoli-merge-trees": "^1.1.1",
        "broccoli-rollup": "^1.0.2",
        "broccoli-stew": "^1.2.0",
        "broccoli-uglify-js": "^0.2.0",
        "broccoli-watchify": "v1.0.0",
        "ember-cli": "2.12.0-beta.1",
        "ember-cli-dependency-checker": "^1.3.0",
        "ember-publisher": "0.0.7",
        "git-repo-version": "0.4.0",
        "json3": "^3.3.2",
        "mocha": "^1.20.1",
        "promises-aplus-tests-phantom": "^2.1.0-revise",
        "release-it": "0.0.10"
    },
    "directories": {
        "lib": "lib"
    },
    "dist": {
        "shasum": "a62c573a4ae4e1dfd0697ebc6242e79c681eaa34",
        "tarball": "https://registry.npmjs.org/rsvp/-/rsvp-3.5.0.tgz"
    },
    "engines": {
        "node": "0.12.* || 4.* || 6.* || 7.*"
    },
    "files": [
        "dist",
        "lib",
        "!dist/test"
    ],
    "gitHead": "3b75eb7a7d00f3c2fa0dbc4720b24bb624e11f4b",
    "homepage": "https://github.com/tildeio/rsvp.js#readme",
    "jsnext:main": "dist/rsvp.es.js",
    "keywords": [
        "promises",
        "futures"
    ],
    "license": "MIT",
    "main": "dist/rsvp.js",
    "maintainers": [
        {
            "name": "wycats"
        },
        {
            "name": "ryanflorence"
        },
        {
            "name": "stefanpenner"
        },
        {
            "name": "fivetanley"
        },
        {
            "name": "mixonic"
        }
    ],
    "module": "dist/rsvp.es.js",
    "name": "rsvp",
    "namespace": "RSVP",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/tildeio/rsvp.js.git",
        "dist": "git@github.com:components/rsvp.js.git"
    },
    "scripts": {
        "build": "ember build --environment production",
        "build:production": "ember build --env production",
        "dry-run-release": "ember build --environment production && release-it --dry-run --non-interactive",
        "lint": "jshint lib",
        "prepublish": "ember build --environment production",
        "start": "ember s",
        "test": "ember test",
        "test:node": "ember build && mocha ./dist/test/browserify",
        "test:server": "ember test --server"
    },
    "version": "3.5.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
