# A wrapper for @rsdoctor/webpack-plugin

## Install

```sh
npm i -D @rsdoctor/webpack-plugin @keqingrong/rsdoctor-webpack-plugin
```

## Usage

webpack:

```js
// webpack.config.js
const RsdoctorWebpackPlugin = require('@keqingrong/rsdoctor-webpack-plugin');

module.exports = {
  // ...
  plugins: [
    process.env.RSDOCTOR &&
      new RsdoctorWebpackPlugin({
        // options
      }),
  ].filter(Boolean),
};
```

ice.js v2:

```js
// build.config.js
module.exports = {
  webpackPlugins: {
    '@keqingrong/rsdoctor-webpack-plugin': {},
  },
};
```

Or

```jsonc
// build.json
{
  "webpackPlugins": {
    "@keqingrong/rsdoctor-webpack-plugin": {}
  }
}
```

## See Also

- [rsdoctor](https://rsdoctor.dev/)
- [ice.js v2](https://v2.ice.work/docs/config/about#webpackplugins-)
