MinCSS
======

Minify CSS with Source Map support.

Forked from [CSSWring][1].
Written with [PostCSS][2].


INSTALLATION
------------

    $ npm install mincss


QUICK USAGE
-----------

    var fs = require('fs');
    var mincss = require('mincss');
    
    var css = fs.readFileSync('test.css', 'utf8');
    fs.writeFileSync('test.min.css', mincss.minify(css).css);

You can pass in options as second parameter to `mincss.minify()`. To preserve
"doc block" style comments (`/*! ... */`), set `preserveComments` option to
`true`. Likewise, to preserve some CSS hacks, set `preserveHacks` option.


CLI USAGE
---------

This package also installs a command line interface.

    $ mincss --help
    Usage:
      mincss [options] [INPUT] [OUTPUT]

    Description:
      Minify CSS with Source Map support.

    Options:
          --sourcemap          Create source map file.
          --preserve-comments  Preserve "doc block" comments.
          --preserve-hacks     Preserve some CSS hacks.
      -h, --help               Show this message.
      -v, --version            Print version information.


LICENSE
-------

MIT


[1]: https://github.com/hail2u/node-csswring
[2]: https://github.com/ai/postcss
