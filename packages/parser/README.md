# @tracespace/parser

A parser for printed circuit board manufacturing files. Compiles [Gerber][gerber] and [NC drill][nc-drill] files into abstract syntax trees based on the [unist][] format.

Part of the [tracespace][] collection of PCB visualization tools.

**This package is still in development and is not yet published**

[gerber]: https://en.wikipedia.org/wiki/Gerber_format
[nc-drill]: https://en.wikipedia.org/wiki/PCB_NC_formats
[unist]: https://unifiedjs.com/
[tracespace]: https://github.com/tracespace/tracespace

## usage

```js
import {createParser} from '@tracespace/parser'
// commonjs is cool, too
// const {createParser} = require('@tracespace/parser')

const parser = createParser()
parser.feed(/* ...some gerber string... */)
const tree = parser.results()
```

### script tag

If you're not using a bundler and you want to try out the parser in a browser, you can use a `script` tag:

```html
<script src="https://unpkg.com/@tracespace/parser"></script>
<script>
  // global variable TracespaceParser now available
  const parser = TracespaceParser.createParser()
</script>
```