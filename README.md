# api documentation for  [rsvp (v3.5.0)](https://github.com/tildeio/rsvp.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-rsvp.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-rsvp) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-rsvp.svg)](https://travis-ci.org/npmdoc/node-npmdoc-rsvp)
#### A lightweight library that provides tools for organizing asynchronous code

[![NPM](https://nodei.co/npm/rsvp.png?downloads=true)](https://www.npmjs.com/package/rsvp)

[![apidoc](https://npmdoc.github.io/node-npmdoc-rsvp/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-rsvp_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-rsvp/build/apidoc.html)

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
            "name": "wycats",
            "email": "wycats@gmail.com"
        },
        {
            "name": "ryanflorence",
            "email": "rpflorence@gmail.com"
        },
        {
            "name": "stefanpenner",
            "email": "stefan.penner@gmail.com"
        },
        {
            "name": "fivetanley",
            "email": "dstanley.stuart@gmail.com"
        },
        {
            "name": "mixonic",
            "email": "matt.beale@madhatted.com"
        }
    ],
    "module": "dist/rsvp.es.js",
    "name": "rsvp",
    "namespace": "RSVP",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "3.5.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module rsvp](#apidoc.module.rsvp)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>Promise (resolver, label)](#apidoc.element.rsvp.Promise)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>all (array, label)](#apidoc.element.rsvp.all)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>allSettled (entries, label)](#apidoc.element.rsvp.allSettled)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>asap (callback, arg)](#apidoc.element.rsvp.asap)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>async (callback, arg)](#apidoc.element.rsvp.async)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>cast (value, label)](#apidoc.element.rsvp.cast)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>configure (name, value)](#apidoc.element.rsvp.configure)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>defer (label)](#apidoc.element.rsvp.defer)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>denodeify (nodeFunc, options)](#apidoc.element.rsvp.denodeify)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>filter (promises, filterFn, label)](#apidoc.element.rsvp.filter)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>hash (object, label)](#apidoc.element.rsvp.hash)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>hashSettled (object, label)](#apidoc.element.rsvp.hashSettled)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>map (promises, mapFn, label)](#apidoc.element.rsvp.map)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>off ()](#apidoc.element.rsvp.off)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>on ()](#apidoc.element.rsvp.on)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>race (array, label)](#apidoc.element.rsvp.race)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>reject (reason, label)](#apidoc.element.rsvp.reject)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>resolve (value, label)](#apidoc.element.rsvp.resolve)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>rethrow (reason)](#apidoc.element.rsvp.rethrow)
1.  object <span class="apidocSignatureSpan">rsvp.</span>EventTarget
1.  object <span class="apidocSignatureSpan">rsvp.</span>Promise.prototype
1.  object <span class="apidocSignatureSpan">rsvp.</span>default

#### [module rsvp.EventTarget](#apidoc.module.rsvp.EventTarget)
1.  [function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>mixin (object)](#apidoc.element.rsvp.EventTarget.mixin)
1.  [function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>off (eventName, callback)](#apidoc.element.rsvp.EventTarget.off)
1.  [function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>on (eventName, callback)](#apidoc.element.rsvp.EventTarget.on)
1.  [function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>trigger (eventName, options, label)](#apidoc.element.rsvp.EventTarget.trigger)

#### [module rsvp.Promise](#apidoc.module.rsvp.Promise)
1.  [function <span class="apidocSignatureSpan">rsvp.</span>Promise (resolver, label)](#apidoc.element.rsvp.Promise.Promise)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.</span>all (entries, label)](#apidoc.element.rsvp.Promise.all)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.</span>cast (object, label)](#apidoc.element.rsvp.Promise.cast)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.</span>race (entries, label)](#apidoc.element.rsvp.Promise.race)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.</span>reject (reason, label)](#apidoc.element.rsvp.Promise.reject)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.</span>resolve (object, label)](#apidoc.element.rsvp.Promise.resolve)

#### [module rsvp.Promise.prototype](#apidoc.module.rsvp.Promise.prototype)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>_onError (reason)](#apidoc.element.rsvp.Promise.prototype._onError)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>catch (onRejection, label)](#apidoc.element.rsvp.Promise.prototype.catch)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>constructor (resolver, label)](#apidoc.element.rsvp.Promise.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>finally (callback, label)](#apidoc.element.rsvp.Promise.prototype.finally)
1.  [function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>then (onFulfillment, onRejection, label)](#apidoc.element.rsvp.Promise.prototype.then)
1.  string <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>_guidKey

#### [module rsvp.default](#apidoc.module.rsvp.default)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>Promise (resolver, label)](#apidoc.element.rsvp.default.Promise)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>all (array, label)](#apidoc.element.rsvp.default.all)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>allSettled (entries, label)](#apidoc.element.rsvp.default.allSettled)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>asap (callback, arg)](#apidoc.element.rsvp.default.asap)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>async (callback, arg)](#apidoc.element.rsvp.default.async)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>cast (value, label)](#apidoc.element.rsvp.default.cast)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>configure (name, value)](#apidoc.element.rsvp.default.configure)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>defer (label)](#apidoc.element.rsvp.default.defer)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>denodeify (nodeFunc, options)](#apidoc.element.rsvp.default.denodeify)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>filter (promises, filterFn, label)](#apidoc.element.rsvp.default.filter)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>hash (object, label)](#apidoc.element.rsvp.default.hash)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>hashSettled (object, label)](#apidoc.element.rsvp.default.hashSettled)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>map (promises, mapFn, label)](#apidoc.element.rsvp.default.map)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>off ()](#apidoc.element.rsvp.default.off)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>on ()](#apidoc.element.rsvp.default.on)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>race (array, label)](#apidoc.element.rsvp.default.race)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>reject (reason, label)](#apidoc.element.rsvp.default.reject)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>resolve (value, label)](#apidoc.element.rsvp.default.resolve)
1.  [function <span class="apidocSignatureSpan">rsvp.default.</span>rethrow (reason)](#apidoc.element.rsvp.default.rethrow)
1.  object <span class="apidocSignatureSpan">rsvp.default.</span>EventTarget



# <a name="apidoc.module.rsvp"></a>[module rsvp](#apidoc.module.rsvp)

#### <a name="apidoc.element.rsvp.Promise"></a>[function <span class="apidocSignatureSpan">rsvp.</span>Promise (resolver, label)](#apidoc.element.rsvp.Promise)
- description and source-code
```javascript
function Promise$1(resolver, label) {
  this._id = counter++;
  this._label = label;
  this._state = undefined;
  this._result = undefined;
  this._subscribers = [];

  config.instrument && instrument$1('created', this);

  if (noop !== resolver) {
    typeof resolver !== 'function' && needsResolver();
    this instanceof Promise$1 ? initializePromise(this, resolver) : needsNew();
  }
}
```
- example usage
```shell
...
section below on TaskJS for more information.

### Basic Usage

'''javascript
var RSVP = require('rsvp');

var promise = new RSVP.Promise(function(resolve, reject) {
  // succeed
  resolve(value);
  // or reject
  reject(error);
});

promise.then(function(value) {
...
```

#### <a name="apidoc.element.rsvp.all"></a>[function <span class="apidocSignatureSpan">rsvp.</span>all (array, label)](#apidoc.element.rsvp.all)
- description and source-code
```javascript
function all$3(array, label) {
  return Promise$1.all(array, label);
}
```
- example usage
```shell
...
is rejected.

'''javascript
var promises = [2, 3, 5, 7, 11, 13].map(function(id){
  return getJSON("/post/" + id + ".json");
});

RSVP.all(promises).then(function(posts) {
  // posts contains an array of results for the given promises
}).catch(function(reason){
  // if any of the promises fails.
});
'''

## Hash of promises
...
```

#### <a name="apidoc.element.rsvp.allSettled"></a>[function <span class="apidocSignatureSpan">rsvp.</span>allSettled (entries, label)](#apidoc.element.rsvp.allSettled)
- description and source-code
```javascript
function allSettled$1(entries, label) {
  return new AllSettled(Promise$1, entries, label).promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.asap"></a>[function <span class="apidocSignatureSpan">rsvp.</span>asap (callback, arg)](#apidoc.element.rsvp.asap)
- description and source-code
```javascript
function asap$1(callback, arg) {
  queue$1[len] = callback;
  queue$1[len + 1] = arg;
  len += 2;
  if (len === 2) {
    // If len is 1, that means that we need to schedule an async flush.
    // If additional callbacks are queued before the queue is flushed, they
    // will be processed by this flush that we are scheduling.
    scheduleFlush$1();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.async"></a>[function <span class="apidocSignatureSpan">rsvp.</span>async (callback, arg)](#apidoc.element.rsvp.async)
- description and source-code
```javascript
function async(callback, arg) {
  return config.async(callback, arg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.cast"></a>[function <span class="apidocSignatureSpan">rsvp.</span>cast (value, label)](#apidoc.element.rsvp.cast)
- description and source-code
```javascript
function resolve$3(value, label) {
  return Promise$1.resolve(value, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.configure"></a>[function <span class="apidocSignatureSpan">rsvp.</span>configure (name, value)](#apidoc.element.rsvp.configure)
- description and source-code
```javascript
function configure(name, value) {
  if (name === 'onerror') {
    // handle for legacy users that expect the actual
    // error to be passed to their function added via
    // 'RSVP.configure('onerror', someFunctionHere);'
    config['on']('error', value);
    return;
  }

  if (arguments.length === 2) {
    config[name] = value;
  } else {
    return config[name];
  }
}
```
- example usage
```shell
...
});
'''


**NOTE:** promises do allow for errors to be handled asynchronously, so
this callback may result in false positives.

**NOTE:** Usage of 'RSVP.configure('onerror', yourCustomFunction);' is
deprecated in favor of using 'RSVP.on'.


## Finally

'finally' will be invoked regardless of the promise's fate, just as native
try/catch/finally behaves.
...
```

#### <a name="apidoc.element.rsvp.defer"></a>[function <span class="apidocSignatureSpan">rsvp.</span>defer (label)](#apidoc.element.rsvp.defer)
- description and source-code
```javascript
function defer$1(label) {
  var deferred = { resolve: undefined, reject: undefined };

  deferred.promise = new Promise$1(function (resolve, reject) {
    deferred.resolve = resolve;
    deferred.reject = reject;
  }, label);

  return deferred;
}
```
- example usage
```shell
...
  or
{ state: 'rejected', reason: reason }
'''

## Deferred

> The 'RSVP.Promise' constructor is generally a better, less error-prone choice
> than 'RSVP.defer()'. Promises are recommended unless the specific
> properties of deferred are needed.

Sometimes one needs to create a deferred object, without immediately specifying
how it will be resolved. These deferred objects are essentially a wrapper around
a promise, whilst providing late access to the 'resolve()' and 'reject()' methods.

A deferred object has this form: '{ promise, resolve(x), reject(r) }'.
...
```

#### <a name="apidoc.element.rsvp.denodeify"></a>[function <span class="apidocSignatureSpan">rsvp.</span>denodeify (nodeFunc, options)](#apidoc.element.rsvp.denodeify)
- description and source-code
```javascript
function denodeify$1(nodeFunc, options) {
  var fn = function fn() {
    var self = this;
    var l = arguments.length;
    var args = new Array(l + 1);
    var promiseInput = false;

    for (var i = 0; i < l; ++i) {
      var arg = arguments[i];

      if (!promiseInput) {
        // TODO: clean this up
        promiseInput = needsPromiseInput(arg);
        if (promiseInput === GET_THEN_ERROR$1) {
          var p = new Promise$1(noop);
          reject(p, GET_THEN_ERROR$1.value);
          return p;
        } else if (promiseInput && promiseInput !== true) {
          arg = wrapThenable(promiseInput, arg);
        }
      }
      args[i] = arg;
    }

    var promise = new Promise$1(noop);

    args[l] = function (err, val) {
      if (err) reject(promise, err);else if (options === undefined) resolve(promise, val);else if (options === true) resolve(promise
, arrayResult(arguments));else if (isArray(options)) resolve(promise, makeObject(arguments, options));else resolve(promise, val);
    };

    if (promiseInput) {
      return handlePromiseInput(promise, args, nodeFunc, self);
    } else {
      return handleValueInput(promise, args, nodeFunc, self);
    }
  };

  fn.__proto__ = nodeFunc;

  return fn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.filter"></a>[function <span class="apidocSignatureSpan">rsvp.</span>filter (promises, filterFn, label)](#apidoc.element.rsvp.filter)
- description and source-code
```javascript
function filter$1(promises, filterFn, label) {
  var promise = isArray(promises) ? resolveAll(promises, label) : resolveSingle(promises, label);
  return promise.then(function (values) {
    if (!isFunction(filterFn)) {
      throw new TypeError("You must pass a function as filter's second argument.");
    }

    var length = values.length;
    var filtered = new Array(length);

    for (var i = 0; i < length; i++) {
      filtered[i] = filterFn(values[i]);
    }

    return resolveAll(filtered, label).then(function (filtered) {
      var results = new Array(length);
      var newLength = 0;

      for (var i = 0; i < length; i++) {
        if (filtered[i]) {
          results[newLength] = values[i];
          newLength++;
        }
      }

      results.length = newLength;

      return results;
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.hash"></a>[function <span class="apidocSignatureSpan">rsvp.</span>hash (object, label)](#apidoc.element.rsvp.hash)
- description and source-code
```javascript
function hash$1(object, label) {
  return new PromiseHash(Promise$1, object, label).promise;
}
```
- example usage
```shell
...

'''javascript
var promises = {
  posts: getJSON("/posts.json"),
  users: getJSON("/users.json")
};

RSVP.hash(promises).then(function(results) {
  console.log(results.users) // print the users.json results
  console.log(results.posts) // print the posts.json results
});
'''

## All settled and hash settled
...
```

#### <a name="apidoc.element.rsvp.hashSettled"></a>[function <span class="apidocSignatureSpan">rsvp.</span>hashSettled (object, label)](#apidoc.element.rsvp.hashSettled)
- description and source-code
```javascript
function hashSettled$1(object, label) {
  return new HashSettled(Promise$1, object, label).promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.map"></a>[function <span class="apidocSignatureSpan">rsvp.</span>map (promises, mapFn, label)](#apidoc.element.rsvp.map)
- description and source-code
```javascript
function map$1(promises, mapFn, label) {
  return Promise$1.all(promises, label).then(function (values) {
    if (!isFunction(mapFn)) {
      throw new TypeError("You must pass a function as map's second argument.");
    }

    var length = values.length;
    var results = new Array(length);

    for (var i = 0; i < length; i++) {
      results[i] = mapFn(values[i]);
    }

    return Promise$1.all(results, label);
  });
}
```
- example usage
```shell
...
Sometimes you might want to work with many promises at once. If you
pass an array of promises to the 'all()' method it will return a new
promise that will be fulfilled when all of the promises in the array
have been fulfilled; or rejected immediately if any promise in the array
is rejected.

'''javascript
var promises = [2, 3, 5, 7, 11, 13].map(function(id){
return getJSON("/post/" + id + ".json");
});

RSVP.all(promises).then(function(posts) {
// posts contains an array of results for the given promises
}).catch(function(reason){
// if any of the promises fails.
...
```

#### <a name="apidoc.element.rsvp.off"></a>[function <span class="apidocSignatureSpan">rsvp.</span>off ()](#apidoc.element.rsvp.off)
- description and source-code
```javascript
function off() {
  config['off'].apply(config, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.on"></a>[function <span class="apidocSignatureSpan">rsvp.</span>on ()](#apidoc.element.rsvp.on)
- description and source-code
```javascript
function on() {
  config['on'].apply(config, arguments);
}
```
- example usage
```shell
...
'RSVP' has a solution for this problem built in.

You can register functions to be called when an uncaught error occurs
within your promises. These callback functions can be anything, but a common
practice is to call 'console.assert' to dump the error to the console.

'''javascript
RSVP.on('error', function(reason) {
  console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'
...
```

#### <a name="apidoc.element.rsvp.race"></a>[function <span class="apidocSignatureSpan">rsvp.</span>race (array, label)](#apidoc.element.rsvp.race)
- description and source-code
```javascript
function race$3(array, label) {
  return Promise$1.race(array, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.reject"></a>[function <span class="apidocSignatureSpan">rsvp.</span>reject (reason, label)](#apidoc.element.rsvp.reject)
- description and source-code
```javascript
function reject$3(reason, label) {
  return Promise$1.reject(reason, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.resolve"></a>[function <span class="apidocSignatureSpan">rsvp.</span>resolve (value, label)](#apidoc.element.rsvp.resolve)
- description and source-code
```javascript
function resolve$3(value, label) {
  return Promise$1.resolve(value, label);
}
```
- example usage
```shell
...

'''javascript
RSVP.on('error', function(reason) {
console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'

'''javascript
RSVP.on('error', function(reason, label) {
if (label) {
  console.error(label);
}
...
```

#### <a name="apidoc.element.rsvp.rethrow"></a>[function <span class="apidocSignatureSpan">rsvp.</span>rethrow (reason)](#apidoc.element.rsvp.rethrow)
- description and source-code
```javascript
function rethrow$1(reason) {
  setTimeout(function () {
    throw reason;
  });
  throw reason;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rsvp.EventTarget"></a>[module rsvp.EventTarget](#apidoc.module.rsvp.EventTarget)

#### <a name="apidoc.element.rsvp.EventTarget.mixin"></a>[function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>mixin (object)](#apidoc.element.rsvp.EventTarget.mixin)
- description and source-code
```javascript
function mixin(object) {
  object['on'] = this['on'];
  object['off'] = this['off'];
  object['trigger'] = this['trigger'];
  object._promiseCallbacks = undefined;
  return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.EventTarget.off"></a>[function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>off (eventName, callback)](#apidoc.element.rsvp.EventTarget.off)
- description and source-code
```javascript
function off(eventName, callback) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      index = undefined;

  if (!callback) {
    allCallbacks[eventName] = [];
    return;
  }

  callbacks = allCallbacks[eventName];

  index = indexOf(callbacks, callback);

  if (index !== -1) {
    callbacks.splice(index, 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.EventTarget.on"></a>[function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>on (eventName, callback)](#apidoc.element.rsvp.EventTarget.on)
- description and source-code
```javascript
function on(eventName, callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('Callback must be a function');
  }

  var allCallbacks = callbacksFor(this),
      callbacks = undefined;

  callbacks = allCallbacks[eventName];

  if (!callbacks) {
    callbacks = allCallbacks[eventName] = [];
  }

  if (indexOf(callbacks, callback) === -1) {
    callbacks.push(callback);
  }
}
```
- example usage
```shell
...
'RSVP' has a solution for this problem built in.

You can register functions to be called when an uncaught error occurs
within your promises. These callback functions can be anything, but a common
practice is to call 'console.assert' to dump the error to the console.

'''javascript
RSVP.on('error', function(reason) {
  console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'
...
```

#### <a name="apidoc.element.rsvp.EventTarget.trigger"></a>[function <span class="apidocSignatureSpan">rsvp.EventTarget.</span>trigger (eventName, options, label)](#apidoc.element.rsvp.EventTarget.trigger)
- description and source-code
```javascript
function trigger(eventName, options, label) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      callback = undefined;

  if (callbacks = allCallbacks[eventName]) {
    // Don't cache the callbacks.length since it may grow
    for (var i = 0; i < callbacks.length; i++) {
      callback = callbacks[i];

      callback(options, label);
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rsvp.Promise"></a>[module rsvp.Promise](#apidoc.module.rsvp.Promise)

#### <a name="apidoc.element.rsvp.Promise.Promise"></a>[function <span class="apidocSignatureSpan">rsvp.</span>Promise (resolver, label)](#apidoc.element.rsvp.Promise.Promise)
- description and source-code
```javascript
function Promise$1(resolver, label) {
  this._id = counter++;
  this._label = label;
  this._state = undefined;
  this._result = undefined;
  this._subscribers = [];

  config.instrument && instrument$1('created', this);

  if (noop !== resolver) {
    typeof resolver !== 'function' && needsResolver();
    this instanceof Promise$1 ? initializePromise(this, resolver) : needsNew();
  }
}
```
- example usage
```shell
...
section below on TaskJS for more information.

### Basic Usage

'''javascript
var RSVP = require('rsvp');

var promise = new RSVP.Promise(function(resolve, reject) {
  // succeed
  resolve(value);
  // or reject
  reject(error);
});

promise.then(function(value) {
...
```

#### <a name="apidoc.element.rsvp.Promise.all"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.</span>all (entries, label)](#apidoc.element.rsvp.Promise.all)
- description and source-code
```javascript
function all$1(entries, label) {
  return new Enumerator(this, entries, true, /* abort on reject */label).promise;
}
```
- example usage
```shell
...
is rejected.

'''javascript
var promises = [2, 3, 5, 7, 11, 13].map(function(id){
  return getJSON("/post/" + id + ".json");
});

RSVP.all(promises).then(function(posts) {
  // posts contains an array of results for the given promises
}).catch(function(reason){
  // if any of the promises fails.
});
'''

## Hash of promises
...
```

#### <a name="apidoc.element.rsvp.Promise.cast"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.</span>cast (object, label)](#apidoc.element.rsvp.Promise.cast)
- description and source-code
```javascript
function resolve$1(object, label) {
<span class="apidocCodeCommentSpan">  /*jshint validthis:true */
</span>  var Constructor = this;

  if (object && typeof object === 'object' && object.constructor === Constructor) {
    return object;
  }

  var promise = new Constructor(noop, label);
  resolve(promise, object);
  return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.Promise.race"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.</span>race (entries, label)](#apidoc.element.rsvp.Promise.race)
- description and source-code
```javascript
function race$1(entries, label) {
<span class="apidocCodeCommentSpan">  /*jshint validthis:true */
</span>  var Constructor = this;

  var promise = new Constructor(noop, label);

  if (!isArray(entries)) {
    reject(promise, new TypeError('You must pass an array to race.'));
    return promise;
  }

  for (var i = 0; promise._state === PENDING && i < entries.length; i++) {
    subscribe(Constructor.resolve(entries[i]), undefined, function (value) {
      return resolve(promise, value);
    }, function (reason) {
      return reject(promise, reason);
    });
  }

  return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.Promise.reject"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.</span>reject (reason, label)](#apidoc.element.rsvp.Promise.reject)
- description and source-code
```javascript
function reject$1(reason, label) {
<span class="apidocCodeCommentSpan">  /*jshint validthis:true */
</span>  var Constructor = this;
  var promise = new Constructor(noop, label);
  reject(promise, reason);
  return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.Promise.resolve"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.</span>resolve (object, label)](#apidoc.element.rsvp.Promise.resolve)
- description and source-code
```javascript
function resolve$1(object, label) {
<span class="apidocCodeCommentSpan">  /*jshint validthis:true */
</span>  var Constructor = this;

  if (object && typeof object === 'object' && object.constructor === Constructor) {
    return object;
  }

  var promise = new Constructor(noop, label);
  resolve(promise, object);
  return promise;
}
```
- example usage
```shell
...

'''javascript
RSVP.on('error', function(reason) {
console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'

'''javascript
RSVP.on('error', function(reason, label) {
if (label) {
  console.error(label);
}
...
```



# <a name="apidoc.module.rsvp.Promise.prototype"></a>[module rsvp.Promise.prototype](#apidoc.module.rsvp.Promise.prototype)

#### <a name="apidoc.element.rsvp.Promise.prototype._onError"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>_onError (reason)](#apidoc.element.rsvp.Promise.prototype._onError)
- description and source-code
```javascript
function _onError(reason) {
  var promise = this;
  config.after(function () {
    if (promise._onError) {
      config['trigger']('error', reason, promise._label);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.Promise.prototype.catch"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>catch (onRejection, label)](#apidoc.element.rsvp.Promise.prototype.catch)
- description and source-code
```javascript
function _catch(onRejection, label) {
  return this.then(undefined, onRejection, label);
}
```
- example usage
```shell
...
  resolve(value);
  // or reject
  reject(error);
});

promise.then(function(value) {
  // success
}).catch(function(error) {
  // failure
});
'''

Once a promise has been resolved or rejected, it cannot be resolved or
rejected again.
...
```

#### <a name="apidoc.element.rsvp.Promise.prototype.constructor"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>constructor (resolver, label)](#apidoc.element.rsvp.Promise.prototype.constructor)
- description and source-code
```javascript
function Promise$1(resolver, label) {
  this._id = counter++;
  this._label = label;
  this._state = undefined;
  this._result = undefined;
  this._subscribers = [];

  config.instrument && instrument$1('created', this);

  if (noop !== resolver) {
    typeof resolver !== 'function' && needsResolver();
    this instanceof Promise$1 ? initializePromise(this, resolver) : needsNew();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.Promise.prototype.finally"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>finally (callback, label)](#apidoc.element.rsvp.Promise.prototype.finally)
- description and source-code
```javascript
function _finally(callback, label) {
  var promise = this;
  var constructor = promise.constructor;

  return promise.then(function (value) {
    return constructor.resolve(callback()).then(function () {
      return value;
    });
  }, function (reason) {
    return constructor.resolve(callback()).then(function () {
      throw reason;
    });
  }, label);
}
```
- example usage
```shell
...

'finally' will be invoked regardless of the promise's fate, just as native
try/catch/finally behaves.

'''js
findAuthor().catch(function(reason){
  return findOtherAuthor();
}).finally(function(){
  // author was either found, or not
});
'''


## Arrays of promises
...
```

#### <a name="apidoc.element.rsvp.Promise.prototype.then"></a>[function <span class="apidocSignatureSpan">rsvp.Promise.prototype.</span>then (onFulfillment, onRejection, label)](#apidoc.element.rsvp.Promise.prototype.then)
- description and source-code
```javascript
function then(onFulfillment, onRejection, label) {
  var _arguments = arguments;

  var parent = this;
  var state = parent._state;

  if (state === FULFILLED && !onFulfillment || state === REJECTED && !onRejection) {
    config.instrument && instrument$1('chained', parent, parent);
    return parent;
  }

  parent._onError = null;

  var child = new parent.constructor(noop, label);
  var result = parent._result;

  config.instrument && instrument$1('chained', parent, child);

  if (state) {
    (function () {
      var callback = _arguments[state - 1];
      config.async(function () {
        return invokeCallback(state, child, callback, result);
      });
    })();
  } else {
    subscribe(parent, child, onFulfillment, onRejection);
  }

  return child;
}
```
- example usage
```shell
...
var promise = new RSVP.Promise(function(resolve, reject) {
  // succeed
  resolve(value);
  // or reject
  reject(error);
});

promise.then(function(value) {
  // success
}).catch(function(error) {
  // failure
});
'''

Once a promise has been resolved or rejected, it cannot be resolved or
...
```



# <a name="apidoc.module.rsvp.default"></a>[module rsvp.default](#apidoc.module.rsvp.default)

#### <a name="apidoc.element.rsvp.default.Promise"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>Promise (resolver, label)](#apidoc.element.rsvp.default.Promise)
- description and source-code
```javascript
function Promise$1(resolver, label) {
  this._id = counter++;
  this._label = label;
  this._state = undefined;
  this._result = undefined;
  this._subscribers = [];

  config.instrument && instrument$1('created', this);

  if (noop !== resolver) {
    typeof resolver !== 'function' && needsResolver();
    this instanceof Promise$1 ? initializePromise(this, resolver) : needsNew();
  }
}
```
- example usage
```shell
...
section below on TaskJS for more information.

### Basic Usage

'''javascript
var RSVP = require('rsvp');

var promise = new RSVP.Promise(function(resolve, reject) {
  // succeed
  resolve(value);
  // or reject
  reject(error);
});

promise.then(function(value) {
...
```

#### <a name="apidoc.element.rsvp.default.all"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>all (array, label)](#apidoc.element.rsvp.default.all)
- description and source-code
```javascript
function all$3(array, label) {
  return Promise$1.all(array, label);
}
```
- example usage
```shell
...
is rejected.

'''javascript
var promises = [2, 3, 5, 7, 11, 13].map(function(id){
  return getJSON("/post/" + id + ".json");
});

RSVP.all(promises).then(function(posts) {
  // posts contains an array of results for the given promises
}).catch(function(reason){
  // if any of the promises fails.
});
'''

## Hash of promises
...
```

#### <a name="apidoc.element.rsvp.default.allSettled"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>allSettled (entries, label)](#apidoc.element.rsvp.default.allSettled)
- description and source-code
```javascript
function allSettled$1(entries, label) {
  return new AllSettled(Promise$1, entries, label).promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.asap"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>asap (callback, arg)](#apidoc.element.rsvp.default.asap)
- description and source-code
```javascript
function asap$1(callback, arg) {
  queue$1[len] = callback;
  queue$1[len + 1] = arg;
  len += 2;
  if (len === 2) {
    // If len is 1, that means that we need to schedule an async flush.
    // If additional callbacks are queued before the queue is flushed, they
    // will be processed by this flush that we are scheduling.
    scheduleFlush$1();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.async"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>async (callback, arg)](#apidoc.element.rsvp.default.async)
- description and source-code
```javascript
function async(callback, arg) {
  return config.async(callback, arg);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.cast"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>cast (value, label)](#apidoc.element.rsvp.default.cast)
- description and source-code
```javascript
function resolve$3(value, label) {
  return Promise$1.resolve(value, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.configure"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>configure (name, value)](#apidoc.element.rsvp.default.configure)
- description and source-code
```javascript
function configure(name, value) {
  if (name === 'onerror') {
    // handle for legacy users that expect the actual
    // error to be passed to their function added via
    // 'RSVP.configure('onerror', someFunctionHere);'
    config['on']('error', value);
    return;
  }

  if (arguments.length === 2) {
    config[name] = value;
  } else {
    return config[name];
  }
}
```
- example usage
```shell
...
});
'''


**NOTE:** promises do allow for errors to be handled asynchronously, so
this callback may result in false positives.

**NOTE:** Usage of 'RSVP.configure('onerror', yourCustomFunction);' is
deprecated in favor of using 'RSVP.on'.


## Finally

'finally' will be invoked regardless of the promise's fate, just as native
try/catch/finally behaves.
...
```

#### <a name="apidoc.element.rsvp.default.defer"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>defer (label)](#apidoc.element.rsvp.default.defer)
- description and source-code
```javascript
function defer$1(label) {
  var deferred = { resolve: undefined, reject: undefined };

  deferred.promise = new Promise$1(function (resolve, reject) {
    deferred.resolve = resolve;
    deferred.reject = reject;
  }, label);

  return deferred;
}
```
- example usage
```shell
...
  or
{ state: 'rejected', reason: reason }
'''

## Deferred

> The 'RSVP.Promise' constructor is generally a better, less error-prone choice
> than 'RSVP.defer()'. Promises are recommended unless the specific
> properties of deferred are needed.

Sometimes one needs to create a deferred object, without immediately specifying
how it will be resolved. These deferred objects are essentially a wrapper around
a promise, whilst providing late access to the 'resolve()' and 'reject()' methods.

A deferred object has this form: '{ promise, resolve(x), reject(r) }'.
...
```

#### <a name="apidoc.element.rsvp.default.denodeify"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>denodeify (nodeFunc, options)](#apidoc.element.rsvp.default.denodeify)
- description and source-code
```javascript
function denodeify$1(nodeFunc, options) {
  var fn = function fn() {
    var self = this;
    var l = arguments.length;
    var args = new Array(l + 1);
    var promiseInput = false;

    for (var i = 0; i < l; ++i) {
      var arg = arguments[i];

      if (!promiseInput) {
        // TODO: clean this up
        promiseInput = needsPromiseInput(arg);
        if (promiseInput === GET_THEN_ERROR$1) {
          var p = new Promise$1(noop);
          reject(p, GET_THEN_ERROR$1.value);
          return p;
        } else if (promiseInput && promiseInput !== true) {
          arg = wrapThenable(promiseInput, arg);
        }
      }
      args[i] = arg;
    }

    var promise = new Promise$1(noop);

    args[l] = function (err, val) {
      if (err) reject(promise, err);else if (options === undefined) resolve(promise, val);else if (options === true) resolve(promise
, arrayResult(arguments));else if (isArray(options)) resolve(promise, makeObject(arguments, options));else resolve(promise, val);
    };

    if (promiseInput) {
      return handlePromiseInput(promise, args, nodeFunc, self);
    } else {
      return handleValueInput(promise, args, nodeFunc, self);
    }
  };

  fn.__proto__ = nodeFunc;

  return fn;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.filter"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>filter (promises, filterFn, label)](#apidoc.element.rsvp.default.filter)
- description and source-code
```javascript
function filter$1(promises, filterFn, label) {
  var promise = isArray(promises) ? resolveAll(promises, label) : resolveSingle(promises, label);
  return promise.then(function (values) {
    if (!isFunction(filterFn)) {
      throw new TypeError("You must pass a function as filter's second argument.");
    }

    var length = values.length;
    var filtered = new Array(length);

    for (var i = 0; i < length; i++) {
      filtered[i] = filterFn(values[i]);
    }

    return resolveAll(filtered, label).then(function (filtered) {
      var results = new Array(length);
      var newLength = 0;

      for (var i = 0; i < length; i++) {
        if (filtered[i]) {
          results[newLength] = values[i];
          newLength++;
        }
      }

      results.length = newLength;

      return results;
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.hash"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>hash (object, label)](#apidoc.element.rsvp.default.hash)
- description and source-code
```javascript
function hash$1(object, label) {
  return new PromiseHash(Promise$1, object, label).promise;
}
```
- example usage
```shell
...

'''javascript
var promises = {
  posts: getJSON("/posts.json"),
  users: getJSON("/users.json")
};

RSVP.hash(promises).then(function(results) {
  console.log(results.users) // print the users.json results
  console.log(results.posts) // print the posts.json results
});
'''

## All settled and hash settled
...
```

#### <a name="apidoc.element.rsvp.default.hashSettled"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>hashSettled (object, label)](#apidoc.element.rsvp.default.hashSettled)
- description and source-code
```javascript
function hashSettled$1(object, label) {
  return new HashSettled(Promise$1, object, label).promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.map"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>map (promises, mapFn, label)](#apidoc.element.rsvp.default.map)
- description and source-code
```javascript
function map$1(promises, mapFn, label) {
  return Promise$1.all(promises, label).then(function (values) {
    if (!isFunction(mapFn)) {
      throw new TypeError("You must pass a function as map's second argument.");
    }

    var length = values.length;
    var results = new Array(length);

    for (var i = 0; i < length; i++) {
      results[i] = mapFn(values[i]);
    }

    return Promise$1.all(results, label);
  });
}
```
- example usage
```shell
...
Sometimes you might want to work with many promises at once. If you
pass an array of promises to the 'all()' method it will return a new
promise that will be fulfilled when all of the promises in the array
have been fulfilled; or rejected immediately if any promise in the array
is rejected.

'''javascript
var promises = [2, 3, 5, 7, 11, 13].map(function(id){
return getJSON("/post/" + id + ".json");
});

RSVP.all(promises).then(function(posts) {
// posts contains an array of results for the given promises
}).catch(function(reason){
// if any of the promises fails.
...
```

#### <a name="apidoc.element.rsvp.default.off"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>off ()](#apidoc.element.rsvp.default.off)
- description and source-code
```javascript
function off() {
  config['off'].apply(config, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.on"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>on ()](#apidoc.element.rsvp.default.on)
- description and source-code
```javascript
function on() {
  config['on'].apply(config, arguments);
}
```
- example usage
```shell
...
'RSVP' has a solution for this problem built in.

You can register functions to be called when an uncaught error occurs
within your promises. These callback functions can be anything, but a common
practice is to call 'console.assert' to dump the error to the console.

'''javascript
RSVP.on('error', function(reason) {
  console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'
...
```

#### <a name="apidoc.element.rsvp.default.race"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>race (array, label)](#apidoc.element.rsvp.default.race)
- description and source-code
```javascript
function race$3(array, label) {
  return Promise$1.race(array, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.reject"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>reject (reason, label)](#apidoc.element.rsvp.default.reject)
- description and source-code
```javascript
function reject$3(reason, label) {
  return Promise$1.reject(reason, label);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rsvp.default.resolve"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>resolve (value, label)](#apidoc.element.rsvp.default.resolve)
- description and source-code
```javascript
function resolve$3(value, label) {
  return Promise$1.resolve(value, label);
}
```
- example usage
```shell
...

'''javascript
RSVP.on('error', function(reason) {
console.assert(false, reason);
});
'''

'RSVP' allows Promises to be labeled: 'Promise.resolve(value, 'I AM A LABEL')'
If provided, this label is passed as the second argument to 'RSVP.on('error')'

'''javascript
RSVP.on('error', function(reason, label) {
if (label) {
  console.error(label);
}
...
```

#### <a name="apidoc.element.rsvp.default.rethrow"></a>[function <span class="apidocSignatureSpan">rsvp.default.</span>rethrow (reason)](#apidoc.element.rsvp.default.rethrow)
- description and source-code
```javascript
function rethrow$1(reason) {
  setTimeout(function () {
    throw reason;
  });
  throw reason;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
