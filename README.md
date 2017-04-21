# npmtest-object.assign

#### basic test coverage for  object.assign (v4.0.4)  [![npm package](https://img.shields.io/npm/v/npmtest-object.assign.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-object.assign) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-object.assign.svg)](https://travis-ci.org/npmtest/node-npmtest-object.assign)

#### ES6 spec-compliant Object.assign shim. From https://github.com/es-shims/es6-shim

[![NPM](https://nodei.co/npm/object.assign.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/object.assign)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-object.assign/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-object.assign/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-object.assign/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-object.assign/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-object.assign/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-object.assign/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-object.assign/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-object.assign/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-object.assign/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-object.assign/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-object.assign/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-object.assign/build/test-report.html](https://npmtest.github.io/node-npmtest-object.assign/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-object.assign/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-object.assign/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-object.assign/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-object.assign/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-object.assign/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-object.assign/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-object.assign/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-object.assign/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "object.assign",
    "version": "4.0.4",
    "author": "Jordan Harband",
    "description": "ES6 spec-compliant Object.assign shim. From https://github.com/es-shims/es6-shim",
    "license": "MIT",
    "main": "index.js",
    "scripts": {
        "pretest": "npm run --silent lint && es-shim-api",
        "test": "npm run --silent tests-only",
        "posttest": "npm run --silent security",
        "tests-only": "npm run --silent test:implementation && npm run --silent test:shim && npm run --silent test:shams",
        "test:native": "node test/native.js",
        "test:shim": "node test/shimmed.js",
        "test:implementation": "node test/index.js",
        "test:shams": "npm run --silent test:shams:getownpropertysymbols && npm run --silent test:shams:corejs",
        "test:shams:corejs": "node test/shams/core-js.js",
        "test:shams:getownpropertysymbols": "node test/shams/get-own-property-symbols.js",
        "coverage": "covert test/*.js",
        "coverage:quiet": "covert test/*.js --quiet",
        "lint": "npm run --silent jscs && npm run --silent eslint",
        "eslint": "eslint *.js test/*.js",
        "jscs": "jscs *.js test/*.js",
        "build": "mkdir -p dist && browserify browserShim.js > dist/browser.js",
        "prepublish": "npm run --silent build",
        "security": "nsp check"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/ljharb/object.assign.git"
    },
    "keywords": [
        "Object.assign",
        "assign",
        "ES6",
        "extend",
        "$.extend",
        "jQuery",
        "_.extend",
        "Underscore",
        "es-shim API",
        "polyfill",
        "shim"
    ],
    "dependencies": {
        "function-bind": "^1.1.0",
        "object-keys": "^1.0.10",
        "define-properties": "^1.1.2"
    },
    "devDependencies": {
        "browserify": "^13.0.1",
        "is": "^3.1.0",
        "tape": "^4.6.0",
        "covert": "^1.1.0",
        "jscs": "^3.0.6",
        "nsp": "^2.5.0",
        "eslint": "^3.0.0",
        "@ljharb/eslint-config": "^6.0.0",
        "get-own-property-symbols": "^0.9.2",
        "core-js": "^2.4.0",
        "@es-shims/api": "^1.2.0",
        "for-each": "^0.3.2"
    },
    "testling": {
        "files": "test/index.js",
        "browsers": [
            "iexplore/6.0..latest",
            "firefox/3.0..6.0",
            "firefox/15.0..latest",
            "firefox/nightly",
            "chrome/4.0..10.0",
            "chrome/20.0..latest",
            "chrome/canary",
            "opera/10.0..latest",
            "opera/next",
            "safari/4.0..latest",
            "ipad/6.0..latest",
            "iphone/6.0..latest",
            "android-browser/4.2"
        ]
    },
    "engines": {
        "node": ">= 0.4"
    },
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
