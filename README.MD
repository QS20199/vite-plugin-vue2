# vite-plugin-vue2 (fork)

This is the fork of the original vite-plugin-vue2, and remove `vue-template-compiler` from package.json.
So this plugin will use parent project's vue-template-compiler.
This change is for being compatible with old Vue version (like vue@2.5.x)

## Usage

- run `yarn add vite-plugin-vue2 --dev`
- add the plugin into `vite.config.js`
``` js
// vite.config.js
const { createVuePlugin } = require('vite-plugin-vue2')

module.exports = {
  plugins: [createVuePlugin(/*options*/)],
}
```

## [Options](https://github.com/underfin/vite-plugin-vue2/blob/master/src/index.ts#L26)

### `vueTemplateOptions`

Type: `Object`<br>
Default: `null`

The options for `@vue/component-compiler-utils`.

### `jsx`

Type: `Boolean`<br>
Default: `false`

The options for jsx transform.

### `jsxOptions`

Type: `Object`<br>

The options for `@vue/babel-preset-jsx`.

## Todo

- SSR Build
- Sourcemap