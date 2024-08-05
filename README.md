geany-lsp
---------

This is a development repository of the LSP plugin for Geany. The plugin
provides the following LSP features:

* Autocompletion
* Function signagure
* Diagnostic messages
* Code lenses
* Semantic token type highlighting
* Hover popup
* Go to symbol definition/declaration
* Go to type definition
* Swap header/source
* Find references
* Find implementations
* Navigation to document/project symbols, files, and line numbers
* Code formatting
* Identical symbol highlighting
* Document symbol renaming
* Project-wide renaming

The plugin API of Geany currently does not support modifying document symbols
in the sidebar so the Symbols tab contents is based on Geany's ctags
symbols instead of LSP symbols.

Main development of the plugin happens in this repository so please report
bugs here. In addition, the plugin code will be uploaded to the
[geany-plugins](https://github.com/geany/geany-plugins) before every release
so if you are interested in the release version only, you can get it from
there.

For building the plugin, you need to compile and install the latest Geany
version (2.1) from git master. Then, you can build and install the LSP plugin
using either
```
./autogen.sh && make && sudo make install
```
or
```
meson setup build && cd build && ninja && sudo ninja install
```

More information about the supported features and configuration can be found
* [in the plugin documentation](https://github.com/techee/geany-lsp/tree/master/lsp/README)
* [in the configuration file](https://github.com/techee/geany-lsp/blob/master/lsp/data/lsp.conf)

---

Jiri Techet, 2024
