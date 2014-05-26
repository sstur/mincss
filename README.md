mincss
======

Minify CSS. That's all.

Written with [PostCSS][1].


INSTALLATION
------------

    $ npm install mincss


QUICK USAGE
-----------

    #!/usr/bin/env node
    
    'use strict';
    
    var fs = require('fs');
    var mincss = require('mincss');
    
    var css = fs.readFileSync('test.css', {
      encoding: 'utf8'
    });
    fs.writeFileSync('test.min.css', mincss.minify(css).css);

If you want to preserve some CSS hacks, set `preserveHacks` property of
this module to `true`.


CLI USAGE
---------

This package also installs a command line interface.

    $ mincss --help
    Usage:
      mincss [options] [INPUT] [OUTPUT]
    
    Description:
      Minify CSS. That's all.
    
    Options:
          --sourcemap       Create source map file.
          --preserve-hacks  Preserve some CSS hacks.
      -h, --help            Show this message.
      -v, --version         Print version information.


LICENSE
-------

MIT


[1]: https://github.com/ai/postcss
