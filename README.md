# api documentation for  [archiver (v1.3.0)](https://github.com/archiverjs/node-archiver)  [![npm package](https://img.shields.io/npm/v/npmdoc-archiver.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-archiver) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-archiver.svg)](https://travis-ci.org/npmdoc/node-npmdoc-archiver)
#### a streaming interface for archive generation

[![NPM](https://nodei.co/npm/archiver.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/archiver)

[![apidoc](https://npmdoc.github.io/node-npmdoc-archiver/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-archiver/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-archiver/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-archiver/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Chris Talkington",
        "url": "http://christalkington.com/"
    },
    "bugs": {
        "url": "https://github.com/archiverjs/node-archiver/issues"
    },
    "dependencies": {
        "archiver-utils": "^1.3.0",
        "async": "^2.0.0",
        "buffer-crc32": "^0.2.1",
        "glob": "^7.0.0",
        "lodash": "^4.8.0",
        "readable-stream": "^2.0.0",
        "tar-stream": "^1.5.0",
        "walkdir": "^0.0.11",
        "zip-stream": "^1.1.0"
    },
    "description": "a streaming interface for archive generation",
    "devDependencies": {
        "archiver-jsdoc-theme": "^1.0.0",
        "chai": "^3.4.0",
        "jsdoc": "~3.4.0",
        "mkdirp": "^0.5.0",
        "mocha": "^3.1.1",
        "rimraf": "^2.4.2",
        "stream-bench": "^0.1.2",
        "tar": "^2.2.1",
        "yauzl": "^2.3.1"
    },
    "directories": {},
    "dist": {
        "shasum": "4f2194d6d8f99df3f531e6881f14f15d55faaf22",
        "tarball": "https://registry.npmjs.org/archiver/-/archiver-1.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "files": [
        "index.js",
        "lib"
    ],
    "gitHead": "14e63cdc327e7630420f15acccbfbd598e3a3c40",
    "homepage": "https://github.com/archiverjs/node-archiver",
    "keywords": [
        "archive",
        "archiver",
        "stream",
        "zip",
        "tar"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "ctalkington"
        }
    ],
    "name": "archiver",
    "optionalDependencies": {},
    "publishConfig": {
        "registry": "https://registry.npmjs.org/"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/archiverjs/node-archiver.git"
    },
    "scripts": {
        "bench": "node benchmark/simple/pack-zip.js",
        "jsdoc": "jsdoc -c jsdoc.json README.md",
        "test": "mocha --reporter dot"
    },
    "version": "1.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module archiver](#apidoc.module.archiver)
1.  [function <span class="apidocSignatureSpan"></span>archiver (format, options)](#apidoc.element.archiver.archiver)
1.  [function <span class="apidocSignatureSpan">archiver.</span>core (format, options)](#apidoc.element.archiver.core)
1.  [function <span class="apidocSignatureSpan">archiver.</span>create (format, options)](#apidoc.element.archiver.create)
1.  [function <span class="apidocSignatureSpan">archiver.</span>registerFormat (format, module)](#apidoc.element.archiver.registerFormat)
1.  [function <span class="apidocSignatureSpan">archiver.</span>toString ()](#apidoc.element.archiver.toString)
1.  object <span class="apidocSignatureSpan">archiver.</span>core.prototype

#### [module archiver.core](#apidoc.module.archiver.core)
1.  [function <span class="apidocSignatureSpan">archiver.</span>core (format, options)](#apidoc.element.archiver.core.core)
1.  [function <span class="apidocSignatureSpan">archiver.core.</span>super_ (options)](#apidoc.element.archiver.core.super_)

#### [module archiver.core.prototype](#apidoc.module.archiver.core.prototype)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_abort ()](#apidoc.element.archiver.core.prototype._abort)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_append (filepath, data)](#apidoc.element.archiver.core.prototype._append)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_finalize ()](#apidoc.element.archiver.core.prototype._finalize)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_maybeFinalize ()](#apidoc.element.archiver.core.prototype._maybeFinalize)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleAppend (source, data, callback)](#apidoc.element.archiver.core.prototype._moduleAppend)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleFinalize ()](#apidoc.element.archiver.core.prototype._moduleFinalize)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_modulePipe ()](#apidoc.element.archiver.core.prototype._modulePipe)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleSupports (key)](#apidoc.element.archiver.core.prototype._moduleSupports)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleUnpipe ()](#apidoc.element.archiver.core.prototype._moduleUnpipe)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_normalizeEntryData (data, stats)](#apidoc.element.archiver.core.prototype._normalizeEntryData)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onModuleError (err)](#apidoc.element.archiver.core.prototype._onModuleError)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onQueueDrain ()](#apidoc.element.archiver.core.prototype._onQueueDrain)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onQueueTask (task, callback)](#apidoc.element.archiver.core.prototype._onQueueTask)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onStatQueueTask (task, callback)](#apidoc.element.archiver.core.prototype._onStatQueueTask)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_shutdown ()](#apidoc.element.archiver.core.prototype._shutdown)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_transform (chunk, encoding, callback)](#apidoc.element.archiver.core.prototype._transform)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_updateQueueTaskWithStats (task, stats)](#apidoc.element.archiver.core.prototype._updateQueueTaskWithStats)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>abort ()](#apidoc.element.archiver.core.prototype.abort)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>append (source, data)](#apidoc.element.archiver.core.prototype.append)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>bulk (mappings)](#apidoc.element.archiver.core.prototype.bulk)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>directory (dirpath, destpath, data)](#apidoc.element.archiver.core.prototype.directory)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>file (filepath, data)](#apidoc.element.archiver.core.prototype.file)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>finalize ()](#apidoc.element.archiver.core.prototype.finalize)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>glob (pattern, options, data)](#apidoc.element.archiver.core.prototype.glob)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>pointer ()](#apidoc.element.archiver.core.prototype.pointer)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>setFormat (format)](#apidoc.element.archiver.core.prototype.setFormat)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>setModule (module)](#apidoc.element.archiver.core.prototype.setModule)
1.  [function <span class="apidocSignatureSpan">archiver.core.prototype.</span>use (plugin)](#apidoc.element.archiver.core.prototype.use)



# <a name="apidoc.module.archiver"></a>[module archiver](#apidoc.module.archiver)

#### <a name="apidoc.element.archiver.archiver"></a>[function <span class="apidocSignatureSpan"></span>archiver (format, options)](#apidoc.element.archiver.archiver)
- description and source-code
```javascript
archiver = function (format, options) {
  return vending.create(format, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core"></a>[function <span class="apidocSignatureSpan">archiver.</span>core (format, options)](#apidoc.element.archiver.core)
- description and source-code
```javascript
core = function (format, options) {
  if (!(this instanceof Archiver)) {
    return new Archiver(format, options);
  }

  if (typeof format !== 'string') {
    options = format;
    format = 'zip';
  }

  options = this.options = util.defaults(options, {
    highWaterMark: 1024 * 1024,
    statConcurrency: 4
  });

  Transform.call(this, options);

  this._entries = [];
  this._format = false;
  this._module = false;
  this._pending = 0;
  this._pointer = 0;

  this._queue = async.queue(this._onQueueTask.bind(this), 1);
  this._queue.drain = this._onQueueDrain.bind(this);

  this._statQueue = async.queue(this._onStatQueueTask.bind(this), options.statConcurrency);

  this._state = {
    aborted: false,
    finalize: false,
    finalizing: false,
    finalized: false,
    modulePiped: false
  };

  this._streams = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.create"></a>[function <span class="apidocSignatureSpan">archiver.</span>create (format, options)](#apidoc.element.archiver.create)
- description and source-code
```javascript
create = function (format, options) {
  if (formats[format]) {
    var instance = new Archiver(format, options);
    instance.setFormat(format);
    instance.setModule(new formats[format](options));

    return instance;
  } else {
    throw new Error('create(' + format + '): format not registered');
  }
}
```
- example usage
```shell
...
*
* @constructor
* @param  {String} format The archive format to use.
* @param  {Object} options See [Archiver]{@link Archiver}
* @return {Archiver}
*/
var vending = function(format, options) {
 return vending.create(format, options);
};

/**
* Creates a new Archiver instance.
*
* @param  {String} format The archive format to use.
* @param  {Object} options See [Archiver]{@link Archiver}
...
```

#### <a name="apidoc.element.archiver.registerFormat"></a>[function <span class="apidocSignatureSpan">archiver.</span>registerFormat (format, module)](#apidoc.element.archiver.registerFormat)
- description and source-code
```javascript
registerFormat = function (format, module) {
  if (formats[format]) {
    throw new Error('register(' + format + '): format already registered');
  }

  if (typeof module !== 'function') {
    throw new Error('register(' + format + '): format module invalid');
  }

  if (typeof module.prototype.append !== 'function' || typeof module.prototype.finalize !== 'function') {
    throw new Error('register(' + format + '): format module missing methods');
  }

  formats[format] = module;
}
```
- example usage
```shell
...
  if (typeof module.prototype.append !== 'function' || typeof module.prototype.finalize !== 'function') {
    throw new Error('register(' + format + '): format module missing methods');
  }

  formats[format] = module;
};

vending.registerFormat('zip', require('./lib/plugins/zip'));
vending.registerFormat('tar', require('./lib/plugins/tar'));
vending.registerFormat('json', require('./lib/plugins/json'));

module.exports = vending;
...
```

#### <a name="apidoc.element.archiver.toString"></a>[function <span class="apidocSignatureSpan">archiver.</span>toString ()](#apidoc.element.archiver.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.archiver.core"></a>[module archiver.core](#apidoc.module.archiver.core)

#### <a name="apidoc.element.archiver.core.core"></a>[function <span class="apidocSignatureSpan">archiver.</span>core (format, options)](#apidoc.element.archiver.core.core)
- description and source-code
```javascript
core = function (format, options) {
  if (!(this instanceof Archiver)) {
    return new Archiver(format, options);
  }

  if (typeof format !== 'string') {
    options = format;
    format = 'zip';
  }

  options = this.options = util.defaults(options, {
    highWaterMark: 1024 * 1024,
    statConcurrency: 4
  });

  Transform.call(this, options);

  this._entries = [];
  this._format = false;
  this._module = false;
  this._pending = 0;
  this._pointer = 0;

  this._queue = async.queue(this._onQueueTask.bind(this), 1);
  this._queue.drain = this._onQueueDrain.bind(this);

  this._statQueue = async.queue(this._onStatQueueTask.bind(this), options.statConcurrency);

  this._state = {
    aborted: false,
    finalize: false,
    finalizing: false,
    finalized: false,
    modulePiped: false
  };

  this._streams = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.super_"></a>[function <span class="apidocSignatureSpan">archiver.core.</span>super_ (options)](#apidoc.element.archiver.core.super_)
- description and source-code
```javascript
function Transform(options) {
  if (!(this instanceof Transform)) return new Transform(options);

  Duplex.call(this, options);

  this._transformState = new TransformState(this);

  var stream = this;

  // start out asking for a readable event once data is transformed.
  this._readableState.needReadable = true;

  // we have implemented the _read method, and done the other things
  // that Readable wants before the first _read call, so unset the
  // sync guard flag.
  this._readableState.sync = false;

  if (options) {
    if (typeof options.transform === 'function') this._transform = options.transform;

    if (typeof options.flush === 'function') this._flush = options.flush;
  }

  // When the writable side finishes, then flush out anything remaining.
  this.once('prefinish', function () {
    if (typeof this._flush === 'function') this._flush(function (er, data) {
      done(stream, er, data);
    });else done(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.archiver.core.prototype"></a>[module archiver.core.prototype](#apidoc.module.archiver.core.prototype)

#### <a name="apidoc.element.archiver.core.prototype._abort"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_abort ()](#apidoc.element.archiver.core.prototype._abort)
- description and source-code
```javascript
_abort = function () {
  this._state.aborted = true;
  this._queue.kill();
  this._statQueue.kill();

  if (this._queue.idle()) {
    this._shutdown();
  }
}
```
- example usage
```shell
...
* @return {this}
*/
Archiver.prototype.abort = function() {
 if (this._state.aborted || this._state.finalized) {
   return this;
 }

 this._abort();

 return this;
};

/**
* Appends an input source (text string, buffer, or stream) to the instance.
*
...
```

#### <a name="apidoc.element.archiver.core.prototype._append"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_append (filepath, data)](#apidoc.element.archiver.core.prototype._append)
- description and source-code
```javascript
_append = function (filepath, data) {
  data = data || {};

  var task = {
    source: null,
    filepath: filepath
  };

  if (!data.name) {
    data.name = filepath;
  }

  data.sourcePath = filepath;
  task.data = data;

  if (data.stats && data.stats instanceof fs.Stats) {
    task = this._updateQueueTaskWithStats(task, data.stats);
    this._queue.push(task);
  } else {
    this._statQueue.push(task);
  }
}
```
- example usage
```shell
...
          }
        }
      } catch(e) {
        self.emit('error', e);
        return;
      }

      self._append(filepath, entryData);
    });
  });

  return this;
};

/**
...
```

#### <a name="apidoc.element.archiver.core.prototype._finalize"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_finalize ()](#apidoc.element.archiver.core.prototype._finalize)
- description and source-code
```javascript
_finalize = function () {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    return;
  }

  this._state.finalizing = true;

  this._moduleFinalize();

  this._state.finalizing = false;
  this._state.finalized = true;
}
```
- example usage
```shell
...
 */
Archiver.prototype._maybeFinalize = function() {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    return false;
  }

  if (this._state.finalize && this._pending === 0 && this._queue.idle() && this._statQueue.idle()) {
    this._finalize();
    return true;
  }

  return false;
};

/**
...
```

#### <a name="apidoc.element.archiver.core.prototype._maybeFinalize"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_maybeFinalize ()](#apidoc.element.archiver.core.prototype._maybeFinalize)
- description and source-code
```javascript
_maybeFinalize = function () {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    return false;
  }

  if (this._state.finalize && this._pending === 0 && this._queue.idle() && this._statQueue.idle()) {
    this._finalize();
    return true;
  }

  return false;
}
```
- example usage
```shell
...
  }

  this._append(filepath, entryData);
}

function onWalkEnd() {
  this._pending--;
  this._maybeFinalize();
}

function onWalkError(err) {
  this.emit('error', 'directory: ' + err);
}

var walker = walkdir(dirpath);
...
```

#### <a name="apidoc.element.archiver.core.prototype._moduleAppend"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleAppend (source, data, callback)](#apidoc.element.archiver.core.prototype._moduleAppend)
- description and source-code
```javascript
_moduleAppend = function (source, data, callback) {
  if (this._state.aborted) {
    callback();
    return;
  }

  this._module.append(source, data, function(err) {
    this._task = null;

    if (this._state.aborted) {
      this._shutdown();
      return;
    }

    if (err) {
      this.emit('error', err);
      setImmediate(callback);
      return;
    }

    /**
     * Fires when the entry's input has been processed and appended to the archive.
     *
     * @event Archiver#entry
     * @type {EntryData}
     */
    this.emit('entry', data);
    this._entries.push(data);

    setImmediate(callback);
  }.bind(this));
}
```
- example usage
```shell
...
Archiver.prototype._onQueueTask = function(task, callback) {
 if (this._state.finalizing || this._state.finalized || this._state.aborted) {
   callback();
   return;
 }

 this._task = task;
 this._moduleAppend(task.source, task.data, callback);
};

/**
* Performs a file stat and reinjects the task back into the queue.
*
* @private
* @param  {Object} task
...
```

#### <a name="apidoc.element.archiver.core.prototype._moduleFinalize"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleFinalize ()](#apidoc.element.archiver.core.prototype._moduleFinalize)
- description and source-code
```javascript
_moduleFinalize = function () {
  if (typeof this._module.finalize === 'function') {
    this._module.finalize();
  } else if (typeof this._module.end === 'function') {
    this._module.end();
  } else {
    this.emit('error', new Error('module: no suitable finalize/end method found'));
    return;
  }
}
```
- example usage
```shell
...
Archiver.prototype._finalize = function() {
 if (this._state.finalizing || this._state.finalized || this._state.aborted) {
   return;
 }

 this._state.finalizing = true;

 this._moduleFinalize();

 this._state.finalizing = false;
 this._state.finalized = true;
};

/**
* Checks the various state variables to determine if we can 'finalize'.
...
```

#### <a name="apidoc.element.archiver.core.prototype._modulePipe"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_modulePipe ()](#apidoc.element.archiver.core.prototype._modulePipe)
- description and source-code
```javascript
_modulePipe = function () {
  this._module.on('error', this._onModuleError.bind(this));
  this._module.pipe(this);
  this._state.modulePiped = true;
}
```
- example usage
```shell
...

 if (this._state.module) {
   this.emit('error', new Error('module: module already set'));
   return this;
 }

 this._module = module;
 this._modulePipe();

 return this;
};

/**
* Returns the current length (in bytes) that has been emitted.
*
...
```

#### <a name="apidoc.element.archiver.core.prototype._moduleSupports"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleSupports (key)](#apidoc.element.archiver.core.prototype._moduleSupports)
- description and source-code
```javascript
_moduleSupports = function (key) {
  if (!this._module.supports || !this._module.supports[key]) {
    return false;
  }

  return this._module.supports[key];
}
```
- example usage
```shell
...
 * @return {Object}
 */
Archiver.prototype._updateQueueTaskWithStats = function(task, stats) {
if (stats.isFile()) {
  task.data.type = 'file';
  task.data.sourceType = 'stream';
  task.source = util.lazyReadStream(task.filepath);
} else if (stats.isDirectory() && this._moduleSupports('directory')) {
  task.data.name = util.trailingSlashIt(task.data.name);
  task.data.type = 'directory';
  task.data.sourcePath = util.trailingSlashIt(task.filepath);
  task.data.sourceType = 'buffer';
  task.source = new Buffer(0);
} else {
  return task;
...
```

#### <a name="apidoc.element.archiver.core.prototype._moduleUnpipe"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_moduleUnpipe ()](#apidoc.element.archiver.core.prototype._moduleUnpipe)
- description and source-code
```javascript
_moduleUnpipe = function () {
  this._module.unpipe(this);
  this._state.modulePiped = false;
}
```
- example usage
```shell
...
/**
* Unpipes the module and ends our internal stream.
*
* @private
* @return void
*/
Archiver.prototype._shutdown = function() {
 this._moduleUnpipe();
 this.end();
};

/**
* Tracks the bytes emitted by our internal stream.
*
* @private
...
```

#### <a name="apidoc.element.archiver.core.prototype._normalizeEntryData"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_normalizeEntryData (data, stats)](#apidoc.element.archiver.core.prototype._normalizeEntryData)
- description and source-code
```javascript
_normalizeEntryData = function (data, stats) {
  data = util.defaults(data, {
    type: 'file',
    name: null,
    date: null,
    mode: null,
    prefix: null,
    sourcePath: null,
    stats: false
  });

  if (stats && data.stats === false) {
    data.stats = stats;
  }

  var isDir = data.type === 'directory';

  if (data.name) {
    if (typeof data.prefix === 'string' && '' !== data.prefix) {
      data.name = data.prefix + '/' + data.name;
      data.prefix = null;
    }

    data.name = util.sanitizePath(data.name);

    if (data.name.slice(-1) === '/') {
      isDir = true;
      data.type = 'directory';
    } else if (isDir) {
      data.name += '/';
    }
  }

  // 511 === 0777; 493 === 0755; 438 === 0666; 420 === 0644
  if (typeof data.mode === 'number') {
    if (win32) {
      data.mode &= 511;
    } else {
      data.mode &= 4095
    }
  } else if (data.stats && data.mode === null) {
    if (win32) {
      data.mode = data.stats.mode & 511;
    } else {
      data.mode = data.stats.mode & 4095;
    }

    // stat isn't reliable on windows; force 0755 for dir
    if (win32 && isDir) {
      data.mode = 493;
    }
  } else if (data.mode === null) {
    data.mode = isDir ? 493 : 420;
  }

  if (data.stats && data.date === null) {
    data.date = data.stats.mtime;
  } else {
    data.date = util.dateify(data.date);
  }

  return data;
}
```
- example usage
```shell
...
   task.data.sourcePath = util.trailingSlashIt(task.filepath);
   task.data.sourceType = 'buffer';
   task.source = new Buffer(0);
 } else {
   return task;
 }

 task.data = this._normalizeEntryData(task.data, stats);
 return task;
};

/**
* Aborts the archiving process, taking a best-effort approach, by:
*
* - removing any pending queue tasks
...
```

#### <a name="apidoc.element.archiver.core.prototype._onModuleError"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onModuleError (err)](#apidoc.element.archiver.core.prototype._onModuleError)
- description and source-code
```javascript
_onModuleError = function (err) {
  this.emit('error', err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype._onQueueDrain"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onQueueDrain ()](#apidoc.element.archiver.core.prototype._onQueueDrain)
- description and source-code
```javascript
_onQueueDrain = function () {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    return;
  }

  if (this._state.finalize && this._pending === 0 && this._queue.idle() && this._statQueue.idle()) {
    this._finalize();
    return;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype._onQueueTask"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onQueueTask (task, callback)](#apidoc.element.archiver.core.prototype._onQueueTask)
- description and source-code
```javascript
_onQueueTask = function (task, callback) {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    callback();
    return;
  }

  this._task = task;
  this._moduleAppend(task.source, task.data, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype._onStatQueueTask"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_onStatQueueTask (task, callback)](#apidoc.element.archiver.core.prototype._onStatQueueTask)
- description and source-code
```javascript
_onStatQueueTask = function (task, callback) {
  if (this._state.finalizing || this._state.finalized || this._state.aborted) {
    callback();
    return;
  }

  fs.stat(task.filepath, function(err, stats) {
    if (this._state.aborted) {
      setImmediate(callback);
      return;
    }

    if (err) {
      this.emit('error', err);
      setImmediate(callback);
      return;
    }

    task = this._updateQueueTaskWithStats(task, stats);

    if (task.source !== null) {
      this._queue.push(task);
      setImmediate(callback);
    } else {
      this.emit('error', new Error('unsupported entry: ' + task.filepath));
      setImmediate(callback);
      return;
    }
  }.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype._shutdown"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_shutdown ()](#apidoc.element.archiver.core.prototype._shutdown)
- description and source-code
```javascript
_shutdown = function () {
  this._moduleUnpipe();
  this.end();
}
```
- example usage
```shell
...
*/
Archiver.prototype._abort = function() {
 this._state.aborted = true;
 this._queue.kill();
 this._statQueue.kill();

 if (this._queue.idle()) {
   this._shutdown();
 }
};

/**
* Internal helper for appending files.
*
* @private
...
```

#### <a name="apidoc.element.archiver.core.prototype._transform"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_transform (chunk, encoding, callback)](#apidoc.element.archiver.core.prototype._transform)
- description and source-code
```javascript
_transform = function (chunk, encoding, callback) {
  if (chunk) {
    this._pointer += chunk.length;
  }

  callback(null, chunk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype._updateQueueTaskWithStats"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>_updateQueueTaskWithStats (task, stats)](#apidoc.element.archiver.core.prototype._updateQueueTaskWithStats)
- description and source-code
```javascript
_updateQueueTaskWithStats = function (task, stats) {
  if (stats.isFile()) {
    task.data.type = 'file';
    task.data.sourceType = 'stream';
    task.source = util.lazyReadStream(task.filepath);
  } else if (stats.isDirectory() && this._moduleSupports('directory')) {
    task.data.name = util.trailingSlashIt(task.data.name);
    task.data.type = 'directory';
    task.data.sourcePath = util.trailingSlashIt(task.filepath);
    task.data.sourceType = 'buffer';
    task.source = new Buffer(0);
  } else {
    return task;
  }

  task.data = this._normalizeEntryData(task.data, stats);
  return task;
}
```
- example usage
```shell
...
    data.name = filepath;
  }

  data.sourcePath = filepath;
  task.data = data;

  if (data.stats && data.stats instanceof fs.Stats) {
    task = this._updateQueueTaskWithStats(task, data.stats);
    this._queue.push(task);
  } else {
    this._statQueue.push(task);
  }
};

/**
...
```

#### <a name="apidoc.element.archiver.core.prototype.abort"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>abort ()](#apidoc.element.archiver.core.prototype.abort)
- description and source-code
```javascript
abort = function () {
  if (this._state.aborted || this._state.finalized) {
    return this;
  }

  this._abort();

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.archiver.core.prototype.append"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>append (source, data)](#apidoc.element.archiver.core.prototype.append)
- description and source-code
```javascript
append = function (source, data) {
  if (this._state.finalize || this._state.aborted) {
    this.emit('error', new Error('append: queue closed'));
    return this;
  }

  data = this._normalizeEntryData(data);

  if (typeof data.name !== 'string' || data.name.length === 0) {
    this.emit('error', new Error('append: entry name must be a non-empty string value'));
    return this;
  }

  if (data.type === 'directory' && !this._moduleSupports('directory')) {
    this.emit('error', new Error('append: entries of "directory" type not currently supported by this module'));
    return this;
  }

  source = util.normalizeInputSource(source);

  if (Buffer.isBuffer(source)) {
    data.sourceType = 'buffer';
  } else if (util.isStream(source)) {
    data.sourceType = 'stream';
  } else {
    this.emit('error', new Error('append: input source must be valid Stream or Buffer instance'));
    return this;
  }

  this._queue.push({
    data: data,
    source: source
  });

  return this;
}
```
- example usage
```shell
...
});

// pipe archive data to the file
archive.pipe(output);

// append a file from stream
var file1 = __dirname + '/file1.txt';
archive.append(fs.createReadStream(file1), { name: 'file1.txt' });

// append a file from string
archive.append('string cheese!', { name: 'file2.txt' });

// append a file from buffer
var buffer3 = new Buffer('buff it!');
archive.append(buffer3, { name: 'file3.txt' });
...
```

#### <a name="apidoc.element.archiver.core.prototype.bulk"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>bulk (mappings)](#apidoc.element.archiver.core.prototype.bulk)
- description and source-code
```javascript
bulk = function (mappings) {
  if (process._loggedBulkDeprecation === false) {
    process._loggedBulkDeprecation = true;
    var warning = 'Archiver.bulk() deprecated since 0.21.0';
    if (typeof process !== 'undefined' && typeof process.emitWarning !== 'undefined') {
      process.emitWarning(warning, 'DeprecationWarning');
    } else {
      console.warn(warning);
    }
  }

  if (this._state.finalize || this._state.aborted) {
    this.emit('error', new Error('bulk: queue closed'));
    return this;
  }

  if (!Array.isArray(mappings)) {
    mappings = [mappings];
  }

  var self = this;
  var files = util.file.normalizeFilesArray(mappings);

  files.forEach(function(file){
    var isExpandedPair = file.orig.expand || false;
    var data = {};
    var dataFunction = false;

    if (typeof file.data === 'function') {
      dataFunction = file.data;
    } else if (typeof file.data === 'object') {
      data = file.data;
    }

    file.src.forEach(function(filepath) {
      var entryData = _.extend({}, data);
      var entryName = isExpandedPair ? file.dest : (file.dest || '') + '/' + filepath;
      entryData.name = util.sanitizePath(entryName);

      if (entryData.name === '.') {
        return;
      }

      try {
        if (dataFunction) {
          entryData = dataFunction(entryData);

          if (typeof entryData !== 'object') {
            throw new Error('bulk: invalid data returned from custom function');
          }
        }
      } catch(e) {
        self.emit('error', e);
        return;
      }

      self._append(filepath, entryData);
    });
  });

  return this;
}
```
- example usage
```shell
...
 * and [minimatch]{@link https://github.com/isaacs/minimatch#properties} documentation
 * for additional properties.
 * @return {this}
 */
Archiver.prototype.bulk = function(mappings) {
if (process._loggedBulkDeprecation === false) {
  process._loggedBulkDeprecation = true;
  var warning = 'Archiver.bulk() deprecated since 0.21.0';
  if (typeof process !== 'undefined' && typeof process.emitWarning !== 'undefined') {
    process.emitWarning(warning, 'DeprecationWarning');
  } else {
    console.warn(warning);
  }
}
...
```

#### <a name="apidoc.element.archiver.core.prototype.directory"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>directory (dirpath, destpath, data)](#apidoc.element.archiver.core.prototype.directory)
- description and source-code
```javascript
directory = function (dirpath, destpath, data) {
  if (this._state.finalize || this._state.aborted) {
    this.emit('error', new Error('directory: queue closed'));
    return this;
  }

  if (typeof dirpath !== 'string' || dirpath.length === 0) {
    this.emit('error', new Error('directory: dirpath must be a non-empty string value'));
    return this;
  }

  this._pending++;

  if (destpath === false) {
    destpath = '';
  } else if (typeof destpath !== 'string'){
    destpath = dirpath;
  }

  var dataFunction = false;
  if (typeof data === 'function') {
    dataFunction = data;
    data = {};
  } else if (typeof data !== 'object') {
    data = {};
  }

  function onWalkPath(filepath, stats){
    var entryData = _.extend({}, data);
    entryData.name = path.relative(dirpath, filepath).replace(/\\/g, '/');
    entryData.prefix = destpath;
    entryData.stats = stats;

    try {
      if (dataFunction) {
        entryData = dataFunction(entryData);

        if (typeof entryData !== 'object') {
          throw new Error('directory: invalid data returned from custom function');
        }
      }
    } catch(e) {
      this.emit('error', e);
      return;
    }

    this._append(filepath, entryData);
  }

  function onWalkEnd() {
    this._pending--;
    this._maybeFinalize();
  }

  function onWalkError(err) {
    this.emit('error', 'directory: ' + err);
  }

  var walker = walkdir(dirpath);

  walker.on('error', onWalkError.bind(this));
  walker.on('directory', onWalkPath.bind(this));
  walker.on('file', onWalkPath.bind(this));
  walker.on('end', onWalkEnd.bind(this));

  return this;
}
```
- example usage
```shell
...
var buffer3 = new Buffer('buff it!');
archive.append(buffer3, { name: 'file3.txt' });

// append a file
archive.file('file1.txt', { name: 'file4.txt' });

// append files from a directory
archive.directory('subdir/');

// append files from a glob pattern
archive.glob('subdir/*.txt');

// finalize the archive (ie we are done appending files but streams have to finish yet)
archive.finalize();
'''
...
```

#### <a name="apidoc.element.archiver.core.prototype.file"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>file (filepath, data)](#apidoc.element.archiver.core.prototype.file)
- description and source-code
```javascript
file = function (filepath, data) {
  if (this._state.finalize || this._state.aborted) {
    this.emit('error', new Error('file: queue closed'));
    return this;
  }

  if (typeof filepath !== 'string' || filepath.length === 0) {
    this.emit('error', new Error('file: filepath must be a non-empty string value'));
    return this;
  }

  this._append(filepath, data);

  return this;
}
```
- example usage
```shell
...
archive.append('string cheese!', { name: 'file2.txt' });

// append a file from buffer
var buffer3 = new Buffer('buff it!');
archive.append(buffer3, { name: 'file3.txt' });

// append a file
archive.file('file1.txt', { name: 'file4.txt' });

// append files from a directory
archive.directory('subdir/');

// append files from a glob pattern
archive.glob('subdir/*.txt');
...
```

#### <a name="apidoc.element.archiver.core.prototype.finalize"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>finalize ()](#apidoc.element.archiver.core.prototype.finalize)
- description and source-code
```javascript
finalize = function () {
  if (this._state.aborted) {
    this.emit('error', new Error('finalize: archive was aborted'));
    return this;
  }

  if (this._state.finalize) {
    this.emit('error', new Error('finalize: archive already finalizing'));
    return this;
  }

  this._state.finalize = true;

  if (this._pending === 0 && this._queue.idle() && this._statQueue.idle()) {
    this._finalize();
  }

  return this;
}
```
- example usage
```shell
...
// append files from a directory
archive.directory('subdir/');

// append files from a glob pattern
archive.glob('subdir/*.txt');

// finalize the archive (ie we are done appending files but streams have to finish yet)
archive.finalize();
'''

## Formats

Archiver ships with out of the box support for TAR and ZIP archives.

You can register additional formats with 'registerFormat'.
...
```

#### <a name="apidoc.element.archiver.core.prototype.glob"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>glob (pattern, options, data)](#apidoc.element.archiver.core.prototype.glob)
- description and source-code
```javascript
glob = function (pattern, options, data) {
  this._pending++;

  options = util.defaults(options, {
    stat: false
  });

  function onGlobEnd() {
    this._pending--;
    this._maybeFinalize();
  }

  function onGlobError(err) {
    this.emit('error', 'glob: ' + err);
  }

  function onGlobMatch(match){
    entryData = _.extend({}, data);

    if (options.cwd) {
      entryData.name = match;
      match = globber._makeAbs(match);
    }

    this._append(match, entryData);
  }

  var globber = glob(pattern, options);
  globber.on('error', onGlobError.bind(this));
  globber.on('match', onGlobMatch.bind(this));
  globber.on('end', onGlobEnd.bind(this));

  return this;
}
```
- example usage
```shell
...
// append a file
archive.file('file1.txt', { name: 'file4.txt' });

// append files from a directory
archive.directory('subdir/');

// append files from a glob pattern
archive.glob('subdir/*.txt');

// finalize the archive (ie we are done appending files but streams have to finish yet)
archive.finalize();
'''

## Formats
...
```

#### <a name="apidoc.element.archiver.core.prototype.pointer"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>pointer ()](#apidoc.element.archiver.core.prototype.pointer)
- description and source-code
```javascript
pointer = function () {
  return this._pointer;
}
```
- example usage
```shell
...
var output = fs.createWriteStream(__dirname + '/example.zip');
var archive = archiver('zip', {
    store: true // Sets the compression method to STORE.
});

// listen for all archive data to be written
output.on('close', function() {
  console.log(archive.pointer() + ' total bytes');
  console.log('archiver has been finalized and the output file descriptor has closed.');
});

// good practice to catch this error explicitly
archive.on('error', function(err) {
  throw err;
});
...
```

#### <a name="apidoc.element.archiver.core.prototype.setFormat"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>setFormat (format)](#apidoc.element.archiver.core.prototype.setFormat)
- description and source-code
```javascript
setFormat = function (format) {
  if (this._format) {
    this.emit('error', new Error('format: archive format already set'));
    return this;
  }

  this._format = format;

  return this;
}
```
- example usage
```shell
...
 * @param  {String} format The archive format to use.
 * @param  {Object} options See [Archiver]{@link Archiver}
 * @return {Archiver}
 */
vending.create = function(format, options) {
  if (formats[format]) {
    var instance = new Archiver(format, options);
    instance.setFormat(format);
    instance.setModule(new formats[format](options));

    return instance;
  } else {
    throw new Error('create(' + format + '): format not registered');
  }
};
...
```

#### <a name="apidoc.element.archiver.core.prototype.setModule"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>setModule (module)](#apidoc.element.archiver.core.prototype.setModule)
- description and source-code
```javascript
setModule = function (module) {
  if (this._state.aborted) {
    this.emit('error', new Error('module: archive was aborted'));
    return this;
  }

  if (this._state.module) {
    this.emit('error', new Error('module: module already set'));
    return this;
  }

  this._module = module;
  this._modulePipe();

  return this;
}
```
- example usage
```shell
...
 * @param  {Object} options See [Archiver]{@link Archiver}
 * @return {Archiver}
 */
vending.create = function(format, options) {
  if (formats[format]) {
    var instance = new Archiver(format, options);
    instance.setFormat(format);
    instance.setModule(new formats[format](options));

    return instance;
  } else {
    throw new Error('create(' + format + '): format not registered');
  }
};
...
```

#### <a name="apidoc.element.archiver.core.prototype.use"></a>[function <span class="apidocSignatureSpan">archiver.core.prototype.</span>use (plugin)](#apidoc.element.archiver.core.prototype.use)
- description and source-code
```javascript
use = function (plugin) {
  this._streams.push(plugin);
  return this;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
