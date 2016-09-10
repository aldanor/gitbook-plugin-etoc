# gitbook-plugin-etoc

[![npm](https://img.shields.io/npm/v/gitbook-plugin-etoc.svg?style=plastic)](https://npmjs.org/package/gitbook-plugin-etoc) [![npm](https://img.shields.io/npm/dm/gitbook-plugin-etoc.svg?style=plastic)](https://npmjs.org/package/gitbook-plugin-etec) [![npm](https://img.shields.io/npm/dt/gitbook-plugin-etoc.svg?style=plastic)](https://npmjs.org/package/gitbook-plugin-etoc)

This plugin will add table of content to the page.
When you build the book, it will insert a table of content automatically or to place where you insert `<!-- toc -->`. Sometimes you may want to disable toc on some page, just add `<!-- notoc -->` on the the markdown page.

## Sample

![screenshot 2016-09-07 23 00 26](https://cloud.githubusercontent.com/assets/1292567/18316915/f26e401c-754e-11e6-9a63-ec3763e4e385.png)

## Config

Add `etoc` in `book.json`.

```
{
  "plugin": ["etoc"]
}
```

It will add toc automatically if the markdown page has `###` header3(mindepth required to generate toc), and the maxdepth of toc is `####` header4 by default. You can also change the default parameter such as:
```
{
  "plugins": [
    "etoc"
  ],
  "pluginsConfig": {
    "etoc": {
      "mindepth": 3,
      "maxdepth": 4,
      "notoc": false
    }
  }
}
```

The configuration json schema is shown as following:
```
"gitbook": {
    "properties": {
        "mindepth": {
          "type": "number",
          "description": "minimal heading level required to generate toc",
          "default": 3
        },
        "maxdepth": {
          "type": "number",
          "description": "maximal heading level to generate toc",
          "default": 4
        },
        "notoc": {
          "type": "boolean",
          "description": "whether to generate toc automatically",
          "default": false
        }
    }
}
```

## LICENSE

MIT
