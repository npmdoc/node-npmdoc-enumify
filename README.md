# npmdoc-enumify

#### api documentation for  [enumify (v1.0.4)](https://github.com/rauschma/enumify#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-enumify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-enumify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-enumify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-enumify)

#### A JavaScript library for enums. To be used by transpiled ES6 (e.g. via Babel).

[![NPM](https://nodei.co/npm/enumify.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/enumify)

- [https://npmdoc.github.io/node-npmdoc-enumify/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-enumify/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-enumify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-enumify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-enumify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-enumify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "//": "babel-register is needed for mocha",
    "author": {
        "name": "Axel Rauschmayer"
    },
    "babel": {
        "presets": [
            "es2015"
        ]
    },
    "bugs": {
        "url": "https://github.com/rauschma/enumify/issues"
    },
    "dependencies": {},
    "description": "A JavaScript library for enums. To be used by transpiled ES6 (e.g. via Babel).",
    "devDependencies": {
        "babel-cli": "^6.2.4",
        "babel-preset-es2015": "^6.3.13",
        "babel-register": "^6.2.0",
        "mocha": "^2.2.5"
    },
    "directories": {},
    "dist": {
        "shasum": "2bb6263071dd4551e54c55755707fad24a40cd7e",
        "tarball": "https://registry.npmjs.org/enumify/-/enumify-1.0.4.tgz"
    },
    "gitHead": "d8a894d1fa58339ffb9f1d584d791843c991aa36",
    "homepage": "https://github.com/rauschma/enumify#readme",
    "license": "MIT",
    "main": "./lib/enumify.js",
    "maintainers": [
        {
            "name": "rauschma"
        }
    ],
    "name": "enumify",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/rauschma/enumify.git"
    },
    "scripts": {
        "build": "babel src --out-dir lib",
        "build-test-es5": "npm run build && babel test --out-dir test-es5 && sed -i '' 's/src\\/enumify/lib\\/enumify/' test-es5/enumify_test.js",
        "mocha": "mocha --ui qunit",
        "prepublish": "npm run build",
        "test": "mocha --ui qunit --compilers js:babel-register",
        "watch": "babel src --out-dir lib --watch"
    },
    "version": "1.0.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
