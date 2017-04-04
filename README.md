# api documentation for  [redux-devtools (v3.3.2)](https://github.com/gaearon/redux-devtools)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-devtools.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-devtools) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-devtools.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-devtools)
#### Redux DevTools with hot reloading and time travel

[![NPM](https://nodei.co/npm/redux-devtools.png?downloads=true)](https://www.npmjs.com/package/redux-devtools)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-redux-devtools_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Abramov",
        "email": "dan.abramov@me.com",
        "url": "http://github.com/gaearon"
    },
    "bugs": {
        "url": "https://github.com/gaearon/redux-devtools/issues"
    },
    "dependencies": {
        "lodash": "^4.2.0",
        "redux-devtools-instrument": "^1.0.1"
    },
    "description": "Redux DevTools with hot reloading and time travel",
    "devDependencies": {
        "babel-cli": "^6.3.17",
        "babel-core": "^6.3.17",
        "babel-eslint": "^4.1.6",
        "babel-loader": "^6.2.0",
        "babel-preset-es2015-loose": "^6.1.3",
        "babel-preset-react": "6.3.13",
        "babel-preset-stage-0": "^6.3.13",
        "cross-env": "3.1.3",
        "eslint": "^0.23",
        "eslint-config-airbnb": "0.0.6",
        "eslint-plugin-react": "^2.3.0",
        "expect": "^1.6.0",
        "isparta": "^3.0.3",
        "jsdom": "^6.5.1",
        "mocha": "^2.2.5",
        "mocha-jsdom": "^1.0.0",
        "react": "^0.14.0",
        "react-addons-test-utils": "^0.14.0",
        "react-dom": "^0.14.0",
        "react-redux": "^4.0.0",
        "redux": "^3.5.2",
        "rimraf": "^2.3.4",
        "webpack": "^1.11.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f427f71964e2b3785b68834b6e4fe99d8da75b5e",
        "tarball": "https://registry.npmjs.org/redux-devtools/-/redux-devtools-3.3.2.tgz"
    },
    "files": [
        "lib",
        "src"
    ],
    "gitHead": "defc8100e1cc8e27b6f87e4e34a5eef5613ff4ec",
    "homepage": "https://github.com/gaearon/redux-devtools",
    "keywords": [
        "redux",
        "devtools",
        "flux",
        "hot reloading",
        "time travel",
        "live edit"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "gaearon",
            "email": "dan.abramov@gmail.com"
        },
        {
            "name": "zalmoxisus",
            "email": "zalmoxisus@gmail.com"
        }
    ],
    "name": "redux-devtools",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "^0.14.0 || ^15.0.0",
        "react-redux": "^4.0.0 || ^5.0.0",
        "redux": "^3.5.2"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/gaearon/redux-devtools.git"
    },
    "scripts": {
        "build": "babel src --out-dir lib",
        "clean": "rimraf lib",
        "lint": "eslint src test examples",
        "prepublish": "npm run lint && npm run test && npm run clean && npm run build",
        "test": "cross-env NODE_ENV=test mocha --compilers js:babel-core/register --recursive",
        "test:cov": "babel-node ./node_modules/.bin/isparta cover ./node_modules/.bin/_mocha -- --recursive",
        "test:watch": "cross-env NODE_ENV=test mocha --compilers js:babel-core/register --recursive --watch"
    },
    "version": "3.3.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module redux-devtools](#apidoc.module.redux-devtools)
