# z-index-manager

Rewrite z-index values to be more manageable.

This CSS:

```css
#something {
  z-index: 18
}

.tom {
  z-index: 2;
}

.another, .z-index {
  z-index: 2;
}

.another, .z-index {
  z-index: -2;
}

#something {
  z-index: 34
}
```

becomes:

```css
#something {
  z-index: 20
}

.tom {
  z-index: 10;
}

.another, .z-index {
  z-index: 10;
}

.another, .z-index {
  z-index: -2;
}

#something {
  z-index: 30
}
```

## Install

```shell
$ npm install -g z-index-manager
```

## Usage

Run `z-index-manager` with the file you want to rewrite. You can also pass a different output file if you want.

```shell
$ z-index-manager [path/to/source] [optional path/to/output]
```

For example:

```shell
$ z-index-manager css/style.css
```

**Note:** It currently ignores negative values.

## License

MIT