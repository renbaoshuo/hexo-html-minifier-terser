# hexo-html-minifier-terser

[![NPM version](https://badge.fury.io/js/hexo-html-minifier-terser.svg)](https://www.npmjs.com/package/hexo-html-minifier-terser)

Minify HTML files with [html-minifier-terser](https://github.com/terser/html-minifier-terser).

## Installation

``` bash
$ npm install html-minifier-terser --save
```

## Options

You can set options of HTMLMinifier in the main `_config.yml` file:

``` yaml
html_minifier:
  exclude: 
```

- **exclude**: Exclude files from being minified. Support [globbing patterns](https://github.com/micromatch/micromatch#extended-globbing).

Default options:

``` yaml
html_minifier:  
  collapseBooleanAttributes: true
  collapseWhitespace: true
  # Ignore '<!-- more -->' https://hexo.io/docs/tag-plugins#Post-Excerpt
  ignoreCustomComments: [ !!js/regexp /^\s*more/]
  removeComments: true
  removeEmptyAttributes: true
  removeScriptTypeAttributes: true
  removeStyleLinkTypeAttributes: true
  minifyJS: true
  minifyCSS: true
```

- **ignoreCustomComments**: Array of regex'es that allow to ignore certain comments, when matched. Need to prepend [`!!js/regexp`](https://github.com/nodeca/js-yaml#supported-yaml-types) to support regex.

Description of the above options and other available options, see [HTMLMinifier](https://github.com/kangax/html-minifier#options-quick-reference)
