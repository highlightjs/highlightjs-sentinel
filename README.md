# `sentinel` - a language definition for highlight.js

This is a [highlight.js](https://highlightjs.org/) language definition for
[Sentinel](https://docs.hashicorp.com/sentinel/), HashiCorp's policy as code
language.

For more about highlight.js, see https://highlightjs.org/

For more about Sentinel, see https://docs.hashicorp.com/sentinel/.

### Usage

Simply include the `highlight.js` script package in your webpage or node app,
load up this module and apply it to `hljs`.

If you're not using a build system and just want to embed this in your webpage:

```html
<script type="text/javascript" src="/path/to/highlight.pack.js"></script>
<script type="text/javascript" src="/path/to/highlightjs-sentinel/sentinel.js"></script>
<script type="text/javascript">
    hljs.registerLanguage('sentinel', hljsDefineSentinel);
    hljs.highlightAll();
</script>
```

If you're using webpack / rollup / browserify / node:

```javascript
var hljs = require('highlightjs');
var hljsDefineSentinel = require('highlightjs-sentinel');

hljsDefineSentinel(hljs);
hljs.highlightAll();
```

### Advanced

This is a pretty simple package, the only thing you might want to do differently
is name the language something other than `sentinel`. If you want to do this,
simply `import { definer } from 'highlightjs-sentinel';` and use it like:
`hljs.registerLanguage('othername', definer);`.

### Author

Chris Marchesi <chrism@vancluevertech.com>

Based on the Go highlight.js language definition, by Stephan Kountso
<steplg@gmail.com> and Evgeny Stepanischev <imbolk@gmail.com>.

### Maintainer

Chris Marchesi <chrism@vancluevertech.com>
