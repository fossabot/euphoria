<p align="left">
    <img width="400" src="docs/euphoria_logo.png">
</p>

[![LICENSE](https://img.shields.io/github/license/syhily/euphoria)](https://github.com/syhily/euphoria/blob/master/LICENSE)
[![Language](https://img.shields.io/badge/Language-Go-blue.svg)](https://golang.org/)
[![Go Report Card](https://goreportcard.com/badge/github.com/syhily/euphoria)](https://goreportcard.com/report/github.com/syhily/euphoria)
[![Github Actions Status](https://github.com/syhily/euphoria/workflows/Euphoria%20CI/badge.svg)](https://github.com/syhily/euphoria/actions?query=workflow%3A%22Euphoria+CI%22)
[![Github Actions Status](https://github.com/syhily/euphoria/workflows/Forntend%20CI/badge.svg)](https://github.com/syhily/euphoria/actions?query=workflow%3A%22Forntend+CI%22)
[![codecov](https://codecov.io/gh/syhily/euphoria/branch/master/graph/badge.svg)](https://codecov.io/gh/syhily/euphoria)
[![contribution](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](CONTRIBUTING.md)

## What is Euphoria?

Euphoria is an open-source personal EPUB book library which was highly inspired
by [talebook](https://github.com/talebook/talebook),
[calibre-web](https://github.com/janeczku/calibre-web) and [BookBrowser](https://github.com/pgaskin/BookBrowser).

It's designed to serve millions of book. Aims for providing high performance, readability comparing with its
competitors. And it's easy to be deployed on any Unix-like systems with only one file.

+ __High performance__

Euphoria didn't used `metadata.db` which was created by calibre directly. We would store all the books's metadata into
[bleve](https://github.com/blevesearch/bleve) which can provide a better searching performance comparing to SQLite3.

+ __Better book organize__

The books' directory architecture is defined by
the [Chinese Library Classification](https://en.wikipedia.org/wiki/Chinese_Library_Classification). We would put the
books into different directories by the categories it belongs.

* __Better book deduplication__

We would deduplication the book by
its [CIP (Cataloging in Publication)](https://www.capub.cn/zbbm/index_zbbm.shtml?id=7) in China
and [ISBN](https://en.wikipedia.org/wiki/International_Standard_Book_Number).

* __Better chinese books metadata management__

A lot of Chinese EPUBs don't generate with a valid metadata. We would correct it
by [CIP database](https://pdc.capub.cn/) and a builtin [Douban](https://www.douban.com/) spider.

## State of this project

The current master branch is unstable and is not recommended for production use. Euphoria 1.0.0 (what will be the first
release version) is currently in the development stage.

## Contributing

Contributions are welcomed and greatly appreciated. See [CONTRIBUTING](CONTRIBUTING.md) for details on submitting
patches and the contribution workflow.

## License

Euphoria is licensed under the Apache 2.0 license. See the [LICENSE](LICENSE) file for details.
