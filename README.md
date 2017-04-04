# api documentation for  [express-graphql (v0.6.4)](https://github.com/graphql/express-graphql#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-express-graphql.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-express-graphql) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-express-graphql.svg)](https://travis-ci.org/npmdoc/node-npmdoc-express-graphql)
#### Production ready GraphQL HTTP middleware.

[![NPM](https://nodei.co/npm/express-graphql.png?downloads=true)](https://www.npmjs.com/package/express-graphql)

[![apidoc](https://npmdoc.github.io/node-npmdoc-express-graphql/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-express-graphql_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-express-graphql/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-express-graphql/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-express-graphql/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "babel": {
        "presets": [
            "es2015"
        ],
        "plugins": [
            "transform-class-properties",
            "transform-flow-strip-types"
        ]
    },
    "bugs": {
        "url": "https://github.com/graphql/express-graphql/issues"
    },
    "contributors": [
        {
            "name": "Lee Byron",
            "email": "lee@leebyron.com",
            "url": "http://leebyron.com/"
        },
        {
            "name": "Daniel Schafer",
            "email": "dschafer@fb.com"
        },
        {
            "name": "Caleb Meredith",
            "email": "calebmeredith8@gmail.com"
        }
    ],
    "dependencies": {
        "accepts": "^1.3.0",
        "content-type": "^1.0.2",
        "http-errors": "^1.3.0",
        "raw-body": "^2.1.0"
    },
    "description": "Production ready GraphQL HTTP middleware.",
    "devDependencies": {
        "babel-cli": "6.22.2",
        "babel-eslint": "7.2.1",
        "babel-plugin-transform-async-to-generator": "6.22.0",
        "babel-plugin-transform-class-properties": "6.22.0",
        "babel-plugin-transform-flow-strip-types": "6.22.0",
        "babel-plugin-transform-runtime": "6.22.0",
        "babel-preset-es2015": "6.24.0",
        "babel-register": "6.24.0",
        "babel-runtime": "6.23.0",
        "body-parser": "1.17.1",
        "chai": "3.5.0",
        "connect": "3.6.0",
        "coveralls": "2.13.0",
        "eslint": "3.18.0",
        "eslint-plugin-babel": "4.1.1",
        "eslint-plugin-flowtype": "2.30.4",
        "express": "4.14.1",
        "express3": "*",
        "flow-bin": "0.42.0",
        "graphql": "0.9.2",
        "isparta": "4.0.0",
        "mocha": "3.2.0",
        "multer": "1.3.0",
        "sane": "1.6.0",
        "sinon": "2.1.0",
        "supertest": "3.0.0",
        "supertest-as-promised": "4.0.2"
    },
    "directories": {
        "lib": "./dist"
    },
    "dist": {
        "shasum": "e51c6281d075613feac72b3fb569440602d3dfe4",
        "tarball": "https://registry.npmjs.org/express-graphql/-/express-graphql-0.6.4.tgz"
    },
    "files": [
        "dist",
        "README.md",
        "LICENSE",
        "PATENTS"
    ],
    "gitHead": "fd4db51c4625e181c441a9480cb969ba766b2c8e",
    "homepage": "https://github.com/graphql/express-graphql#readme",
    "keywords": [
        "express",
        "connect",
        "http",
        "graphql",
        "middleware",
        "api"
    ],
    "license": "BSD-3-Clause",
    "main": "dist/index.js",
    "maintainers": [
        {
            "name": "fb",
            "email": "opensource+npm@fb.com"
        },
        {
            "name": "leebyron",
            "email": "lee@leebyron.com"
        },
        {
            "name": "wincent",
            "email": "greg@hurrell.net"
        }
    ],
    "name": "express-graphql",
    "optionalDependencies": {},
    "options": {
        "mocha": "--require resources/mocha-bootload src/**/__tests__/**/*.js"
    },
    "peerDependencies": {
        "graphql": "^0.5.0-b || ^0.6.0 || ^0.7.0 || ^0.8.0-b || ^0.9.0"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/graphql/express-graphql.git"
    },
    "scripts": {
        "build": "rm -rf dist/* && babel src --ignore __tests__ --out-dir dist",
        "check": "flow check",
        "cover": "babel-node node_modules/.bin/isparta cover --root src --report html node_modules/.bin/_mocha -- $npm_package_options_mocha",
        "cover:lcov": "babel-node node_modules/.bin/isparta cover --root src --report lcovonly node_modules/.bin/_mocha -- $npm_package_options_mocha",
        "lint": "eslint src",
        "prepublish": ". ./resources/prepublish.sh",
        "preversion": "npm test",
        "test": "npm run lint && npm run check && npm run testonly",
        "testonly": "mocha $npm_package_options_mocha",
        "watch": "node resources/watch.js"
    },
    "version": "0.6.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module express-graphql](#apidoc.module.express-graphql)
1.  [function <span class="apidocSignatureSpan">express-graphql.</span>getGraphQLParams (request)](#apidoc.element.express-graphql.getGraphQLParams)



# <a name="apidoc.module.express-graphql"></a>[module express-graphql](#apidoc.module.express-graphql)

#### <a name="apidoc.element.express-graphql.getGraphQLParams"></a>[function <span class="apidocSignatureSpan">express-graphql.</span>getGraphQLParams (request)](#apidoc.element.express-graphql.getGraphQLParams)
- description and source-code
```javascript
function getGraphQLParams(request) {
  return (0, _parseBody.parseBody)(request).then(function (bodyData) {
    var urlData = request.url && _url2.default.parse(request.url, true).query || {};
    return parseGraphQLParams(urlData, bodyData);
  });
}
```
- example usage
```shell
...
Given an HTTP Request, this returns a Promise for the parameters relevant to
running a GraphQL request. This function is used internally to handle the
incoming request, you may use it directly for building other similar services.

'''js
const graphqlHTTP = require('express-graphql');

graphqlHTTP.getGraphQLParams(request).then(params => {
  // do something...
})
'''


## Debugging Tips
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
