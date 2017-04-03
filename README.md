# api documentation for  [webpagetest (v0.3.4)](http://github.com/marcelduran/webpagetest-api)  [![npm package](https://img.shields.io/npm/v/npmdoc-webpagetest.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webpagetest) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webpagetest.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webpagetest)
#### WebPageTest API wrapper for NodeJS

[![NPM](https://nodei.co/npm/webpagetest.png?downloads=true)](https://www.npmjs.com/package/webpagetest)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpagetest/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webpagetest_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpagetest/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webpagetest/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webpagetest/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marcel Duran",
        "email": "github@marcelduran.com",
        "url": "http://github.com/marcelduran"
    },
    "bin": {
        "webpagetest": "bin/webpagetest"
    },
    "bugs": {
        "url": "http://github.com/marcelduran/webpagetest-api/issues"
    },
    "dependencies": {
        "commander": "^2.7.1",
        "csv": "^0.4.1",
        "entities": "^1.1.1",
        "mocha": "^2.2.4",
        "xml2js": "^0.4.6"
    },
    "description": "WebPageTest API wrapper for NodeJS",
    "devDependencies": {
        "nock": "~1.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "af0d74c5d44bbc0456601d02e0a4bcd4785b1182",
        "tarball": "https://registry.npmjs.org/webpagetest/-/webpagetest-0.3.4.tgz"
    },
    "engines": {
        "node": ">=0.10.1"
    },
    "gitHead": "55dff8e5c690e4e6e1e5ed5c6a1312340eb280d2",
    "homepage": "http://github.com/marcelduran/webpagetest-api",
    "keywords": [
        "webpagetest",
        "api",
        "performance",
        "test",
        "browser"
    ],
    "license": "MIT",
    "main": "lib/webpagetest.js",
    "maintainers": [
        {
            "name": "marcelduran",
            "email": "marcelduran@gmail.com"
        }
    ],
    "name": "webpagetest",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/marcelduran/webpagetest-api.git"
    },
    "scripts": {
        "test": "./node_modules/mocha/bin/mocha -R spec test/*-test.js"
    },
    "version": "0.3.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webpagetest](#apidoc.module.webpagetest)
