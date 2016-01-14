gobject-minor-mode --- Emacs minor mode for editing GObject C source code
======

In the C coding style widely used in GNOME, identifiers are written in
camel case and function arguments are aligned to the right end.  That
makes it a bit cumbersome to keep your code consistent with the style
with ordinary editor commands.

gobject-minor-mode is an Emacs minor mode intended to help editing C
source code in that style.  It mainly provides two features: text
alignment and snippet insersion.

Install
------

* Type "make"
* Copy .elc files somewhere in your load-path
* Add the following lines to ~/.emacs/init.el:

```
(autoload 'gobject-minor-mode "gobject-minor-mode" "GObject minor mode" t)
(add-hook 'c-mode-hook 'gobject-minor-mode)
```

Usage
------

* To align argument list at point: C-c C-g a
* To align function declarations in the current region: C-c C-g f

* To insert "module_object": C-c C-g c
* To insert "MODULE_OBJECT": C-c C-g C
* To insert "ModuleObject": C-c C-g C-c
* To insert custom snippets: C-c C-g s
