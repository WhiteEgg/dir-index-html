# dir-index-html

> Directory listing HTML for `go-btfs` gateways

**NOTE:** This repo is not intended to be used as a standalone project! This code is used by the gateway code within [`go-btfs`](https://github.com/btfs/go-btfs). In the long term, once the the gateway is extracted from `go-btfs`, the code in this repo will be merged into that gateway package.

## Updating

When making updates to the directory listing page template, please note the following:

1. Make your changes to the (human-friendly) source documents in the `src` directory
2. Before testing or releasing, make sure to run the build script to update the minified version in the top-level directory:

```bash
> npm run build
```
3. To get your updates into `go-btfs`, you'll need to do the following:
     - Cut a new, appropriately versioned release of `dir-index-html` (don't forget to bump the version number in `package.json`)
     - Make a PR against `go-btfs` following [these instructions](https://github.com/TRON-US/go-btfs/tree/master/assets#updating-dir-index-html) for updating the directory index

## Testing

1. Make sure you have [Go](https://golang.org/dl/) installed
2. Start the test server, which lives in its own directory:

```bash
> cd test
> go run .
```
This will listen on [`localhost:3000`](http://localhost:3000/) and reload the template every time you refresh the page.

If you get a "no such file or directory" error upon trying `go run .`, make sure you ran `npm run build` to generate the minified artifact that the test is looking for.

## License

MIT
