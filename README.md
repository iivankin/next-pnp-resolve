# NextPnpResolve

## Usage

- Apply [this](https://gist.github.com/iivankin/61027542406a71e0ea5434593d8ebec1) patch (this is temp).
- In the `next.config.js` add following:

```js
const { resolveDependency } = require('next-pnp-resolve');

{
	...
	experimental: {
		...
		fileTraceResolve: resolveDependency
	},
}
```

Now you can build!

### Files that you need to manually copy if outputStandalone

- `.yarn/releases`
- `.pnp.*`
- `yarn.lock`
- `.yarnrc.yml`

Run command: `yarn node server.js`
