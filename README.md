# nci-express
[![Build Status](https://travis-ci.org/node-ci/nci-express.svg?branch=master)](https://travis-ci.org/node-ci/nci-express)

[express](https://github.com/expressjs/express) plugin for [nci](https://github.com/node-ci/nci)
to simplify http related plugins development


## Installation

```sh
npm install nci-express
```

## Usage

Add this plugin to the `plugins` section at server config before any plugin that using it.
```yml
plugins:
    - nci-express
    - nci-plugin-with-express
```

Add this plugin to `peerDependencies` at your plugin package.json

Just use `app.express` as express instance
```js
exports.register = function(app) {
	app.express.get('/some/route', function(req, res) {
		res.json({ok: true})
	});
};
```

Look at [nci-shields](https://github.com/node-ci/nci-shields) as example.

## License

[The MIT License](https://raw.githubusercontent.com/node-ci/nci-express/master/LICENSE)
