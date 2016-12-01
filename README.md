# NG6-starter with basic implementation of Bootstrap and jQuery

This is the sample how to get work Bootstrap with NG6-starter by AngularClass (https://github.com/AngularClass/NG6-starter).


## What you need


### 1 - install dependencies in package.json

```
    "bootstrap": "3.3.7",
    "bootstrap-loader": "1.3.1",
    "bootstrap-sass": "^3.3.7",
    "extract-text-webpack-plugin": "1.0.1",
    "resolve-url-loader": "^1.6.0",
    "url-loader": "^0.5.7",
    "file-loader": "0.9.0",
    "jquery" : "3.1.1"
```


### 2 - require bootsrap loader and jquery in app.js

```
require('bootstrap-loader');

var $ = require('jquery');
window.jQuery = $;
```


### 3 - edit webpack.config.js

```
...
  {test: /\.(woff|woff2)(\?v=[0-9]\.[0-9]\.[0-9])?$/, loader: "url-loader?limit=10000&minetype=application/font-woff" },
  {test: /\.(ttf|eot|svg)(\?v=[0-9]\.[0-9]\.[0-9])?$/, loader: "file-loader" }
...
    new webpack.ProvidePlugin({
      $: "jquery",
      jQuery: "jquery"
    }),
    ...
```


## Info

There are samples of bootstrap components in home.html which are displayed correctly. This commit is working for me but there are some errors/important information during building which I would like to solve soon.