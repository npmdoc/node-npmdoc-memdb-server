# api documentation for  [memdb-server (v0.5.7)](https://github.com/rain1017/memdb)  [![npm package](https://img.shields.io/npm/v/npmdoc-memdb-server.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-memdb-server) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-memdb-server.svg)](https://travis-ci.org/npmdoc/node-npmdoc-memdb-server)
#### Distributed Transactional In-Memory Database

[![NPM](https://nodei.co/npm/memdb-server.png?downloads=true)](https://www.npmjs.com/package/memdb-server)

[![apidoc](https://npmdoc.github.io/node-npmdoc-memdb-server/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-memdb-server_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-memdb-server/build/apidoc.html)

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
            "name": "rain1017",
            "email": "rain1017@gmail.com"
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
            "name": "rain1017",
            "email": "rain1017@gmail.com"
        }
    ],
    "name": "memdb-server",
    "optionalDependencies": {},
    "private": false,
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module memdb-server](#apidoc.module.memdb-server)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>autoConnect (opts)](#apidoc.element.memdb-server.autoConnect)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>autoconnection (opts)](#apidoc.element.memdb-server.autoconnection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>backendlocker (opts)](#apidoc.element.memdb-server.backendlocker)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>client ()](#apidoc.element.memdb-server.client)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>collection (opts)](#apidoc.element.memdb-server.collection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>connect (opts)](#apidoc.element.memdb-server.connect)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>connectBackend (backend)](#apidoc.element.memdb-server.connectBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>connection (opts)](#apidoc.element.memdb-server.connection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>database (opts)](#apidoc.element.memdb-server.database)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>document (opts)](#apidoc.element.memdb-server.document)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>protocol (opts)](#apidoc.element.memdb-server.protocol)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>shard (opts)](#apidoc.element.memdb-server.shard)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>slave (opts)](#apidoc.element.memdb-server.slave)
1.  object <span class="apidocSignatureSpan">memdb-server.</span>autoconnection.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>backendlocker.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>client.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>clientpool
1.  object <span class="apidocSignatureSpan">memdb-server.</span>collection.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>config
1.  object <span class="apidocSignatureSpan">memdb-server.</span>connection.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>database.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>document.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>indexbuilder
1.  object <span class="apidocSignatureSpan">memdb-server.</span>modifier
1.  object <span class="apidocSignatureSpan">memdb-server.</span>protocol.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>server
1.  object <span class="apidocSignatureSpan">memdb-server.</span>shard.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>slave.prototype
1.  object <span class="apidocSignatureSpan">memdb-server.</span>utils

#### [module memdb-server.autoconnection](#apidoc.module.memdb-server.autoconnection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>autoconnection (opts)](#apidoc.element.memdb-server.autoconnection.autoconnection)

#### [module memdb-server.autoconnection.prototype](#apidoc.module.memdb-server.autoconnection.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_connection ()](#apidoc.element.memdb-server.autoconnection.prototype._connection)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_runTask (shardId)](#apidoc.element.memdb-server.autoconnection.prototype._runTask)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_runTransaction (func, conn, shardId)](#apidoc.element.memdb-server.autoconnection.prototype._runTransaction)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_shard (shardId)](#apidoc.element.memdb-server.autoconnection.prototype._shard)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_task (method, args, shardId)](#apidoc.element.memdb-server.autoconnection.prototype._task)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>close ()](#apidoc.element.memdb-server.autoconnection.prototype.close)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>collection (name)](#apidoc.element.memdb-server.autoconnection.prototype.collection)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>eval ()](#apidoc.element.memdb-server.autoconnection.prototype.eval)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>flushBackend ()](#apidoc.element.memdb-server.autoconnection.prototype.flushBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>info ()](#apidoc.element.memdb-server.autoconnection.prototype.info)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>openConnection (shardId)](#apidoc.element.memdb-server.autoconnection.prototype.openConnection)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>resetCounter ()](#apidoc.element.memdb-server.autoconnection.prototype.resetCounter)
1.  [function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>transaction (func, shardId)](#apidoc.element.memdb-server.autoconnection.prototype.transaction)

#### [module memdb-server.backendlocker](#apidoc.module.memdb-server.backendlocker)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>backendlocker (opts)](#apidoc.element.memdb-server.backendlocker.backendlocker)

#### [module memdb-server.backendlocker.prototype](#apidoc.module.memdb-server.backendlocker.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>_docKey (docId)](#apidoc.element.memdb-server.backendlocker.prototype._docKey)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>_heartbeatKey (shardId)](#apidoc.element.memdb-server.backendlocker.prototype._heartbeatKey)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>clearHeartbeat ()](#apidoc.element.memdb-server.backendlocker.prototype.clearHeartbeat)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>getActiveShards ()](#apidoc.element.memdb-server.backendlocker.prototype.getActiveShards)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>getHolderId (docId)](#apidoc.element.memdb-server.backendlocker.prototype.getHolderId)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>heartbeat ()](#apidoc.element.memdb-server.backendlocker.prototype.heartbeat)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>isAlive (shardId)](#apidoc.element.memdb-server.backendlocker.prototype.isAlive)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>isHeld (docId, shardId)](#apidoc.element.memdb-server.backendlocker.prototype.isHeld)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>start ()](#apidoc.element.memdb-server.backendlocker.prototype.start)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>stop ()](#apidoc.element.memdb-server.backendlocker.prototype.stop)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>tryLock (docId, shardId)](#apidoc.element.memdb-server.backendlocker.prototype.tryLock)
1.  [function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>unlock (docId)](#apidoc.element.memdb-server.backendlocker.prototype.unlock)

#### [module memdb-server.client](#apidoc.module.memdb-server.client)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>client ()](#apidoc.element.memdb-server.client.client)
1.  [function <span class="apidocSignatureSpan">memdb-server.client.</span>super_ ()](#apidoc.element.memdb-server.client.super_)

#### [module memdb-server.client.prototype](#apidoc.module.memdb-server.client.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>connect (host, port)](#apidoc.element.memdb-server.client.prototype.connect)
1.  [function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>disconnect ()](#apidoc.element.memdb-server.client.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>request (connId, method, args)](#apidoc.element.memdb-server.client.prototype.request)

#### [module memdb-server.clientpool](#apidoc.module.memdb-server.clientpool)
1.  [function <span class="apidocSignatureSpan">memdb-server.clientpool.</span>getClient (host, port)](#apidoc.element.memdb-server.clientpool.getClient)

#### [module memdb-server.collection](#apidoc.module.memdb-server.collection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>collection (opts)](#apidoc.element.memdb-server.collection.collection)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.</span>super_ ()](#apidoc.element.memdb-server.collection.super_)

#### [module memdb-server.collection.prototype](#apidoc.module.memdb-server.collection.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_checkId (id)](#apidoc.element.memdb-server.collection.prototype._checkId)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_checkName (name)](#apidoc.element.memdb-server.collection.prototype._checkName)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_findByIndex (indexKey, indexValue, fields, opts)](#apidoc.element.memdb-server.collection.prototype._findByIndex)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_finishIndexTasks (id)](#apidoc.element.memdb-server.collection.prototype._finishIndexTasks)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_indexCollectionName (indexKey)](#apidoc.element.memdb-server.collection.prototype._indexCollectionName)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_insertById (id, doc)](#apidoc.element.memdb-server.collection.prototype._insertById)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_key (id)](#apidoc.element.memdb-server.collection.prototype._key)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_removeById (id, opts)](#apidoc.element.memdb-server.collection.prototype._removeById)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_updateById (id, modifier, opts)](#apidoc.element.memdb-server.collection.prototype._updateById)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>close ()](#apidoc.element.memdb-server.collection.prototype.close)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>commitIndex ()](#apidoc.element.memdb-server.collection.prototype.commitIndex)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>commitOneIndex (indexKey, indexValue, changedIds, config)](#apidoc.element.memdb-server.collection.prototype.commitOneIndex)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>count (query, opts)](#apidoc.element.memdb-server.collection.prototype.count)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>find (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.find)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findById (id, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findById)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findByIdReadOnly (id, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findByIdReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findOne (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findOne)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findOneReadOnly (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findOneReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findReadOnly (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>insert (docs)](#apidoc.element.memdb-server.collection.prototype.insert)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>lock (id)](#apidoc.element.memdb-server.collection.prototype.lock)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>onUpdateIndex (id, indexKey, oldValue, newValue)](#apidoc.element.memdb-server.collection.prototype.onUpdateIndex)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>remove (query, opts)](#apidoc.element.memdb-server.collection.prototype.remove)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>rollbackIndex ()](#apidoc.element.memdb-server.collection.prototype.rollbackIndex)
1.  [function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>update (query, modifier, opts)](#apidoc.element.memdb-server.collection.prototype.update)

#### [module memdb-server.config](#apidoc.module.memdb-server.config)
1.  [function <span class="apidocSignatureSpan">memdb-server.config.</span>clusterConfig ()](#apidoc.element.memdb-server.config.clusterConfig)
1.  [function <span class="apidocSignatureSpan">memdb-server.config.</span>getShardIds ()](#apidoc.element.memdb-server.config.getShardIds)
1.  [function <span class="apidocSignatureSpan">memdb-server.config.</span>init (confPath, shardId)](#apidoc.element.memdb-server.config.init)
1.  [function <span class="apidocSignatureSpan">memdb-server.config.</span>shardConfig (shardId)](#apidoc.element.memdb-server.config.shardConfig)

#### [module memdb-server.connection](#apidoc.module.memdb-server.connection)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>connection (opts)](#apidoc.element.memdb-server.connection.connection)

#### [module memdb-server.connection.prototype](#apidoc.module.memdb-server.connection.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>close ()](#apidoc.element.memdb-server.connection.prototype.close)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>commit ()](#apidoc.element.memdb-server.connection.prototype.commit)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>count (name)](#apidoc.element.memdb-server.connection.prototype.count)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>find (name)](#apidoc.element.memdb-server.connection.prototype.find)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findById (name)](#apidoc.element.memdb-server.connection.prototype.findById)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findByIdReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findByIdReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findOne (name)](#apidoc.element.memdb-server.connection.prototype.findOne)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findOneReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findOneReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>flushBackend ()](#apidoc.element.memdb-server.connection.prototype.flushBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>getCollection (name, isIndex)](#apidoc.element.memdb-server.connection.prototype.getCollection)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>insert (name)](#apidoc.element.memdb-server.connection.prototype.insert)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>isDirty ()](#apidoc.element.memdb-server.connection.prototype.isDirty)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>lock (name)](#apidoc.element.memdb-server.connection.prototype.lock)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>remove (name)](#apidoc.element.memdb-server.connection.prototype.remove)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>rollback ()](#apidoc.element.memdb-server.connection.prototype.rollback)
1.  [function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>update (name)](#apidoc.element.memdb-server.connection.prototype.update)

#### [module memdb-server.database](#apidoc.module.memdb-server.database)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>database (opts)](#apidoc.element.memdb-server.database.database)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.</span>super_ ()](#apidoc.element.memdb-server.database.super_)

#### [module memdb-server.database.prototype](#apidoc.module.memdb-server.database.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>connect ()](#apidoc.element.memdb-server.database.prototype.connect)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>disconnect (connId)](#apidoc.element.memdb-server.database.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>execute (connId, method, args, opts)](#apidoc.element.memdb-server.database.prototype.execute)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>getConnection (id)](#apidoc.element.memdb-server.database.prototype.getConnection)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>start ()](#apidoc.element.memdb-server.database.prototype.start)
1.  [function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>stop (force)](#apidoc.element.memdb-server.database.prototype.stop)

#### [module memdb-server.document](#apidoc.module.memdb-server.document)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>document (opts)](#apidoc.element.memdb-server.document.document)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.</span>super_ ()](#apidoc.element.memdb-server.document.super_)

#### [module memdb-server.document.prototype](#apidoc.module.memdb-server.document.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getChanged ()](#apidoc.element.memdb-server.document.prototype._getChanged)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getCommited ()](#apidoc.element.memdb-server.document.prototype._getCommited)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getIndexValue (indexKey, opts)](#apidoc.element.memdb-server.document.prototype._getIndexValue)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_unlock ()](#apidoc.element.memdb-server.document.prototype._unlock)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_waitUnlock ()](#apidoc.element.memdb-server.document.prototype._waitUnlock)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>commit (connId)](#apidoc.element.memdb-server.document.prototype.commit)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>ensureLocked (connId)](#apidoc.element.memdb-server.document.prototype.ensureLocked)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>exists (connId)](#apidoc.element.memdb-server.document.prototype.exists)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>find (connId, fields)](#apidoc.element.memdb-server.document.prototype.find)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>insert (connId, doc)](#apidoc.element.memdb-server.document.prototype.insert)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>isFree ()](#apidoc.element.memdb-server.document.prototype.isFree)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>isLocked (connId)](#apidoc.element.memdb-server.document.prototype.isLocked)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>lock (connId)](#apidoc.element.memdb-server.document.prototype.lock)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>modify (connId, cmd, param)](#apidoc.element.memdb-server.document.prototype.modify)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>remove (connId)](#apidoc.element.memdb-server.document.prototype.remove)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>rollback (connId)](#apidoc.element.memdb-server.document.prototype.rollback)
1.  [function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>update (connId, modifier, opts)](#apidoc.element.memdb-server.document.prototype.update)

#### [module memdb-server.indexbuilder](#apidoc.module.memdb-server.indexbuilder)
1.  [function <span class="apidocSignatureSpan">memdb-server.indexbuilder.</span>drop (conf, collName, keys)](#apidoc.element.memdb-server.indexbuilder.drop)
1.  [function <span class="apidocSignatureSpan">memdb-server.indexbuilder.</span>rebuild (conf, collName, keys, opts)](#apidoc.element.memdb-server.indexbuilder.rebuild)

#### [module memdb-server.modifier](#apidoc.module.memdb-server.modifier)

#### [module memdb-server.protocol](#apidoc.module.memdb-server.protocol)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>protocol (opts)](#apidoc.element.memdb-server.protocol.protocol)
1.  [function <span class="apidocSignatureSpan">memdb-server.protocol.</span>super_ ()](#apidoc.element.memdb-server.protocol.super_)

#### [module memdb-server.protocol.prototype](#apidoc.module.memdb-server.protocol.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.protocol.prototype.</span>disconnect ()](#apidoc.element.memdb-server.protocol.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">memdb-server.protocol.prototype.</span>send (msg)](#apidoc.element.memdb-server.protocol.prototype.send)

#### [module memdb-server.server](#apidoc.module.memdb-server.server)
1.  [function <span class="apidocSignatureSpan">memdb-server.server.</span>start (opts)](#apidoc.element.memdb-server.server.start)

#### [module memdb-server.shard](#apidoc.module.memdb-server.shard)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>shard (opts)](#apidoc.element.memdb-server.shard.shard)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.</span>super_ ()](#apidoc.element.memdb-server.shard.super_)

#### [module memdb-server.shard.prototype](#apidoc.module.memdb-server.shard.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_addDoc (key, obj)](#apidoc.element.memdb-server.shard.prototype._addDoc)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_cancelIdleTimeout (key)](#apidoc.element.memdb-server.shard.prototype._cancelIdleTimeout)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_doc (key)](#apidoc.element.memdb-server.shard.prototype._doc)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_ensureState (state)](#apidoc.element.memdb-server.shard.prototype._ensureState)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_isLoaded (key)](#apidoc.element.memdb-server.shard.prototype._isLoaded)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_load (key)](#apidoc.element.memdb-server.shard.prototype._load)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_lockBackend (key)](#apidoc.element.memdb-server.shard.prototype._lockBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_persistent (key)](#apidoc.element.memdb-server.shard.prototype._persistent)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_resolveKey (key)](#apidoc.element.memdb-server.shard.prototype._resolveKey)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_setCommited (key)](#apidoc.element.memdb-server.shard.prototype._setCommited)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_startIdleTimeout (key)](#apidoc.element.memdb-server.shard.prototype._startIdleTimeout)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_unload (key)](#apidoc.element.memdb-server.shard.prototype._unload)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_unlockBackend (key)](#apidoc.element.memdb-server.shard.prototype._unlockBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>commit (connId, keys)](#apidoc.element.memdb-server.shard.prototype.commit)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>find (connId, key, fields)](#apidoc.element.memdb-server.shard.prototype.find)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>findReadOnly (connId, key, fields)](#apidoc.element.memdb-server.shard.prototype.findReadOnly)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>flushBackend (connId)](#apidoc.element.memdb-server.shard.prototype.flushBackend)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>gc ()](#apidoc.element.memdb-server.shard.prototype.gc)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>insert (connId, key, doc)](#apidoc.element.memdb-server.shard.prototype.insert)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>isLocked (connId, key)](#apidoc.element.memdb-server.shard.prototype.isLocked)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>lock (connId, key)](#apidoc.element.memdb-server.shard.prototype.lock)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>remove (connId, key)](#apidoc.element.memdb-server.shard.prototype.remove)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>restoreFromSlave ()](#apidoc.element.memdb-server.shard.prototype.restoreFromSlave)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>rollback (connId, keys)](#apidoc.element.memdb-server.shard.prototype.rollback)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>start ()](#apidoc.element.memdb-server.shard.prototype.start)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>stop ()](#apidoc.element.memdb-server.shard.prototype.stop)
1.  [function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>update (connId, key, doc, opts)](#apidoc.element.memdb-server.shard.prototype.update)

#### [module memdb-server.slave](#apidoc.module.memdb-server.slave)
1.  [function <span class="apidocSignatureSpan">memdb-server.</span>slave (opts)](#apidoc.element.memdb-server.slave.slave)

#### [module memdb-server.slave.prototype](#apidoc.module.memdb-server.slave.prototype)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>_extractKey (existKey)](#apidoc.element.memdb-server.slave.prototype._extractKey)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>_redisKey (key)](#apidoc.element.memdb-server.slave.prototype._redisKey)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>clear ()](#apidoc.element.memdb-server.slave.prototype.clear)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>del (key)](#apidoc.element.memdb-server.slave.prototype.del)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>getAllKeys ()](#apidoc.element.memdb-server.slave.prototype.getAllKeys)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>getMulti (keys)](#apidoc.element.memdb-server.slave.prototype.getMulti)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>set (key, doc)](#apidoc.element.memdb-server.slave.prototype.set)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>setMulti (docs)](#apidoc.element.memdb-server.slave.prototype.setMulti)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>start ()](#apidoc.element.memdb-server.slave.prototype.start)
1.  [function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>stop ()](#apidoc.element.memdb-server.slave.prototype.stop)

#### [module memdb-server.utils](#apidoc.module.memdb-server.utils)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>clone (obj)](#apidoc.element.memdb-server.utils.clone)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>deleteObjPath (obj, path)](#apidoc.element.memdb-server.utils.deleteObjPath)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>escapeField (str)](#apidoc.element.memdb-server.utils.escapeField)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>extendPromise (P)](#apidoc.element.memdb-server.utils.extendPromise)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>forceHashMap ()](#apidoc.element.memdb-server.utils.forceHashMap)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>getObjPath (obj, path)](#apidoc.element.memdb-server.utils.getObjPath)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>hrtimer (autoStart)](#apidoc.element.memdb-server.utils.hrtimer)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>isDict (obj)](#apidoc.element.memdb-server.utils.isDict)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>isEmpty (obj)](#apidoc.element.memdb-server.utils.isEmpty)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>mongoForEach (itor, func)](#apidoc.element.memdb-server.utils.mongoForEach)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>rateCounter (opts)](#apidoc.element.memdb-server.utils.rateCounter)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>remoteExec (ip, cmd, opts)](#apidoc.element.memdb-server.utils.remoteExec)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>setObjPath (obj, path, value)](#apidoc.element.memdb-server.utils.setObjPath)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>timeCounter ()](#apidoc.element.memdb-server.utils.timeCounter)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>unescapeField (str)](#apidoc.element.memdb-server.utils.unescapeField)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>uuid ()](#apidoc.element.memdb-server.utils.uuid)
1.  [function <span class="apidocSignatureSpan">memdb-server.utils.</span>waitUntil (fn, checkInterval)](#apidoc.element.memdb-server.utils.waitUntil)



# <a name="apidoc.module.memdb-server"></a>[module memdb-server](#apidoc.module.memdb-server)

#### <a name="apidoc.element.memdb-server.autoConnect"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>autoConnect (opts)](#apidoc.element.memdb-server.autoConnect)
- description and source-code
```javascript
autoConnect = function (opts){
    var conn = new AutoConnection(opts);
    return P.resolve(conn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.autoconnection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>autoconnection (opts)](#apidoc.element.memdb-server.autoconnection)
- description and source-code
```javascript
autoconnection = function (opts){
    opts = opts || {};

    this.db = opts.db;

    this.config = {
        maxConnection : opts.maxConnection || DEFAULT_MAX_CONNECTION,
        connectionIdleTimeout : opts.connectionIdleTimeout || DEFAULT_CONNECTION_IDLE_TIMEOUT,
        maxPendingTask : opts.maxPendingTask || DEFAULT_MAX_PENDING_TASK,
        reconnectInterval : opts.reconnectInterval || DEFAULT_RECONNECT_INTERVAL,

        // allow concurrent request inside one connection, internal use only
        concurrentInConnection : opts.concurrentInConnection || false,

        // {shardId : {host : '127.0.0.1', port : 31017}}
        shards : opts.shards || {},
    };

    if(this.config.concurrentInConnection){
        this.config.maxConnection = 1;
    }

    var shardIds = Object.keys(this.config.shards);
    if(shardIds.length === 0){
        throw new Error('please specify opts.shards');
    }

    var shards = {};
    shardIds.forEach(function(shardId){
        shards[shardId] = {
            connections : {}, // {connId : connection}
            freeConnections : {}, // {connId : true}
            connectionTimeouts : {}, // {connId : timeout}
            pendingTasks : [],
            reconnectInterval : null,
        };
    });
    this.shards = shards;

    this.openConnectionLock = new AsyncLock({Promise : P, maxPending : 10000});
    this.collections = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.backendlocker"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>backendlocker (opts)](#apidoc.element.memdb-server.backendlocker)
- description and source-code
```javascript
backendlocker = function (opts){
    opts = opts || {};

    this.shardId = opts.shardId;
    this.config = {
        host : opts.host || '127.0.0.1',
        port : opts.port || 6379,
        db : opts.db || 0,
        options : opts.options || {},
        prefix : opts.prefix || 'bl$',
        heartbeatPrefix  : opts.heartbeatPrefix || 'hb$',
        heartbeatTimeout : opts.heartbeatTimeout,
        heartbeatInterval : opts.heartbeatInterval,
    };

    this.client = null;
    this.heartbeatInterval = null;

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shardId);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.client"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>client ()](#apidoc.element.memdb-server.client)
- description and source-code
```javascript
client = function (){
    EventEmitter.call(this);

    this.protocol = null;
    this.seq = 1;
    this.requests = {}; //{seq : deferred}
    this.domains = {}; //{seq : domain} saved domains

    this.disconnectDeferred = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>collection (opts)](#apidoc.element.memdb-server.collection)
- description and source-code
```javascript
collection = function (opts){
    opts = opts || {};

    this.name = opts.name;
    this._checkName(this.name);

    this.shard = opts.shard;
    this.conn = opts.conn;
    this.config = opts.config || {};
    this.config.maxCollision = this.config.maxCollision || DEFAULT_MAX_COLLISION;

    // {indexKey : {indexValue : {id1 : 1, id2 : -1}}}
    this.changedIndexes = utils.forceHashMap();

    this.pendingIndexTasks = utils.forceHashMap(); //{id, [Promise]}

    this.updateIndexEvent = 'updateIndex$' + this.name + '$' + this.conn._id;
    this.shard.on(this.updateIndexEvent, this.onUpdateIndex.bind(this));

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);

    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.connect"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>connect (opts)](#apidoc.element.memdb-server.connect)
- description and source-code
```javascript
connect = function (opts){
    var conn = new Connection(opts);
    return P.try(function(){
        return conn.connect();
    })
    .thenReturn(conn);
}
```
- example usage
```shell
...

            P.try(function(){
if(msg.method === 'connect'){
    var clientVersion = msg.args[0];
    if(parseFloat(clientVersion) < parseFloat(consts.minClientVersion)){
        throw new Error('client version not supported, please upgrade');
    }
    var connId = db.connect().connId;
    connIds[connId] = true;
    return {
        connId : connId,
    };
}
if(!msg.connId){
    throw new Error('connId is required');
...
```

#### <a name="apidoc.element.memdb-server.connectBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>connectBackend (backend)](#apidoc.element.memdb-server.connectBackend)
- description and source-code
```javascript
connectBackend = function (backend){
    var mongodb = P.promisifyAll(require('mongodb'));
    return P.promisify(mongodb.MongoClient.connect)(backend.url, backend.options)
    .then(function(db){
        var getCollection = db.collection;
        db.collection = function(){
            var coll = getCollection.apply(db, arguments);
            var disabledMethods = ['createIndex', 'drop', 'dropIndex', 'dropIndexes', 'ensureIndex',
            'findAndModify', 'getCollection', 'getDB', 'insert', 'remove', 'renameCollection', 'save', 'update'];
            disabledMethods.forEach(function(method){
                coll[method] = function(){
                    throw new Error('write to backend is forbidden');
                };
            });
            return coll;
        };
        return db;
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.connection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>connection (opts)](#apidoc.element.memdb-server.connection)
- description and source-code
```javascript
connection = function (opts){
    opts = opts || {};

    this._id = opts._id;
    this.shard = opts.shard;

    this.config = opts.config || {};
    this.collections = {};

    this.lockedKeys = utils.forceHashMap();

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.database"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>database (opts)](#apidoc.element.memdb-server.database)
- description and source-code
```javascript
database = function (opts){
    // clone since we want to modify it
    opts = utils.clone(opts) || {};

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + opts.shardId);

    this.connections = utils.forceHashMap();
    this.connectionLock = new AsyncLock({Promise : P});

    this.dbWrappers = utils.forceHashMap(); //{connId : dbWrapper}

    this.opsCounter = utils.rateCounter();
    this.tpsCounter = utils.rateCounter();

    opts.slowQuery = opts.slowQuery || DEFAULT_SLOWQUERY;

    // Parse index config
    opts.collections = opts.collections || {};

    Object.keys(opts.collections).forEach(function(name){
        var collection = opts.collections[name];
        var indexes = {};
        (collection.indexes || []).forEach(function(index){
            if(!Array.isArray(index.keys)){
                index.keys = [index.keys];
            }
            var indexKey = JSON.stringify(index.keys.sort());
            if(indexes[indexKey]){
                throw new Error('Duplicate index keys - ' + indexKey);
            }

            delete index.keys;
            indexes[indexKey] = index;
        });
        collection.indexes = indexes;
    });

    this.logger.info('parsed opts: %j', opts);

    this.shard = new Shard(opts);

    this.config = opts;

    this.timeCounter = utils.timeCounter();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.document"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>document (opts)](#apidoc.element.memdb-server.document)
- description and source-code
```javascript
document = function (opts){ //jshint ignore:line
    opts = opts || {};

    if(!opts.hasOwnProperty('_id')){
        throw new Error('_id is not specified');
    }
    this._id = opts._id;

    var doc = opts.doc || null;
    if(typeof(doc) !== 'object'){
        throw new Error('doc must be object');
    }
    if(!!doc){
        doc._id = this._id;
    }

    this.commited = doc;
    this.changed = undefined; // undefined means no change, while null means removed
    this.connId = null; // Connection that hold the document lock

    this.locker = opts.locker;
    this.lockKey = opts.lockKey;
    if(!this.locker){
        this.locker = new AsyncLock({
                            Promise : P,
                            timeout : opts.lockTimeout || DEFAULT_LOCK_TIMEOUT
                            });
        this.lockKey = '';
    }

    this.releaseCallback = null;

    this.indexes = opts.indexes || {};

    this.savedIndexValues = {}; //{indexKey : indexValue}

    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.protocol"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>protocol (opts)](#apidoc.element.memdb-server.protocol)
- description and source-code
```javascript
protocol = function (opts){
    EventEmitter.call(this);

    opts = opts || {};

    this.socket = opts.socket;
    this.socket.setEncoding('utf8');

    this.maxMsgLength = opts.maxMsgLength || DEFAULT_MAX_MSG_LENGTH;

    this.remainLine = '';

    var self = this;
    this.socket.on('data', function(data){
        // message is json encoded and splited by '\n'
        var lines = data.split('\n');
        for(var i=0; i<lines.length - 1; i++){
            try{
                var msg = '';
                if(i === 0){
                    msg = JSON.parse(self.remainLine + lines[i]);
                    self.remainLine = '';
                }
                else{
                    msg = JSON.parse(lines[i]);
                }
                self.emit('msg', msg);
            }
            catch(err){
                logger.error(err.stack);
            }
        }
        self.remainLine = lines[lines.length - 1];
    });

    this.socket.on('close', function(hadError){
        self.emit('close', hadError);
    });

    this.socket.on('connect', function(){
        self.emit('connect');
    });

    this.socket.on('error', function(err){
        self.emit('error', err);
    });

    this.socket.on('timeout', function(){
        self.emit('timeout');
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.shard"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>shard (opts)](#apidoc.element.memdb-server.shard)
- description and source-code
```javascript
shard = function (opts){
    EventEmitter.call(this);

    opts = opts || {};

    this._id = opts.shardId;
    if(!this._id){
        throw new Error('shardId is empty');
    }
    this._id = this._id.toString();
    if(this._id.indexOf('$') !== -1){
        throw new Error('shardId can not contain "$"');
    }

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this._id);

    this.config = {
        locking : opts.locking || {},
        backend : opts.backend || {},
        slave : opts.slave || {},

        shards : opts.shards || {},

        idleTimeout : opts.hasOwnProperty('idleTimeout') ? opts.idleTimeout : DEFAULT_IDLE_TIMEOUT,
        persistentDelay : opts.hasOwnProperty('persistentDelay') ?  opts.persistentDelay : DEFAULT_PERSISTENT_DELAY,

        heartbeatInterval : opts.heartbeatInterval || DEFAULT_HEARTBEAT_INTERVAL,
        heartbeatTimeout : opts.heartbeatTimeout || DEFAULT_HEARTBEAT_TIMEOUT,
        backendLockTimeout : opts.backendLockTimeout || DEFAULT_BACKEND_LOCK_TIMEOUT,
        backendLockRetryInterval : opts.backendLockRetryInterval || DEFAULT_BACKEND_LOCK_RETRY_INTERVAL,
        reloadDelay : opts.reloadDelay || DEFAULT_RELOAD_DELAY,
        lockTimeout : opts.lockTimeout || DEFAULT_LOCK_TIMEOUT,

        memoryLimit : opts.memoryLimit || DEFAULT_MEMORY_LIMIT,
        gcCount : opts.gcCount || DEFAULT_GC_COUNT,
        gcInterval : opts.gcInterval || DEFAULT_GC_INTERVAL,

        disableSlave : opts.disableSlave || false,

        collections : opts.collections || {},
    };

    // global locking
    var lockerConf = this.config.locking;
    lockerConf.shardId = this._id;
    lockerConf.heartbeatTimeout = this.config.heartbeatTimeout;
    lockerConf.heartbeatInterval = this.config.heartbeatInterval;
    this.backendLocker = new BackendLocker(lockerConf);

    // backend storage
    var backendConf = this.config.backend;
    backendConf.shardId = this._id;
    this.backend = backends.create(backendConf);

    // slave redis
    var slaveConf = this.config.slave;
    slaveConf.shardId = this._id;
    this.slave = new Slave(slaveConf);

    // memdb client to communicate with other shards
    this.autoconn = new AutoConnection({
        shards : this.config.shards,
        concurrentInConnection : true,
    });

    // Document storage {key : doc}
    this.docs = utils.forceHashMap();

    // Newly commited docs (for incremental _save)
    this.commitedKeys = utils.forceHashMap(); // {key : version}

    // Idle timeout before unload
    this.idleTimeouts = utils.forceHashMap(); // {key : timeout}

    // Doc persistent timeout
    this.persistentTimeouts = utils.forceHashMap(); // {key : timeout}

    // GC interval
    this.gcInterval = null;

    // Lock async operations for each key
    this.keyLock = new AsyncLock({Promise : P});

    // Task locker
    this.taskLock = new AsyncLock({Promise : P});

    // Doc locker
    this.docLock = new AsyncLock({
        timeout : this.config.lockTimeout,
        Promise : P,
    });

    // Current concurrent commiting processes
    this.commitingCount = 0;

    // Current key unloading task
    this.unloadingKeys = utils.forceHashMap();

    this.loadCounter = utils.rateCounter();
    this.unloadCounter = utils.rateCounter();
    this.persistentCounter = utils.rateCounter();

    this.state = STATE.INITED;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.slave"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>slave (opts)](#apidoc.element.memdb-server.slave)
- description and source-code
```javascript
slave = function (opts){
    opts = opts || {};

    this.shardId = opts.shardId;

    this.config = {
        host : opts.host || '127.0.0.1',
        port : opts.port || 6379,
        db : opts.db || 0,
        options : opts.options || {},
    };

    this.client = null;
    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shardId);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.autoconnection"></a>[module memdb-server.autoconnection](#apidoc.module.memdb-server.autoconnection)

#### <a name="apidoc.element.memdb-server.autoconnection.autoconnection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>autoconnection (opts)](#apidoc.element.memdb-server.autoconnection.autoconnection)
- description and source-code
```javascript
autoconnection = function (opts){
    opts = opts || {};

    this.db = opts.db;

    this.config = {
        maxConnection : opts.maxConnection || DEFAULT_MAX_CONNECTION,
        connectionIdleTimeout : opts.connectionIdleTimeout || DEFAULT_CONNECTION_IDLE_TIMEOUT,
        maxPendingTask : opts.maxPendingTask || DEFAULT_MAX_PENDING_TASK,
        reconnectInterval : opts.reconnectInterval || DEFAULT_RECONNECT_INTERVAL,

        // allow concurrent request inside one connection, internal use only
        concurrentInConnection : opts.concurrentInConnection || false,

        // {shardId : {host : '127.0.0.1', port : 31017}}
        shards : opts.shards || {},
    };

    if(this.config.concurrentInConnection){
        this.config.maxConnection = 1;
    }

    var shardIds = Object.keys(this.config.shards);
    if(shardIds.length === 0){
        throw new Error('please specify opts.shards');
    }

    var shards = {};
    shardIds.forEach(function(shardId){
        shards[shardId] = {
            connections : {}, // {connId : connection}
            freeConnections : {}, // {connId : true}
            connectionTimeouts : {}, // {connId : timeout}
            pendingTasks : [],
            reconnectInterval : null,
        };
    });
    this.shards = shards;

    this.openConnectionLock = new AsyncLock({Promise : P, maxPending : 10000});
    this.collections = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.autoconnection.prototype"></a>[module memdb-server.autoconnection.prototype](#apidoc.module.memdb-server.autoconnection.prototype)

#### <a name="apidoc.element.memdb-server.autoconnection.prototype._connection"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_connection ()](#apidoc.element.memdb-server.autoconnection.prototype._connection)
- description and source-code
```javascript
_connection = function (){
    var info = process.domain && process.domain.__memdb__;
    if(!info){
        throw new Error('You are not in any transaction scope');
    }
    var shard = this._shard(info.shard);
    var conn = shard.connections[info.conn];
    if(!conn){
        throw new Error('connection ' + info.conn + ' not exist');
    }
    return conn;
}
```
- example usage
```shell
...
proto.collection = function(name){
var self = this;
if(!this.collections[name]){
    var collection = {};
    // Method must be called inside transaction
    consts.collMethods.forEach(function(method){
        collection[method] = function(){
            var conn = self._connection();
            var args = [name].concat([].slice.call(arguments));
            return conn[method].apply(conn, args);
        };
    });

    this.collections[name] = collection;
}
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype._runTask"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_runTask (shardId)](#apidoc.element.memdb-server.autoconnection.prototype._runTask)
- description and source-code
```javascript
_runTask = function (shardId){
    var self = this;
    var shard = this._shard(shardId);

    if(shard.pendingTasks.length === 0){
        return;
    }

    var connIds = Object.keys(shard.freeConnections);
    if(connIds.length === 0){
        return this.openConnection(shardId);
    }

    var connId = connIds[0];
    var conn = shard.connections[connId];
    if(!this.config.concurrentInConnection){
        delete shard.freeConnections[connId];
    }

    var task = shard.pendingTasks.shift();

    if(this.config.concurrentInConnection){
        // start run next before current task finish
        setImmediate(function(){
            self._runTask(shardId);
        });
    }

    return P.try(function(){
        if(task.method === '__t'){
            var func = task.args[0];
            return self._runTransaction(func, conn, shardId);
        }
        else{
            var method = conn[task.method];
            if(typeof(method) !== 'function'){
                throw new Error('invalid method - ' + task.method);
            }
            return method.apply(conn, task.args);
        }
    })
    .then(function(ret){
        task.deferred.resolve(ret);
    }, function(err){
        task.deferred.reject(err);
    })
    .finally(function(){
        if(shard.connections.hasOwnProperty(connId)){
            shard.freeConnections[connId] = true;
        }

        setImmediate(function(){
            self._runTask(shardId);
        });
    })
    .catch(function(e){
        logger.error(e.stack);
    });
}
```
- example usage
```shell
...
    conn.on('close', function(){
        logger.info('[shard:%s][conn:%s] connection closed', shardId, connId);
        delete shard.connections[connId];
        delete shard.freeConnections[connId];
    });

    setImmediate(function(){
        return self._runTask(shardId);
    });
}, function(e){
    if(!shard.reconnectInterval){
        shard.reconnectInterval = setInterval(function(){
            return self.openConnection(shardId);
        }, self.config.reconnectInterval);
    }
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype._runTransaction"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_runTransaction (func, conn, shardId)](#apidoc.element.memdb-server.autoconnection.prototype._runTransaction)
- description and source-code
```javascript
_runTransaction = function (func, conn, shardId){
    if(typeof(func) !== 'function'){
        throw new Error('Function is required');
    }

    var deferred = P.defer();

    var scope = domain.create();
    scope.__memdb__ = {shard: shardId, conn: conn._connId, trans : uuid.v4()};

    var self = this;
    scope.run(function(){
        logger.info('[shard:%s][conn:%s] transaction start', shardId, conn._connId);

        var startTick = Date.now();

        return P.try(function(){
            return func();
        })
        .then(function(ret){
            return conn.commit()
            .then(function(){
                logger.info('[shard:%s][conn:%s] transaction done (%sms)', shardId, conn._connId, Date.now() - startTick);
                delete scope.__memdb__;
                deferred.resolve(ret);
            });
        }, function(err){
            return conn.rollback()
            .then(function(){
                logger.error('[shard:%s][conn:%s] transaction error %s', shardId, conn._connId, err.stack);
                delete scope.__memdb__;
                deferred.reject(err);
            });
        })
        .catch(function(e){
            logger.error(e.stack);
            deferred.reject(e);
        });
    });

    return deferred.promise;
}
```
- example usage
```shell
...
        self._runTask(shardId);
    });
}

return P.try(function(){
    if(task.method === '__t'){
        var func = task.args[0];
        return self._runTransaction(func, conn, shardId);
    }
    else{
        var method = conn[task.method];
        if(typeof(method) !== 'function'){
            throw new Error('invalid method - ' + task.method);
        }
        return method.apply(conn, task.args);
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype._shard"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_shard (shardId)](#apidoc.element.memdb-server.autoconnection.prototype._shard)
- description and source-code
```javascript
_shard = function (shardId){
    var shard = this.shards[shardId];
    if(!shard){
        throw new Error('shard ' + shardId + ' not exist');
    }
    return shard;
}
```
- example usage
```shell
...
    });
};

proto.openConnection = function(shardId){
    var self = this;

    return this.openConnectionLock.acquire(shardId, function(){
var shard = self._shard(shardId);
if(Object.keys(shard.connections).length >= self.config.maxConnection){
    return;
}

var conn = new Connection({
                        host : self.config.shards[shardId].host,
                        port : self.config.shards[shardId].port,
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype._task"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>_task (method, args, shardId)](#apidoc.element.memdb-server.autoconnection.prototype._task)
- description and source-code
```javascript
_task = function (method, args, shardId){
    var deferred = P.defer();
    try{
        if(!shardId){
            var shardIds = Object.keys(this.shards);
            if(shardIds.length > 1){
                throw new Error('You must specify shardId');
            }
            shardId = shardIds[0];
        }

        var shard = this._shard(shardId);

        if(shard.pendingTasks.length >= this.config.maxPendingTask){
            throw new Error('Too much pending tasks');
        }

        shard.pendingTasks.push({
            method : method,
            args : args,
            deferred : deferred
        });

        var self = this;
        setImmediate(function(){
            return self._runTask(shardId);
        });
    }
    catch(err){
        deferred.reject(err);
    }
    finally{
        return deferred.promise;
    }
}
```
- example usage
```shell
...
    if(method === 'commit' || method === 'rollback'){
        return;
    }
    // Methods not bind to transaction
    proto[method] = function(){
        var shardId = arguments[0];
        var args = [].slice.call(arguments, 1);
        return this._task(method, args, shardId);
    };
});

proto.transaction = function(func, shardId){
    return this._task('__t', [func], shardId);
};
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.close"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>close ()](#apidoc.element.memdb-server.autoconnection.prototype.close)
- description and source-code
```javascript
close = function (){
    var self = this;
    // Close all connections to all shards
    return P.map(Object.keys(this.shards), function(shardId){
        var shard = self.shards[shardId];

        clearInterval(shard.reconnectInterval);
        shard.reconnectInterval = null;

        // reject all pending tasks
        shard.pendingTasks.forEach(function(task){
            task.deferred.reject(new Error('connection closed'));
        });
        shard.pendingTasks = [];

        // close all connections
        var connections = shard.connections;
        return P.map(Object.keys(connections), function(connId){
            var conn = connections[connId];
            if(conn){
                return conn.close();
            }
        });
    })
    .then(function(){
        logger.info('autoConnection closed');
    })
    .catch(function(err){
        logger.error(err.stack);
    });
}
```
- example usage
```shell
...
var proto = Connection.prototype;

proto.close = function(){
if(this.isDirty()){
    this.rollback();
}
for(var name in this.collections){
    this.collections[name].close();
}
};

consts.collMethods.forEach(function(method){
proto[method] = function(name){
    var collection = this.getCollection(name);
    // remove 'name' arg
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.collection"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>collection (name)](#apidoc.element.memdb-server.autoconnection.prototype.collection)
- description and source-code
```javascript
collection = function (name){
    var self = this;
    if(!this.collections[name]){
        var collection = {};
        // Method must be called inside transaction
        consts.collMethods.forEach(function(method){
            collection[method] = function(){
                var conn = self._connection();
                var args = [name].concat([].slice.call(arguments));
                return conn[method].apply(conn, args);
            };
        });

        this.collections[name] = collection;
    }
    return this.collections[name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.eval"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>eval ()](#apidoc.element.memdb-server.autoconnection.prototype.eval)
- description and source-code
```javascript
eval = function (){
    var shardId = arguments[0];
    var args = [].slice.call(arguments, 1);
    return this._task(method, args, shardId);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.flushBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>flushBackend ()](#apidoc.element.memdb-server.autoconnection.prototype.flushBackend)
- description and source-code
```javascript
flushBackend = function (){
    var shardId = arguments[0];
    var args = [].slice.call(arguments, 1);
    return this._task(method, args, shardId);
}
```
- example usage
```shell
...
    this.lockedKeys = {};

    this.logger.debug('[conn:%s] rolledback', this._id);
    return true;
};

proto.flushBackend = function(){
    return this.shard.flushBackend(this._id);
};

// for internal use
proto.$unload = function(key){
    return this.shard.$unload(key);
};
// for internal use
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.info"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>info ()](#apidoc.element.memdb-server.autoconnection.prototype.info)
- description and source-code
```javascript
info = function (){
    var shardId = arguments[0];
    var args = [].slice.call(arguments, 1);
    return this._task(method, args, shardId);
}
```
- example usage
```shell
...
.then(function(){
    if(this.shardId && this.config.heartbeatInterval > 0){
        this.heartbeatInterval = setInterval(this.heartbeat.bind(this), this.config.heartbeatInterval);
        return this.heartbeat();
    }
})
.then(function(){
    this.logger.info('backendLocker started %s:%s:%s', this.config.host, this.config.port, this.config.db);
});
};

proto.stop = function(){
return P.bind(this)
.then(function(){
    clearInterval(this.heartbeatInterval);
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.openConnection"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>openConnection (shardId)](#apidoc.element.memdb-server.autoconnection.prototype.openConnection)
- description and source-code
```javascript
openConnection = function (shardId){
    var self = this;

    return this.openConnectionLock.acquire(shardId, function(){
        var shard = self._shard(shardId);
        if(Object.keys(shard.connections).length >= self.config.maxConnection){
            return;
        }

        var conn = new Connection({
                                host : self.config.shards[shardId].host,
                                port : self.config.shards[shardId].port,
                                idleTimeout : self.config.connectionIdleTimeout
                            });

        return conn.connect()
        .then(function(connId){
            clearInterval(shard.reconnectInterval);
            shard.reconnectInterval = null;

            shard.connections[connId] = conn;

            logger.info('[shard:%s][conn:%s] open connection', shardId, connId);

            shard.freeConnections[connId] = true;

            conn.on('close', function(){
                logger.info('[shard:%s][conn:%s] connection closed', shardId, connId);
                delete shard.connections[connId];
                delete shard.freeConnections[connId];
            });

            setImmediate(function(){
                return self._runTask(shardId);
            });
        }, function(e){
            if(!shard.reconnectInterval){
                shard.reconnectInterval = setInterval(function(){
                    return self.openConnection(shardId);
                }, self.config.reconnectInterval);
            }
            logger.error(e.stack);

            if(Object.keys(shard.connections).length === 0){
                logger.error('No connection available for shard %s', shardId);

                // no available connection, reject all pending tasks
                shard.pendingTasks.forEach(function(task){
                    task.deferred.reject(e);
                });
                shard.pendingTasks = [];
            }
        });
    })
    .catch(function(e){
        logger.error(e.stack);
    });
}
```
- example usage
```shell
...

setImmediate(function(){
    return self._runTask(shardId);
});
        }, function(e){
if(!shard.reconnectInterval){
    shard.reconnectInterval = setInterval(function(){
        return self.openConnection(shardId);
    }, self.config.reconnectInterval);
}
logger.error(e.stack);

if(Object.keys(shard.connections).length === 0){
    logger.error('No connection available for shard %s', shardId);
...
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.resetCounter"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>resetCounter ()](#apidoc.element.memdb-server.autoconnection.prototype.resetCounter)
- description and source-code
```javascript
resetCounter = function (){
    var shardId = arguments[0];
    var args = [].slice.call(arguments, 1);
    return this._task(method, args, shardId);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.autoconnection.prototype.transaction"></a>[function <span class="apidocSignatureSpan">memdb-server.autoconnection.prototype.</span>transaction (func, shardId)](#apidoc.element.memdb-server.autoconnection.prototype.transaction)
- description and source-code
```javascript
transaction = function (func, shardId){
    return this._task('__t', [func], shardId);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.backendlocker"></a>[module memdb-server.backendlocker](#apidoc.module.memdb-server.backendlocker)

#### <a name="apidoc.element.memdb-server.backendlocker.backendlocker"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>backendlocker (opts)](#apidoc.element.memdb-server.backendlocker.backendlocker)
- description and source-code
```javascript
backendlocker = function (opts){
    opts = opts || {};

    this.shardId = opts.shardId;
    this.config = {
        host : opts.host || '127.0.0.1',
        port : opts.port || 6379,
        db : opts.db || 0,
        options : opts.options || {},
        prefix : opts.prefix || 'bl$',
        heartbeatPrefix  : opts.heartbeatPrefix || 'hb$',
        heartbeatTimeout : opts.heartbeatTimeout,
        heartbeatInterval : opts.heartbeatInterval,
    };

    this.client = null;
    this.heartbeatInterval = null;

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shardId);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.backendlocker.prototype"></a>[module memdb-server.backendlocker.prototype](#apidoc.module.memdb-server.backendlocker.prototype)

#### <a name="apidoc.element.memdb-server.backendlocker.prototype._docKey"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>_docKey (docId)](#apidoc.element.memdb-server.backendlocker.prototype._docKey)
- description and source-code
```javascript
_docKey = function (docId){
    return this.config.prefix + docId;
}
```
- example usage
```shell
...
});
};

proto.tryLock = function(docId, shardId){
this.logger.debug('tryLock %s', docId);

var self = this;
return this.client.setnxAsync(this._docKey(docId), shardId || this.shardId)
.then(function(ret){
    if(ret === 1){
        self.logger.debug('locked %s', docId);
        return true;
    }
    else{
        return false;
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype._heartbeatKey"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>_heartbeatKey (shardId)](#apidoc.element.memdb-server.backendlocker.prototype._heartbeatKey)
- description and source-code
```javascript
_heartbeatKey = function (shardId){
    return this.config.heartbeatPrefix + shardId;
}
```
- example usage
```shell
...
proto.heartbeat = function(){
    var timeout = Math.floor(this.config.heartbeatTimeout / 1000);
    if(timeout <= 0){
        timeout = 1;
    }

    var self = this;
    return this.client.setexAsync(this._heartbeatKey(this.shardId), timeout, 1)
    .then(function(){
        self.logger.debug('heartbeat');
    })
    .catch(function(err){
        self.logger.error(err.stack);
    });
};
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.clearHeartbeat"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>clearHeartbeat ()](#apidoc.element.memdb-server.backendlocker.prototype.clearHeartbeat)
- description and source-code
```javascript
clearHeartbeat = function (){
    return this.client.delAsync(this._heartbeatKey(this.shardId));
}
```
- example usage
```shell
...
});
};

proto.stop = function(){
return P.bind(this)
.then(function(){
    clearInterval(this.heartbeatInterval);
    return this.clearHeartbeat();
})
.then(function(){
    return this.client.quitAsync();
})
.then(function(){
    this.logger.info('backendLocker stoped');
});
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.getActiveShards"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>getActiveShards ()](#apidoc.element.memdb-server.backendlocker.prototype.getActiveShards)
- description and source-code
```javascript
getActiveShards = function (){
    var prefix = this.config.heartbeatPrefix;
    return this.client.keysAsync(prefix + '*')
    .then(function(keys){
        return keys.map(function(key){
            return key.slice(prefix.length);
        });
    });
}
```
- example usage
```shell
...
lockingConf.heartbeatInterval = 0;
var backendLocker = new BackendLocker(lockingConf);

return P.try(function(){
    return backendLocker.start();
})
.then(function(){
    return backendLocker.getActiveShards();
})
.then(function(shardIds){
    if(shardIds.length > 0){
        throw new Error('You should shutdown all shards first');
    }
})
.finally(function(){
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.getHolderId"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>getHolderId (docId)](#apidoc.element.memdb-server.backendlocker.prototype.getHolderId)
- description and source-code
```javascript
getHolderId = function (docId){
    return this.client.getAsync(this._docKey(docId));
}
```
- example usage
```shell
...

proto.getHolderId = function(docId){
    return this.client.getAsync(this._docKey(docId));
};

proto.isHeld = function(docId, shardId){
    var self = this;
    return this.getHolderId(docId)
    .then(function(ret){
        return ret === (shardId || self.shardId);
    });
};

// concurrency safe between shards
// not concurrency safe in same shard
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.heartbeat"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>heartbeat ()](#apidoc.element.memdb-server.backendlocker.prototype.heartbeat)
- description and source-code
```javascript
heartbeat = function (){
    var timeout = Math.floor(this.config.heartbeatTimeout / 1000);
    if(timeout <= 0){
        timeout = 1;
    }

    var self = this;
    return this.client.setexAsync(this._heartbeatKey(this.shardId), timeout, 1)
    .then(function(){
        self.logger.debug('heartbeat');
    })
    .catch(function(err){
        self.logger.error(err.stack);
    });
}
```
- example usage
```shell
...
                }
            });
        }
    })
    .then(function(){
        if(this.shardId && this.config.heartbeatInterval > 0){
            this.heartbeatInterval = setInterval(this.heartbeat.bind(this), this.config.heartbeatInterval);
            return this.heartbeat();
        }
    })
    .then(function(){
        this.logger.info('backendLocker started %s:%s:%s', this.config.host, this.config.port, this.config.db);
    });
};
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.isAlive"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>isAlive (shardId)](#apidoc.element.memdb-server.backendlocker.prototype.isAlive)
- description and source-code
```javascript
isAlive = function (shardId){
    return this.client.existsAsync(this._heartbeatKey(shardId || this.shardId))
    .then(function(ret){
        return !!ret;
    });
}
```
- example usage
```shell
...
    this.client.on('error', function(err){
        self.logger.error(err.stack);
    });
    return this.client.selectAsync(this.config.db);
})
.then(function(){
    if(this.shardId){
        return this.isAlive()
        .then(function(ret){
            if(ret){
                throw new Error('Current shard is running in some other process');
            }
        });
    }
})
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.isHeld"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>isHeld (docId, shardId)](#apidoc.element.memdb-server.backendlocker.prototype.isHeld)
- description and source-code
```javascript
isHeld = function (docId, shardId){
    var self = this;
    return this.getHolderId(docId)
    .then(function(ret){
        return ret === (shardId || self.shardId);
    });
}
```
- example usage
```shell
...

// concurrency safe between shards
// not concurrency safe in same shard
proto.unlock = function(docId){
    this.logger.debug('unlock %s', docId);

    var self = this;
    return this.isHeld(docId)
    .then(function(held){
        if(held){
            return self.client.delAsync(self._docKey(docId));
        }
    });
};
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.start"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>start ()](#apidoc.element.memdb-server.backendlocker.prototype.start)
- description and source-code
```javascript
start = function (){
    return P.bind(this)
    .then(function(){
        this.client = redis.createClient(this.config.port, this.config.host, {retry_max_delay : 10 * 1000, enable_offline_queue :
true});
        var self = this;
        this.client.on('error', function(err){
            self.logger.error(err.stack);
        });
        return this.client.selectAsync(this.config.db);
    })
    .then(function(){
        if(this.shardId){
            return this.isAlive()
            .then(function(ret){
                if(ret){
                    throw new Error('Current shard is running in some other process');
                }
            });
        }
    })
    .then(function(){
        if(this.shardId && this.config.heartbeatInterval > 0){
            this.heartbeatInterval = setInterval(this.heartbeat.bind(this), this.config.heartbeatInterval);
            return this.heartbeat();
        }
    })
    .then(function(){
        this.logger.info('backendLocker started %s:%s:%s', this.config.host, this.config.port, this.config.db);
    });
}
```
- example usage
```shell
...

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
var self = this;
return this.shard.start()
.then(function(){
    self.logger.info('database started');
});
};

proto.stop = function(force){
var self = this;
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.stop"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>stop ()](#apidoc.element.memdb-server.backendlocker.prototype.stop)
- description and source-code
```javascript
stop = function (){
    return P.bind(this)
    .then(function(){
        clearInterval(this.heartbeatInterval);
        return this.clearHeartbeat();
    })
    .then(function(){
        return this.client.quitAsync();
    })
    .then(function(){
        this.logger.info('backendLocker stoped');
    });
}
```
- example usage
```shell
...
self.logger.info('database started');
    });
};

proto.stop = function(force){
    var self = this;

    this.opsCounter.stop();
    this.tpsCounter.stop();

    return P.try(function(){
// Make sure no new request come anymore

// Wait for all operations finish
return utils.waitUntil(function(){
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.tryLock"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>tryLock (docId, shardId)](#apidoc.element.memdb-server.backendlocker.prototype.tryLock)
- description and source-code
```javascript
tryLock = function (docId, shardId){
    this.logger.debug('tryLock %s', docId);

    var self = this;
    return this.client.setnxAsync(this._docKey(docId), shardId || this.shardId)
    .then(function(ret){
        if(ret === 1){
            self.logger.debug('locked %s', docId);
            return true;
        }
        else{
            return false;
        }
    });
}
```
- example usage
```shell
...
    });
};

// internal method, not concurrency safe
proto._lockBackend = function(key){
    var self = this;
    return P.try(function(){
return self.backendLocker.tryLock(key);
    })
    .then(function(success){
if(success){
    return;
}

var startTick = Date.now();
...
```

#### <a name="apidoc.element.memdb-server.backendlocker.prototype.unlock"></a>[function <span class="apidocSignatureSpan">memdb-server.backendlocker.prototype.</span>unlock (docId)](#apidoc.element.memdb-server.backendlocker.prototype.unlock)
- description and source-code
```javascript
unlock = function (docId){
    this.logger.debug('unlock %s', docId);

    var self = this;
    return this.isHeld(docId)
    .then(function(held){
        if(held){
            return self.client.delAsync(self._docKey(docId));
        }
    });
}
```
- example usage
```shell
...
    };

    return tryLock(self.config.backendLockRetryInterval);
});
};

proto._unlockBackend = function(key){
return this.backendLocker.unlock(key);
};

// internal method, not concurrency safe
proto._persistent = function(key){
if(!this.commitedKeys.hasOwnProperty(key)){
    return; // no change
}
...
```



# <a name="apidoc.module.memdb-server.client"></a>[module memdb-server.client](#apidoc.module.memdb-server.client)

#### <a name="apidoc.element.memdb-server.client.client"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>client ()](#apidoc.element.memdb-server.client.client)
- description and source-code
```javascript
client = function (){
    EventEmitter.call(this);

    this.protocol = null;
    this.seq = 1;
    this.requests = {}; //{seq : deferred}
    this.domains = {}; //{seq : domain} saved domains

    this.disconnectDeferred = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.client.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.client.</span>super_ ()](#apidoc.element.memdb-server.client.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.client.prototype"></a>[module memdb-server.client.prototype](#apidoc.module.memdb-server.client.prototype)

#### <a name="apidoc.element.memdb-server.client.prototype.connect"></a>[function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>connect (host, port)](#apidoc.element.memdb-server.client.prototype.connect)
- description and source-code
```javascript
connect = function (host, port){
    if(!!this.protocol){
        throw new Error('connect already called');
    }

    var self = this;
    logger.debug('start connect to %s:%s', host, port);

    var connectDeferred = P.defer();

    var socket = net.createConnection(port, host);

    this.protocol = new Protocol({socket : socket});

    this.protocol.once('connect', function(){
        logger.info('connected to %s:%s', host, port);
        connectDeferred.resolve();
    });

    this.protocol.on('close', function(){
        logger.info('disconnected from %s:%s', host, port);

        // reject all remaining requests
        for(var seq in self.requests){
            process.domain = self.domains[seq];
            self.requests[seq].reject(new Error('connection closed'));
        }
        self.requests = {};
        self.domains = {};

        // Server will not disconnect if the client process exit immediately
        // So delay resolve promise
        if(self.disconnectDeferred){
            setTimeout(function(){
                self.disconnectDeferred.resolve();
            }, 1);
        }
        self.protocol = null;

        self.emit('close');
    });

    this.protocol.on('msg', function(msg){
        var request = self.requests[msg.seq];
        if(!request){
            return;
        }

        // restore saved domain
        process.domain = self.domains[msg.seq];

        if(!msg.err){
            logger.info('%s:%s => %j', host, port, msg);
            request.resolve(msg.data);
        }
        else{
            logger.error('%s:%s => %j', host, port, msg);
            request.reject(msg.err);
        }
        delete self.requests[msg.seq];
        delete self.domains[msg.seq];
    });

    this.protocol.on('error', function(err){
        if(!connectDeferred.isResolved()){
            connectDeferred.reject(err);
        }
        // Reject all pending requests
        Object.keys(self.requests).forEach(function(seq){
            // restore saved domain
            process.domain = self.domains[seq];
            self.requests[seq].reject(err);

            delete self.domains[seq];
            delete self.requests[seq];
        });
    });

    this.protocol.on('timeout', function(){
        self.disconnect();
    });

    return connectDeferred.promise;
}
```
- example usage
```shell
...

            P.try(function(){
if(msg.method === 'connect'){
    var clientVersion = msg.args[0];
    if(parseFloat(clientVersion) < parseFloat(consts.minClientVersion)){
        throw new Error('client version not supported, please upgrade');
    }
    var connId = db.connect().connId;
    connIds[connId] = true;
    return {
        connId : connId,
    };
}
if(!msg.connId){
    throw new Error('connId is required');
...
```

#### <a name="apidoc.element.memdb-server.client.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>disconnect ()](#apidoc.element.memdb-server.client.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (){
    if(!this.protocol){
        return;
    }

    this.disconnectDeferred = P.defer();
    this.protocol.disconnect();

    return this.disconnectDeferred.promise;
}
```
- example usage
```shell
...
            connId : connId,
        };
    }
    if(!msg.connId){
        throw new Error('connId is required');
    }
    if(msg.method === 'disconnect'){
        return db.disconnect(msg.connId)
        .then(function(){
            delete connIds[msg.connId];
        });
    }
    return db.execute(msg.connId, msg.method, msg.args);
})
.then(function(ret){
...
```

#### <a name="apidoc.element.memdb-server.client.prototype.request"></a>[function <span class="apidocSignatureSpan">memdb-server.client.prototype.</span>request (connId, method, args)](#apidoc.element.memdb-server.client.prototype.request)
- description and source-code
```javascript
request = function (connId, method, args){
    if(!this.protocol){
        throw new Error('not connected');
    }

    var seq = this.seq++;

    var deferred = P.defer();
    this.requests[seq] = deferred;

    var msg = {
        seq : seq,
        connId : connId,
        method : method,
        args : args,
    };

    this.protocol.send(msg);

    // save domain
    this.domains[seq] = process.domain;

    logger.info('%s:%s <= %j', this.protocol.socket.remoteAddress, this.protocol.socket.remotePort, msg);

    return deferred.promise;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.clientpool"></a>[module memdb-server.clientpool](#apidoc.module.memdb-server.clientpool)

#### <a name="apidoc.element.memdb-server.clientpool.getClient"></a>[function <span class="apidocSignatureSpan">memdb-server.clientpool.</span>getClient (host, port)](#apidoc.element.memdb-server.clientpool.getClient)
- description and source-code
```javascript
getClient = function (host, port){
    var key = host + ':' + port;

    return connectLock.acquire(key, function(){
        if(clients[key]){
            return clients[key];
        }

        var client = new Client();
        client.setMaxListeners(1025);

        return P.try(function(){
            return client.connect(host, port);
        })
        .then(function(){
            clients[key] = client;

            client.on('close', function(){
                delete clients[key];
            });
            return client;
        });
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.collection"></a>[module memdb-server.collection](#apidoc.module.memdb-server.collection)

#### <a name="apidoc.element.memdb-server.collection.collection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>collection (opts)](#apidoc.element.memdb-server.collection.collection)
- description and source-code
```javascript
collection = function (opts){
    opts = opts || {};

    this.name = opts.name;
    this._checkName(this.name);

    this.shard = opts.shard;
    this.conn = opts.conn;
    this.config = opts.config || {};
    this.config.maxCollision = this.config.maxCollision || DEFAULT_MAX_COLLISION;

    // {indexKey : {indexValue : {id1 : 1, id2 : -1}}}
    this.changedIndexes = utils.forceHashMap();

    this.pendingIndexTasks = utils.forceHashMap(); //{id, [Promise]}

    this.updateIndexEvent = 'updateIndex$' + this.name + '$' + this.conn._id;
    this.shard.on(this.updateIndexEvent, this.onUpdateIndex.bind(this));

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);

    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.</span>super_ ()](#apidoc.element.memdb-server.collection.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.collection.prototype"></a>[module memdb-server.collection.prototype](#apidoc.module.memdb-server.collection.prototype)

#### <a name="apidoc.element.memdb-server.collection.prototype._checkId"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_checkId (id)](#apidoc.element.memdb-server.collection.prototype._checkId)
- description and source-code
```javascript
_checkId = function (id){
    if(typeof(id) === 'string'){
        return id;
    }
    else if(typeof(id) === 'number'){
        return id.toString();
    }
    throw new Error('id must be number or string');
}
```
- example usage
```shell
...
if(!utils.isDict(doc)){
    throw new Error('doc must be a dictionary');
}

if(id === null || id === undefined){
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
})
.then(function(){
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._checkName"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_checkName (name)](#apidoc.element.memdb-server.collection.prototype._checkName)
- description and source-code
```javascript
_checkName = function (name){
    if(!name){
        throw new Error('Collection name can not empty');
    }
    if(typeof(name) !== 'string'){
        throw new Error('Collection name must be string');
    }
    if(name.indexOf('$') !== -1){
        throw new Error('Collection name can not contain "$"');
    }
    if(name.indexOf('system.') === 0){
        throw new Error('Collection name can not begin with "system."');
    }
}
```
- example usage
```shell
...

var DEFAULT_MAX_COLLISION = 10000;

var Collection = function(opts){
opts = opts || {};

this.name = opts.name;
this._checkName(this.name);

this.shard = opts.shard;
this.conn = opts.conn;
this.config = opts.config || {};
this.config.maxCollision = this.config.maxCollision || DEFAULT_MAX_COLLISION;

// {indexKey : {indexValue : {id1 : 1, id2 : -1}}}
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._findByIndex"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_findByIndex (indexKey, indexValue, fields, opts)](#apidoc.element.memdb-server.collection.prototype._findByIndex)
- description and source-code
```javascript
_findByIndex = function (indexKey, indexValue, fields, opts){
    opts = opts || {};
    var self = this;

    var indexCollection = this.conn.getCollection(this._indexCollectionName(indexKey), true);

    var nolock = opts.nolock;

    return P.try(function(){
        opts.nolock = true; // force not using lock
        return indexCollection.findById(indexValue, 'format ids', opts);
    })
    .then(function(doc){
        opts.nolock = nolock; // restore param

        var ids = utils.forceHashMap();

        if(doc){
            doc.ids.forEach(function(id){
                ids[id] = 1;
            });
        }

        var changedIds = (self.changedIndexes[indexKey] && self.changedIndexes[indexKey][indexValue]) || {};
        for(var id in changedIds){
            if(changedIds[id] === 1){
                ids[id] = 1;
            }
            else{
                delete ids[id];
            }
        }

        ids = Object.keys(ids);
        if(opts && opts.count){ // return count only
            return ids.length;
        }
        if(opts && opts.limit){
            ids = ids.slice(0, opts.limit);
        }

        var docs = [];
        ids.sort(); // keep id in order, avoid deadlock
        return P.each(ids, function(id){
            return self.findById(id, fields, opts)
            .then(function(doc){
                // WARN: This is possible that doc is null due to index collection is not locked
                if(!!doc){
                    docs.push(doc);
                }
            });
        })
        .thenReturn(docs);
    });
}
```
- example usage
```shell
...
    if(ignores.indexOf(value) !== -1){
        throw new Error('value ' + value + ' for key ' + key + ' is ignored in index');
    }
    return value;
});
var indexValue = JSON.stringify(values);

return this._findByIndex(indexKey, indexValue, fields, opts);
};

proto.findOne = function(query, fields, opts){
opts = opts || {};
opts.limit = 1;
return this.find(query, fields, opts)
.then(function(docs){
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._finishIndexTasks"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_finishIndexTasks (id)](#apidoc.element.memdb-server.collection.prototype._finishIndexTasks)
- description and source-code
```javascript
_finishIndexTasks = function (id){
    if(!this.pendingIndexTasks[id]){
        return;
    }
    // Save domain
    var d = process.domain;
    var self = this;
    return P.each(self.pendingIndexTasks[id], function(promise){
        return promise;
    })
    .finally(function(){
        delete self.pendingIndexTasks[id];
        // Restore domain
        process.domain = d;
    });
}
```
- example usage
```shell
...
return P.try(function(){
    return self.lock(id);
})
.then(function(){
    return self.shard.insert(self.conn._id, self._key(id), doc);
})
.then(function(){
    return self._finishIndexTasks(id);
})
.thenReturn(id);
};

proto.find = function(query, fields, opts){
if(typeof(query) === 'number' || typeof(query) === 'string'){
    return this.findById(query, fields, opts);
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._indexCollectionName"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_indexCollectionName (indexKey)](#apidoc.element.memdb-server.collection.prototype._indexCollectionName)
- description and source-code
```javascript
_indexCollectionName = function (indexKey){
    var keys = JSON.parse(indexKey).map(function(key){
        return utils.escapeField(key);
    });
    return 'index.' + utils.escapeField(this.name) + '.' + keys.join('.');
}
```
- example usage
```shell
...
});
};

proto._findByIndex = function(indexKey, indexValue, fields, opts){
opts = opts || {};
var self = this;

var indexCollection = this.conn.getCollection(this._indexCollectionName(indexKey), true);

var nolock = opts.nolock;

return P.try(function(){
    opts.nolock = true; // force not using lock
    return indexCollection.findById(indexValue, 'format ids', opts);
})
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._insertById"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_insertById (id, doc)](#apidoc.element.memdb-server.collection.prototype._insertById)
- description and source-code
```javascript
_insertById = function (id, doc){
    if(!utils.isDict(doc)){
        throw new Error('doc must be a dictionary');
    }

    if(id === null || id === undefined){
        id = utils.uuid();
    }
    id = this._checkId(id);
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
}
```
- example usage
```shell
...

proto.close = function(){
    this.shard.removeListener(this.updateIndexEvent, this.onUpdateIndex);
};

proto.insert = function(docs){
    if(!Array.isArray(docs)){
        return this._insertById(docs && docs._id, docs);
    }

    var self = this;
    return P.mapSeries(docs, function(doc){ //disable concurrent to avoid race condition
        return self._insertById(doc && doc._id, doc);
    });
};
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._key"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_key (id)](#apidoc.element.memdb-server.collection.prototype._key)
- description and source-code
```javascript
_key = function (id){
    return this.name + '$' + id;
}
```
- example usage
```shell
...
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
};
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._removeById"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_removeById (id, opts)](#apidoc.element.memdb-server.collection.prototype._removeById)
- description and source-code
```javascript
_removeById = function (id, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.remove(self.conn._id, self._key(id), opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
}
```
- example usage
```shell
...
    return self.find(query, '_id');
})
.then(function(ret){
    if(!ret || ret.length === 0){
        return 0;
    }
    if(!Array.isArray(ret)){
        return self._removeById(ret._id, opts)
        .thenReturn(1);
    }
    return P.each(ret, function(doc){
        return self._removeById(doc._id, opts);
    })
    .thenReturn(ret.length);
});
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype._updateById"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>_updateById (id, modifier, opts)](#apidoc.element.memdb-server.collection.prototype._updateById)
- description and source-code
```javascript
_updateById = function (id, modifier, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.update(self.conn._id, self._key(id), modifier, opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
}
```
- example usage
```shell
...
    }
    // upsert
    if(typeof(query) === 'string' || typeof(query) === 'number'){
        query = {_id : query};
    }
    return self.insert(query)
    .then(function(id){
        return self._updateById(id, modifier, opts);
    })
    .thenReturn(1);
}

if(!Array.isArray(ret)){
    return self._updateById(ret._id, modifier, opts)
    .thenReturn(1);
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.close"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>close ()](#apidoc.element.memdb-server.collection.prototype.close)
- description and source-code
```javascript
close = function (){
    this.shard.removeListener(this.updateIndexEvent, this.onUpdateIndex);
}
```
- example usage
```shell
...
var proto = Connection.prototype;

proto.close = function(){
if(this.isDirty()){
    this.rollback();
}
for(var name in this.collections){
    this.collections[name].close();
}
};

consts.collMethods.forEach(function(method){
proto[method] = function(name){
    var collection = this.getCollection(name);
    // remove 'name' arg
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.commitIndex"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>commitIndex ()](#apidoc.element.memdb-server.collection.prototype.commitIndex)
- description and source-code
```javascript
commitIndex = function (){
    var self = this;

    // must update in sorted order to avoid dead lock
    return P.each(Object.keys(this.changedIndexes).sort(), function(indexKey){
        var changedIndex = self.changedIndexes[indexKey];
        var config = self.config.indexes[indexKey];

        return P.each(Object.keys(changedIndex).sort(), function(indexValue){
            var changedIds = changedIndex[indexValue];

            return self.commitOneIndex(indexKey, indexValue, changedIds, config);
        });
    })
    .then(function(){
        self.changedIndexes = utils.forceHashMap();
    });
}
```
- example usage
```shell
...
};
});

proto.commit = function(){
var self = this;
return P.each(Object.keys(this.collections), function(name){
    var collection = self.collections[name];
    return collection.commitIndex();
})
.then(function(){
    return self.shard.commit(self._id, Object.keys(self.lockedKeys));
})
.then(function(){
    self.lockedKeys = {};
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.commitOneIndex"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>commitOneIndex (indexKey, indexValue, changedIds, config)](#apidoc.element.memdb-server.collection.prototype.commitOneIndex)
- description and source-code
```javascript
commitOneIndex = function (indexKey, indexValue, changedIds, config){

    var indexCollection = this.conn.getCollection(this._indexCollectionName(indexKey), true);

    var modifier = {$pushAll : {ids : []}, $pullAll : {ids : []}};

    var countDelta = 0;
    for(var id in changedIds){
        if(changedIds[id] === 1){
            modifier.$pushAll.ids.push(id);
            countDelta++;
        }
        else{
            modifier.$pullAll.ids.push(id);
            countDelta--;
        }
    }

    var self = this;
    return P.try(function(){
        return indexCollection.find(indexValue, 'ids');
    })
    .then(function(ret){
        var oldCount = ret ? ret.ids.length : 0;

        var newCount = oldCount + countDelta;
        if(config.unique && newCount > 1){
            throw new Error('duplicate value - ' + indexValue + ' for unique index - ' + indexKey);
        }
        if(newCount > config.maxCollision){
            throw new Error('too many documents have value - ' + indexValue + ' for index - ' + indexKey);
        }

        if(newCount > 0){
            return indexCollection.update(indexValue, modifier, {upsert : true});
        }
        else if(newCount === 0){
            return indexCollection.remove(indexValue);
        }
        else{
            throw new Error(util.format('index corrupted: %s %s, please rebuild index', self.name, indexKey));
        }
    });
}
```
- example usage
```shell
...

if(!config.unique){
    return;
}

return P.try(function(){
    if(oldValue !== null){
        return self.commitOneIndex(indexKey, oldValue, changedIndex[oldValue], config)
        .then(function(){
            delete changedIndex[oldValue];
        });
    }
})
.then(function(){
    if(newValue !== null){
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.count"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>count (query, opts)](#apidoc.element.memdb-server.collection.prototype.count)
- description and source-code
```javascript
count = function (query, opts){
    opts = opts || {};
    opts.count = true;
    var self = this;
    return P.try(function(){
        return self.find(query, null, opts);
    })
    .then(function(ret){
        if(typeof(ret) === 'number'){
            return ret;
        }
        else if(Array.isArray(ret)){
            return ret.length;
        }
        else if(!ret){
            return 0;
        }
        throw new Error('Unexpected find result - ' + ret);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection.prototype.find"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>find (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.find)
- description and source-code
```javascript
find = function (query, fields, opts){
    if(typeof(query) === 'number' || typeof(query) === 'string'){
        return this.findById(query, fields, opts);
    }

    if(!utils.isDict(query)){
        throw new Error('invalid query');
    }

    if(query.hasOwnProperty('_id')){
        return this.findById(query._id, fields, opts)
        .then(function(doc){
            if(!doc){
                return [];
            }
            return [doc];
        });
    }

    var keys = Object.keys(query).sort();
    if(keys.length === 0){
        throw new Error('You must specify query key');
    }

    var indexKey = JSON.stringify(keys);

    var indexConfig = this.config.indexes && this.config.indexes[indexKey];
    if(!indexConfig){
        throw new Error('No index configured for keys - ' + indexKey);
    }

    var valueIgnore = indexConfig.valueIgnore || {};
    var values = keys.map(function(key){
        var value = query[key];
        if(value === null || value === undefined){
            throw new Error('query value can not be null or undefined');
        }
        var ignores = valueIgnore[key] || [];
        if(ignores.indexOf(value) !== -1){
            throw new Error('value ' + value + ' for key ' + key + ' is ignored in index');
        }
        return value;
    });
    var indexValue = JSON.stringify(values);

    return this._findByIndex(indexKey, indexValue, fields, opts);
}
```
- example usage
```shell
...

return this._findByIndex(indexKey, indexValue, fields, opts);
};

proto.findOne = function(query, fields, opts){
opts = opts || {};
opts.limit = 1;
return this.find(query, fields, opts)
.then(function(docs){
    if(!Array.isArray(docs)){
        return docs;
    }
    if(docs.length === 0){
        return null;
    }
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.findById"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findById (id, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findById)
- description and source-code
```javascript
findById = function (id, fields, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        if(opts && opts.readonly){
            return self.shard.findReadOnly(self.conn._id, self._key(id), fields);
        }

        return P.try(function(){
            if(opts && opts.nolock){
                return;
            }
            return self.lock(id);
        })
        .then(function(){
            return self.shard.find(self.conn._id, self._key(id), fields, opts);
        });
    });
}
```
- example usage
```shell
...
    return self._finishIndexTasks(id);
})
.thenReturn(id);
};

proto.find = function(query, fields, opts){
if(typeof(query) === 'number' || typeof(query) === 'string'){
    return this.findById(query, fields, opts);
}

if(!utils.isDict(query)){
    throw new Error('invalid query');
}

if(query.hasOwnProperty('_id')){
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.findByIdReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findByIdReadOnly (id, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findByIdReadOnly)
- description and source-code
```javascript
findByIdReadOnly = function (id, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findById(id, fields, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection.prototype.findOne"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findOne (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findOne)
- description and source-code
```javascript
findOne = function (query, fields, opts){
    opts = opts || {};
    opts.limit = 1;
    return this.find(query, fields, opts)
    .then(function(docs){
        if(!Array.isArray(docs)){
            return docs;
        }
        if(docs.length === 0){
            return null;
        }
        return docs[0];
    });
}
```
- example usage
```shell
...
    opts.readonly = true;
    return this.find(query, fields, opts);
};

proto.findOneReadOnly = function(query, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findOne(query, fields, opts);
};

proto.findByIdReadOnly = function(id, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findById(id, fields, opts);
};
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.findOneReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findOneReadOnly (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findOneReadOnly)
- description and source-code
```javascript
findOneReadOnly = function (query, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findOne(query, fields, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection.prototype.findReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>findReadOnly (query, fields, opts)](#apidoc.element.memdb-server.collection.prototype.findReadOnly)
- description and source-code
```javascript
findReadOnly = function (query, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.find(query, fields, opts);
}
```
- example usage
```shell
...

proto.findById = function(id, fields, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
if(opts && opts.readonly){
    return self.shard.findReadOnly(self.conn._id, self._key(id), fields);
}

return P.try(function(){
    if(opts && opts.nolock){
        return;
    }
    return self.lock(id);
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.insert"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>insert (docs)](#apidoc.element.memdb-server.collection.prototype.insert)
- description and source-code
```javascript
insert = function (docs){
    if(!Array.isArray(docs)){
        return this._insertById(docs && docs._id, docs);
    }

    var self = this;
    return P.mapSeries(docs, function(doc){ //disable concurrent to avoid race condition
        return self._insertById(doc && doc._id, doc);
    });
}
```
- example usage
```shell
...
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
};
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.lock"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>lock (id)](#apidoc.element.memdb-server.collection.prototype.lock)
- description and source-code
```javascript
lock = function (id){
    id = this._checkId(id);
    if(this.shard.isLocked(this.conn._id, this._key(id))){
        return;
    }

    var self = this;
    return this.shard.lock(this.conn._id, this._key(id))
    .then(function(ret){
        self.emit('lock', id);
        return ret;
    });
}
```
- example usage
```shell
...
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
})
.then(function(){
    return self.shard.insert(self.conn._id, self._key(id), doc);
})
.then(function(){
    return self._finishIndexTasks(id);
})
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.onUpdateIndex"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>onUpdateIndex (id, indexKey, oldValue, newValue)](#apidoc.element.memdb-server.collection.prototype.onUpdateIndex)
- description and source-code
```javascript
onUpdateIndex = function (id, indexKey, oldValue, newValue){
    this.logger.debug('onUpdateIndex(%s, %s, %s, %s)', id, indexKey, oldValue, newValue);

    var self = this;
    var promise = P.try(function(){

        var config = self.config.indexes[indexKey];
        if(!config){
            throw new Error('index - ' + indexKey + ' not configured');
        }
        if(!self.changedIndexes[indexKey]){
            self.changedIndexes[indexKey] = utils.forceHashMap();
        }

        var changedIndex = self.changedIndexes[indexKey];

        if(oldValue !== null){
            if(!changedIndex[oldValue]){
                changedIndex[oldValue] = utils.forceHashMap();
            }
            if(changedIndex[oldValue][id] === 1){
                delete changedIndex[oldValue][id];
            }
            else{
                changedIndex[oldValue][id] = -1;
            }
        }
        if(newValue !== null){
            if(!changedIndex[newValue]){
                changedIndex[newValue] = utils.forceHashMap();
            }
            if(changedIndex[newValue][id] === -1){
                delete changedIndex[oldValue][id];
            }
            else{
                changedIndex[newValue][id] = 1;
            }
        }

        if(!config.unique){
            return;
        }

        return P.try(function(){
            if(oldValue !== null){
                return self.commitOneIndex(indexKey, oldValue, changedIndex[oldValue], config)
                .then(function(){
                    delete changedIndex[oldValue];
                });
            }
        })
        .then(function(){
            if(newValue !== null){
                return self.commitOneIndex(indexKey, newValue, changedIndex[newValue], config)
                .then(function(){
                    delete changedIndex[newValue];
                });
            }
        });
    });

    if(!this.pendingIndexTasks[id]){
        this.pendingIndexTasks[id] = [];
    }
    this.pendingIndexTasks[id].push(promise);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.collection.prototype.remove"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>remove (query, opts)](#apidoc.element.memdb-server.collection.prototype.remove)
- description and source-code
```javascript
remove = function (query, opts){
    var self = this;
    return P.try(function(){
        return self.find(query, '_id');
    })
    .then(function(ret){
        if(!ret || ret.length === 0){
            return 0;
        }
        if(!Array.isArray(ret)){
            return self._removeById(ret._id, opts)
            .thenReturn(1);
        }
        return P.each(ret, function(doc){
            return self._removeById(doc._id, opts);
        })
        .thenReturn(ret.length);
    });
}
```
- example usage
```shell
...
};

proto._removeById = function(id, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.remove(self.conn._id, self._key(id), opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.lock = function(id){
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.rollbackIndex"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>rollbackIndex ()](#apidoc.element.memdb-server.collection.prototype.rollbackIndex)
- description and source-code
```javascript
rollbackIndex = function (){
    this.changedIndexes = utils.forceHashMap();
}
```
- example usage
```shell
...
});
};

// sync method
proto.rollback = function(){
var self = this;
Object.keys(this.collections).forEach(function(name){
    self.collections[name].rollbackIndex();
});

this.shard.rollback(this._id, Object.keys(this.lockedKeys));
this.lockedKeys = {};

this.logger.debug('[conn:%s] rolledback', this._id);
return true;
...
```

#### <a name="apidoc.element.memdb-server.collection.prototype.update"></a>[function <span class="apidocSignatureSpan">memdb-server.collection.prototype.</span>update (query, modifier, opts)](#apidoc.element.memdb-server.collection.prototype.update)
- description and source-code
```javascript
update = function (query, modifier, opts){
    opts = opts || {};
    var self = this;

    return P.try(function(){
        return self.find(query, '_id');
    })
    .then(function(ret){
        if(!ret || ret.length === 0){
            if(!opts.upsert){
                return 0;
            }
            // upsert
            if(typeof(query) === 'string' || typeof(query) === 'number'){
                query = {_id : query};
            }
            return self.insert(query)
            .then(function(id){
                return self._updateById(id, modifier, opts);
            })
            .thenReturn(1);
        }

        if(!Array.isArray(ret)){
            return self._updateById(ret._id, modifier, opts)
            .thenReturn(1);
        }
        return P.each(ret, function(doc){
            return self._updateById(doc._id, modifier, opts);
        })
        .thenReturn(ret.length);
    });
}
```
- example usage
```shell
...
};

proto._updateById = function(id, modifier, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.update(self.conn._id, self._key(id), modifier, opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.remove = function(query, opts){
...
```



# <a name="apidoc.module.memdb-server.config"></a>[module memdb-server.config](#apidoc.module.memdb-server.config)

#### <a name="apidoc.element.memdb-server.config.clusterConfig"></a>[function <span class="apidocSignatureSpan">memdb-server.config.</span>clusterConfig ()](#apidoc.element.memdb-server.config.clusterConfig)
- description and source-code
```javascript
clusterConfig = function (){
    return _config;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.config.getShardIds"></a>[function <span class="apidocSignatureSpan">memdb-server.config.</span>getShardIds ()](#apidoc.element.memdb-server.config.getShardIds)
- description and source-code
```javascript
getShardIds = function (){
    if(!_config){
        throw new Error('please config.init first');
    }
    return Object.keys(_config.shards);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.config.init"></a>[function <span class="apidocSignatureSpan">memdb-server.config.</span>init (confPath, shardId)](#apidoc.element.memdb-server.config.init)
- description and source-code
```javascript
init = function (confPath, shardId){
    var searchPaths = [];
    var homePath = process.env.HOME || process.env.HOMEPATH || process.env.USERPROFILE;

    var localDataPath = path.join(homePath, '.memdb');
    mkdirp(localDataPath);

    searchPaths = confPath ? [confPath] : [path.join(homePath, '.memdb/memdb.conf.js'), '/etc/memdb.conf.js'];

    var conf = null;
    for(var i=0; i<searchPaths.length; i++){
        if(fs.existsSync(searchPaths[i])){
            confPath = path.resolve(searchPaths[i]);
            conf = require(confPath);
            exports.path = confPath;
            break;
        }
    }
    if(!conf){
        if(confPath){
            throw new Error('config file not found - ' + searchPaths);
        }

        // copy and load default config
        var confTemplatePath = path.join(__dirname, '../memdb.conf.js');
        var defaultConfPath = path.join(localDataPath, 'memdb.conf.js');
        fs.copySync(confTemplatePath, defaultConfPath);

        conf = require(defaultConfPath);
    }

    // Configure promise
    if(conf.promise && conf.promise.longStackTraces){
        P.longStackTraces();
    }

    // Configure log
    var logConf = conf.log || {};

    var logPath = logConf.path || path.join(localDataPath, 'log');
    mkdirp(logPath);

    console.log('log path: %s', logPath);
    memdbLogger.configure(path.join(__dirname, 'log4js.json'), {shardId : shardId || '$', base : logPath});

    var level = logConf.level || 'INFO';
    memdbLogger.setGlobalLogLevel(memdbLogger.levels[level]);

    // heapdump
    if(conf.heapdump){
        require('heapdump');
    }

    _config = conf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.config.shardConfig"></a>[function <span class="apidocSignatureSpan">memdb-server.config.</span>shardConfig (shardId)](#apidoc.element.memdb-server.config.shardConfig)
- description and source-code
```javascript
shardConfig = function (shardId){
    if(!_config){
        throw new Error('please config.init first');
    }

    var conf = utils.clone(_config);

    var shardConf = conf.shards && conf.shards[shardId];
    if(!shardConf){
        throw new Error('shard ' + shardId + ' not configured');
    }
    // Override shard specific config
    for(var key in shardConf){
        conf[key] = shardConf[key];
    }

    conf.shardId = shardId;
    return conf;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.connection"></a>[module memdb-server.connection](#apidoc.module.memdb-server.connection)

#### <a name="apidoc.element.memdb-server.connection.connection"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>connection (opts)](#apidoc.element.memdb-server.connection.connection)
- description and source-code
```javascript
connection = function (opts){
    opts = opts || {};

    this._id = opts._id;
    this.shard = opts.shard;

    this.config = opts.config || {};
    this.collections = {};

    this.lockedKeys = utils.forceHashMap();

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.connection.prototype"></a>[module memdb-server.connection.prototype](#apidoc.module.memdb-server.connection.prototype)

#### <a name="apidoc.element.memdb-server.connection.prototype.close"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>close ()](#apidoc.element.memdb-server.connection.prototype.close)
- description and source-code
```javascript
close = function (){
    if(this.isDirty()){
        this.rollback();
    }
    for(var name in this.collections){
        this.collections[name].close();
    }
}
```
- example usage
```shell
...
var proto = Connection.prototype;

proto.close = function(){
if(this.isDirty()){
    this.rollback();
}
for(var name in this.collections){
    this.collections[name].close();
}
};

consts.collMethods.forEach(function(method){
proto[method] = function(name){
    var collection = this.getCollection(name);
    // remove 'name' arg
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.commit"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>commit ()](#apidoc.element.memdb-server.connection.prototype.commit)
- description and source-code
```javascript
commit = function (){
    var self = this;
    return P.each(Object.keys(this.collections), function(name){
        var collection = self.collections[name];
        return collection.commitIndex();
    })
    .then(function(){
        return self.shard.commit(self._id, Object.keys(self.lockedKeys));
    })
    .then(function(){
        self.lockedKeys = {};

        self.logger.debug('[conn:%s] commited', self._id);
        return true;
    });
}
```
- example usage
```shell
...
proto.commit = function(){
var self = this;
return P.each(Object.keys(this.collections), function(name){
    var collection = self.collections[name];
    return collection.commitIndex();
})
.then(function(){
    return self.shard.commit(self._id, Object.keys(self.lockedKeys));
})
.then(function(){
    self.lockedKeys = {};

    self.logger.debug('[conn:%s] commited', self._id);
    return true;
});
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.count"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>count (name)](#apidoc.element.memdb-server.connection.prototype.count)
- description and source-code
```javascript
count = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.connection.prototype.find"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>find (name)](#apidoc.element.memdb-server.connection.prototype.find)
- description and source-code
```javascript
find = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...

return this._findByIndex(indexKey, indexValue, fields, opts);
};

proto.findOne = function(query, fields, opts){
opts = opts || {};
opts.limit = 1;
return this.find(query, fields, opts)
.then(function(docs){
    if(!Array.isArray(docs)){
        return docs;
    }
    if(docs.length === 0){
        return null;
    }
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.findById"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findById (name)](#apidoc.element.memdb-server.connection.prototype.findById)
- description and source-code
```javascript
findById = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
    return self._finishIndexTasks(id);
})
.thenReturn(id);
};

proto.find = function(query, fields, opts){
if(typeof(query) === 'number' || typeof(query) === 'string'){
    return this.findById(query, fields, opts);
}

if(!utils.isDict(query)){
    throw new Error('invalid query');
}

if(query.hasOwnProperty('_id')){
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.findByIdReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findByIdReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findByIdReadOnly)
- description and source-code
```javascript
findByIdReadOnly = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.connection.prototype.findOne"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findOne (name)](#apidoc.element.memdb-server.connection.prototype.findOne)
- description and source-code
```javascript
findOne = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
    opts.readonly = true;
    return this.find(query, fields, opts);
};

proto.findOneReadOnly = function(query, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findOne(query, fields, opts);
};

proto.findByIdReadOnly = function(id, fields, opts){
    opts = opts || {};
    opts.readonly = true;
    return this.findById(id, fields, opts);
};
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.findOneReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findOneReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findOneReadOnly)
- description and source-code
```javascript
findOneReadOnly = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.connection.prototype.findReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>findReadOnly (name)](#apidoc.element.memdb-server.connection.prototype.findReadOnly)
- description and source-code
```javascript
findReadOnly = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...

proto.findById = function(id, fields, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
if(opts && opts.readonly){
    return self.shard.findReadOnly(self.conn._id, self._key(id), fields);
}

return P.try(function(){
    if(opts && opts.nolock){
        return;
    }
    return self.lock(id);
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.flushBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>flushBackend ()](#apidoc.element.memdb-server.connection.prototype.flushBackend)
- description and source-code
```javascript
flushBackend = function (){
    return this.shard.flushBackend(this._id);
}
```
- example usage
```shell
...
    this.lockedKeys = {};

    this.logger.debug('[conn:%s] rolledback', this._id);
    return true;
};

proto.flushBackend = function(){
    return this.shard.flushBackend(this._id);
};

// for internal use
proto.$unload = function(key){
    return this.shard.$unload(key);
};
// for internal use
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.getCollection"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>getCollection (name, isIndex)](#apidoc.element.memdb-server.connection.prototype.getCollection)
- description and source-code
```javascript
getCollection = function (name, isIndex){
    if(!isIndex && name && name.indexOf('index.') === 0){
        throw new Error('Collection name can not begin with "index."');
    }

    var self = this;
    if(!this.collections[name]){
        var collection = new Collection({
            name : name,
            shard : this.shard,
            conn : this,
            config : this.config.collections[name] || {},
        });

        collection.on('lock', function(id){
            var key = name + '$' + id;
            self.lockedKeys[key] = true;
        });

        this.collections[name] = collection;
    }
    return this.collections[name];
}
```
- example usage
```shell
...
});
};

proto._findByIndex = function(indexKey, indexValue, fields, opts){
opts = opts || {};
var self = this;

var indexCollection = this.conn.getCollection(this._indexCollectionName(indexKey), true);

var nolock = opts.nolock;

return P.try(function(){
    opts.nolock = true; // force not using lock
    return indexCollection.findById(indexValue, 'format ids', opts);
})
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.insert"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>insert (name)](#apidoc.element.memdb-server.connection.prototype.insert)
- description and source-code
```javascript
insert = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
};
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.isDirty"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>isDirty ()](#apidoc.element.memdb-server.connection.prototype.isDirty)
- description and source-code
```javascript
isDirty = function (){
    return Object.keys(this.lockedKeys).length > 0;
}
```
- example usage
```shell
...

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
};

var proto = Connection.prototype;

proto.close = function(){
    if(this.isDirty()){
        this.rollback();
    }
    for(var name in this.collections){
        this.collections[name].close();
    }
};
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.lock"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>lock (name)](#apidoc.element.memdb-server.connection.prototype.lock)
- description and source-code
```javascript
lock = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
})
.then(function(){
    return self.shard.insert(self.conn._id, self._key(id), doc);
})
.then(function(){
    return self._finishIndexTasks(id);
})
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.remove"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>remove (name)](#apidoc.element.memdb-server.connection.prototype.remove)
- description and source-code
```javascript
remove = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
};

proto._removeById = function(id, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.remove(self.conn._id, self._key(id), opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.lock = function(id){
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.rollback"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>rollback ()](#apidoc.element.memdb-server.connection.prototype.rollback)
- description and source-code
```javascript
rollback = function (){
    var self = this;
    Object.keys(this.collections).forEach(function(name){
        self.collections[name].rollbackIndex();
    });

    this.shard.rollback(this._id, Object.keys(this.lockedKeys));
    this.lockedKeys = {};

    this.logger.debug('[conn:%s] rolledback', this._id);
    return true;
}
```
- example usage
```shell
...
    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
};

var proto = Connection.prototype;

proto.close = function(){
    if(this.isDirty()){
        this.rollback();
    }
    for(var name in this.collections){
        this.collections[name].close();
    }
};

consts.collMethods.forEach(function(method){
...
```

#### <a name="apidoc.element.memdb-server.connection.prototype.update"></a>[function <span class="apidocSignatureSpan">memdb-server.connection.prototype.</span>update (name)](#apidoc.element.memdb-server.connection.prototype.update)
- description and source-code
```javascript
update = function (name){
    var collection = this.getCollection(name);
    // remove 'name' arg
    var args = [].slice.call(arguments, 1);

    this.logger.debug('[conn:%s] %s.%s(%j)', this._id, name, method, args);
    return collection[method].apply(collection, args);
}
```
- example usage
```shell
...
};

proto._updateById = function(id, modifier, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.update(self.conn._id, self._key(id), modifier, opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.remove = function(query, opts){
...
```



# <a name="apidoc.module.memdb-server.database"></a>[module memdb-server.database](#apidoc.module.memdb-server.database)

#### <a name="apidoc.element.memdb-server.database.database"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>database (opts)](#apidoc.element.memdb-server.database.database)
- description and source-code
```javascript
database = function (opts){
    // clone since we want to modify it
    opts = utils.clone(opts) || {};

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + opts.shardId);

    this.connections = utils.forceHashMap();
    this.connectionLock = new AsyncLock({Promise : P});

    this.dbWrappers = utils.forceHashMap(); //{connId : dbWrapper}

    this.opsCounter = utils.rateCounter();
    this.tpsCounter = utils.rateCounter();

    opts.slowQuery = opts.slowQuery || DEFAULT_SLOWQUERY;

    // Parse index config
    opts.collections = opts.collections || {};

    Object.keys(opts.collections).forEach(function(name){
        var collection = opts.collections[name];
        var indexes = {};
        (collection.indexes || []).forEach(function(index){
            if(!Array.isArray(index.keys)){
                index.keys = [index.keys];
            }
            var indexKey = JSON.stringify(index.keys.sort());
            if(indexes[indexKey]){
                throw new Error('Duplicate index keys - ' + indexKey);
            }

            delete index.keys;
            indexes[indexKey] = index;
        });
        collection.indexes = indexes;
    });

    this.logger.info('parsed opts: %j', opts);

    this.shard = new Shard(opts);

    this.config = opts;

    this.timeCounter = utils.timeCounter();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.database.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.database.</span>super_ ()](#apidoc.element.memdb-server.database.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.database.prototype"></a>[module memdb-server.database.prototype](#apidoc.module.memdb-server.database.prototype)

#### <a name="apidoc.element.memdb-server.database.prototype.connect"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>connect ()](#apidoc.element.memdb-server.database.prototype.connect)
- description and source-code
```javascript
connect = function (){
    var connId = utils.uuid();
    var opts = {
        _id : connId,
        shard : this.shard,
        config : this.config,
        logger : this.logger
    };
    var conn = new Connection(opts);
    this.connections[connId] = conn;

    var self = this;
    var dbWrapper = {};
    consts.collMethods.concat(consts.connMethods).forEach(function(method){
        dbWrapper[method] = function(){
            return self.execute(connId, method, [].slice.call(arguments));
        };
    });
    this.dbWrappers[connId] = dbWrapper;

    this.logger.info('[conn:%s] connection created', connId);
    return {
        connId : connId,
    };
}
```
- example usage
```shell
...

            P.try(function(){
if(msg.method === 'connect'){
    var clientVersion = msg.args[0];
    if(parseFloat(clientVersion) < parseFloat(consts.minClientVersion)){
        throw new Error('client version not supported, please upgrade');
    }
    var connId = db.connect().connId;
    connIds[connId] = true;
    return {
        connId : connId,
    };
}
if(!msg.connId){
    throw new Error('connId is required');
...
```

#### <a name="apidoc.element.memdb-server.database.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>disconnect (connId)](#apidoc.element.memdb-server.database.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (connId){
    var self = this;
    return P.try(function(){
        var conn = self.getConnection(connId);
        return self.execute(connId, 'close', [], {ignoreConcurrent : true});
    })
    .then(function(){
        delete self.connections[connId];
        delete self.dbWrappers[connId];
        self.logger.info('[conn:%s] connection closed', connId);
    });
}
```
- example usage
```shell
...
            connId : connId,
        };
    }
    if(!msg.connId){
        throw new Error('connId is required');
    }
    if(msg.method === 'disconnect'){
        return db.disconnect(msg.connId)
        .then(function(){
            delete connIds[msg.connId];
        });
    }
    return db.execute(msg.connId, msg.method, msg.args);
})
.then(function(ret){
...
```

#### <a name="apidoc.element.memdb-server.database.prototype.execute"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>execute (connId, method, args, opts)](#apidoc.element.memdb-server.database.prototype.execute)
- description and source-code
```javascript
execute = function (connId, method, args, opts){
    opts = opts || {};
    var self = this;

    if(method[0] === '$'){ // Internal method (allow concurrent call)
        var conn = this.getConnection(connId);
        return conn[method].apply(conn, args);
    }

    if(method === 'info'){
        return {
            connId : connId,
            ver : consts.version,
            uptime : process.uptime(),
            mem : process.memoryUsage(),
            // rate for last 1, 5, 15 minutes
            ops : [this.opsCounter.rate(60), this.opsCounter.rate(300), this.opsCounter.rate(900)],
            tps : [this.tpsCounter.rate(60), this.tpsCounter.rate(300), this.tpsCounter.rate(900)],
            lps : [this.shard.loadCounter.rate(60), this.shard.loadCounter.rate(300), this.shard.loadCounter.rate(900)],
            ups : [this.shard.unloadCounter.rate(60), this.shard.unloadCounter.rate(300), this.shard.unloadCounter.rate(900)],
            pps : [this.shard.persistentCounter.rate(60), this.shard.persistentCounter.rate(300), this.shard.persistentCounter.rate
(900)],
            counter : this.timeCounter.getCounts(),
        };
    }
    else if(method === 'resetCounter'){
        this.opsCounter.reset();
        this.tpsCounter.reset();
        this.shard.loadCounter.reset();
        this.shard.unloadCounter.reset();
        this.shard.persistentCounter.reset();

        this.timeCounter.reset();
        return;
    }
    else if(method === 'eval'){
        var script = args[0] || '';
        var sandbox = args[1] || {};
        sandbox.require = require;
        sandbox.P = P;
        sandbox._ = _;
        sandbox.db = this.dbWrappers[connId];

        var context = vm.createContext(sandbox);

        return vm.runInContext(script, context);
    }

    // Query in the same connection must execute in series
    // This is usually a client bug here
    if(this.connectionLock.isBusy(connId) && !opts.ignoreConcurrent){
        var err = new Error(util.format('[conn:%s] concurrent query on same connection. %s(%j)', connId, method, args));
        this.logger.error(err);
        throw err;
    }

    // Ensure series execution in same connection
    return this.connectionLock.acquire(connId, function(cb){
        self.logger.debug('[conn:%s] start %s(%j)...', connId, method, args);
        if(method === 'commit' || method === 'rollback'){
            self.tpsCounter.inc();
        }
        else{
            self.opsCounter.inc();
        }

        var hrtimer = utils.hrtimer(true);
        var conn = null;

        return P.try(function(){
            conn = self.getConnection(connId);

            var func = conn[method];
            if(typeof(func) !== 'function'){
                throw new Error('unsupported command - ' + method);
            }
            return func.apply(conn, args);
        })
        .then(function(ret){
            var timespan = hrtimer.stop();
            var level = timespan < self.config.slowQuery ? 'info' : 'warn'; // warn slow query
            self.logger[level]('[conn:%s] %s(%j) => %j (%sms)', connId, method, args, ret, timespan);

            var category = method;
            if(consts.collMethods.indexOf(method) !== -1){
                category += ':' + args[0];
            }
            self.timeCounter.add(category, timespan);

            return ret;
        }, function(err){
            var timespan = hrtimer.stop();
            self.logger.error('[conn:%s] %s(%j) => %s (%sms)', connId, method, args, err.stack ? err.stack : err, timespan);

            if(conn){
                conn.rollback();
            }

            // Rethrow to client
            throw err;
        })
        .nodeify(cb);
    });
}
```
- example usage
```shell
...
var conn = new Connection(opts);
this.connections[connId] = conn;

var self = this;
var dbWrapper = {};
consts.collMethods.concat(consts.connMethods).forEach(function(method){
    dbWrapper[method] = function(){
        return self.execute(connId, method, [].slice.call(arguments));
    };
});
this.dbWrappers[connId] = dbWrapper;

this.logger.info('[conn:%s] connection created', connId);
return {
    connId : connId,
...
```

#### <a name="apidoc.element.memdb-server.database.prototype.getConnection"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>getConnection (id)](#apidoc.element.memdb-server.database.prototype.getConnection)
- description and source-code
```javascript
getConnection = function (id){
    var conn = this.connections[id];
    if(!conn){
        throw new Error('connection ' + id + ' not exist');
    }
    return conn;
}
```
- example usage
```shell
...
    connId : connId,
};
};

proto.disconnect = function(connId){
var self = this;
return P.try(function(){
    var conn = self.getConnection(connId);
    return self.execute(connId, 'close', [], {ignoreConcurrent : true});
})
.then(function(){
    delete self.connections[connId];
    delete self.dbWrappers[connId];
    self.logger.info('[conn:%s] connection closed', connId);
});
...
```

#### <a name="apidoc.element.memdb-server.database.prototype.start"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>start ()](#apidoc.element.memdb-server.database.prototype.start)
- description and source-code
```javascript
start = function (){
    var self = this;
    return this.shard.start()
    .then(function(){
        self.logger.info('database started');
    });
}
```
- example usage
```shell
...

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
var self = this;
return this.shard.start()
.then(function(){
    self.logger.info('database started');
});
};

proto.stop = function(force){
var self = this;
...
```

#### <a name="apidoc.element.memdb-server.database.prototype.stop"></a>[function <span class="apidocSignatureSpan">memdb-server.database.prototype.</span>stop (force)](#apidoc.element.memdb-server.database.prototype.stop)
- description and source-code
```javascript
stop = function (force){
    var self = this;

    this.opsCounter.stop();
    this.tpsCounter.stop();

    return P.try(function(){
        // Make sure no new request come anymore

        // Wait for all operations finish
        return utils.waitUntil(function(){
            return !self.connectionLock.isBusy();
        });
    })
    .then(function(){
        self.logger.debug('all requests finished');
        return self.shard.stop(force);
    })
    .then(function(){
        self.logger.info('database stoped');
    });
}
```
- example usage
```shell
...
self.logger.info('database started');
    });
};

proto.stop = function(force){
    var self = this;

    this.opsCounter.stop();
    this.tpsCounter.stop();

    return P.try(function(){
// Make sure no new request come anymore

// Wait for all operations finish
return utils.waitUntil(function(){
...
```



# <a name="apidoc.module.memdb-server.document"></a>[module memdb-server.document](#apidoc.module.memdb-server.document)

#### <a name="apidoc.element.memdb-server.document.document"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>document (opts)](#apidoc.element.memdb-server.document.document)
- description and source-code
```javascript
document = function (opts){ //jshint ignore:line
    opts = opts || {};

    if(!opts.hasOwnProperty('_id')){
        throw new Error('_id is not specified');
    }
    this._id = opts._id;

    var doc = opts.doc || null;
    if(typeof(doc) !== 'object'){
        throw new Error('doc must be object');
    }
    if(!!doc){
        doc._id = this._id;
    }

    this.commited = doc;
    this.changed = undefined; // undefined means no change, while null means removed
    this.connId = null; // Connection that hold the document lock

    this.locker = opts.locker;
    this.lockKey = opts.lockKey;
    if(!this.locker){
        this.locker = new AsyncLock({
                            Promise : P,
                            timeout : opts.lockTimeout || DEFAULT_LOCK_TIMEOUT
                            });
        this.lockKey = '';
    }

    this.releaseCallback = null;

    this.indexes = opts.indexes || {};

    this.savedIndexValues = {}; //{indexKey : indexValue}

    EventEmitter.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.document.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.document.</span>super_ ()](#apidoc.element.memdb-server.document.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.document.prototype"></a>[module memdb-server.document.prototype](#apidoc.module.memdb-server.document.prototype)

#### <a name="apidoc.element.memdb-server.document.prototype._getChanged"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getChanged ()](#apidoc.element.memdb-server.document.prototype._getChanged)
- description and source-code
```javascript
_getChanged = function (){
    return this.changed !== undefined ? this.changed : this.commited;
}
```
- example usage
```shell
...
};

util.inherits(Document, EventEmitter);

var proto = Document.prototype;

proto.find = function(connId, fields){
var doc = this.isLocked(connId) ? this._getChanged() : this.commited;

if(doc === null){
    return null;
}

if(!fields){
    return doc;
...
```

#### <a name="apidoc.element.memdb-server.document.prototype._getCommited"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getCommited ()](#apidoc.element.memdb-server.document.prototype._getCommited)
- description and source-code
```javascript
_getCommited = function (){
    return this.commited;
}
```
- example usage
```shell
...

// internal method, not concurrency safe
proto._persistent = function(key){
if(!this.commitedKeys.hasOwnProperty(key)){
    return; // no change
}

var doc = this._doc(key)._getCommited();
var ver = this.commitedKeys[key]; // get current version

var self = this;
var res = this._resolveKey(key);

return this.backend.set(res.name, res.id, doc)
.then(function(){
...
```

#### <a name="apidoc.element.memdb-server.document.prototype._getIndexValue"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_getIndexValue (indexKey, opts)](#apidoc.element.memdb-server.document.prototype._getIndexValue)
- description and source-code
```javascript
_getIndexValue = function (indexKey, opts){
    opts = opts || {};

    var self = this;
    var indexValue = JSON.parse(indexKey).sort().map(function(key){
        var doc = self._getChanged();
        var value = !!doc ? doc[key] : undefined;
        // null and undefined is not included in index
        if(value === null || value === undefined){
            return undefined;
        }
        if(['number', 'string', 'boolean'].indexOf(typeof(value)) === -1){
            throw new Error('invalid value for indexed key ' + indexKey);
        }
        var ignores = opts.valueIgnore ? opts.valueIgnore[key] || [] : [];
        if(ignores.indexOf(value) !== -1){
            return undefined;
        }
        return value;
    });

    // Return null if one of the value is undefined
    if(indexValue.indexOf(undefined) !== -1){
        return null;
    }
    return JSON.stringify(indexValue);
}
```
- example usage
```shell
...
};

proto.modify = function(connId, cmd, param){
this.ensureLocked(connId);

for(var indexKey in this.indexes){
    if(!this.savedIndexValues.hasOwnProperty(indexKey)){
        this.savedIndexValues[indexKey] = this._getIndexValue(indexKey, this.indexes[indexKey]);
    }
}

var modifyFunc = modifier[cmd];
if(typeof(modifyFunc) !== 'function'){
    throw new Error('invalid modifier - ' + cmd);
}
...
```

#### <a name="apidoc.element.memdb-server.document.prototype._unlock"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_unlock ()](#apidoc.element.memdb-server.document.prototype._unlock)
- description and source-code
```javascript
_unlock = function (){
    if(this.connId === null){
        return;
    }

    this.connId = null;
    var releaseCallback = this.releaseCallback;
    this.releaseCallback = null;

    releaseCallback();

    this.emit('unlock');
}
```
- example usage
```shell
...

if(this.changed !== undefined){
    this.commited = this.changed;
}
this.changed = undefined;

this.emit('commit');
this._unlock();
};

proto.rollback = function(connId){
this.ensureLocked(connId);

this.changed = undefined;
...
```

#### <a name="apidoc.element.memdb-server.document.prototype._waitUnlock"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>_waitUnlock ()](#apidoc.element.memdb-server.document.prototype._waitUnlock)
- description and source-code
```javascript
_waitUnlock = function (){
    var deferred = P.defer();
    var self = this;
    this.locker.acquire(this.lockKey, function(){
        deferred.resolve();
    })
    .catch(function(err){
        deferred.reject(new Error('doc._waitUnlock failed - ' + self.lockKey));
    });
    return deferred.promise;
}
```
- example usage
```shell
...
this.logger.debug('start unload %s', key);

var doc = this.docs[key];

return P.bind(this)
.then(function(){
    // Wait all existing lock release
    return doc._waitUnlock();
})
.then(function(){
    // Persistent immediately
    return this._persistent(key);
})
.then(function(){
    if(!this.config.disableSlave){
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.commit"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>commit (connId)](#apidoc.element.memdb-server.document.prototype.commit)
- description and source-code
```javascript
commit = function (connId){
    this.ensureLocked(connId);

    if(this.changed !== undefined){
        this.commited = this.changed;
    }
    this.changed = undefined;

    this.emit('commit');
    this._unlock();
}
```
- example usage
```shell
...
proto.commit = function(){
var self = this;
return P.each(Object.keys(this.collections), function(name){
    var collection = self.collections[name];
    return collection.commitIndex();
})
.then(function(){
    return self.shard.commit(self._id, Object.keys(self.lockedKeys));
})
.then(function(){
    self.lockedKeys = {};

    self.logger.debug('[conn:%s] commited', self._id);
    return true;
});
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.ensureLocked"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>ensureLocked (connId)](#apidoc.element.memdb-server.document.prototype.ensureLocked)
- description and source-code
```javascript
ensureLocked = function (connId){
    if(!this.isLocked(connId)){
        throw new Error('doc not locked by ' + connId);
    }
}
```
- example usage
```shell
...
    for(var cmd in modifier){
        this.modify(connId, cmd, modifier[cmd]);
    }
}
};

proto.modify = function(connId, cmd, param){
this.ensureLocked(connId);

for(var indexKey in this.indexes){
    if(!this.savedIndexValues.hasOwnProperty(indexKey)){
        this.savedIndexValues[indexKey] = this._getIndexValue(indexKey, this.indexes[indexKey]);
    }
}
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.exists"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>exists (connId)](#apidoc.element.memdb-server.document.prototype.exists)
- description and source-code
```javascript
exists = function (connId){
    return this.isLocked(connId) ? this._getChanged() !== null: this.commited !== null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.document.prototype.find"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>find (connId, fields)](#apidoc.element.memdb-server.document.prototype.find)
- description and source-code
```javascript
find = function (connId, fields){
    var doc = this.isLocked(connId) ? this._getChanged() : this.commited;

    if(doc === null){
        return null;
    }

    if(!fields){
        return doc;
    }

    var includeFields = [], excludeFields = [];

    if(typeof(fields) === 'string'){
        includeFields = fields.split(' ');
    }
    else if(typeof(fields) === 'object'){
        for(var field in fields){
            if(!!fields[field]){
                includeFields.push(field);
            }
            else{
                excludeFields.push(field);
            }
        }
        if(includeFields.length > 0 && excludeFields.length > 0){
            throw new Error('Can not specify both include and exclude fields');
        }
    }

    var ret = null;
    if(includeFields.length > 0){
        ret = {};
        includeFields.forEach(function(field){
            if(doc.hasOwnProperty(field)){
                ret[field] = doc[field];
            }
        });
        ret._id = this._id;
    }
    else if(excludeFields.length > 0){
        ret = {};
        for(var key in doc){
            ret[key] = doc[key];
        }
        excludeFields.forEach(function(key){
            delete ret[key];
        });
    }
    else{
        ret = doc;
    }

    return ret;
}
```
- example usage
```shell
...

return this._findByIndex(indexKey, indexValue, fields, opts);
};

proto.findOne = function(query, fields, opts){
opts = opts || {};
opts.limit = 1;
return this.find(query, fields, opts)
.then(function(docs){
    if(!Array.isArray(docs)){
        return docs;
    }
    if(docs.length === 0){
        return null;
    }
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.insert"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>insert (connId, doc)](#apidoc.element.memdb-server.document.prototype.insert)
- description and source-code
```javascript
insert = function (connId, doc){
    this.modify(connId, '$insert',  doc);
}
```
- example usage
```shell
...
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
};
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.isFree"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>isFree ()](#apidoc.element.memdb-server.document.prototype.isFree)
- description and source-code
```javascript
isFree = function (){
    return this.connId === null;
}
```
- example usage
```shell
...
};

proto.find = function(connId, key, fields){
    this._ensureState(STATE.RUNNING);
    var self = this;

    if(this.docs[key]){ //already loaded
if(this.docs[key].isFree()){
    // restart idle timer if doc doesn't locked by anyone
    this._cancelIdleTimeout(key);
    this._startIdleTimeout(key);
}

var ret = this.docs[key].find(connId, fields);
self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.isLocked"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>isLocked (connId)](#apidoc.element.memdb-server.document.prototype.isLocked)
- description and source-code
```javascript
isLocked = function (connId){
    return this.connId === connId && connId !== null && connId !== undefined;
}
```
- example usage
```shell
...
.then(function(){
    return self._finishIndexTasks(id);
});
};

proto.lock = function(id){
id = this._checkId(id);
if(this.shard.isLocked(this.conn._id, this._key(id))){
    return;
}

var self = this;
return this.shard.lock(this.conn._id, this._key(id))
.then(function(ret){
    self.emit('lock', id);
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.lock"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>lock (connId)](#apidoc.element.memdb-server.document.prototype.lock)
- description and source-code
```javascript
lock = function (connId){
    if(connId === null || connId === undefined){
        throw new Error('connId is null');
    }

    var deferred = P.defer();
    if(this.isLocked(connId)){
        deferred.resolve();
    }
    else{
        var self = this;
        this.locker.acquire(this.lockKey, function(release){
            self.connId = connId;
            self.releaseCallback = release;

            self.emit('lock');
            deferred.resolve();
        })
        .catch(function(err){
            if(!deferred.isResolved()){
                deferred.reject(new Error('doc.lock failed - ' + self.lockKey));
            }
        });
    }
    return deferred.promise;
}
```
- example usage
```shell
...
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
})
.then(function(){
    return self.shard.insert(self.conn._id, self._key(id), doc);
})
.then(function(){
    return self._finishIndexTasks(id);
})
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.modify"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>modify (connId, cmd, param)](#apidoc.element.memdb-server.document.prototype.modify)
- description and source-code
```javascript
modify = function (connId, cmd, param){
    this.ensureLocked(connId);

    for(var indexKey in this.indexes){
        if(!this.savedIndexValues.hasOwnProperty(indexKey)){
            this.savedIndexValues[indexKey] = this._getIndexValue(indexKey, this.indexes[indexKey]);
        }
    }

    var modifyFunc = modifier[cmd];
    if(typeof(modifyFunc) !== 'function'){
        throw new Error('invalid modifier - ' + cmd);
    }

    if(this.changed === undefined){ //copy on write
        this.changed = utils.clone(this.commited);
    }

    this.changed = modifyFunc(this.changed, param);

    // id is immutable
    if(!!this.changed){
        this.changed._id = this._id;
    }

    for(indexKey in this.indexes){
        var value = this._getIndexValue(indexKey, this.indexes[indexKey]);

        if(value !== this.savedIndexValues[indexKey]){
            logger.trace('%s.updateIndex(%s, %s, %s)', this._id, indexKey, this.savedIndexValues[indexKey], value);
            this.emit('updateIndex', connId, indexKey, this.savedIndexValues[indexKey], value);

            this.savedIndexValues[indexKey] = value;
        }
    }

    logger.trace('%s.modify(%s, %j) => %j', this._id, cmd, param, this.changed);
}
```
- example usage
```shell
...
};

proto.exists = function(connId){
    return this.isLocked(connId) ? this._getChanged() !== null: this.commited !== null;
};

proto.insert = function(connId, doc){
    this.modify(connId, '$insert',  doc);
};

proto.remove = function(connId){
    this.modify(connId, '$remove');
};

proto.update = function(connId, modifier, opts){
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.remove"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>remove (connId)](#apidoc.element.memdb-server.document.prototype.remove)
- description and source-code
```javascript
remove = function (connId){
    this.modify(connId, '$remove');
}
```
- example usage
```shell
...
};

proto._removeById = function(id, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.remove(self.conn._id, self._key(id), opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.lock = function(id){
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.rollback"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>rollback (connId)](#apidoc.element.memdb-server.document.prototype.rollback)
- description and source-code
```javascript
rollback = function (connId){
    this.ensureLocked(connId);

    this.changed = undefined;

    this.savedIndexValues = {};

    this.emit('rollback');
    this._unlock();
}
```
- example usage
```shell
...
    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
};

var proto = Connection.prototype;

proto.close = function(){
    if(this.isDirty()){
        this.rollback();
    }
    for(var name in this.collections){
        this.collections[name].close();
    }
};

consts.collMethods.forEach(function(method){
...
```

#### <a name="apidoc.element.memdb-server.document.prototype.update"></a>[function <span class="apidocSignatureSpan">memdb-server.document.prototype.</span>update (connId, modifier, opts)](#apidoc.element.memdb-server.document.prototype.update)
- description and source-code
```javascript
update = function (connId, modifier, opts){
    opts = opts || {};
    if(!modifier){
        throw new Error('modifier is empty');
    }

    modifier = modifier || {};

    var isModify = false;
    for(var field in modifier){
        isModify = (field[0] === '$');
        break;
    }

    if(!isModify){
        this.modify(connId, '$replace', modifier);
    }
    else{
        for(var cmd in modifier){
            this.modify(connId, cmd, modifier[cmd]);
        }
    }
}
```
- example usage
```shell
...
};

proto._updateById = function(id, modifier, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.update(self.conn._id, self._key(id), modifier, opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.remove = function(query, opts){
...
```



# <a name="apidoc.module.memdb-server.indexbuilder"></a>[module memdb-server.indexbuilder](#apidoc.module.memdb-server.indexbuilder)

#### <a name="apidoc.element.memdb-server.indexbuilder.drop"></a>[function <span class="apidocSignatureSpan">memdb-server.indexbuilder.</span>drop (conf, collName, keys)](#apidoc.element.memdb-server.indexbuilder.drop)
- description and source-code
```javascript
drop = function (conf, collName, keys){
    if(!Array.isArray(keys)){
        keys = keys.split(' ');
    }
    var indexKey = JSON.stringify(keys.sort());
    conf.backend.shardId = '$';
    var backend = backends.create(conf.backend);
    var indexCollName = Collection.prototype._indexCollectionName.call({name : collName}, indexKey);

    return ensureShutDown(conf.locking)
    .then(function(){
        return backend.start();
    })
    .then(function(){
        return backend.drop(indexCollName);
    })
    .finally(function(){
        logger.warn('Droped index %s %s', collName, indexKey);
        return backend.stop();
    });
}
```
- example usage
```shell
...
    var indexCollName = Collection.prototype._indexCollectionName.call({name : collName}, indexKey);

    return ensureShutDown(conf.locking)
    .then(function(){
        return backend.start();
    })
    .then(function(){
        return backend.drop(indexCollName);
    })
    .finally(function(){
        logger.warn('Droped index %s %s', collName, indexKey);
        return backend.stop();
    });
};
...
```

#### <a name="apidoc.element.memdb-server.indexbuilder.rebuild"></a>[function <span class="apidocSignatureSpan">memdb-server.indexbuilder.</span>rebuild (conf, collName, keys, opts)](#apidoc.element.memdb-server.indexbuilder.rebuild)
- description and source-code
```javascript
rebuild = function (conf, collName, keys, opts){
    opts = opts || {};
    if(!Array.isArray(keys)){
        keys = keys.split(' ');
    }
    var indexKey = JSON.stringify(keys.sort());
    conf.backend.shardId = '$';
    var backend = backends.create(conf.backend);

    var indexCollName = Collection.prototype._indexCollectionName.call({name : collName}, indexKey);

    logger.warn('Start rebuild index %s %s', collName, indexKey);

    return ensureShutDown(conf.locking)
    .then(function(){
        return backend.start();
    })
    .then(function(){
        return backend.drop(indexCollName);
    })
    .then(function(){
        return backend.getAll(collName);
    })
    .then(function(itor){
        return utils.mongoForEach(itor, function(item){
            var indexValue = Document.prototype._getIndexValue.call({_getChanged : function(){return item;}}, indexKey, opts);
            if(!indexValue){
                return;
            }

            return P.try(function(){
                return backend.get(indexCollName, indexValue);
            })
            .then(function(doc){
                if(!doc){
                    doc = {_id: indexValue, ids : []};
                }
                else if(opts.unique){
                    throw new Error('Duplicate value for unique key ' + indexKey);
                }

                if(doc.ids.indexOf(item._id) === -1){
                    doc.ids.push(item._id);
                }
                return backend.set(indexCollName, indexValue, doc);
            });
        });
    })
    .then(function(){
        logger.warn('Finish rebuild index %s %s', collName, indexKey);
        return backend.stop();
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.modifier"></a>[module memdb-server.modifier](#apidoc.module.memdb-server.modifier)



# <a name="apidoc.module.memdb-server.protocol"></a>[module memdb-server.protocol](#apidoc.module.memdb-server.protocol)

#### <a name="apidoc.element.memdb-server.protocol.protocol"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>protocol (opts)](#apidoc.element.memdb-server.protocol.protocol)
- description and source-code
```javascript
protocol = function (opts){
    EventEmitter.call(this);

    opts = opts || {};

    this.socket = opts.socket;
    this.socket.setEncoding('utf8');

    this.maxMsgLength = opts.maxMsgLength || DEFAULT_MAX_MSG_LENGTH;

    this.remainLine = '';

    var self = this;
    this.socket.on('data', function(data){
        // message is json encoded and splited by '\n'
        var lines = data.split('\n');
        for(var i=0; i<lines.length - 1; i++){
            try{
                var msg = '';
                if(i === 0){
                    msg = JSON.parse(self.remainLine + lines[i]);
                    self.remainLine = '';
                }
                else{
                    msg = JSON.parse(lines[i]);
                }
                self.emit('msg', msg);
            }
            catch(err){
                logger.error(err.stack);
            }
        }
        self.remainLine = lines[lines.length - 1];
    });

    this.socket.on('close', function(hadError){
        self.emit('close', hadError);
    });

    this.socket.on('connect', function(){
        self.emit('connect');
    });

    this.socket.on('error', function(err){
        self.emit('error', err);
    });

    this.socket.on('timeout', function(){
        self.emit('timeout');
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.protocol.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.protocol.</span>super_ ()](#apidoc.element.memdb-server.protocol.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.protocol.prototype"></a>[module memdb-server.protocol.prototype](#apidoc.module.memdb-server.protocol.prototype)

#### <a name="apidoc.element.memdb-server.protocol.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">memdb-server.protocol.prototype.</span>disconnect ()](#apidoc.element.memdb-server.protocol.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (){
    this.socket.end();
}
```
- example usage
```shell
...
            connId : connId,
        };
    }
    if(!msg.connId){
        throw new Error('connId is required');
    }
    if(msg.method === 'disconnect'){
        return db.disconnect(msg.connId)
        .then(function(){
            delete connIds[msg.connId];
        });
    }
    return db.execute(msg.connId, msg.method, msg.args);
})
.then(function(ret){
...
```

#### <a name="apidoc.element.memdb-server.protocol.prototype.send"></a>[function <span class="apidocSignatureSpan">memdb-server.protocol.prototype.</span>send (msg)](#apidoc.element.memdb-server.protocol.prototype.send)
- description and source-code
```javascript
send = function (msg){
    var data = JSON.stringify(msg) + '\n';
    if(data.length > this.maxMsgLength){
        throw new Error('msg length exceed limit');
    }

    var ret = this.socket.write(data);
    if(!ret){
        logger.warn('socket.write return false');
    }
}
```
- example usage
```shell
...
        resp.err = {
            message : err.message,
            stack : err.stack,
        };
        resp.data = null;
    })
    .then(function(){
        protocol.send(resp);
        logger.debug('[conn:%s] %s <= %j', msg.connId, remoteAddress, resp);
    })
    .catch(function(e){
        logger.error(e.stack);
    });
});
...
```



# <a name="apidoc.module.memdb-server.server"></a>[module memdb-server.server](#apidoc.module.memdb-server.server)

#### <a name="apidoc.element.memdb-server.server.start"></a>[function <span class="apidocSignatureSpan">memdb-server.server.</span>start (opts)](#apidoc.element.memdb-server.server.start)
- description and source-code
```javascript
start = function (opts){
    var deferred = P.defer();

    var logger = memdbLogger.getLogger('memdb', __filename, 'shard:' + opts.shardId);
    logger.warn('starting %s...', opts.shardId);

    var bind = opts.bind || '0.0.0.0';
    var port = opts.port || DEFAULT_PORT;

    var db = new Database(opts);

    var sockets = utils.forceHashMap();

    var _isShutingDown = false;

    var server = net.createServer(function(socket){

        var clientId = uuid.v4();
        sockets[clientId] = socket;

        var connIds = utils.forceHashMap();
        var remoteAddress = socket.remoteAddress;
        var protocol = new Protocol({socket : socket});

        protocol.on('msg', function(msg){
            logger.debug('[conn:%s] %s => %j', msg.connId, remoteAddress, msg);
            var resp = {seq : msg.seq};

            P.try(function(){
                if(msg.method === 'connect'){
                    var clientVersion = msg.args[0];
                    if(parseFloat(clientVersion) < parseFloat(consts.minClientVersion)){
                        throw new Error('client version not supported, please upgrade');
                    }
                    var connId = db.connect().connId;
                    connIds[connId] = true;
                    return {
                        connId : connId,
                    };
                }
                if(!msg.connId){
                    throw new Error('connId is required');
                }
                if(msg.method === 'disconnect'){
                    return db.disconnect(msg.connId)
                    .then(function(){
                        delete connIds[msg.connId];
                    });
                }
                return db.execute(msg.connId, msg.method, msg.args);
            })
            .then(function(ret){
                resp.err = null;
                resp.data = ret;
            }, function(err){
                resp.err = {
                    message : err.message,
                    stack : err.stack,
                };
                resp.data = null;
            })
            .then(function(){
                protocol.send(resp);
                logger.debug('[conn:%s] %s <= %j', msg.connId, remoteAddress, resp);
            })
            .catch(function(e){
                logger.error(e.stack);
            });
        });

        protocol.on('close', function(){
            P.map(Object.keys(connIds), function(connId){
                return db.disconnect(connId);
            })
            .then(function(){
                connIds = utils.forceHashMap();
                delete sockets[clientId];
                logger.info('client %s disconnected', remoteAddress);
            })
            .catch(function(e){
                logger.error(e.stack);
            });
        });

        protocol.on('error', function(e){
            logger.error(e.stack);
        });

        logger.info('client %s connected', remoteAddress);
    });

    server.on('error', function(err){
        logger.error(err.stack);

        if(!deferred.isResolved()){
            deferred.reject(err);
        }
    });

    P.try(function(){
        return P.promisify(server.listen, server)(port, bind);
    })
    .then(function(){
        return db.start();
    })
    .then(function(){
        logger.warn('server started on %s:%s', bind, port);
        deferred.resolve();
    })
    .catch(function(err){
        logger.error(err.stack);
        deferred.reject(err);
    });

    var shutdown = function(){
        logger.warn('receive shutdown signal');

        if(_isShutingDown){
            return;
        }
        _isShutingDown = true;

        return P.try(function(){
            var deferred = P.defer();

            server.once('close', function(){
                logger.debug('on server close');
                deferred.resolve();
            });

            server.close();

            Object.keys(sockets).forEach(function(id){
                try{
                    sockets[id].end();
                    sockets[id].destroy();
                } ...
```
- example usage
```shell
...

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
var self = this;
return this.shard.start()
.then(function(){
    self.logger.info('database started');
});
};

proto.stop = function(force){
var self = this;
...
```



# <a name="apidoc.module.memdb-server.shard"></a>[module memdb-server.shard](#apidoc.module.memdb-server.shard)

#### <a name="apidoc.element.memdb-server.shard.shard"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>shard (opts)](#apidoc.element.memdb-server.shard.shard)
- description and source-code
```javascript
shard = function (opts){
    EventEmitter.call(this);

    opts = opts || {};

    this._id = opts.shardId;
    if(!this._id){
        throw new Error('shardId is empty');
    }
    this._id = this._id.toString();
    if(this._id.indexOf('$') !== -1){
        throw new Error('shardId can not contain "$"');
    }

    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this._id);

    this.config = {
        locking : opts.locking || {},
        backend : opts.backend || {},
        slave : opts.slave || {},

        shards : opts.shards || {},

        idleTimeout : opts.hasOwnProperty('idleTimeout') ? opts.idleTimeout : DEFAULT_IDLE_TIMEOUT,
        persistentDelay : opts.hasOwnProperty('persistentDelay') ?  opts.persistentDelay : DEFAULT_PERSISTENT_DELAY,

        heartbeatInterval : opts.heartbeatInterval || DEFAULT_HEARTBEAT_INTERVAL,
        heartbeatTimeout : opts.heartbeatTimeout || DEFAULT_HEARTBEAT_TIMEOUT,
        backendLockTimeout : opts.backendLockTimeout || DEFAULT_BACKEND_LOCK_TIMEOUT,
        backendLockRetryInterval : opts.backendLockRetryInterval || DEFAULT_BACKEND_LOCK_RETRY_INTERVAL,
        reloadDelay : opts.reloadDelay || DEFAULT_RELOAD_DELAY,
        lockTimeout : opts.lockTimeout || DEFAULT_LOCK_TIMEOUT,

        memoryLimit : opts.memoryLimit || DEFAULT_MEMORY_LIMIT,
        gcCount : opts.gcCount || DEFAULT_GC_COUNT,
        gcInterval : opts.gcInterval || DEFAULT_GC_INTERVAL,

        disableSlave : opts.disableSlave || false,

        collections : opts.collections || {},
    };

    // global locking
    var lockerConf = this.config.locking;
    lockerConf.shardId = this._id;
    lockerConf.heartbeatTimeout = this.config.heartbeatTimeout;
    lockerConf.heartbeatInterval = this.config.heartbeatInterval;
    this.backendLocker = new BackendLocker(lockerConf);

    // backend storage
    var backendConf = this.config.backend;
    backendConf.shardId = this._id;
    this.backend = backends.create(backendConf);

    // slave redis
    var slaveConf = this.config.slave;
    slaveConf.shardId = this._id;
    this.slave = new Slave(slaveConf);

    // memdb client to communicate with other shards
    this.autoconn = new AutoConnection({
        shards : this.config.shards,
        concurrentInConnection : true,
    });

    // Document storage {key : doc}
    this.docs = utils.forceHashMap();

    // Newly commited docs (for incremental _save)
    this.commitedKeys = utils.forceHashMap(); // {key : version}

    // Idle timeout before unload
    this.idleTimeouts = utils.forceHashMap(); // {key : timeout}

    // Doc persistent timeout
    this.persistentTimeouts = utils.forceHashMap(); // {key : timeout}

    // GC interval
    this.gcInterval = null;

    // Lock async operations for each key
    this.keyLock = new AsyncLock({Promise : P});

    // Task locker
    this.taskLock = new AsyncLock({Promise : P});

    // Doc locker
    this.docLock = new AsyncLock({
        timeout : this.config.lockTimeout,
        Promise : P,
    });

    // Current concurrent commiting processes
    this.commitingCount = 0;

    // Current key unloading task
    this.unloadingKeys = utils.forceHashMap();

    this.loadCounter = utils.rateCounter();
    this.unloadCounter = utils.rateCounter();
    this.persistentCounter = utils.rateCounter();

    this.state = STATE.INITED;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.shard.super_"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.</span>super_ ()](#apidoc.element.memdb-server.shard.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.shard.prototype"></a>[module memdb-server.shard.prototype](#apidoc.module.memdb-server.shard.prototype)

#### <a name="apidoc.element.memdb-server.shard.prototype._addDoc"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_addDoc (key, obj)](#apidoc.element.memdb-server.shard.prototype._addDoc)
- description and source-code
```javascript
_addDoc = function (key, obj){
    var self = this;

    var res = this._resolveKey(key);
    var coll = this.config.collections[res.name];
    var indexes = (coll && coll.indexes) || {};

    var opts = {
        _id : res.id,
        doc: obj,
        indexes: indexes,
        locker : this.docLock,
        lockKey : key,
    };
    var doc = new Document(opts);

    this._startIdleTimeout(key);

    doc.on('lock', function(){
        self._cancelIdleTimeout(key);
    });

    doc.on('unlock', function(){
        self._startIdleTimeout(key);
    });

    doc.on('commit', function(){
        self._setCommited(key);

        // delay sometime and persistent to backend
        if(!self.persistentTimeouts.hasOwnProperty(key) && self.config.persistentDelay >= 0){
            self.persistentTimeouts[key] = setTimeout(function(){
                delete self.persistentTimeouts[key];
                return self.keyLock.acquire(key, function(){
                    return self._persistent(key);
                })
                .catch(function(err){
                    self.logger.error(err.stack);
                });
            }, self.config.persistentDelay);
        }
    });

    doc.on('updateIndex', function(connId, indexKey, oldValue, newValue){
        // pass event to collection
        self.emit('updateIndex$' + res.name + '$' + connId, res.id, indexKey, oldValue, newValue);
    });

    // Loaded at this instant
    self.docs[key] = doc;
}
```
- example usage
```shell
...
        obj = ret;
        if(!self.config.disableSlave){
            // Sync data to slave
            return self.slave.set(key, obj);
        }
    })
    .then(function(){
        self._addDoc(key, obj);

        self.loadCounter.inc();
        self.logger.info('loaded %s', key);
    });
};

proto._addDoc = function(key, obj){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._cancelIdleTimeout"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_cancelIdleTimeout (key)](#apidoc.element.memdb-server.shard.prototype._cancelIdleTimeout)
- description and source-code
```javascript
_cancelIdleTimeout = function (key){
    clearTimeout(this.idleTimeouts[key]);
    delete this.idleTimeouts[key];
}
```
- example usage
```shell
...
proto.find = function(connId, key, fields){
this._ensureState(STATE.RUNNING);
var self = this;

if(this.docs[key]){ //already loaded
    if(this.docs[key].isFree()){
        // restart idle timer if doc doesn't locked by anyone
        this._cancelIdleTimeout(key);
        this._startIdleTimeout(key);
    }

    var ret = this.docs[key].find(connId, fields);
    self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
    return ret;
}
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._doc"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_doc (key)](#apidoc.element.memdb-server.shard.prototype._doc)
- description and source-code
```javascript
_doc = function (key){
    if(!this.docs.hasOwnProperty(key)){
        throw new Error(key + ' is not loaded');
    }
    return this.docs[key];
}
```
- example usage
```shell
...
});
};

proto.update = function(connId, key, doc, opts){
this._ensureState(STATE.RUNNING);

// Since lock is called before, so doc is loaded for sure
var ret = this._doc(key).update(connId, doc, opts);

this.logger.debug('[conn:%s] update(%s, %j, %j) => %s', connId, key, doc, opts, ret);
return ret;
};

proto.insert = function(connId, key, doc){
this._ensureState(STATE.RUNNING);
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._ensureState"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_ensureState (state)](#apidoc.element.memdb-server.shard.prototype._ensureState)
- description and source-code
```javascript
_ensureState = function (state){
    if(this.state !== state){
        throw new Error(util.format('Server state is incorrect, expected %s, actual %s', state, this.state));
    }
}
```
- example usage
```shell
...
};

util.inherits(Shard, EventEmitter);

var proto = Shard.prototype;

proto.start = function(){
this._ensureState(STATE.INITED);
this.state = STATE.STARTING;

return P.bind(this)
.then(function(){
    return this.backendLocker.start();
})
.then(function(){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._isLoaded"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_isLoaded (key)](#apidoc.element.memdb-server.shard.prototype._isLoaded)
- description and source-code
```javascript
_isLoaded = function (key){
    return !!this.docs[key];
}
```
- example usage
```shell
...
return this.docs[key] && this.docs[key].isLocked(connId);
};

proto.findReadOnly = function(connId, key, fields){
this._ensureState(STATE.RUNNING);
var self = this;

if(this._isLoaded(key)){
    return this.find(connId, key, fields);
}
return P.try(function(){
    return self.backendLocker.getHolderId(key);
})
.then(function(shardId){
    if(!shardId || shardId === self._id){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._load"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_load (key)](#apidoc.element.memdb-server.shard.prototype._load)
- description and source-code
```javascript
_load = function (key){
    if(this.docs[key]){ // already loaded
        return;
    }

    this.logger.debug('start load %s', key);

    var obj = null;

    var self = this;
    return P.try(function(){
        // get backend lock
        return self._lockBackend(key);
    })
    .then(function(){
        var res = self._resolveKey(key);

        return self.backend.get(res.name, res.id);
    })
    .then(function(ret){
        obj = ret;
        if(!self.config.disableSlave){
            // Sync data to slave
            return self.slave.set(key, obj);
        }
    })
    .then(function(){
        self._addDoc(key, obj);

        self.loadCounter.inc();
        self.logger.info('loaded %s', key);
    });
}
```
- example usage
```shell
...
    var ret = this.docs[key].find(connId, fields);
    self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
    return ret;
}

return this.keyLock.acquire(key, function(){
    return P.try(function(){
        return self._load(key);
    })
    .then(function(){
        return self.docs[key].find(connId, fields);
    })
    .then(function(ret){
        self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
        return ret;
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._lockBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_lockBackend (key)](#apidoc.element.memdb-server.shard.prototype._lockBackend)
- description and source-code
```javascript
_lockBackend = function (key){
    var self = this;
    return P.try(function(){
        return self.backendLocker.tryLock(key);
    })
    .then(function(success){
        if(success){
            return;
        }

        var startTick = Date.now();

        var tryLock = function(wait){
            return P.try(function(){
                return self.backendLocker.getHolderId(key);
            })
            .then(function(shardId){
                if(shardId === self._id){
                    // already locked
                    return;
                }

                return P.try(function(){
                    if(shardId){
                        // notify holder to unload the doc
                        return self.autoconn.$unload(shardId, key);
                    }
                    else{
                        return true;
                    }
                })
                .then(function(success){
                    if(success){
                        return self.backendLocker.tryLock(key);
                    }
                    else{
                        return false;
                    }
                })
                .then(function(success){
                    if(success){
                        self.logger.debug('locked backend doc - %s (%sms)', key, Date.now() - startTick);
                        return;
                    }

                    if(Date.now() - startTick >= self.config.backendLockTimeout){
                        throw new Error('lock backend doc - ' + key + ' timed out');
                    }

                    // delay some time and try again
                    return P.delay(wait / 2 + _.random(wait))
                    .then(function(){
                        return tryLock(wait);
                    });
                });
            });
        };

        return tryLock(self.config.backendLockRetryInterval);
    });
}
```
- example usage
```shell
...
this.logger.debug('start load %s', key);

var obj = null;

var self = this;
return P.try(function(){
    // get backend lock
    return self._lockBackend(key);
})
.then(function(){
    var res = self._resolveKey(key);

    return self.backend.get(res.name, res.id);
})
.then(function(ret){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._persistent"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_persistent (key)](#apidoc.element.memdb-server.shard.prototype._persistent)
- description and source-code
```javascript
_persistent = function (key){
    if(!this.commitedKeys.hasOwnProperty(key)){
        return; // no change
    }

    var doc = this._doc(key)._getCommited();
    var ver = this.commitedKeys[key]; // get current version

    var self = this;
    var res = this._resolveKey(key);

    return this.backend.set(res.name, res.id, doc)
    .then(function(){
        // no new change, remove the flag
        if(self.commitedKeys[key] === ver){
            delete self.commitedKeys[key];
        }

        self.persistentCounter.inc();
        self.logger.debug('persistented %s', key);
    });
}
```
- example usage
```shell
...
    self._setCommited(key);

    // delay sometime and persistent to backend
    if(!self.persistentTimeouts.hasOwnProperty(key) && self.config.persistentDelay >= 0){
        self.persistentTimeouts[key] = setTimeout(function(){
            delete self.persistentTimeouts[key];
            return self.keyLock.acquire(key, function(){
                return self._persistent(key);
            })
            .catch(function(err){
                self.logger.error(err.stack);
            });
        }, self.config.persistentDelay);
    }
});
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._resolveKey"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_resolveKey (key)](#apidoc.element.memdb-server.shard.prototype._resolveKey)
- description and source-code
```javascript
_resolveKey = function (key){
    var i = key.indexOf('$');
    if(i === -1){
        throw new Error('invalid key: ' + key);
    }
    return {name : key.slice(0, i), id : key.slice(i + 1)};
}
```
- example usage
```shell
...

var self = this;
return P.try(function(){
    // get backend lock
    return self._lockBackend(key);
})
.then(function(){
    var res = self._resolveKey(key);

    return self.backend.get(res.name, res.id);
})
.then(function(ret){
    obj = ret;
    if(!self.config.disableSlave){
        // Sync data to slave
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._setCommited"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_setCommited (key)](#apidoc.element.memdb-server.shard.prototype._setCommited)
- description and source-code
```javascript
_setCommited = function (key){
    if(!this.commitedKeys.hasOwnProperty(key)){
        this.commitedKeys[key] = 0;
    }
    this.commitedKeys[key]++;
}
```
- example usage
```shell
...
    });

    doc.on('unlock', function(){
self._startIdleTimeout(key);
    });

    doc.on('commit', function(){
self._setCommited(key);

// delay sometime and persistent to backend
if(!self.persistentTimeouts.hasOwnProperty(key) && self.config.persistentDelay >= 0){
    self.persistentTimeouts[key] = setTimeout(function(){
        delete self.persistentTimeouts[key];
        return self.keyLock.acquire(key, function(){
            return self._persistent(key);
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._startIdleTimeout"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_startIdleTimeout (key)](#apidoc.element.memdb-server.shard.prototype._startIdleTimeout)
- description and source-code
```javascript
_startIdleTimeout = function (key){
    if(!this.config.idleTimeout){
        return;
    }

    var self = this;
    this.idleTimeouts[key] = setTimeout(function(){
        return self.keyLock.acquire(key, function(){
            if(self.docs[key]){
                self.logger.debug('%s idle timed out, will unload', key);
                return self._unload(key);
            }
        })
        .catch(function(e){
            self.logger.error(e.stack);
        });
    }, this.config.idleTimeout);
}
```
- example usage
```shell
...
this._ensureState(STATE.RUNNING);
var self = this;

if(this.docs[key]){ //already loaded
    if(this.docs[key].isFree()){
        // restart idle timer if doc doesn't locked by anyone
        this._cancelIdleTimeout(key);
        this._startIdleTimeout(key);
    }

    var ret = this.docs[key].find(connId, fields);
    self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
    return ret;
}
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._unload"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_unload (key)](#apidoc.element.memdb-server.shard.prototype._unload)
- description and source-code
```javascript
_unload = function (key){
    if(!this.docs[key]){ //already unloaded
        return;
    }

    this.logger.debug('start unload %s', key);

    var doc = this.docs[key];

    return P.bind(this)
    .then(function(){
        // Wait all existing lock release
        return doc._waitUnlock();
    })
    .then(function(){
        // Persistent immediately
        return this._persistent(key);
    })
    .then(function(){
        if(!this.config.disableSlave){
            // sync data to slave
            return this.slave.del(key);
        }
    })
    .then(function(){
        this._cancelIdleTimeout(key);

        if(this.persistentTimeouts.hasOwnProperty(key)){
            clearTimeout(this.persistentTimeouts[key]);
            delete this.persistentTimeouts[key];
        }

        doc.removeAllListeners('commit');
        doc.removeAllListeners('updateIndex');
        doc.removeAllListeners('lock');
        doc.removeAllListeners('unlock');

        // _unloaded at this instant
        delete this.docs[key];

        // Release backend lock
        return this._unlockBackend(key);
    })
    .then(function(){
        this.unloadCounter.inc();

        this.logger.info('unloaded %s', key);
    });
}
```
- example usage
```shell
...
.then(function(){
    this.logger.debug('all commit processes finished');
    // WARN: Make sure all connections are closed now

    var self = this;
    return P.mapLimit(Object.keys(this.docs), function(key){
        return self.keyLock.acquire(key, function(){
            return self._unload(key);
        })
        .catch(function(e){
            self.logger.error(e.stack);
        });
    });
})
.then(function(){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype._unlockBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>_unlockBackend (key)](#apidoc.element.memdb-server.shard.prototype._unlockBackend)
- description and source-code
```javascript
_unlockBackend = function (key){
    return this.backendLocker.unlock(key);
}
```
- example usage
```shell
...
// or a redundant backend lock is held caused by unsuccessful unload
self.logger.warn('this shard does not hold %s', key);

return P.try(function(){
    return self.slave.del(key);
})
.then(function(){
    return self._unlockBackend(key);
})
.then(function(){
    deferred.resolve(true);
}, function(e){
    deferred.reject(e);
    throw e;
});
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.commit"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>commit (connId, keys)](#apidoc.element.memdb-server.shard.prototype.commit)
- description and source-code
```javascript
commit = function (connId, keys){
    this._ensureState(STATE.RUNNING);

    if(!Array.isArray(keys)){
        keys = [keys];
    }
    if(keys.length === 0){
        return;
    }

    var self = this;

    keys.forEach(function(key){
        if(!self.isLocked(connId, key)){
            throw new Error('[conn:%s] %s not locked', connId, key);
        }
    });

    this.commitingCount++;

    // commit is not concurrency safe for same connection.
    // but database.js guarantee that every request from same connection are in series.
    return P.try(function(){
        if(self.config.disableSlave){
            return;
        }

        // Sync data to slave
        if(keys.length === 1){
            var key = keys[0];
            var doc = self._doc(key)._getChanged();
            return self.slave.set(key, doc);
        }
        else{
            var docs = utils.forceHashMap();
            keys.forEach(function(key){
                docs[key] = self._doc(key)._getChanged();
            });
            return self.slave.setMulti(docs);
        }
        //TODO: possibly loss consistency
        //      if setMulti return failed but actually sccuess
    })
    .then(function(){
        // Real Commit
        keys.forEach(function(key){
            self._doc(key).commit(connId);
        });

        self.logger.debug('[conn:%s] commit(%j)', connId, keys);
    })
    .finally(function(ret){
        self.commitingCount--;
    });
}
```
- example usage
```shell
...
proto.commit = function(){
var self = this;
return P.each(Object.keys(this.collections), function(name){
    var collection = self.collections[name];
    return collection.commitIndex();
})
.then(function(){
    return self.shard.commit(self._id, Object.keys(self.lockedKeys));
})
.then(function(){
    self.lockedKeys = {};

    self.logger.debug('[conn:%s] commited', self._id);
    return true;
});
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.find"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>find (connId, key, fields)](#apidoc.element.memdb-server.shard.prototype.find)
- description and source-code
```javascript
find = function (connId, key, fields){
    this._ensureState(STATE.RUNNING);
    var self = this;

    if(this.docs[key]){ //already loaded
        if(this.docs[key].isFree()){
            // restart idle timer if doc doesn't locked by anyone
            this._cancelIdleTimeout(key);
            this._startIdleTimeout(key);
        }

        var ret = this.docs[key].find(connId, fields);
        self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
        return ret;
    }

    return this.keyLock.acquire(key, function(){
        return P.try(function(){
            return self._load(key);
        })
        .then(function(){
            return self.docs[key].find(connId, fields);
        })
        .then(function(ret){
            self.logger.debug('[conn:%s] find(%s, %j) => %j', connId, key, fields, ret);
            return ret;
        });
    });
}
```
- example usage
```shell
...

return this._findByIndex(indexKey, indexValue, fields, opts);
};

proto.findOne = function(query, fields, opts){
opts = opts || {};
opts.limit = 1;
return this.find(query, fields, opts)
.then(function(docs){
    if(!Array.isArray(docs)){
        return docs;
    }
    if(docs.length === 0){
        return null;
    }
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.findReadOnly"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>findReadOnly (connId, key, fields)](#apidoc.element.memdb-server.shard.prototype.findReadOnly)
- description and source-code
```javascript
findReadOnly = function (connId, key, fields){
    this._ensureState(STATE.RUNNING);
    var self = this;

    if(this._isLoaded(key)){
        return this.find(connId, key, fields);
    }
    return P.try(function(){
        return self.backendLocker.getHolderId(key);
    })
    .then(function(shardId){
        if(!shardId || shardId === self._id){
            return self.find(connId, key, fields);
        }
        return self.autoconn.$findReadOnly(shardId, key, fields);
    });
}
```
- example usage
```shell
...

proto.findById = function(id, fields, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
if(opts && opts.readonly){
    return self.shard.findReadOnly(self.conn._id, self._key(id), fields);
}

return P.try(function(){
    if(opts && opts.nolock){
        return;
    }
    return self.lock(id);
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.flushBackend"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>flushBackend (connId)](#apidoc.element.memdb-server.shard.prototype.flushBackend)
- description and source-code
```javascript
flushBackend = function (connId){
    this._ensureState(STATE.RUNNING);
    var self = this;

    return this.taskLock.acquire('', function(){
        return P.mapLimit(Object.keys(self.commitedKeys), function(key){
            return self.keyLock.acquire(key, function(){
                return self._persistent(key);
            });
        });
    })
    .then(function(){
        self.logger.warn('[conn:%s] flushed Backend', connId);
        return true;
    });
}
```
- example usage
```shell
...
    this.lockedKeys = {};

    this.logger.debug('[conn:%s] rolledback', this._id);
    return true;
};

proto.flushBackend = function(){
    return this.shard.flushBackend(this._id);
};

// for internal use
proto.$unload = function(key){
    return this.shard.$unload(key);
};
// for internal use
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.gc"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>gc ()](#apidoc.element.memdb-server.shard.prototype.gc)
- description and source-code
```javascript
gc = function (){
    if(this.state !== STATE.RUNNING){
        return;
    }
    if(this.taskLock.isBusy('')){
        return;
    }

    var self = this;
    return this.taskLock.acquire('', function(){
        var usage = process.memoryUsage();
        var memSize = usage.heapUsed;

        if(memSize < self.config.memoryLimit * 1024 * 1024){
            // Memory not reach limit, no need to gc
            return;
        }

        self.logger.warn('Start GC. Memory usage is too high, please reduce idleTimeout. %j', usage);

        var startTick = Date.now();

        // remove some doc
        var keys = [], count = 0;
        for(var key in self.docs){
            keys.push(key);
            count++;
            if(count >= self.config.gcCount){
                break;
            }
        }

        return P.mapLimit(keys, function(key){
            return self.keyLock.acquire(key, function(){
                return self._unload(key);
            })
            .catch(function(e){
                self.logger.error(e.stack);
            });
        })
        .then(function(){
            self.logger.warn('Finish GC in %s ms. %s docs have been unloaded.', Date.now() - startTick, keys.length);
        })
        .then(function(){
            process.nextTick(self.gc.bind(self));
        });
    })
    .catch(function(e){
        self.logger.error(e.stack);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.shard.prototype.insert"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>insert (connId, key, doc)](#apidoc.element.memdb-server.shard.prototype.insert)
- description and source-code
```javascript
insert = function (connId, key, doc){
    this._ensureState(STATE.RUNNING);

    var ret = this._doc(key).insert(connId, doc);
    this.logger.debug('[conn:%s] insert(%s, %j) => %s', connId, key, doc, ret);
    return ret;
}
```
- example usage
```shell
...
    doc._id = id;

    var self = this;
    return P.try(function(){
        return self.lock(id);
    })
    .then(function(){
        return self.shard.insert(self.conn._id, self._key(id), doc);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    })
    .thenReturn(id);
};
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.isLocked"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>isLocked (connId, key)](#apidoc.element.memdb-server.shard.prototype.isLocked)
- description and source-code
```javascript
isLocked = function (connId, key){
    return this.docs[key] && this.docs[key].isLocked(connId);
}
```
- example usage
```shell
...
.then(function(){
    return self._finishIndexTasks(id);
});
};

proto.lock = function(id){
id = this._checkId(id);
if(this.shard.isLocked(this.conn._id, this._key(id))){
    return;
}

var self = this;
return this.shard.lock(this.conn._id, this._key(id))
.then(function(ret){
    self.emit('lock', id);
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.lock"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>lock (connId, key)](#apidoc.element.memdb-server.shard.prototype.lock)
- description and source-code
```javascript
lock = function (connId, key){
    this._ensureState(STATE.RUNNING);

    if(this.isLocked(connId, key)){
        return true;
    }

    this.logger.debug('[conn:%s] shard.lock(%s) start', connId, key);

    var self = this;
    return this.keyLock.acquire(key, function(){
        return P.try(function(){
            return self._load(key);
        })
        .then(function(){
            return self.docs[key].lock(connId)
            .then(function(){
                self.logger.debug('[conn:%s] shard.lock(%s) success', connId, key);
                return true;
            }, function(e){
                throw new Error(util.format('[conn:%s] shard.lock(%s) failed', connId, key));
            });
        });
    });
}
```
- example usage
```shell
...
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
})
.then(function(){
    return self.shard.insert(self.conn._id, self._key(id), doc);
})
.then(function(){
    return self._finishIndexTasks(id);
})
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.remove"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>remove (connId, key)](#apidoc.element.memdb-server.shard.prototype.remove)
- description and source-code
```javascript
remove = function (connId, key){
    this._ensureState(STATE.RUNNING);

    var ret = this._doc(key).remove(connId);
    this.logger.debug('[conn:%s] remove(%s) => %s', connId, key, ret);
    return ret;
}
```
- example usage
```shell
...
};

proto._removeById = function(id, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.remove(self.conn._id, self._key(id), opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.lock = function(id){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.restoreFromSlave"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>restoreFromSlave ()](#apidoc.element.memdb-server.shard.prototype.restoreFromSlave)
- description and source-code
```javascript
restoreFromSlave = function (){
    this._ensureState(STATE.STARTING);

    return P.bind(this)
    .then(function(){
        return this.slave.getAllKeys();
    })
    .then(function(keys){
        if(keys.length === 0){
            return;
        }

        this.logger.error('Server not stopped properly, will restore data from slave');

        return P.bind(this)
        .then(function(){
            return this.slave.getMulti(keys);
        })
        .then(function(items){
            var self = this;
            return P.mapLimit(Object.keys(items), function(key){
                return self.keyLock.acquire(key, function(){
                    self._addDoc(key, items[key]);
                    // persistent all docs to backend
                    self._setCommited(key);
                    return self._persistent(key);
                });
            });
        })
        .then(function(){
            this.logger.warn('restored %s keys from slave', keys.length);
        });
    });
}
```
- example usage
```shell
...
    .then(function(){
if(!this.config.disableSlave){
    return this.slave.start();
}
    })
    .then(function(){
if(!this.config.disableSlave){
    return this.restoreFromSlave();
}
    })
    .then(function(){
this.gcInterval = setInterval(this.gc.bind(this), this.config.gcInterval);

this.state = STATE.RUNNING;
this.emit('start');
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.rollback"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>rollback (connId, keys)](#apidoc.element.memdb-server.shard.prototype.rollback)
- description and source-code
```javascript
rollback = function (connId, keys){
    // Skip state check

    if(!Array.isArray(keys)){
        keys = [keys];
    }

    var self = this;
    keys.forEach(function(key){
        self._doc(key).rollback(connId);
    });

    this.logger.debug('[conn:%s] rollback(%j)', connId, keys);
}
```
- example usage
```shell
...
    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
};

var proto = Connection.prototype;

proto.close = function(){
    if(this.isDirty()){
        this.rollback();
    }
    for(var name in this.collections){
        this.collections[name].close();
    }
};

consts.collMethods.forEach(function(method){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.start"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>start ()](#apidoc.element.memdb-server.shard.prototype.start)
- description and source-code
```javascript
start = function (){
    this._ensureState(STATE.INITED);
    this.state = STATE.STARTING;

    return P.bind(this)
    .then(function(){
        return this.backendLocker.start();
    })
    .then(function(){
        return this.backend.start();
    })
    .then(function(){
        if(!this.config.disableSlave){
            return this.slave.start();
        }
    })
    .then(function(){
        if(!this.config.disableSlave){
            return this.restoreFromSlave();
        }
    })
    .then(function(){
        this.gcInterval = setInterval(this.gc.bind(this), this.config.gcInterval);

        this.state = STATE.RUNNING;
        this.emit('start');
        this.logger.info('shard started');
    });
}
```
- example usage
```shell
...

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
var self = this;
return this.shard.start()
.then(function(){
    self.logger.info('database started');
});
};

proto.stop = function(force){
var self = this;
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.stop"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>stop ()](#apidoc.element.memdb-server.shard.prototype.stop)
- description and source-code
```javascript
stop = function (){
    this._ensureState(STATE.RUNNING);

    // This will prevent any further requests
    // All commited data will be saved, while uncommited data will be rolled back
    this.state = STATE.STOPING;

    clearInterval(this.gcInterval);

    return P.bind(this)
    .then(function(){
        // Wait for all running task finish
        return this.taskLock.acquire('', function(){});
    })
    .then(function(){
        this.logger.debug('all running tasks finished');

        // Wait for all commit process finish
        var deferred = P.defer();
        var self = this;
        var check = function(){
            if(self.commitingCount <= 0){
                deferred.resolve();
            }
            else{
                setTimeout(check, 200);
            }
        };
        check();
        return deferred.promise;
    })
    .then(function(){
        this.logger.debug('all commit processes finished');
        // WARN: Make sure all connections are closed now

        var self = this;
        return P.mapLimit(Object.keys(this.docs), function(key){
            return self.keyLock.acquire(key, function(){
                return self._unload(key);
            })
            .catch(function(e){
                self.logger.error(e.stack);
            });
        });
    })
    .then(function(){
        this.logger.debug('all docs unloaded');

        this.loadCounter.stop();
        this.unloadCounter.stop();
        this.persistentCounter.stop();

        if(!this.config.disableSlave){
            return this.slave.stop();
        }
    })
    .then(function(){
        return this.backend.stop();
    })
    .then(function(){
        return this.backendLocker.stop();
    })
    .then(function(){
        return this.autoconn.close();
    })
    .then(function(){
        this.state = STATE.STOPED;
        this.emit('stop');
        this.logger.info('shard stoped');
    });
}
```
- example usage
```shell
...
self.logger.info('database started');
    });
};

proto.stop = function(force){
    var self = this;

    this.opsCounter.stop();
    this.tpsCounter.stop();

    return P.try(function(){
// Make sure no new request come anymore

// Wait for all operations finish
return utils.waitUntil(function(){
...
```

#### <a name="apidoc.element.memdb-server.shard.prototype.update"></a>[function <span class="apidocSignatureSpan">memdb-server.shard.prototype.</span>update (connId, key, doc, opts)](#apidoc.element.memdb-server.shard.prototype.update)
- description and source-code
```javascript
update = function (connId, key, doc, opts){
    this._ensureState(STATE.RUNNING);

    // Since lock is called before, so doc is loaded for sure
    var ret = this._doc(key).update(connId, doc, opts);

    this.logger.debug('[conn:%s] update(%s, %j, %j) => %s', connId, key, doc, opts, ret);
    return ret;
}
```
- example usage
```shell
...
};

proto._updateById = function(id, modifier, opts){
    id = this._checkId(id);

    var self = this;
    return P.try(function(){
        return self.shard.update(self.conn._id, self._key(id), modifier, opts);
    })
    .then(function(){
        return self._finishIndexTasks(id);
    });
};

proto.remove = function(query, opts){
...
```



# <a name="apidoc.module.memdb-server.slave"></a>[module memdb-server.slave](#apidoc.module.memdb-server.slave)

#### <a name="apidoc.element.memdb-server.slave.slave"></a>[function <span class="apidocSignatureSpan">memdb-server.</span>slave (opts)](#apidoc.element.memdb-server.slave.slave)
- description and source-code
```javascript
slave = function (opts){
    opts = opts || {};

    this.shardId = opts.shardId;

    this.config = {
        host : opts.host || '127.0.0.1',
        port : opts.port || 6379,
        db : opts.db || 0,
        options : opts.options || {},
    };

    this.client = null;
    this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shardId);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.memdb-server.slave.prototype"></a>[module memdb-server.slave.prototype](#apidoc.module.memdb-server.slave.prototype)

#### <a name="apidoc.element.memdb-server.slave.prototype._extractKey"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>_extractKey (existKey)](#apidoc.element.memdb-server.slave.prototype._extractKey)
- description and source-code
```javascript
_extractKey = function (existKey){
    var words = existKey.split('$');
    return words.slice(2, words.length).join('$');
}
```
- example usage
```shell
...
return P.bind(this)
.then(function(){
    return this.client.keysAsync(this._redisKey('*'));
})
.then(function(keys){
    var self = this;
    return keys.map(function(key){
        return self._extractKey(key);
    });
});
};

proto.clear = function(){
this.logger.debug('slave clear');
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype._redisKey"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>_redisKey (key)](#apidoc.element.memdb-server.slave.prototype._redisKey)
- description and source-code
```javascript
_redisKey = function (key){
    return 'bk$' + this.shardId + '$' + key;
}
```
- example usage
```shell
...
    .then(function(){
        this.logger.info('slave stoped');
    });
};

proto.set = function(key, doc){
    this.logger.debug('slave set %s', key);
    return this.client.setAsync(this._redisKey(key), JSON.stringify(doc));
};

proto.del = function(key){
    this.logger.debug('slave del %s', key);
    return this.client.delAsync(this._redisKey(key));
};
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.clear"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>clear ()](#apidoc.element.memdb-server.slave.prototype.clear)
- description and source-code
```javascript
clear = function (){
    this.logger.debug('slave clear');

    return P.bind(this)
    .then(function(){
        return this.client.keysAsync(this._redisKey('*'));
    })
    .then(function(keys){
        var multi = this.client.multi();
        keys.forEach(function(key){
            multi = multi.del(key);
        });
        return multi.execAsync();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.slave.prototype.del"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>del (key)](#apidoc.element.memdb-server.slave.prototype.del)
- description and source-code
```javascript
del = function (key){
    this.logger.debug('slave del %s', key);
    return this.client.delAsync(this._redisKey(key));
}
```
- example usage
```shell
...
    this.keyLock.acquire(key, function(){
        if(!self.docs[key]){
// possibly timing issue
// or a redundant backend lock is held caused by unsuccessful unload
self.logger.warn('this shard does not hold %s', key);

return P.try(function(){
    return self.slave.del(key);
})
.then(function(){
    return self._unlockBackend(key);
})
.then(function(){
    deferred.resolve(true);
}, function(e){
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.getAllKeys"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>getAllKeys ()](#apidoc.element.memdb-server.slave.prototype.getAllKeys)
- description and source-code
```javascript
getAllKeys = function (){
    this.logger.debug('slave getAllKeys');

    return P.bind(this)
    .then(function(){
        return this.client.keysAsync(this._redisKey('*'));
    })
    .then(function(keys){
        var self = this;
        return keys.map(function(key){
            return self._extractKey(key);
        });
    });
}
```
- example usage
```shell
...
};

proto.restoreFromSlave = function(){
    this._ensureState(STATE.STARTING);

    return P.bind(this)
    .then(function(){
return this.slave.getAllKeys();
    })
    .then(function(keys){
if(keys.length === 0){
    return;
}

this.logger.error('Server not stopped properly, will restore data from slave');
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.getMulti"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>getMulti (keys)](#apidoc.element.memdb-server.slave.prototype.getMulti)
- description and source-code
```javascript
getMulti = function (keys){
    this.logger.debug('slave getMulti');

    var self = this;
    var multi = this.client.multi();
    keys.forEach(function(key){
        multi = multi.get(self._redisKey(key));
    });

    return multi.execAsync()
    .then(function(results){
        var docs = {};
        for(var i in keys){
            var key = keys[i];
            if(!!results[i]){
                docs[key] = JSON.parse(results[i]);
            }
        }
        return docs;
    });
}
```
- example usage
```shell
...
    return;
}

this.logger.error('Server not stopped properly, will restore data from slave');

return P.bind(this)
.then(function(){
    return this.slave.getMulti(keys);
})
.then(function(items){
    var self = this;
    return P.mapLimit(Object.keys(items), function(key){
        return self.keyLock.acquire(key, function(){
            self._addDoc(key, items[key]);
            // persistent all docs to backend
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.set"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>set (key, doc)](#apidoc.element.memdb-server.slave.prototype.set)
- description and source-code
```javascript
set = function (key, doc){
    this.logger.debug('slave set %s', key);
    return this.client.setAsync(this._redisKey(key), JSON.stringify(doc));
}
```
- example usage
```shell
...
            else if(opts.unique){
                throw new Error('Duplicate value for unique key ' + indexKey);
            }

            if(doc.ids.indexOf(item._id) === -1){
                doc.ids.push(item._id);
            }
            return backend.set(indexCollName, indexValue, doc);
        });
    });
})
.then(function(){
    logger.warn('Finish rebuild index %s %s', collName, indexKey);
    return backend.stop();
});
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.setMulti"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>setMulti (docs)](#apidoc.element.memdb-server.slave.prototype.setMulti)
- description and source-code
```javascript
setMulti = function (docs){
    this.logger.debug('slave setMulti');

    var multi = this.client.multi();
    for(var key in docs){
        var doc = docs[key];
        multi = multi.set(this._redisKey(key), JSON.stringify(doc));
    }

    return multi.execAsync();
}
```
- example usage
```shell
...
        return self.slave.set(key, doc);
    }
    else{
        var docs = utils.forceHashMap();
        keys.forEach(function(key){
            docs[key] = self._doc(key)._getChanged();
        });
        return self.slave.setMulti(docs);
    }
    //TODO: possibly loss consistency
    //      if setMulti return failed but actually sccuess
})
.then(function(){
    // Real Commit
    keys.forEach(function(key){
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.start"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>start ()](#apidoc.element.memdb-server.slave.prototype.start)
- description and source-code
```javascript
start = function (){
    return P.bind(this)
    .then(function(){
        this.client = redis.createClient(this.config.port, this.config.host, this.config.options);
        var self = this;
        this.client.on('error', function(err){
            self.logger.error(err.stack);
        });
        return this.client.selectAsync(this.config.db);
    })
    .then(function(){
        this.logger.info('slave started %s:%s:%s', this.config.host, this.config.port, this.config.db);
    });
}
```
- example usage
```shell
...

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
var self = this;
return this.shard.start()
.then(function(){
    self.logger.info('database started');
});
};

proto.stop = function(force){
var self = this;
...
```

#### <a name="apidoc.element.memdb-server.slave.prototype.stop"></a>[function <span class="apidocSignatureSpan">memdb-server.slave.prototype.</span>stop ()](#apidoc.element.memdb-server.slave.prototype.stop)
- description and source-code
```javascript
stop = function (){
    return P.bind(this)
    .then(function(){
        return this.client.quitAsync();
    })
    .then(function(){
        this.logger.info('slave stoped');
    });
}
```
- example usage
```shell
...
self.logger.info('database started');
    });
};

proto.stop = function(force){
    var self = this;

    this.opsCounter.stop();
    this.tpsCounter.stop();

    return P.try(function(){
// Make sure no new request come anymore

// Wait for all operations finish
return utils.waitUntil(function(){
...
```



# <a name="apidoc.module.memdb-server.utils"></a>[module memdb-server.utils](#apidoc.module.memdb-server.utils)

#### <a name="apidoc.element.memdb-server.utils.clone"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>clone (obj)](#apidoc.element.memdb-server.utils.clone)
- description and source-code
```javascript
clone = function (obj){
    return JSON.parse(JSON.stringify(obj));
}
```
- example usage
```shell
...
};

exports.shardConfig = function(shardId){
if(!_config){
    throw new Error('please config.init first');
}

var conf = utils.clone(_config);

var shardConf = conf.shards && conf.shards[shardId];
if(!shardConf){
    throw new Error('shard ' + shardId + ' not configured');
}
// Override shard specific config
for(var key in shardConf){
...
```

#### <a name="apidoc.element.memdb-server.utils.deleteObjPath"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>deleteObjPath (obj, path)](#apidoc.element.memdb-server.utils.deleteObjPath)
- description and source-code
```javascript
deleteObjPath = function (obj, path){
    if(typeof(obj) !== 'object'){
        throw new Error('not object');
    }
    var current = obj;
    var fields = path.split('.');
    var finalField = fields.pop();
    fields.forEach(function(field){
        if(!!current){
            current = current[field];
        }
    });
    if(current !== undefined){
        delete current[finalField];
    }
}
```
- example usage
```shell
...

exports.$unset = function(doc, param){
if(doc === null){
    throw new Error('doc not exist');
}
for(var path in param){
    if(!!param[path]){
        utils.deleteObjPath(doc, path);
    }
}
return doc;
};

exports.$inc = function(doc, param){
if(doc === null){
...
```

#### <a name="apidoc.element.memdb-server.utils.escapeField"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>escapeField (str)](#apidoc.element.memdb-server.utils.escapeField)
- description and source-code
```javascript
escapeField = function (str){
    return str.replace(/\\/g, '\\\\').replace(/\$/g, '\\u0024').replace(/\./g, '\\u002e');
}
```
- example usage
```shell
...
        process.domain = d;
    });
};

// 'index.name.key1.key2'
proto._indexCollectionName = function(indexKey){
    var keys = JSON.parse(indexKey).map(function(key){
        return utils.escapeField(key);
    });
    return 'index.' + utils.escapeField(this.name) + '.' + keys.join('.');
};

proto._key = function(id){
    return this.name + '$' + id;
};
...
```

#### <a name="apidoc.element.memdb-server.utils.extendPromise"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>extendPromise (P)](#apidoc.element.memdb-server.utils.extendPromise)
- description and source-code
```javascript
extendPromise = function (P){
    // This is designed for large array
    // The original map with concurrency option does not release memory
    P.mapLimit = function(items, fn, limit){
        if(!limit){
            limit = 1000;
        }
        var groups = [];
        var group = [];
        items.forEach(function(item){
            group.push(item);
            if(group.length >= limit){
                groups.push(group);
                group = [];
            }
        });
        if(group.length > 0){
            groups.push(group);
        }

        var results = [];
        var promise = P.resolve();
        groups.forEach(function(group){
            promise = promise.then(function(){
                return P.map(group, fn)
                .then(function(ret){
                    ret.forEach(function(item){
                        results.push(item);
                    });
                });
            });
        });
        return promise.thenReturn(results);
    };

    P.mapSeries = function(items, fn){
        var results = [];
        return P.each(items, function(item){
            return P.try(function(){
                return fn(item);
            })
            .then(function(ret){
                results.push(ret);
            });
        })
        .thenReturn(results);
    };
}
```
- example usage
```shell
...
var vm = require('vm');
var AsyncLock = require('async-lock');
var _ = require('lodash');

var DEFAULT_SLOWQUERY = 2000;

// Extend promise
utils.extendPromise(P);

var Database = function(opts){
// clone since we want to modify it
opts = utils.clone(opts) || {};

this.logger = Logger.getLogger('memdb', __filename, 'shard:' + opts.shardId);
...
```

#### <a name="apidoc.element.memdb-server.utils.forceHashMap"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>forceHashMap ()](#apidoc.element.memdb-server.utils.forceHashMap)
- description and source-code
```javascript
forceHashMap = function (){
    var obj = {k : 1};
    delete obj.k;
    return obj;
}
```
- example usage
```shell
...

this.shard = opts.shard;
this.conn = opts.conn;
this.config = opts.config || {};
this.config.maxCollision = this.config.maxCollision || DEFAULT_MAX_COLLISION;

// {indexKey : {indexValue : {id1 : 1, id2 : -1}}}
this.changedIndexes = utils.forceHashMap();

this.pendingIndexTasks = utils.forceHashMap(); //{id, [Promise]}

this.updateIndexEvent = 'updateIndex$' + this.name + '$' + this.conn._id;
this.shard.on(this.updateIndexEvent, this.onUpdateIndex.bind(this));

this.logger = Logger.getLogger('memdb', __filename, 'shard:' + this.shard._id);
...
```

#### <a name="apidoc.element.memdb-server.utils.getObjPath"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>getObjPath (obj, path)](#apidoc.element.memdb-server.utils.getObjPath)
- description and source-code
```javascript
getObjPath = function (obj, path){
    var current = obj;
    path.split('.').forEach(function(field){
        if(!!current){
            current = current[field];
        }
    });
    return current;
}
```
- example usage
```shell
...
};

exports.$inc = function(doc, param){
if(doc === null){
    throw new Error('doc not exist');
}
for(var path in param){
    var value = utils.getObjPath(doc, path);
    var delta = param[path];
    if(value === undefined){
        value = 0;
    }
    if(typeof(value) !== 'number' || typeof(delta) !== 'number'){
        throw new Error('$inc non-number');
    }
...
```

#### <a name="apidoc.element.memdb-server.utils.hrtimer"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>hrtimer (autoStart)](#apidoc.element.memdb-server.utils.hrtimer)
- description and source-code
```javascript
hrtimer = function (autoStart){
    var total = 0;
    var starttime = null;

    var timer = {
        start : function(){
            if(starttime){
                return;
            }
            starttime = process.hrtime();
        },
        stop : function(){
            if(!starttime){
                return;
            }
            var timedelta = process.hrtime(starttime);
            total += timedelta[0] * 1000 + timedelta[1] / 1000000;
            return total;
        },
        total : function(){
            return total; //in ms
        },
    };

    if(autoStart){
        timer.start();
    }
    return timer;
}
```
- example usage
```shell
...
        if(method === 'commit' || method === 'rollback'){
self.tpsCounter.inc();
        }
        else{
self.opsCounter.inc();
        }

        var hrtimer = utils.hrtimer(true);
        var conn = null;

        return P.try(function(){
conn = self.getConnection(connId);

var func = conn[method];
if(typeof(func) !== 'function'){
...
```

#### <a name="apidoc.element.memdb-server.utils.isDict"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>isDict (obj)](#apidoc.element.memdb-server.utils.isDict)
- description and source-code
```javascript
isDict = function (obj){
    return typeof(obj) === 'object' && obj !== null && !Array.isArray(obj);
}
```
- example usage
```shell
...
var self = this;
return P.mapSeries(docs, function(doc){ //disable concurrent to avoid race condition
    return self._insertById(doc && doc._id, doc);
});
};

proto._insertById = function(id, doc){
if(!utils.isDict(doc)){
    throw new Error('doc must be a dictionary');
}

if(id === null || id === undefined){
    id = utils.uuid();
}
id = this._checkId(id);
...
```

#### <a name="apidoc.element.memdb-server.utils.isEmpty"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>isEmpty (obj)](#apidoc.element.memdb-server.utils.isEmpty)
- description and source-code
```javascript
isEmpty = function (obj){
    for(var key in obj){
        return false;
    }
    return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.utils.mongoForEach"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>mongoForEach (itor, func)](#apidoc.element.memdb-server.utils.mongoForEach)
- description and source-code
```javascript
mongoForEach = function (itor, func){
    var deferred = P.defer();

    var next = function(err){
        if(err){
            return deferred.reject(err);
        }
        // async iterator with .next(cb)
        itor.next(function(err, value){
            if(err){
                return deferred.reject(err);
            }
            if(value === null){
                return deferred.resolve();
            }
            P.try(function(){
                return func(value);
            })
            .nodeify(next);
        });
    };
    next();

    return deferred.promise;
}
```
- example usage
```shell
...
    .then(function(){
        return backend.drop(indexCollName);
    })
    .then(function(){
        return backend.getAll(collName);
    })
    .then(function(itor){
        return utils.mongoForEach(itor, function(item){
var indexValue = Document.prototype._getIndexValue.call({_getChanged : function(){return item;}}, indexKey, opts);
if(!indexValue){
    return;
}

return P.try(function(){
    return backend.get(indexCollName, indexValue);
...
```

#### <a name="apidoc.element.memdb-server.utils.rateCounter"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>rateCounter (opts)](#apidoc.element.memdb-server.utils.rateCounter)
- description and source-code
```javascript
rateCounter = function (opts){
    opts = opts || {};
    var perserveSeconds = opts.perserveSeconds || 3600;
    var sampleSeconds = opts.sampleSeconds || 5;

    var counts = {};
    var cleanInterval = null;

    var getCurrentSlot = function(){
        return Math.floor(Date.now() / 1000 / sampleSeconds);
    };

    var beginSlot = getCurrentSlot();

    var counter = {
        inc : function(){
            var slotNow = getCurrentSlot();
            if(!counts.hasOwnProperty(slotNow)){
                counts[slotNow] = 0;
            }
            counts[slotNow]++;
        },

        reset : function(){
            counts = {};
            beginSlot = getCurrentSlot();
        },

        clean : function(){
            var slotNow = getCurrentSlot();
            Object.keys(counts).forEach(function(slot){
                if(slot < slotNow - Math.floor(perserveSeconds / sampleSeconds)){
                    delete counts[slot];
                }
            });
        },

        rate : function(lastSeconds){
            var slotNow = getCurrentSlot();
            var total = 0;
            var startSlot = slotNow - Math.floor(lastSeconds / sampleSeconds);
            if(startSlot < beginSlot){
                startSlot = beginSlot;
            }
            for(var slot = startSlot; slot < slotNow; slot++){
                total += counts[slot] || 0;
            }
            return total / ((slotNow - startSlot) * sampleSeconds);
        },

        stop : function(){
            clearInterval(cleanInterval);
        },

        counts : function(){
            return counts;
        }
    };

    cleanInterval = setInterval(function(){
        counter.clean();
    }, sampleSeconds * 1000);

    return counter;
}
```
- example usage
```shell
...
this.logger = Logger.getLogger('memdb', __filename, 'shard:' + opts.shardId);

this.connections = utils.forceHashMap();
this.connectionLock = new AsyncLock({Promise : P});

this.dbWrappers = utils.forceHashMap(); //{connId : dbWrapper}

this.opsCounter = utils.rateCounter();
this.tpsCounter = utils.rateCounter();

opts.slowQuery = opts.slowQuery || DEFAULT_SLOWQUERY;

// Parse index config
opts.collections = opts.collections || {};
...
```

#### <a name="apidoc.element.memdb-server.utils.remoteExec"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>remoteExec (ip, cmd, opts)](#apidoc.element.memdb-server.utils.remoteExec)
- description and source-code
```javascript
remoteExec = function (ip, cmd, opts){
    ip = ip || '127.0.0.1';
    opts = opts || {};
    var user = opts.user || process.env.USER;
    var successCodes = opts.successCodes || [0];

    var child = null;
    // localhost with current user
    if((ip === '127.0.0.1' || ip.toLowerCase() === 'localhost') && user === process.env.USER){
        child = child_process.spawn('bash', ['-c', cmd]);
    }
    // run remote via ssh
    else{
        child = child_process.spawn('ssh', ['-o StrictHostKeyChecking=no', user + '@' + ip, 'bash -c \'' + cmd + '\'']);
    }

    var deferred = P.defer();
    var stdout = '', stderr = '';
    child.stdout.on('data', function(data){
        stdout += data;
    });
    child.stderr.on('data', function(data){
        stderr += data;
    });
    child.on('exit', function(code, signal){
        if(successCodes.indexOf(code) !== -1){
            deferred.resolve(stdout);
        }
        else{
            deferred.reject(new Error(util.format('remoteExec return code %s on %s@%s - %s\n%s', code, user, ip, cmd, stderr)));
        }
    });
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.utils.setObjPath"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>setObjPath (obj, path, value)](#apidoc.element.memdb-server.utils.setObjPath)
- description and source-code
```javascript
setObjPath = function (obj, path, value){
    if(typeof(obj) !== 'object'){
        throw new Error('not object');
    }
    var current = obj;
    var fields = path.split('.');
    var finalField = fields.pop();
    fields.forEach(function(field){
        if(!current.hasOwnProperty(field)){
            current[field] = {};
        }
        current = current[field];
        if(typeof(current) !== 'object'){
            throw new Error('field ' + path + ' exists and not a object');
        }
    });
    current[finalField] = value;
}
```
- example usage
```shell
...

exports.$set = function(doc, param){
if(doc === null){
    throw new Error('doc not exist');
}
for(var path in param){
    verifyDoc(param[path]);
    utils.setObjPath(doc, path, param[path]);
}
return doc;
};

exports.$unset = function(doc, param){
if(doc === null){
    throw new Error('doc not exist');
...
```

#### <a name="apidoc.element.memdb-server.utils.timeCounter"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>timeCounter ()](#apidoc.element.memdb-server.utils.timeCounter)
- description and source-code
```javascript
timeCounter = function (){
    var counts = {};

    return {
        add : function(name, time){
            if(!counts.hasOwnProperty(name)){
                counts[name] = [0, 0, 0]; // total, count, average
            }
            var count = counts[name];
            count[0] += time;
            count[1]++;
            count[2] = count[0] / count[1];
        },
        reset : function(){
            counts = {};
        },
        getCounts : function(){
            return counts;
        },
    };
}
```
- example usage
```shell
...

    this.logger.info('parsed opts: %j', opts);

    this.shard = new Shard(opts);

    this.config = opts;

    this.timeCounter = utils.timeCounter();
};

util.inherits(Database, EventEmitter);

var proto = Database.prototype;

proto.start = function(){
...
```

#### <a name="apidoc.element.memdb-server.utils.unescapeField"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>unescapeField (str)](#apidoc.element.memdb-server.utils.unescapeField)
- description and source-code
```javascript
unescapeField = function (str){
    return str.replace(/\\u002e/g, '.').replace(/\\u0024/g, '$').replace(/\\\\/g, '\\');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.memdb-server.utils.uuid"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>uuid ()](#apidoc.element.memdb-server.utils.uuid)
- description and source-code
```javascript
uuid = function (){
    return uuid.v4();
}
```
- example usage
```shell
...

proto._insertById = function(id, doc){
if(!utils.isDict(doc)){
    throw new Error('doc must be a dictionary');
}

if(id === null || id === undefined){
    id = utils.uuid();
}
id = this._checkId(id);
doc._id = id;

var self = this;
return P.try(function(){
    return self.lock(id);
...
```

#### <a name="apidoc.element.memdb-server.utils.waitUntil"></a>[function <span class="apidocSignatureSpan">memdb-server.utils.</span>waitUntil (fn, checkInterval)](#apidoc.element.memdb-server.utils.waitUntil)
- description and source-code
```javascript
waitUntil = function (fn, checkInterval){
    if(!checkInterval){
        checkInterval = 100;
    }

    var deferred = P.defer();
    var check = function(){
        if(fn()){
            deferred.resolve();
        }
        else{
            setTimeout(check, checkInterval);
        }
    };
    check();

    return deferred.promise;
}
```
- example usage
```shell
...
this.opsCounter.stop();
this.tpsCounter.stop();

return P.try(function(){
    // Make sure no new request come anymore

    // Wait for all operations finish
    return utils.waitUntil(function(){
        return !self.connectionLock.isBusy();
    });
})
.then(function(){
    self.logger.debug('all requests finished');
    return self.shard.stop(force);
})
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
