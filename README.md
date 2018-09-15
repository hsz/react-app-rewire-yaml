# react-app-rewire-yaml

[![Dependency Status](https://img.shields.io/david/hsz/react-app-rewire-yaml.svg?style=flat-square)](https://david-dm.org/hsz/react-app-rewire-yaml)
[![Dev Dependency Status](https://img.shields.io/david/dev/hsz/react-app-rewire-yaml.svg?style=flat-square)](https://david-dm.org/hsz/react-app-rewire-yaml)
[![Version](https://img.shields.io/npm/v/react-app-rewire-yaml.svg?style=flat-square)](https://www.npmjs.com/package/react-app-rewire-yaml)
[![Month Download](https://img.shields.io/npm/dm/react-app-rewire-yaml.svg?style=flat-square)](https://www.npmjs.com/package/react-app-rewire-yaml)
[![License](https://img.shields.io/npm/l/react-app-rewire-yaml.svg?style=flat-square)](https://www.npmjs.com/package/react-app-rewire-yaml)

Add [yaml-loader](https://github.com/okonet/yaml-loader) together with
[yaml-lint-loader](https://github.com/hsz/yaml-lint-loader) and
[json-loader](https://github.com/webpack-contrib/json-loader) to your
[create-react-app](https://github.com/facebookincubator/create-react-app) via
[react-app-rewired](https://github.com/timarney/react-app-rewired).

## Installation

```
yarn add --dev react-app-rewire-yaml
```

OR

```
npm install --save-dev react-app-rewire-yaml
```

## Usage

In your react-app-rewired configuration:

```js
/* config-overrides.js */

const rewireYAML = require('react-app-rewire-yaml');

module.exports = function override(config, env) {
    // ...
    config = rewireYAML(config, env);
    // ...
    return config;
}
```

In your React application:

```jsx
import data from './data.yaml'

const App = () => (
  <div>
    {data.key}
  </div>
);
```