1.  boolean <span class="apidocSignatureSpan">redux-devtools.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-devtools.</span>createDevTools (children)](#apidoc.element.redux-devtools.createDevTools)
1.  [function <span class="apidocSignatureSpan">redux-devtools.</span>instrument ()](#apidoc.element.redux-devtools.instrument)
1.  [function <span class="apidocSignatureSpan">redux-devtools.</span>persistState (sessionId)](#apidoc.element.redux-devtools.persistState)
1.  object <span class="apidocSignatureSpan">redux-devtools.</span>ActionCreators
1.  object <span class="apidocSignatureSpan">redux-devtools.</span>ActionTypes

#### [module redux-devtools.ActionCreators](#apidoc.module.redux-devtools.ActionCreators)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>commit ()](#apidoc.element.redux-devtools.ActionCreators.commit)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>importState (nextLiftedState, noRecompute)](#apidoc.element.redux-devtools.ActionCreators.importState)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>jumpToAction (actionId)](#apidoc.element.redux-devtools.ActionCreators.jumpToAction)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>jumpToState (index)](#apidoc.element.redux-devtools.ActionCreators.jumpToState)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>lockChanges (status)](#apidoc.element.redux-devtools.ActionCreators.lockChanges)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>pauseRecording (status)](#apidoc.element.redux-devtools.ActionCreators.pauseRecording)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>performAction (action)](#apidoc.element.redux-devtools.ActionCreators.performAction)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>reorderAction (actionId, beforeActionId)](#apidoc.element.redux-devtools.ActionCreators.reorderAction)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>reset ()](#apidoc.element.redux-devtools.ActionCreators.reset)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>rollback ()](#apidoc.element.redux-devtools.ActionCreators.rollback)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>setActionsActive (start, end)](#apidoc.element.redux-devtools.ActionCreators.setActionsActive)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>sweep ()](#apidoc.element.redux-devtools.ActionCreators.sweep)
1.  [function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>toggleAction (id)](#apidoc.element.redux-devtools.ActionCreators.toggleAction)

#### [module redux-devtools.createDevTools](#apidoc.module.redux-devtools.createDevTools)
1.  boolean <span class="apidocSignatureSpan">redux-devtools.createDevTools.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-devtools.createDevTools.</span>default (children)](#apidoc.element.redux-devtools.createDevTools.default)

#### [module redux-devtools.persistState](#apidoc.module.redux-devtools.persistState)
1.  boolean <span class="apidocSignatureSpan">redux-devtools.persistState.</span>__esModule
1.  [function <span class="apidocSignatureSpan">redux-devtools.persistState.</span>default (sessionId)](#apidoc.element.redux-devtools.persistState.default)



# <a name="apidoc.module.redux-devtools"></a>[module redux-devtools](#apidoc.module.redux-devtools)

#### <a name="apidoc.element.redux-devtools.createDevTools"></a>[function <span class="apidocSignatureSpan">redux-devtools.</span>createDevTools (children)](#apidoc.element.redux-devtools.createDevTools)
- description and source-code
```javascript
function createDevTools(children) {
  var _class, _temp;

  var monitorElement = _react.Children.only(children);
  var monitorProps = monitorElement.props;
  var Monitor = monitorElement.type;
  var ConnectedMonitor = (0, _reactRedux.connect)(function (state) {
    return state;
  })(Monitor);

  return _temp = _class = function (_Component) {
    _inherits(DevTools, _Component);

    function DevTools(props, context) {
      _classCallCheck(this, DevTools);

      var _this = _possibleConstructorReturn(this, _Component.call(this, props, context));

      if (!props.store && !context.store) {
        console.error('Redux DevTools could not render. You must pass the Redux store ' + 'to <DevTools> either as a "store" prop
 or by wrapping it in a ' + '<Provider store={store}>.');
        return _possibleConstructorReturn(_this);
      }

      if (context.store) {
        _this.liftedStore = context.store.liftedStore;
      } else {
        _this.liftedStore = props.store.liftedStore;
      }

      if (!_this.liftedStore) {
        console.error('Redux DevTools could not render. Did you forget to include ' + 'DevTools.instrument() in your store enhancer
 chain before ' + 'using createStore()?');
      }
      return _this;
    }

    DevTools.prototype.render = function render() {
      if (!this.liftedStore) {
        return null;
      }

      return _react2.default.createElement(ConnectedMonitor, _extends({}, monitorProps, {
        store: this.liftedStore }));
    };

    return DevTools;
  }(_react.Component), _class.contextTypes = {
    store: _react.PropTypes.object
  }, _class.propTypes = {
    store: _react.PropTypes.object
  }, _class.instrument = function (options) {
    return (0, _reduxDevtoolsInstrument2.default)(function (state, action) {
      return Monitor.update(monitorProps, state, action);
    }, options);
  }, _temp;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.instrument"></a>[function <span class="apidocSignatureSpan">redux-devtools.</span>instrument ()](#apidoc.element.redux-devtools.instrument)
- description and source-code
```javascript
function instrument() {
  var monitorReducer = arguments.length <= 0 || arguments[0] === undefined ? function () {
    return null;
  } : arguments[0];
  var options = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

<span class="apidocCodeCommentSpan">  /* eslint-disable no-eq-null */
</span>  if (options.maxAge != null && options.maxAge < 2) {
    /* eslint-enable */
    throw new Error('DevTools.instrument({ maxAge }) option, if specified, ' + 'may not be less than 2.');
  }

  return function (createStore) {
    return function (reducer, initialState, enhancer) {

      function liftReducer(r) {
        if (typeof r !== 'function') {
          if (r && typeof r.default === 'function') {
            throw new Error('Expected the reducer to be a function. ' + 'Instead got an object with a "default" field. ' + 'Did
you pass a module instead of the default export? ' + 'Try passing require(...).default instead.');
          }
          throw new Error('Expected the reducer to be a function.');
        }
        return liftReducerWith(r, initialState, monitorReducer, options);
      }

      var liftedStore = createStore(liftReducer(reducer), enhancer);
      if (liftedStore.liftedStore) {
        throw new Error('DevTools instrumentation should not be applied more than once. ' + 'Check your store configuration.');
      }

      return unliftStore(liftedStore, liftReducer);
    };
  };
}
```
- example usage
```shell
...

### Browser Extension

If you don’t want to bother with installing Redux DevTools and integrating it into your project, consider using [Redux DevTools
Extension](https://github.com/zalmoxisus/redux-devtools-extension) for Chrome and Firefox. It provides access to the most popular
 monitors, is easy to configure to filter actions, and doesn’t require installing any packages.

### Setup Instructions

Read the installation [walkthrough](./docs/Walkthrough.md) for integration instructions and usage examples ('<DevTools>' component
, 'DevTools.instrument()', exclude from production builds, gotchas).

### Running Examples

Clone the project:

'''
git clone https://github.com/gaearon/redux-devtools.git
...
```

#### <a name="apidoc.element.redux-devtools.persistState"></a>[function <span class="apidocSignatureSpan">redux-devtools.</span>persistState (sessionId)](#apidoc.element.redux-devtools.persistState)
- description and source-code
```javascript
function persistState(sessionId) {
  var deserializeState = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : _identity2.default;
  var deserializeAction = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : _identity2.default;

  if (!sessionId) {
    return function (next) {
      return function () {
        return next.apply(undefined, arguments);
      };
    };
  }

  function deserialize(state) {
    return _extends({}, state, {
      actionsById: (0, _mapValues2.default)(state.actionsById, function (liftedAction) {
        return _extends({}, liftedAction, {
          action: deserializeAction(liftedAction.action)
        });
      }),
      committedState: deserializeState(state.committedState),
      computedStates: state.computedStates.map(function (computedState) {
        return _extends({}, computedState, {
          state: deserializeState(computedState.state)
        });
      })
    });
  }

  return function (next) {
    return function (reducer, initialState, enhancer) {
      var key = 'redux-dev-session-' + sessionId;

      var finalInitialState = void 0;
      try {
        var json = localStorage.getItem(key);
        if (json) {
          finalInitialState = deserialize(JSON.parse(json)) || initialState;
          next(reducer, initialState);
        }
      } catch (e) {
        console.warn('Could not read debug session from localStorage:', e);
        try {
          localStorage.removeItem(key);
        } finally {
          finalInitialState = undefined;
        }
      }

      var store = next(reducer, finalInitialState, enhancer);

      return _extends({}, store, {
        dispatch: function dispatch(action) {
          store.dispatch(action);

          try {
            localStorage.setItem(key, JSON.stringify(store.getState()));
          } catch (e) {
            console.warn('Could not write debug session to localStorage:', e);
          }

          return action;
        }
      });
    };
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-devtools.ActionCreators"></a>[module redux-devtools.ActionCreators](#apidoc.module.redux-devtools.ActionCreators)

#### <a name="apidoc.element.redux-devtools.ActionCreators.commit"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>commit ()](#apidoc.element.redux-devtools.ActionCreators.commit)
- description and source-code
```javascript
function commit() {
  return { type: ActionTypes.COMMIT, timestamp: Date.now() };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.importState"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>importState (nextLiftedState, noRecompute)](#apidoc.element.redux-devtools.ActionCreators.importState)
- description and source-code
```javascript
function importState(nextLiftedState, noRecompute) {
  return { type: ActionTypes.IMPORT_STATE, nextLiftedState: nextLiftedState, noRecompute: noRecompute };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.jumpToAction"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>jumpToAction (actionId)](#apidoc.element.redux-devtools.ActionCreators.jumpToAction)
- description and source-code
```javascript
function jumpToAction(actionId) {
  return { type: ActionTypes.JUMP_TO_ACTION, actionId: actionId };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.jumpToState"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>jumpToState (index)](#apidoc.element.redux-devtools.ActionCreators.jumpToState)
- description and source-code
```javascript
function jumpToState(index) {
  return { type: ActionTypes.JUMP_TO_STATE, index: index };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.lockChanges"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>lockChanges (status)](#apidoc.element.redux-devtools.ActionCreators.lockChanges)
- description and source-code
```javascript
function lockChanges(status) {
  return { type: ActionTypes.LOCK_CHANGES, status: status };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.pauseRecording"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>pauseRecording (status)](#apidoc.element.redux-devtools.ActionCreators.pauseRecording)
- description and source-code
```javascript
function pauseRecording(status) {
  return { type: ActionTypes.PAUSE_RECORDING, status: status };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.performAction"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>performAction (action)](#apidoc.element.redux-devtools.ActionCreators.performAction)
- description and source-code
```javascript
function performAction(action) {
  if (!(0, _isPlainObject2.default)(action)) {
    throw new Error('Actions must be plain objects. ' + 'Use custom middleware for async actions.');
  }

  if (typeof action.type === 'undefined') {
    throw new Error('Actions may not have an undefined "type" property. ' + 'Have you misspelled a constant?');
  }

  return { type: ActionTypes.PERFORM_ACTION, action: action, timestamp: Date.now() };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.reorderAction"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>reorderAction (actionId, beforeActionId)](#apidoc.element.redux-devtools.ActionCreators.reorderAction)
- description and source-code
```javascript
function reorderAction(actionId, beforeActionId) {
  return { type: ActionTypes.REORDER_ACTION, actionId: actionId, beforeActionId: beforeActionId };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.reset"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>reset ()](#apidoc.element.redux-devtools.ActionCreators.reset)
- description and source-code
```javascript
function reset() {
  return { type: ActionTypes.RESET, timestamp: Date.now() };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.rollback"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>rollback ()](#apidoc.element.redux-devtools.ActionCreators.rollback)
- description and source-code
```javascript
function rollback() {
  return { type: ActionTypes.ROLLBACK, timestamp: Date.now() };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.setActionsActive"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>setActionsActive (start, end)](#apidoc.element.redux-devtools.ActionCreators.setActionsActive)
- description and source-code
```javascript
function setActionsActive(start, end) {
  var active = arguments.length <= 2 || arguments[2] === undefined ? true : arguments[2];

  return { type: ActionTypes.SET_ACTIONS_ACTIVE, start: start, end: end, active: active };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.sweep"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>sweep ()](#apidoc.element.redux-devtools.ActionCreators.sweep)
- description and source-code
```javascript
function sweep() {
  return { type: ActionTypes.SWEEP };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.redux-devtools.ActionCreators.toggleAction"></a>[function <span class="apidocSignatureSpan">redux-devtools.ActionCreators.</span>toggleAction (id)](#apidoc.element.redux-devtools.ActionCreators.toggleAction)
- description and source-code
```javascript
function toggleAction(id) {
  return { type: ActionTypes.TOGGLE_ACTION, id: id };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-devtools.createDevTools"></a>[module redux-devtools.createDevTools](#apidoc.module.redux-devtools.createDevTools)

#### <a name="apidoc.element.redux-devtools.createDevTools.default"></a>[function <span class="apidocSignatureSpan">redux-devtools.createDevTools.</span>default (children)](#apidoc.element.redux-devtools.createDevTools.default)
- description and source-code
```javascript
function createDevTools(children) {
  var _class, _temp;

  var monitorElement = _react.Children.only(children);
  var monitorProps = monitorElement.props;
  var Monitor = monitorElement.type;
  var ConnectedMonitor = (0, _reactRedux.connect)(function (state) {
    return state;
  })(Monitor);

  return _temp = _class = function (_Component) {
    _inherits(DevTools, _Component);

    function DevTools(props, context) {
      _classCallCheck(this, DevTools);

      var _this = _possibleConstructorReturn(this, _Component.call(this, props, context));

      if (!props.store && !context.store) {
        console.error('Redux DevTools could not render. You must pass the Redux store ' + 'to <DevTools> either as a "store" prop
 or by wrapping it in a ' + '<Provider store={store}>.');
        return _possibleConstructorReturn(_this);
      }

      if (context.store) {
        _this.liftedStore = context.store.liftedStore;
      } else {
        _this.liftedStore = props.store.liftedStore;
      }

      if (!_this.liftedStore) {
        console.error('Redux DevTools could not render. Did you forget to include ' + 'DevTools.instrument() in your store enhancer
 chain before ' + 'using createStore()?');
      }
      return _this;
    }

    DevTools.prototype.render = function render() {
      if (!this.liftedStore) {
        return null;
      }

      return _react2.default.createElement(ConnectedMonitor, _extends({}, monitorProps, {
        store: this.liftedStore }));
    };

    return DevTools;
  }(_react.Component), _class.contextTypes = {
    store: _react.PropTypes.object
  }, _class.propTypes = {
    store: _react.PropTypes.object
  }, _class.instrument = function (options) {
    return (0, _reduxDevtoolsInstrument2.default)(function (state, action) {
      return Monitor.update(monitorProps, state, action);
    }, options);
  }, _temp;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.redux-devtools.persistState"></a>[module redux-devtools.persistState](#apidoc.module.redux-devtools.persistState)

#### <a name="apidoc.element.redux-devtools.persistState.default"></a>[function <span class="apidocSignatureSpan">redux-devtools.persistState.</span>default (sessionId)](#apidoc.element.redux-devtools.persistState.default)
- description and source-code
```javascript
function persistState(sessionId) {
  var deserializeState = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : _identity2.default;
  var deserializeAction = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : _identity2.default;

  if (!sessionId) {
    return function (next) {
      return function () {
        return next.apply(undefined, arguments);
      };
    };
  }

  function deserialize(state) {
    return _extends({}, state, {
      actionsById: (0, _mapValues2.default)(state.actionsById, function (liftedAction) {
        return _extends({}, liftedAction, {
          action: deserializeAction(liftedAction.action)
        });
      }),
      committedState: deserializeState(state.committedState),
      computedStates: state.computedStates.map(function (computedState) {
        return _extends({}, computedState, {
          state: deserializeState(computedState.state)
        });
      })
    });
  }

  return function (next) {
    return function (reducer, initialState, enhancer) {
      var key = 'redux-dev-session-' + sessionId;

      var finalInitialState = void 0;
      try {
        var json = localStorage.getItem(key);
        if (json) {
          finalInitialState = deserialize(JSON.parse(json)) || initialState;
          next(reducer, initialState);
        }
      } catch (e) {
        console.warn('Could not read debug session from localStorage:', e);
        try {
          localStorage.removeItem(key);
        } finally {
          finalInitialState = undefined;
        }
      }

      var store = next(reducer, finalInitialState, enhancer);

      return _extends({}, store, {
        dispatch: function dispatch(action) {
          store.dispatch(action);

          try {
            localStorage.setItem(key, JSON.stringify(store.getState()));
          } catch (e) {
            console.warn('Could not write debug session to localStorage:', e);
          }

          return action;
        }
      });
    };
  };
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
