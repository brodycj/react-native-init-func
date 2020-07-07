# react-native-init-func

[![license](https://img.shields.io/github/license/brodybits/react-native-init-func?style=flat-square)](./LICENSE.md)
[![npm](https://img.shields.io/npm/v/react-native-init-func?style=flat-square)](https://www.npmjs.com/package/react-native-init-func)

programmatic React Native initialization function from the CLI

exports the flexible `init` command function from `@react-native-community/cli`

## usage

sample usage:

```js
const init = require('react-native-init-func')

;(async () => {
  await init(['demo'], { template: 'react-native-tvos@latest' })

  console.log('demo is now ready')
})()
```

or with a custom relative `directory` option:

```js
const init = require('react-native-init-func')

;(async () => {
  await init(['demo'], {
    directory: 'react-native-awesome-module/demo',
    template: 'react-native-tvos@latest'
  })

  console.log('react-native-awesome-module/demo is now ready')
})()
```

### major quirk

This function seems to change the process cwd. It is recommended to resolve any relative paths needed before calling this function.

## License

[MIT LICENSE](./LICENSE.md)
