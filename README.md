# api documentation for  [mercury (v14.1.0)](https://github.com/Raynos/mercury)  [![npm package](https://img.shields.io/npm/v/npmdoc-mercury.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mercury) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mercury.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mercury)
#### A truly modular frontend framework

[![NPM](https://nodei.co/npm/mercury.png?downloads=true)](https://www.npmjs.com/package/mercury)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mercury/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mercury_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mercury/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mercury/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mercury/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Raynos",
        "email": "raynos2@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/Raynos/mercury/issues",
        "email": "raynos2@gmail.com"
    },
    "contributors": [
        {
            "name": "Raynos"
        },
        {
            "name": "Matt-Esch"
        },
        {
            "name": "neonstalwart"
        },
        {
            "name": "parshap"
        },
        {
            "name": "nrw"
        }
    ],
    "dependencies": {
        "dom-delegator": "^13.0.1",
        "geval": "^2.1.1",
        "http-hash-router": "~1.1.0",
        "main-loop": "^3.1.0",
        "observ": "^0.2.0",
        "observ-array": "^3.1.0",
        "observ-struct": "^5.0.1",
        "observ-varhash": "^1.0.2",
        "value-event": "^5.0.0",
        "vdom-thunk": "^3.0.0",
        "virtual-dom": "^2.1.1",
        "xtend": "^4.0.0"
    },
    "description": "A truly modular frontend framework",
    "devDependencies": {
        "backbone": "^1.1.2",
        "browserify": "^3.38.0",
        "callify": "^0.2.0",
        "coveralls": "^2.11.1",
        "cuid": "^1.2.1",
        "disc": "^1.3.0",
        "function-bind": "^0.1.0",
        "global": "^4.2.1",
        "hash-router": "^0.4.0",
        "immutable": "^3.6.2",
        "indexhtmlify": "^1.2.0",
        "istanbul": "^0.2.16",
        "javascript-editor": "^0.2.1",
        "jquery": "^2.1.4",
        "json-globals": "^0.2.1",
        "lint-trap": "^1.0.1",
        "marked": "^0.3.2",
        "mercury-jsxify": "^0.14.0",
        "min-document": "^2.9.0",
        "next-tick": "^0.2.2",
        "node-hook": "^0.1.0",
        "opn": "^1.0.1",
        "pre-commit": "0.0.7",
        "process": "^0.7.0",
        "raf": "^2.0.1",
        "rcss": "^0.1.5",
        "require-modify": "^0.1.0",
        "rimraf": "^2.2.8",
        "route-map": "^0.1.0",
        "run-browser": "^1.3.1",
        "run-parallel": "^1.0.0",
        "run-series": "^1.0.2",
        "st": "^0.4.1",
        "synthetic-dom-events": "git://github.com/Raynos/synthetic-dom-events.git",
        "tap-spec": "^0.2.0",
        "tape": "^2.13.2",
        "valid-email": "0.0.1",
        "vdom-to-html": "~1.2.5",
        "vdom-virtualize": "0.0.5",
        "vtree-select": "^1.0.1",
        "weakmap-shim": "^1.1.0",
        "zuul": "^1.9.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9789a5b59ac2faa98fe4e9a7d9f7207ff3814acb",
        "tarball": "https://registry.npmjs.org/mercury/-/mercury-14.1.0.tgz"
    },
    "gitHead": "15512903702a4b496a98c3526595ca91acac68db",
    "homepage": "https://github.com/Raynos/mercury",
    "keywords": [
        "framework",
        "frontend",
        "virtual",
        "react",
        "modular",
        "web"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "http://github.com/Raynos/mercury/raw/master/LICENSE"
        }
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "raynos",
            "email": "raynos2@gmail.com"
        },
        {
            "name": "mattesch",
            "email": "matt@mattesch.info"
        }
    ],
    "name": "mercury",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/Raynos/mercury.git"
    },
    "scripts": {
        "browser": "run-browser test/index.js",
        "build": "node bin/build.js",
        "cover": "istanbul cover --report html --print detail ./test/index.js",
        "disc": "browserify index.js --full-paths | discify > disc.html && opn disc.html",
        "dist": "node bin/dist.js",
        "dist-publish": "npm run dist && git add dist/mercury.js && git commit -m 'dist' && npm publish",
        "examples": "node bin/example-server.js",
        "lint": "lint-trap",
        "modules-docs": "node bin/modules-docs.js",
        "phantom": "run-browser test/index.js -b | tap-spec",
        "test": "npm run lint && node test/index.js | tap-spec",
        "travis-test": "npm run phantom && npm run cover && istanbul report lcov && ((cat coverage/lcov.info | coveralls) || exit 0) && zuul -- test/index.js",
        "view-cover": "istanbul report html && opn coverage/index.html"
    },
    "version": "14.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mercury](#apidoc.module.mercury)
