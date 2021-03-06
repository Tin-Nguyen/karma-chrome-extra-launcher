# karma-chrome-extra-launcher

> Launcher for Google Chrome and Google Chrome Canary. Adding use custom agent

## Installation

**This plugin ships with Karma by default, so you don't need to install it, it should just work ;-)**

The easiest way is to keep `karma-chrome-extra-launcher` as a devDependency in your `package.json`.
```json
{
  "devDependencies": {
    "karma": "~0.10",
    "karma-chrome-extra-launcher": "~0.1"
  }
}
```

You can simple do it by:
```bash
npm install karma-chrome-extra-launcher --save-dev
```

## Configuration
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
    browsers: ['ChromeExtra', 'Chrome_without_security'],

    // you can define custom flags
    customLaunchers: {
      Chrome_without_security: {
        base: 'ChromeExtra',
        flags: ['--disable-web-security']
      }
    }
  });
};
```

You can pass list of browsers as a CLI argument too:
```bash
karma start --browsers ChromeExtra,Chrome_without_security
```

----

For more information on Karma see the [homepage].


[homepage]: http://tin-nguyen.github.com
