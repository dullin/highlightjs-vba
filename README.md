# vba - a language grammar for highlight.js

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading Highlight.js.  You'll use the minified version found in the `dist` directory.  This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" charset="UTF-8"
  src="/path/to/highlightjs-vba/dist/vba.min.js"></script>
<script type="text/javascript">
  hljs.initHighlightingOnLoad();
</script>
```

### Using directly from the UNPKG CDN

```html
<script type="text/javascript"
  src="https://unpkg.com/highlightjs-vba/dist/vba.min.js"></script>
```

- More info: <https://unpkg.com>

### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlightjs');
var hljsVba = require('highlightjs-vba');

hljs.registerLanguage("vba", hljsVba);
hljs.initHighlightingOnLoad();
```


## License

Highlight.js is released under the MIT License. See [LICENSE][1] file
for details.

### Author

Hugo Leblanc <admin@hololink.org>

### Generating the dist files 
From [this issue](https://github.com/highlightjs/highlightjs-cypher/issues/9)

```
node  --stack-size=65500  ./tools/build.js -t cdn
```

## Links

- The official site for the Highlight.js library is <https://highlightjs.org/>.
- The Highlight.js GitHub project: <https://github.com/highlightjs/highlight.js>

[1]: https://github.com/dullin/highlightjs-vba/blob/master/LICENSE
