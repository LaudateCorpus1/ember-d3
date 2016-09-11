# ember-d3 [![Build Status](https://travis-ci.org/brzpegasus/ember-d3.svg?branch=master)](https://travis-ci.org/ivanvanderbyl/ember-cli-d3-shape) [![Ember Observer Score](https://emberobserver.com/badges/ember-cli-d3-shape.svg)](https://emberobserver.com/addons/ember-cli-d3-shape) [![npm version](https://badge.fury.io/js/ember-cli-d3-shape.svg)](https://badge.fury.io/js/ember-cli-d3-shape) [![Dependency Status](https://david-dm.org/ivanvanderbyl/ember-cli-d3-shape.svg)](https://david-dm.org/ivanvanderbyl/ember-cli-d3-shape) [![devDependency Status](https://david-dm.org/ivanvanderbyl/ember-cli-d3-shape/dev-status.svg)](https://david-dm.org/brzpegasus/ember-d3.svg#info=devDependencies)

Ember shim for loading `d3@4.x.x`. To install:

```
ember install ember-d3
```

D3 modules are loaded from NPM as ES2015 modules. It includes `d3-shape` and all version 4 modules in D3 `4.x`.

**If you're looking for the `ember-d3` for `d3@3.x`, see the `v3` branch.**

## Advanced Installation

If you need a specified d3 version, add this to your project:

```
npm install --save-dev d3@4.1.1
```

## Example usage:

```js
import { line } from 'd3-shape';
import { scaleOrdinal } from 'd3-scale';
import { extent } from 'd3-array';
```

## Svelte Builds

In case you do not want to include *all* of d3's dependencies, you may whitelist the packages
that you want to include in your project's `config/environment.js` file.

For example, if you only wanted to use `d3-scale`, you would do:

```js
// config/environment.js
module.exports = function() {
  return {
    'ember-cli-d3-shape': {
      only: ['d3-scale']
    }
  };
};
```

Or if you want to exclude a package:

```js
// config/environment.js
module.exports = function() {
  return {
    'ember-cli-d3-shape': {
      except: ['d3-scale']
    }
  };
};
```

**Note**: Even though you only add `d3-scale`, it has a few transitive d3 dependencies.
These are added to your project automatically.

## Running Tests

* `npm test` (Runs `ember try:testall` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`
