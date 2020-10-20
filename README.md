Jsi is a **javascript**-ish interpreter with builtin websocket-server, sqlite and **C**-extensibility. 


- Sites: [Docs](https://docs.jsish.org) | [jsish.org](https://jsish.org) | [github.com](https://github.com/pcmacdon/jsish)
- Links: [Start](./lib/web/md/Start.md) | [Index](./lib/web/md/Index.md) | [Issues](https://github.com/pcmacdon/jsish/issues)

### Quick-Start

Download a binary for [linux](http://jsish.org/bin/jsish) / [win](http://jsish.org/bin/jsish.exe):

    wget http://jsish.org/bin/jsish;  chmod u+x jsish
    wget http://jsish.org/bin/jsish.exe

Or build from [source](http://jsish.org/jsi.zip):
 
    wget http://jsish.org/jsi.zip;  unzip jsi.zip;  cd jsi;  make
    
&#x1f6a9; See [Start](./lib/web/md/Start.md).
    
### Usage

    ./jsish -W -docs /          # Jsi web-docs.
    ./jsish -S mysqlite.db      # Sqlite web-gui.
    
Compile and run a simple C-extension.

    ./jsish -c -jsc "function add(n1:number, n2:number=1):number { n1+=n2; \nRETURN(n1);\n }" Sum 
    ./jsish -e 'require("Sum",0); return Sum.add(9,3);'
