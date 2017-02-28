[![NPM](https://nodei.co/npm/hexo-prismjs-plugin.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/hexo-prismjs-plugin/)

# Hexo Prism.js Plugin
Since `highlight.js` didn't support JSX syntax properly, I wrote this plugin to replace
Hexo's default code highlight plugin.

## Install
```
npm i -S hexo-prismjs-plugin
```
## Usage
First, you should edit your `_config.yml` by adding following configuration.

```yaml
prism_plugin:
  mode: 'preprocess'    # realtime or preprocess
  theme: 'default'
  line_number: false    # default false
  auto_import_assets: true   # default true
```

Note: check `_config.yml` `highlight` option. Make sure that
```yaml
highlight:
  enable: false
```

- `mode`:
  - realtime  (Parse code on browser in real time)
  - preprocess  (Preprocess code in node)

- `theme`:
  - default
  - coy
  - dark
  - funky
  - okaidia
  - solarizedlight
  - tomorrow
  - twilight

- `line_number`:
  - true (Show line numbers)
  - false (Default, Hide line numbers)

- `auto_import_assets`
  - true (insert automaticaly css and js files)
  - false (let you choose another prism.js theme file or you own)

If you want avoid AMP validation errors, disable auto import asseets

And then, clean and generate project by running command:

```
hexo clean
hexo generate
```

## Supported languages
You could find the supported languages here:
http://prismjs.com/#languages-list