1.  [function <span class="apidocSignatureSpan">webpagetest.</span>scriptToString (data)](#apidoc.element.webpagetest.scriptToString)
1.  number <span class="apidocSignatureSpan">webpagetest.</span>defaultListenPort
1.  number <span class="apidocSignatureSpan">webpagetest.</span>defaultWaitResultsPort
1.  object <span class="apidocSignatureSpan">webpagetest.</span>filenames
1.  object <span class="apidocSignatureSpan">webpagetest.</span>helper
1.  object <span class="apidocSignatureSpan">webpagetest.</span>mapping
1.  object <span class="apidocSignatureSpan">webpagetest.</span>paths
1.  object <span class="apidocSignatureSpan">webpagetest.</span>server
1.  string <span class="apidocSignatureSpan">webpagetest.</span>defaultServer

#### [module webpagetest.helper](#apidoc.module.webpagetest.helper)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>WPTAPIError (code, message)](#apidoc.element.webpagetest.helper.WPTAPIError)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>csvParser (data, callback)](#apidoc.element.webpagetest.helper.csvParser)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>csvToObj ()](#apidoc.element.webpagetest.helper.csvToObj)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>dataURI (data)](#apidoc.element.webpagetest.helper.dataURI)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>dryRun (config, path)](#apidoc.element.webpagetest.helper.dryRun)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>localhost (local, defaultPort)](#apidoc.element.webpagetest.helper.localhost)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>netLogParser (data)](#apidoc.element.webpagetest.helper.netLogParser)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>normalizeServer (server)](#apidoc.element.webpagetest.helper.normalizeServer)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>scriptToString (data)](#apidoc.element.webpagetest.helper.scriptToString)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>setQuery (map, options, query)](#apidoc.element.webpagetest.helper.setQuery)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>tsvToObj ()](#apidoc.element.webpagetest.helper.tsvToObj)
1.  [function <span class="apidocSignatureSpan">webpagetest.helper.</span>xmlToObj (xml, callback)](#apidoc.element.webpagetest.helper.xmlToObj)

#### [module webpagetest.mapping](#apidoc.module.webpagetest.mapping)
1.  [function <span class="apidocSignatureSpan">webpagetest.mapping.</span>setOptions (command, query)](#apidoc.element.webpagetest.mapping.setOptions)
1.  object <span class="apidocSignatureSpan">webpagetest.mapping.</span>commands
1.  object <span class="apidocSignatureSpan">webpagetest.mapping.</span>options

#### [module webpagetest.server](#apidoc.module.webpagetest.server)
1.  [function <span class="apidocSignatureSpan">webpagetest.server.</span>listen (local, options, callback)](#apidoc.element.webpagetest.server.listen)



# <a name="apidoc.module.webpagetest"></a>[module webpagetest](#apidoc.module.webpagetest)

#### <a name="apidoc.element.webpagetest.scriptToString"></a>[function <span class="apidocSignatureSpan">webpagetest.</span>scriptToString (data)](#apidoc.element.webpagetest.scriptToString)
- description and source-code
```javascript
function scriptToString(data) {
  var script = [];

  data.forEach(function dataEach(step) {
    var key, value;

    if (typeof step === 'string') {
      script.push(step);
    } else if (typeof step === 'object') {
      key = [Object.keys(step)[0]];
      value = step[key];
      if (value !== undefined && value !== null && value !== '') {
        key = key.concat(value);
      }
      script.push(key.join(TAB));
    }
  });

  return script.join(NEWLINE);
}
```
- example usage
```shell
...

#### Notes

* 'getWaterfallImage' and 'getScreenshotImage' callback function has a third parameter 'info' which is an object with '{type: 'image
/jpeg or png', encoding: 'utf8 or binary'}'
* 'scriptToString' script array values 1-N are optional. e.g:

'''javascript
var script = wpt.scriptToString([
{logData: 0},
{navigate: 'http://foo.com/login'},
{logData: 1},
{setValue: ['name=username', 'johndoe']},
{setValue: ['name=password', '12345']},
{submitForm: 'action=http://foo.com/main'},
'waitForComplete'
...
```



# <a name="apidoc.module.webpagetest.helper"></a>[module webpagetest.helper](#apidoc.module.webpagetest.helper)

#### <a name="apidoc.element.webpagetest.helper.WPTAPIError"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>WPTAPIError (code, message)](#apidoc.element.webpagetest.helper.WPTAPIError)
- description and source-code
```javascript
function WPTAPIError(code, message) {
  this.name = 'WPTAPIError';
  this.code = code || 0;
  this.message = message || this.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.csvParser"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>csvParser (data, callback)](#apidoc.element.webpagetest.helper.csvParser)
- description and source-code
```javascript
function csvParser(data, callback) {
  csv.parse(data.toString(), { columns: true }, function(err, data) {
    if (err) {
      callback.bind(this, err);
    }
    csv.transform(data, function(row) {
      var key, value;
      for (key in row) {
        value = row[key].replace(/<b>|<\/b>/g, '');
        row[key] = entities.decode(value, 2);
      }
      return row;
    }, callback.bind(this));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.csvToObj"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>csvToObj ()](#apidoc.element.webpagetest.helper.csvToObj)
- description and source-code
```javascript
csvToObj = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.dataURI"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>dataURI (data)](#apidoc.element.webpagetest.helper.dataURI)
- description and source-code
```javascript
function dataURI(data) {
  return new Buffer(data || '', 'binary').toString('base64');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.dryRun"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>dryRun (config, path)](#apidoc.element.webpagetest.helper.dryRun)
- description and source-code
```javascript
function dryRun(config, path) {
  path = url.parse(path, true);

  return {
    url: url.format({
      protocol: config.protocol,
      hostname: config.hostname,
      port: (config.port !== 80 && config.port !== 443 ?
        config.port : undefined),
      pathname: path.pathname,
      query: path.query
    })
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.localhost"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>localhost (local, defaultPort)](#apidoc.element.webpagetest.helper.localhost)
- description and source-code
```javascript
function localhost(local, defaultPort) {
  // edge case when hostname:port is not informed via cli
  if (local === undefined || local === 'true') {
    local = [defaultPort];
  } else {
    local = local.toString().split(':');
  }

  return {
    hostname: reIp.test(local[0]) || isNaN(parseInt(local[0], 10)) &&
      local[0] ? local[0] : os.hostname(),
    port: parseInt(local[1] || (!reIp.test(local[0]) && local[0]), 10) ||
      defaultPort
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.netLogParser"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>netLogParser (data)](#apidoc.element.webpagetest.helper.netLogParser)
- description and source-code
```javascript
function netLogParser(data) {
  data = (data || '{}').toString();
  if (data.slice(data.length - 3) === ',\r\n') {
    data = data.slice(0, data.length - 3) + ']}';
  }

  return JSON.parse(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.normalizeServer"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>normalizeServer (server)](#apidoc.element.webpagetest.helper.normalizeServer)
- description and source-code
```javascript
function normalizeServer(server) {
  // normalize hostname
  if (!reProtocol.test(server)) {
    server = 'http://' + server;
  }
  server = url.parse(server);

  return {
    protocol: server.protocol,
    hostname: server.hostname,
    auth: server.auth,
    pathname: server.pathname,
    port: parseInt(server.port, 10) || (server.protocol === 'https:' ? 443 : 80)
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.scriptToString"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>scriptToString (data)](#apidoc.element.webpagetest.helper.scriptToString)
- description and source-code
```javascript
function scriptToString(data) {
  var script = [];

  data.forEach(function dataEach(step) {
    var key, value;

    if (typeof step === 'string') {
      script.push(step);
    } else if (typeof step === 'object') {
      key = [Object.keys(step)[0]];
      value = step[key];
      if (value !== undefined && value !== null && value !== '') {
        key = key.concat(value);
      }
      script.push(key.join(TAB));
    }
  });

  return script.join(NEWLINE);
}
```
- example usage
```shell
...

#### Notes

* 'getWaterfallImage' and 'getScreenshotImage' callback function has a third parameter 'info' which is an object with '{type: 'image
/jpeg or png', encoding: 'utf8 or binary'}'
* 'scriptToString' script array values 1-N are optional. e.g:

'''javascript
var script = wpt.scriptToString([
{logData: 0},
{navigate: 'http://foo.com/login'},
{logData: 1},
{setValue: ['name=username', 'johndoe']},
{setValue: ['name=password', '12345']},
{submitForm: 'action=http://foo.com/main'},
'waitForComplete'
...
```

#### <a name="apidoc.element.webpagetest.helper.setQuery"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>setQuery (map, options, query)](#apidoc.element.webpagetest.helper.setQuery)
- description and source-code
```javascript
function setQuery(map, options, query) {
  query = query || {};
  options = options || {};

  map.options.forEach(function eachOpts(opt) {
    Object.keys(opt).forEach(function eachOpt(key) {
      var param = opt[key],
          name = param.name,
          value = options[name] || options[key];

      if (value !== undefined && param.api) {
        if (param.array) {
          value = [].concat(value).join(' ');
        }
        query[param.api] = param.bool ? param.invert ?
          (value ? 0 : 1) : (value ? 1 : 0) : value;
      }
    });
  });

  return query;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.tsvToObj"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>tsvToObj ()](#apidoc.element.webpagetest.helper.tsvToObj)
- description and source-code
```javascript
tsvToObj = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.webpagetest.helper.xmlToObj"></a>[function <span class="apidocSignatureSpan">webpagetest.helper.</span>xmlToObj (xml, callback)](#apidoc.element.webpagetest.helper.xmlToObj)
- description and source-code
```javascript
function xmlToObj(xml, callback) {
  parser.parseString(xml, function (err, obj) {
    if (err) {
      callback(err);
    }

    normalizeObj(obj);
    callback(undefined, obj);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.webpagetest.mapping"></a>[module webpagetest.mapping](#apidoc.module.webpagetest.mapping)

#### <a name="apidoc.element.webpagetest.mapping.setOptions"></a>[function <span class="apidocSignatureSpan">webpagetest.mapping.</span>setOptions (command, query)](#apidoc.element.webpagetest.mapping.setOptions)
- description and source-code
```javascript
function setOptions(command, query) {
  var count, opts;

  command = commands[command];
  if (!command) {
    return;
  }

  opts = {};
  count = Object.keys(query).length;

  [options.common].concat(command.options).some(function someTypes(options) {
    if (!options) {
      return;
    }
    Object.keys(options).some(function someOptions(key) {
      var valid = options[key].valid;

      if (query.hasOwnProperty(key)) {
        if (options[key].bool) {
          opts[options[key].name] = !reBool.test(query[key]);
        } else if (!valid || (valid && valid.test(query[key]))) {
          opts[options[key].name] = decodeURIComponent(query[key]);
        }
        count -= 1;
      }

      return count === 0;
    });

    return count === 0;
  });

  return opts;
}
```
- example usage
```shell
...
if (method && method !== 'listen') {
  // id, url or script
  if (uri.id) {
    args.push(decodeURIComponent(uri.id));
  }

  // options
  args.push(mapping.setOptions(uri.command, uri.query));

  // callback
  args.push(output.bind(res, callback));

  this[method].apply(this, args);
} else {
  // help
...
```



# <a name="apidoc.module.webpagetest.server"></a>[module webpagetest.server](#apidoc.module.webpagetest.server)

#### <a name="apidoc.element.webpagetest.server.listen"></a>[function <span class="apidocSignatureSpan">webpagetest.server.</span>listen (local, options, callback)](#apidoc.element.webpagetest.server.listen)
- description and source-code
```javascript
function listen(local, options, callback) {
  var server;

  if (fs.existsSync(options.key) && fs.existsSync(options.cert)) {
    server = https.createServer({
      key: fs.readFileSync(path.resolve(process.cwd(), options.key)),
      cert: fs.readFileSync(path.resolve(process.cwd(), options.cert))
    }, route.bind(this));
  } else {
    server = http.createServer(route.bind(this));
  }

  server.on('error', function listenError(err) {
    if (typeof callback === 'function') {
      callback(err);
    }
  }).on('listening', function listenError() {
    if (typeof callback === 'function') {
      callback(undefined, {
        server: server,
        protocol: server instanceof https.Server ? 'https' : 'http',
        hostname: local.hostname,
        port: local.port,
        url: url.format({
          protocol: server instanceof https.Server ? 'https' : 'http',
          hostname: local.hostname,
          port: local.port
        })
      });
    }
  }).listen(local.port);

  buildHelp(url.format(this.config.hostname));

  return server;
}
```
- example usage
```shell
...
#### Notes
* port _8080_ is optional, default port is _7791_
* 'wpt.foo.com' is overriding the default 'www.webpagetest.org' server but can still be overridden with 'server' option
* when _--key_ and _--cert_ are provided, HTTPS is used instead of default HTTP server

### Module
'''javascript
var server = wpt.listen(8080, function(err, data) {
if (err) throw err;
console.log('listening on ' + data.url);
}); // listen on port 8080 (optional), default port is 7791

setTimeout(function() {
server.close(function() {
  console.log('server closed');
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
