# npmdoc-memdb-server

#### api documentation for  [memdb-server (v0.5.7)](https://github.com/rain1017/memdb)  [![npm package](https://img.shields.io/npm/v/npmdoc-memdb-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-memdb-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-memdb-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-memdb-server)

#### Distributed Transactional In-Memory Database

[![NPM](https://nodei.co/npm/memdb-server.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/memdb-server)

- [https://npmdoc.github.io/node-npmdoc-memdb-server/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-memdb-server/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-memdb-server/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-memdb-server/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-memdb-server/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-memdb-server/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "rain1017"
    },
    "bin": {
        "memdbd": "./bin/memdbd",
        "memdb": "./bin/memdb",
        "memdbindex": "./bin/memdbindex",
        "memdbcluster": "./bin/memdbcluster"
    },
    "bugs": {
        "url": "https://github.com/rain1017/memdb/issues"
    },
    "contributors": [
        {
            "name": "rain1017"
        }
    ],
    "dependencies": {
        "async-lock": "~0.3.5",
        "bluebird": "2.9.34",
        "fs-extra": "~0.23.1",
        "heapdump": "~0.3.5",
        "hiredis": "~0.4.0",
        "lodash": "~3.10.1",
        "memdb-logger": "~0.1.7",
        "minimist": "~1.1.1",
        "mkdirp": "~0.5.1",
        "mongodb": "2.0.39",
        "mongoose": "4.1.5",
        "node-uuid": "~1.4.3",
        "redis": "~0.12.1"
    },
    "description": "Distributed Transactional In-Memory Database",
    "devDependencies": {
        "blanket": "~1.1.6",
        "grunt-cli": "~0.1.13",
        "grunt-concurrent": "~0.4.1",
        "grunt-contrib-clean": "~0.6.0",
        "grunt-contrib-jshint": "~0.10.0",
        "grunt-contrib-watch": "~0.6.1",
        "grunt-env": "~0.4.2",
        "grunt-mocha-test": "~0.12.6",
        "grunt-nodemon": "~0.2.0",
        "load-grunt-tasks": "~2.0.0",
        "should": "~4.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9bdf3812186ba71e45ecace34ea5ae2fd49eceb4",
        "tarball": "https://registry.npmjs.org/memdb-server/-/memdb-server-0.5.7.tgz"
    },
    "engines": {
        "node": ">=0.12.5"
    },
    "gitHead": "8346a3f4865829b48d380d4c939f6fb7c244464e",
    "homepage": "https://github.com/rain1017/memdb",
    "keywords": [
        "mongodb",
        "transaction",
        "mongoose",
        "newsql",
        "distributed",
        "database",
        "memory"
    ],
    "maintainers": [
        {
            "name": "rain1017"
        }
    ],
    "name": "memdb-server",
    "optionalDependencies": {},
    "private": false,
    "repository": {
        "type": "git",
        "url": "git+https://github.com/rain1017/memdb.git"
    },
    "scripts": {
        "start": "grunt",
        "test": "grunt test"
    },
    "version": "0.5.7"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
