# vscode-stylelint-mixins

A [Visual Studio Code](https://code.visualstudio.com/) extension to lint [CSS](https://www.w3.org/Style/CSS/)/[SCSS](https://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax)/[Less](http://lesscss.org/) with [stylelint](https://stylelint.io/), support multiple options.

Fork from [vscode-stylelint-plus](https://github.com/hex-ci/vscode-stylelint-plus).

![screenshot](https://raw.githubusercontent.com/hisanshao/vscode-stylelint-mixins/master/media/screenshot.png)

## Installation

1. Execute `Extensions: Install Extensions` command from [Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette).
2. Type `@sort:installs stylelint-mixins` into the search form and install the topmost one.

Read the [extension installation guide](https://code.visualstudio.com/docs/editor/extension-gallery) for more details.

### Optional (but recommended) setup

<img align="right" width="430" alt="duplicate messages from both the built-in linter and vscode-stylelint-mixins" src="https://raw.githubusercontent.com/hisanshao/vscode-stylelint-mixins/master/media/duplicate.png">

To prevent both [the editor built-in linters](https://code.visualstudio.com/docs/languages/css#_syntax-verification-linting) `[css]` `[less]` `[scss]` and this extension `[stylelint]` from reporting essentially the same errors like in the screenshot, disable the built-in ones in User or Workspace [setting](https://code.visualstudio.com/docs/getstarted/settings):

```json
"css.validate": false,
"less.validate": false,
"scss.validate": false
```

## Usage

Once a user follows [the stylelint startup guide](https://github.com/stylelint/stylelint#getting-started) by creating a [configuration](https://stylelint.io/user-guide/configuration/) file or by editing [`stylelint.*` VSCode settings](#extension-settings), stylelint automatically validates documents with these [language identifiers](https://code.visualstudio.com/docs/languages/overview#_language-id):

<img align="right" width="430" alt="UI to select a language identifier" src="https://raw.githubusercontent.com/hisanshao/vscode-stylelint-mixins/master/media/language.png">

* CSS (`css`)
* HTML (`html`)
* Less (`less`)
* JavaScript (`javascript`)
* JavaScript React (`javascriptreact`)
* Markdown (`markdown`)
* [Markdown+MathML (`source.markdown.math`)](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)
* [PostCSS (`postcss`)](https://marketplace.visualstudio.com/items?itemName=mhmadhamster.postcss-language)
* [Sass (`sass`)](https://marketplace.visualstudio.com/items?itemName=robinbentley.sass-indented)
* SCSS (`scss`)
* styled-components
  * [Official (`source.css.styled`)](https://marketplace.visualstudio.com/items?itemName=jpoissonnier.vscode-styled-components)
  * [Userland (`styled-css`)](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)
* [Sugarss (`sugarss`)](https://marketplace.visualstudio.com/items?itemName=mhmadhamster.postcss-language)
* [Svelte (`svelte`)](https://marketplace.visualstudio.com/items?itemName=JamesBirtles.svelte-vscode)
* TypeScript (`typescript`)
* TypeScript React (`typescriptreact`)
* [Vue (`vue`, `vue-html`, `vue-postcss`)](https://marketplace.visualstudio.com/items?itemName=octref.vetur)
* XML (`xml`)
* XSL (`xsl`)

### Extension settings

Though it's highly recommended to add a [stylelint configuration file](https://stylelint.io/user-guide/example-config/) to the current workspace folder instead, the following extension [settings](https://code.visualstudio.com/docs/getstarted/settings) are also available.

#### stylelint.enable

Type: `boolean`  
Default: `true`

Control whether this extension is enabled or not.

#### stylelint.autoFixOnSave

Type: `boolean`  
Default: `false`

Turns auto fix on save on or off.

#### stylelint.allowEmptyInput

Type: `boolean`  
Default: `false`

Control whether stylelint file can be empty or not.

#### stylelint.ignoreDisables

Type: `boolean`  
Default: `false`

If true, all disable comments (e.g. /* stylelint-disable block-no-empty */) will be ignored.

#### stylelint.configOverrides

Type: `Object`  
Default: `null`

Set stylelint [`configOverrides`](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/node-api.md#configoverrides) option.

#### stylelint.config

Type: `Object`  
Default: `null`

Set stylelint [`config`](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/node-api.md#config) option.

#### stylelint.configFile

Type: `string`  
Default: `null`

Set stylelint [`configFile`](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/node-api.md#configFile) option.

#### stylelint.configBasedir

Type: `string`  
Default: `null`

Set stylelint [`configBasedir`](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/node-api.md#configBasedir) option.

#### stylelint.ignorePath

Type: `string`  
Default: `null`

Set stylelint [`ignorePath`](https://github.com/stylelint/stylelint/blob/master/docs/user-guide/node-api.md#ignorePath) option.

## License

[ISC License](./LICENSE.txt) © 2018- 2019 Watanabe Shinnosuke
