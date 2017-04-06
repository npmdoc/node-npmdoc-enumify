# api documentation for  [enumify (v1.0.4)](https://github.com/rauschma/enumify#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-enumify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-enumify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-enumify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-enumify)
#### A JavaScript library for enums. To be used by transpiled ES6 (e.g. via Babel).

[![NPM](https://nodei.co/npm/enumify.png?downloads=true)](https://www.npmjs.com/package/enumify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-enumify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-enumify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-enumify/build/apidoc.html)

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
            "name": "rauschma",
            "email": "axel@rauschma.de"
        }
    ],
    "name": "enumify",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module enumify](#apidoc.module.enumify)
1.  [function <span class="apidocSignatureSpan">enumify.</span>Enum ()](#apidoc.element.enumify.Enum)
1.  [function <span class="apidocSignatureSpan">enumify.</span>copyProperties (target, source)](#apidoc.element.enumify.copyProperties)



# <a name="apidoc.module.enumify"></a>[module enumify](#apidoc.module.enumify)

#### <a name="apidoc.element.enumify.Enum"></a>[function <span class="apidocSignatureSpan">enumify.</span>Enum ()](#apidoc.element.enumify.Enum)
- description and source-code
```javascript
function Enum() {
    var instanceProperties = arguments.length <= 0 || arguments[0] === undefined ? undefined : arguments[0];

    _classCallCheck(this, Enum);

    // new.target would be better than this.constructor,
    // but isn’t supported by Babel
    if ({}.hasOwnProperty.call(this.constructor, INITIALIZED)) {
        throw new Error('Enum classes can’t be instantiated');
    }
    if ((typeof instanceProperties === 'undefined' ? 'undefined' : _typeof(instanceProperties)) === 'object' && instanceProperties
 !== null) {
        copyProperties(this, instanceProperties);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.enumify.copyProperties"></a>[function <span class="apidocSignatureSpan">enumify.</span>copyProperties (target, source)](#apidoc.element.enumify.copyProperties)
- description and source-code
```javascript
function copyProperties(target, source) {
    // Ideally, we’d use Reflect.ownKeys() here,
    // but I don’t want to depend on a polyfill
    var _iteratorNormalCompletion3 = true;
    var _didIteratorError3 = false;
    var _iteratorError3 = undefined;

    try {
        for (var _iterator3 = Object.getOwnPropertyNames(source)[Symbol.iterator](), _step3; !(_iteratorNormalCompletion3 = (_step3
 = _iterator3.next()).done); _iteratorNormalCompletion3 = true) {
            var key = _step3.value;

            var desc = Object.getOwnPropertyDescriptor(source, key);
            Object.defineProperty(target, key, desc);
        }
    } catch (err) {
        _didIteratorError3 = true;
        _iteratorError3 = err;
    } finally {
        try {
            if (!_iteratorNormalCompletion3 && _iterator3.return) {
                _iterator3.return();
            }
        } finally {
            if (_didIteratorError3) {
                throw _iteratorError3;
            }
        }
    }

    return target;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
