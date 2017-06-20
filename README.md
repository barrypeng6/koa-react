### create project
```
mkdir koa-react && cd koa-react
npm init -y
```

### folder structure

```
koa-react
│
└───build
│
└───server
│    └──server.js
│
└───src
│    └──index.js
│     
│   webpack.consfig.js
│   .babelrc
└── package.json
```

### webpack install
```
npm install --save-dev webpack
```

### webpack config
webpack.config.js
```
var path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'build')
  },
  module: {
    rules: [
      {
        test: /\.js$/,
        use: [
          'babel-loader'
        ]
      }
    ]
  }
};
```

### babel install
compiler for ES6, JSX, React
```
npm install --save-dev babel-cli babel-preset-env babel-preset-react
```

### babel config
webpack.config.js
```
module.exports = {
  ...
  module: {
    rules: [
      {
        test: /\.js$/,
        use: [
          'babel-loader'
        ]
      }
    ]
  }
};
```
.babelrc
```
"preset": ["env", "react"]
```
