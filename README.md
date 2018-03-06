# react-app-rewire-yaml

Add [yaml-loader](https://github.com/okonet/yaml-loader) together with
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
```js
import data from './data.yaml'

const App = () => (
  <div>
    {data.key}
  </div>
);
```