1.  [function <span class="apidocSignatureSpan">mercury.</span>BaseEvent (lambda)](#apidoc.element.mercury.BaseEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>Delegator (opts)](#apidoc.element.mercury.Delegator)
1.  [function <span class="apidocSignatureSpan">mercury.</span>app (elem, observ, render, opts)](#apidoc.element.mercury.app)
1.  [function <span class="apidocSignatureSpan">mercury.</span>array (initialList)](#apidoc.element.mercury.array)
1.  [function <span class="apidocSignatureSpan">mercury.</span>changeEvent (fn, data, opts)](#apidoc.element.mercury.changeEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>channels (funcs, context)](#apidoc.element.mercury.channels)
1.  [function <span class="apidocSignatureSpan">mercury.</span>clickEvent (fn, data, opts)](#apidoc.element.mercury.clickEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>computed (observables, lambda)](#apidoc.element.mercury.computed)
1.  [function <span class="apidocSignatureSpan">mercury.</span>create (vnode, opts)](#apidoc.element.mercury.create)
1.  [function <span class="apidocSignatureSpan">mercury.</span>diff (a, b)](#apidoc.element.mercury.diff)
1.  [function <span class="apidocSignatureSpan">mercury.</span>event (fn, data, opts)](#apidoc.element.mercury.event)
1.  [function <span class="apidocSignatureSpan">mercury.</span>h (tagName, properties, children)](#apidoc.element.mercury.h)
1.  [function <span class="apidocSignatureSpan">mercury.</span>handles (funcs, context)](#apidoc.element.mercury.handles)
1.  [function <span class="apidocSignatureSpan">mercury.</span>hash (struct)](#apidoc.element.mercury.hash)
1.  [function <span class="apidocSignatureSpan">mercury.</span>input (names)](#apidoc.element.mercury.input)
1.  [function <span class="apidocSignatureSpan">mercury.</span>keyEvent (fn, data, opts)](#apidoc.element.mercury.keyEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>main (initialState, view, opts)](#apidoc.element.mercury.main)
1.  [function <span class="apidocSignatureSpan">mercury.</span>partial (fn)](#apidoc.element.mercury.partial)
1.  [function <span class="apidocSignatureSpan">mercury.</span>patch (rootNode, patches, renderOptions)](#apidoc.element.mercury.patch)
1.  [function <span class="apidocSignatureSpan">mercury.</span>send (fn, data, opts)](#apidoc.element.mercury.send)
1.  [function <span class="apidocSignatureSpan">mercury.</span>sendChange (fn, data, opts)](#apidoc.element.mercury.sendChange)
1.  [function <span class="apidocSignatureSpan">mercury.</span>sendClick (fn, data, opts)](#apidoc.element.mercury.sendClick)
1.  [function <span class="apidocSignatureSpan">mercury.</span>sendKey (fn, data, opts)](#apidoc.element.mercury.sendKey)
1.  [function <span class="apidocSignatureSpan">mercury.</span>sendSubmit (fn, data, opts)](#apidoc.element.mercury.sendSubmit)
1.  [function <span class="apidocSignatureSpan">mercury.</span>sendValue (fn, data, opts)](#apidoc.element.mercury.sendValue)
1.  [function <span class="apidocSignatureSpan">mercury.</span>state (obj)](#apidoc.element.mercury.state)
1.  [function <span class="apidocSignatureSpan">mercury.</span>struct (struct)](#apidoc.element.mercury.struct)
1.  [function <span class="apidocSignatureSpan">mercury.</span>submitEvent (fn, data, opts)](#apidoc.element.mercury.submitEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>value (value)](#apidoc.element.mercury.value)
1.  [function <span class="apidocSignatureSpan">mercury.</span>valueEvent (fn, data, opts)](#apidoc.element.mercury.valueEvent)
1.  [function <span class="apidocSignatureSpan">mercury.</span>varhash (hash, createValue)](#apidoc.element.mercury.varhash)
1.  [function <span class="apidocSignatureSpan">mercury.</span>watch (observable, listener)](#apidoc.element.mercury.watch)

#### [module mercury.Delegator](#apidoc.module.mercury.Delegator)
1.  [function <span class="apidocSignatureSpan">mercury.</span>Delegator (opts)](#apidoc.element.mercury.Delegator.Delegator)
1.  [function <span class="apidocSignatureSpan">mercury.Delegator.</span>allocateHandle (func)](#apidoc.element.mercury.Delegator.allocateHandle)
1.  [function <span class="apidocSignatureSpan">mercury.Delegator.</span>transformHandle (handle, broadcast)](#apidoc.element.mercury.Delegator.transformHandle)



# <a name="apidoc.module.mercury"></a>[module mercury](#apidoc.module.mercury)

#### <a name="apidoc.element.mercury.BaseEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>BaseEvent (lambda)](#apidoc.element.mercury.BaseEvent)
- description and source-code
```javascript
function BaseEvent(lambda) {
    return EventHandler;

    function EventHandler(fn, data, opts) {
        var handler = {
            fn: fn,
            data: data !== undefined ? data : {},
            opts: opts || {},
            handleEvent: handleEvent
        }

        if (fn && fn.type === 'dom-delegator-handle') {
            return Delegator.transformHandle(fn,
                handleLambda.bind(handler))
        }

        return handler;
    }

    function handleLambda(ev, broadcast) {
        if (this.opts.startPropagation && ev.startPropagation) {
            ev.startPropagation();
        }

        return lambda.call(this, ev, broadcast)
    }

    function handleEvent(ev) {
        var self = this

        if (self.opts.startPropagation && ev.startPropagation) {
            ev.startPropagation()
        }

        lambda.call(self, ev, broadcast)

        function broadcast(value) {
            if (typeof self.fn === 'function') {
                self.fn(value)
            } else {
                self.fn.write(value)
            }
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.Delegator"></a>[function <span class="apidocSignatureSpan">mercury.</span>Delegator (opts)](#apidoc.element.mercury.Delegator)
- description and source-code
```javascript
function Delegator(opts) {
    opts = opts || {}
    var document = opts.document || globalDocument

    var cacheKey = document[cacheTokenKey]

    if (!cacheKey) {
        cacheKey =
            document[cacheTokenKey] = cuid()
    }

    var delegator = delegatorCache.delegators[cacheKey]

    if (!delegator) {
        delegator = delegatorCache.delegators[cacheKey] =
            new DOMDelegator(document)
    }

    if (opts.defaultEvents !== false) {
        for (var i = 0; i < commonEvents.length; i++) {
            delegator.listenTo(commonEvents[i])
        }
    }

    return delegator
}
```
- example usage
```shell
...
function app(elem, observ, render, opts) {
if (!elem) {
    throw new Error(
        'Element does not exist. ' +
        'Mercury cannot be initialized.');
}

mercury.Delegator(opts);
var loop = mercury.main(observ(), render, extend({
    diff: mercury.diff,
    create: mercury.create,
    patch: mercury.patch
}, opts));

elem.appendChild(loop.target);
...
```

#### <a name="apidoc.element.mercury.app"></a>[function <span class="apidocSignatureSpan">mercury.</span>app (elem, observ, render, opts)](#apidoc.element.mercury.app)
- description and source-code
```javascript
function app(elem, observ, render, opts) {
    if (!elem) {
        throw new Error(
            'Element does not exist. ' +
            'Mercury cannot be initialized.');
    }

    mercury.Delegator(opts);
    var loop = mercury.main(observ(), render, extend({
        diff: mercury.diff,
        create: mercury.create,
        patch: mercury.patch
    }, opts));

    elem.appendChild(loop.target);

    return observ(loop.update);
}
```
- example usage
```shell
...
           type: 'button',
           value: 'Click me!',
           'ev-click': hg.send(state.channels.clicks)
       })
   ]);
};

hg.app(document.body, App(), App.render);
'''

### Basic Examples

- [count](examples/count.js)
- [shared-state](examples/shared-state.js)
- [bmi-counter](examples/bmi-counter.js)
...
```

#### <a name="apidoc.element.mercury.array"></a>[function <span class="apidocSignatureSpan">mercury.</span>array (initialList)](#apidoc.element.mercury.array)
- description and source-code
```javascript
function ObservArray(initialList) {
    // list is the internal mutable list observ instances that
    // all methods on 'obs' dispatch to.
    var list = initialList
    var initialState = []

    // copy state out of initialList into initialState
    list.forEach(function (observ, index) {
        initialState[index] = typeof observ === "function" ?
            observ() : observ
    })

    var obs = Observ(initialState)
    obs.splice = splice

    // override set and store original for later use
    obs._observSet = obs.set
    obs.set = set

    obs.get = get
    obs.getLength = getLength
    obs.put = put
    obs.transaction = transaction

    // you better not mutate this list directly
    // this is the list of observs instances
    obs._list = list

    var removeListeners = list.map(function (observ) {
        return typeof observ === "function" ?
            addListener(obs, observ) :
            null
    });
    // this is a list of removal functions that must be called
    // when observ instances are removed from 'obs.list'
    // not calling this means we do not GC our observ change
    // listeners. Which causes rage bugs
    obs._removeListeners = removeListeners

    obs._type = "observ-array"
    obs._version = "3"

    return ArrayMethods(obs, list)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.changeEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>changeEvent (fn, data, opts)](#apidoc.element.mercury.changeEvent)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.channels"></a>[function <span class="apidocSignatureSpan">mercury.</span>channels (funcs, context)](#apidoc.element.mercury.channels)
- description and source-code
```javascript
function channels(funcs, context) {
    return Object.keys(funcs).reduce(createHandle, {});

    function createHandle(acc, name) {
        var handle = mercury.Delegator.allocateHandle(
            funcs[name].bind(null, context));

        acc[name] = handle;
        return acc;
    }
}
```
- example usage
```shell
...
        copy.channels = mercury.value(null);
    } else if ($handles) {
        copy.handles = mercury.value(null);
    }

    var observ = mercury.struct(copy);
    if ($channels) {
        observ.channels.set(mercury.channels($channels, observ));
    } else if ($handles) {
        observ.handles.set(mercury.channels($handles, observ));
    }
    return observ;
}

function channels(funcs, context) {
...
```

#### <a name="apidoc.element.mercury.clickEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>clickEvent (fn, data, opts)](#apidoc.element.mercury.clickEvent)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.computed"></a>[function <span class="apidocSignatureSpan">mercury.</span>computed (observables, lambda)](#apidoc.element.mercury.computed)
- description and source-code
```javascript
function computed(observables, lambda) {
    var values = observables.map(function (o) {
        return o()
    })
    var result = Observable(lambda.apply(null, values))

    observables.forEach(function (o, index) {
        o(function (newValue) {
            values[index] = newValue
            result.set(lambda.apply(null, values))
        })
    })

    return result
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.create"></a>[function <span class="apidocSignatureSpan">mercury.</span>create (vnode, opts)](#apidoc.element.mercury.create)
- description and source-code
```javascript
function createElement(vnode, opts) {
    var doc = opts ? opts.document || document : document
    var warn = opts ? opts.warn : null

    vnode = handleThunk(vnode).a

    if (isWidget(vnode)) {
        return vnode.init()
    } else if (isVText(vnode)) {
        return doc.createTextNode(vnode.text)
    } else if (!isVNode(vnode)) {
        if (warn) {
            warn("Item is not a valid virtual dom node", vnode)
        }
        return null
    }

    var node = (vnode.namespace === null) ?
        doc.createElement(vnode.tagName) :
        doc.createElementNS(vnode.namespace, vnode.tagName)

    var props = vnode.properties
    applyProperties(node, props)

    var children = vnode.children

    for (var i = 0; i < children.length; i++) {
        var childNode = createElement(children[i], opts)
        if (childNode) {
            node.appendChild(childNode)
        }
    }

    return node
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.diff"></a>[function <span class="apidocSignatureSpan">mercury.</span>diff (a, b)](#apidoc.element.mercury.diff)
- description and source-code
```javascript
function diff(a, b) {
    var patch = { a: a }
    walk(a, b, patch, 0)
    return patch
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.event"></a>[function <span class="apidocSignatureSpan">mercury.</span>event (fn, data, opts)](#apidoc.element.mercury.event)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.h"></a>[function <span class="apidocSignatureSpan">mercury.</span>h (tagName, properties, children)](#apidoc.element.mercury.h)
- description and source-code
```javascript
function h(tagName, properties, children) {
    var childNodes = [];
    var tag, props, key, namespace;

    if (!children && isChildren(properties)) {
        children = properties;
        props = {};
    }

    props = props || properties || {};
    tag = parseTag(tagName, props);

    // support keys
    if (props.hasOwnProperty('key')) {
        key = props.key;
        props.key = undefined;
    }

    // support namespace
    if (props.hasOwnProperty('namespace')) {
        namespace = props.namespace;
        props.namespace = undefined;
    }

    // fix cursor bug
    if (tag === 'INPUT' &&
        !namespace &&
        props.hasOwnProperty('value') &&
        props.value !== undefined &&
        !isHook(props.value)
    ) {
        props.value = softSetHook(props.value);
    }

    transformProperties(props);

    if (children !== undefined && children !== null) {
        addChild(children, childNodes, tag, props);
    }


    return new VNode(tag, props, childNodes, key, namespace);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.handles"></a>[function <span class="apidocSignatureSpan">mercury.</span>handles (funcs, context)](#apidoc.element.mercury.handles)
- description and source-code
```javascript
function channels(funcs, context) {
    return Object.keys(funcs).reduce(createHandle, {});

    function createHandle(acc, name) {
        var handle = mercury.Delegator.allocateHandle(
            funcs[name].bind(null, context));

        acc[name] = handle;
        return acc;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.hash"></a>[function <span class="apidocSignatureSpan">mercury.</span>hash (struct)](#apidoc.element.mercury.hash)
- description and source-code
```javascript
function ObservStruct(struct) {
    var keys = Object.keys(struct)

    var initialState = {}
    var currentTransaction = NO_TRANSACTION
    var nestedTransaction = NO_TRANSACTION

    keys.forEach(function (key) {
        if (blackList.indexOf(key) !== -1) {
            throw new Error("cannot create an observ-struct " +
                "with a key named '" + key + "'.\n" +
                blackListReasons[key]);
        }

        var observ = struct[key]
        initialState[key] = typeof observ === "function" ?
            observ() : observ
    })

    var obs = Observ(initialState)
    keys.forEach(function (key) {
        var observ = struct[key]
        obs[key] = observ

        if (typeof observ === "function") {
            observ(function (value) {
                if (nestedTransaction === value) {
                    return
                }

                var state = extend(obs())
                state[key] = value
                var diff = {}
                diff[key] = value && value._diff ?
                    value._diff : value

                setNonEnumerable(state, "_diff", diff)
                currentTransaction = state
                obs.set(state)
                currentTransaction = NO_TRANSACTION
            })
        }
    })
    var _set = obs.set
    obs.set = function trackDiff(value) {
        if (currentTransaction === value) {
            return _set(value)
        }

        var newState = extend(value)
        setNonEnumerable(newState, "_diff", value)
        _set(newState)
    }

    obs(function (newState) {
        if (currentTransaction === newState) {
            return
        }

        keys.forEach(function (key) {
            var observ = struct[key]
            var newObservValue = newState[key]

            if (typeof observ === "function" &&
                observ() !== newObservValue
            ) {
                nestedTransaction = newObservValue
                observ.set(newState[key])
                nestedTransaction = NO_TRANSACTION
            }
        })
    })

    obs._type = "observ-struct"
    obs._version = "5"

    return obs
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.input"></a>[function <span class="apidocSignatureSpan">mercury.</span>input (names)](#apidoc.element.mercury.input)
- description and source-code
```javascript
function input(names) {
    if (!names) {
        return SingleEvent();
    }

    return MultipleEvent(names);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.keyEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>keyEvent (fn, data, opts)](#apidoc.element.mercury.keyEvent)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.main"></a>[function <span class="apidocSignatureSpan">mercury.</span>main (initialState, view, opts)](#apidoc.element.mercury.main)
- description and source-code
```javascript
function main(initialState, view, opts) {
    opts = opts || {}

    var currentState = initialState
    var create = opts.create
    var diff = opts.diff
    var patch = opts.patch
    var redrawScheduled = false

    var tree = opts.initialTree || view(currentState, 0);
    var target = opts.target || create(tree, opts)
    var inRenderingTransaction = false

    currentState = null

    var loop = {
        state: initialState,
        target: target,
        update: update
    }
    return loop

    function update(state) {
        if (inRenderingTransaction) {
            throw InvalidUpdateInRender({
                diff: state._diff,
                stringDiff: JSON.stringify(state._diff)
            })
        }

        if (currentState === null && !redrawScheduled) {
            redrawScheduled = true
            raf(redraw)
        }

        currentState = state
        loop.state = state
    }

    function redraw(time) {
        redrawScheduled = false
        if (currentState === null) {
            return
        }

        inRenderingTransaction = true
        var newTree = view(currentState, time)

        if (opts.createOnly) {
            inRenderingTransaction = false
            create(newTree, opts)
        } else {
            var patches = diff(tree, newTree, opts)
            inRenderingTransaction = false
            target = patch(target, patches, opts)
        }

        tree = newTree
        currentState = null
    }
}
```
- example usage
```shell
...
if (!elem) {
    throw new Error(
        'Element does not exist. ' +
        'Mercury cannot be initialized.');
}

mercury.Delegator(opts);
var loop = mercury.main(observ(), render, extend({
    diff: mercury.diff,
    create: mercury.create,
    patch: mercury.patch
}, opts));

elem.appendChild(loop.target);
...
```

#### <a name="apidoc.element.mercury.partial"></a>[function <span class="apidocSignatureSpan">mercury.</span>partial (fn)](#apidoc.element.mercury.partial)
- description and source-code
```javascript
function partial(fn) {
    var args = copyOver(arguments, 1);
    var firstArg = args[0];
    var key;

    var eqArgs = eq || shallowEq;

    if (typeof firstArg === 'object' && firstArg !== null) {
        if ('key' in firstArg) {
            key = firstArg.key;
        } else if ('id' in firstArg) {
            key = firstArg.id;
        }
    }

    return new Thunk(fn, args, key, eqArgs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.patch"></a>[function <span class="apidocSignatureSpan">mercury.</span>patch (rootNode, patches, renderOptions)](#apidoc.element.mercury.patch)
- description and source-code
```javascript
function patch(rootNode, patches, renderOptions) {
    renderOptions = renderOptions || {}
    renderOptions.patch = renderOptions.patch && renderOptions.patch !== patch
        ? renderOptions.patch
        : patchRecursive
    renderOptions.render = renderOptions.render || render

    return renderOptions.patch(rootNode, patches, renderOptions)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.send"></a>[function <span class="apidocSignatureSpan">mercury.</span>send (fn, data, opts)](#apidoc.element.mercury.send)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
...

App.render = function render(state) {
    return h('div.counter', [
        'The state ', h('code', 'clickCount'),
        ' has value: ' + state.value + '.', h('input.button', {
            type: 'button',
            value: 'Click me!',
            'ev-click': hg.send(state.channels.clicks)
        })
    ]);
};

hg.app(document.body, App(), App.render);
'''
...
```

#### <a name="apidoc.element.mercury.sendChange"></a>[function <span class="apidocSignatureSpan">mercury.</span>sendChange (fn, data, opts)](#apidoc.element.mercury.sendChange)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.sendClick"></a>[function <span class="apidocSignatureSpan">mercury.</span>sendClick (fn, data, opts)](#apidoc.element.mercury.sendClick)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.sendKey"></a>[function <span class="apidocSignatureSpan">mercury.</span>sendKey (fn, data, opts)](#apidoc.element.mercury.sendKey)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.sendSubmit"></a>[function <span class="apidocSignatureSpan">mercury.</span>sendSubmit (fn, data, opts)](#apidoc.element.mercury.sendSubmit)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.sendValue"></a>[function <span class="apidocSignatureSpan">mercury.</span>sendValue (fn, data, opts)](#apidoc.element.mercury.sendValue)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.state"></a>[function <span class="apidocSignatureSpan">mercury.</span>state (obj)](#apidoc.element.mercury.state)
- description and source-code
```javascript
function state(obj) {
    var copy = extend(obj);
    var $channels = copy.channels;
    var $handles = copy.handles;

    if ($channels) {
        copy.channels = mercury.value(null);
    } else if ($handles) {
        copy.handles = mercury.value(null);
    }

    var observ = mercury.struct(copy);
    if ($channels) {
        observ.channels.set(mercury.channels($channels, observ));
    } else if ($handles) {
        observ.handles.set(mercury.channels($handles, observ));
    }
    return observ;
}
```
- example usage
```shell
...
'use strict';

var document = require('global/document');
var hg = require('mercury');
var h = require('mercury').h;

function App() {
    return hg.state({
        value: hg.value(0),
        channels: {
            clicks: incrementCounter
        }
    });
}
...
```

#### <a name="apidoc.element.mercury.struct"></a>[function <span class="apidocSignatureSpan">mercury.</span>struct (struct)](#apidoc.element.mercury.struct)
- description and source-code
```javascript
function ObservStruct(struct) {
    var keys = Object.keys(struct)

    var initialState = {}
    var currentTransaction = NO_TRANSACTION
    var nestedTransaction = NO_TRANSACTION

    keys.forEach(function (key) {
        if (blackList.indexOf(key) !== -1) {
            throw new Error("cannot create an observ-struct " +
                "with a key named '" + key + "'.\n" +
                blackListReasons[key]);
        }

        var observ = struct[key]
        initialState[key] = typeof observ === "function" ?
            observ() : observ
    })

    var obs = Observ(initialState)
    keys.forEach(function (key) {
        var observ = struct[key]
        obs[key] = observ

        if (typeof observ === "function") {
            observ(function (value) {
                if (nestedTransaction === value) {
                    return
                }

                var state = extend(obs())
                state[key] = value
                var diff = {}
                diff[key] = value && value._diff ?
                    value._diff : value

                setNonEnumerable(state, "_diff", diff)
                currentTransaction = state
                obs.set(state)
                currentTransaction = NO_TRANSACTION
            })
        }
    })
    var _set = obs.set
    obs.set = function trackDiff(value) {
        if (currentTransaction === value) {
            return _set(value)
        }

        var newState = extend(value)
        setNonEnumerable(newState, "_diff", value)
        _set(newState)
    }

    obs(function (newState) {
        if (currentTransaction === newState) {
            return
        }

        keys.forEach(function (key) {
            var observ = struct[key]
            var newObservValue = newState[key]

            if (typeof observ === "function" &&
                observ() !== newObservValue
            ) {
                nestedTransaction = newObservValue
                observ.set(newState[key])
                nestedTransaction = NO_TRANSACTION
            }
        })
    })

    obs._type = "observ-struct"
    obs._version = "5"

    return obs
}
```
- example usage
```shell
...

    if ($channels) {
        copy.channels = mercury.value(null);
    } else if ($handles) {
        copy.handles = mercury.value(null);
    }

    var observ = mercury.struct(copy);
    if ($channels) {
        observ.channels.set(mercury.channels($channels, observ));
    } else if ($handles) {
        observ.handles.set(mercury.channels($handles, observ));
    }
    return observ;
}
...
```

#### <a name="apidoc.element.mercury.submitEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>submitEvent (fn, data, opts)](#apidoc.element.mercury.submitEvent)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.value"></a>[function <span class="apidocSignatureSpan">mercury.</span>value (value)](#apidoc.element.mercury.value)
- description and source-code
```javascript
function Observable(value) {
    var listeners = []
    value = value === undefined ? null : value

    observable.set = function (v) {
        value = v
        listeners.forEach(function (f) {
            f(v)
        })
    }

    return observable

    function observable(listener) {
        if (!listener) {
            return value
        }

        listeners.push(listener)

        return function remove() {
            listeners.splice(listeners.indexOf(listener), 1)
        }
    }
}
```
- example usage
```shell
...

var document = require('global/document');
var hg = require('mercury');
var h = require('mercury').h;

function App() {
    return hg.state({
        value: hg.value(0),
        channels: {
            clicks: incrementCounter
        }
    });
}

function incrementCounter(state) {
...
```

#### <a name="apidoc.element.mercury.valueEvent"></a>[function <span class="apidocSignatureSpan">mercury.</span>valueEvent (fn, data, opts)](#apidoc.element.mercury.valueEvent)
- description and source-code
```javascript
function EventHandler(fn, data, opts) {
    var handler = {
        fn: fn,
        data: data !== undefined ? data : {},
        opts: opts || {},
        handleEvent: handleEvent
    }

    if (fn && fn.type === 'dom-delegator-handle') {
        return Delegator.transformHandle(fn,
            handleLambda.bind(handler))
    }

    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.varhash"></a>[function <span class="apidocSignatureSpan">mercury.</span>varhash (hash, createValue)](#apidoc.element.mercury.varhash)
- description and source-code
```javascript
function ObservVarhash(hash, createValue) {
  createValue = createValue || function (obj) { return obj }

  var initialState = {}
  var currentTransaction = NO_TRANSACTION
  var nestedTransaction = NO_TRANSACTION

  var obs = Observ(initialState)
  setNonEnumerable(obs, '_removeListeners', {})

  setNonEnumerable(obs, 'get', get.bind(obs))
  setNonEnumerable(obs, 'put', put.bind(obs))
  setNonEnumerable(obs, 'delete', del.bind(obs))

  for (var key in hash) {
    obs[key] = isFn(hash[key]) ? hash[key] : createValue(hash[key], key)

    if (isFn(obs[key])) {
      obs._removeListeners[key] = obs[key](watch(obs, key))
    }
  }

  var _set = obs.set

  obs.set = function trackDiff (value) {
    if (currentTransaction === value) {
      return _set(value)
    }

    var newState = extend(value)
    setNonEnumerable(newState, '_diff', value)

    _set(newState)
  }
  setNonEnumerable(obs, 'set', obs.set)

  var newState = {}
  for (key in hash) {
    var observ = obs[key]
    checkKey(key)
    newState[key] = isFn(observ) ? observ() : observ
  }
  obs.set(newState)

  obs(function (newState) {
    if (currentTransaction === newState) {
      return
    }

    for (var key in hash) {
      var observ = hash[key]
      var newObservValue = newState[key]

      if (isFn(observ) && observ() !== newState[key]) {
        nestedTransaction = newObservValue
        observ.set(newState[key])
        nestedTransaction = NO_TRANSACTION
      }
    }
  })

  function put (key, val) {
    checkKey(key)

    if (val === undefined) {
      throw new Error('cannot varhash.put(key, undefined).')
    }

    var observ = isFn(val) ? val : createValue(val, key)
    var state = extend(this())

    state[key] = isFn(observ) ? observ() : observ

    if (isFn(this._removeListeners[key])) {
      this._removeListeners[key]()
    }

    this._removeListeners[key] = isFn(observ)
      ? observ(watch(this, key)) : null

    setNonEnumerable(state, '_diff', diff(key, state[key]))

    this[key] = observ

    currentTransaction = state
    _set(state)
    currentTransaction = NO_TRANSACTION

    return this
  }

  function del (key) {
    var state = extend(this())
    if (isFn(this._removeListeners[key])) {
      this._removeListeners[key]()
    }

    delete this._removeListeners[key]
    delete state[key]
    delete this[key]

    setNonEnumerable(state, '_diff', diff(key, undefined))
    _set(state)

    return this
  }

  return obs

  // processing
  function watch (obs, key) {
    return function (value) {
      if (nestedTransaction === value) {
        return
      }

      var state = extend(obs())
      state[key] = value

      setNonEnumerable(state, '_diff', diff(key, value))

      currentTransaction = state
      obs.set(state)
      currentTransaction = NO_TRANSACTION
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mercury.watch"></a>[function <span class="apidocSignatureSpan">mercury.</span>watch (observable, listener)](#apidoc.element.mercury.watch)
- description and source-code
```javascript
function watch(observable, listener) {
    var remove = observable(listener)
    listener(observable())
    return remove
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mercury.Delegator"></a>[module mercury.Delegator](#apidoc.module.mercury.Delegator)

#### <a name="apidoc.element.mercury.Delegator.Delegator"></a>[function <span class="apidocSignatureSpan">mercury.</span>Delegator (opts)](#apidoc.element.mercury.Delegator.Delegator)
- description and source-code
```javascript
function Delegator(opts) {
    opts = opts || {}
    var document = opts.document || globalDocument

    var cacheKey = document[cacheTokenKey]

    if (!cacheKey) {
        cacheKey =
            document[cacheTokenKey] = cuid()
    }

    var delegator = delegatorCache.delegators[cacheKey]

    if (!delegator) {
        delegator = delegatorCache.delegators[cacheKey] =
            new DOMDelegator(document)
    }

    if (opts.defaultEvents !== false) {
        for (var i = 0; i < commonEvents.length; i++) {
            delegator.listenTo(commonEvents[i])
        }
    }

    return delegator
}
```
- example usage
```shell
...
function app(elem, observ, render, opts) {
if (!elem) {
    throw new Error(
        'Element does not exist. ' +
        'Mercury cannot be initialized.');
}

mercury.Delegator(opts);
var loop = mercury.main(observ(), render, extend({
    diff: mercury.diff,
    create: mercury.create,
    patch: mercury.patch
}, opts));

elem.appendChild(loop.target);
...
```

#### <a name="apidoc.element.mercury.Delegator.allocateHandle"></a>[function <span class="apidocSignatureSpan">mercury.Delegator.</span>allocateHandle (func)](#apidoc.element.mercury.Delegator.allocateHandle)
- description and source-code
```javascript
function allocateHandle(func) {
    var handle = new Handle()

    HANDLER_STORE(handle).func = func;

    return handle
}
```
- example usage
```shell
...
    return observ;
}

function channels(funcs, context) {
    return Object.keys(funcs).reduce(createHandle, {});

    function createHandle(acc, name) {
        var handle = mercury.Delegator.allocateHandle(
            funcs[name].bind(null, context));

        acc[name] = handle;
        return acc;
    }
}
...
```

#### <a name="apidoc.element.mercury.Delegator.transformHandle"></a>[function <span class="apidocSignatureSpan">mercury.Delegator.</span>transformHandle (handle, broadcast)](#apidoc.element.mercury.Delegator.transformHandle)
- description and source-code
```javascript
function transformHandle(handle, broadcast) {
    var func = HANDLER_STORE(handle).func

    return this.allocateHandle(function (ev) {
        broadcast(ev, func);
    })
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
