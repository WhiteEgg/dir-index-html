# dir-index-html

> Directory listing HTML for go-btfs gateways

This repo is not be used standalone. It's used by the gateway code in go-btfs. It'll be merged into the gateway package, once the gateway has been extracted from go-btfs.

## Updating

1. Make changes to _both_ dir-index.html and dir-index-uncat.html.
2. Follow the instructions in [go-btfs](https://github.com/TRON-US/go-btfs/tree/master/assets#updating-dir-index-html) for updating the directory index.

## Testing

1. Install [go](https://golang.org/dl/).
2. Run the test server:

```bash
> cd test
> go run .
```

This will listen on `localhost:3000` and re-load the template every time you refresh the page.

## License

MIT
