# Render Source

### Render source code to HTML, RTF or PDF

This code was adapted from https://github.com/foiegreis/Py2pdf/blob/main/py2pdf.py by Greta Russi (@foiegreis) 2024 and modified extensively to support rendering an entire codebase to a selected output format. Requires having **Ghostscript** and **Enscript** installed and available on the path for this program to function. Works on Mac OSX (brew) and Linux (apt).

I realised I am using f-strings in a way that only works on Python 3.13 

usage: render_source.py \[-h\] -i INPUT -o OUTPUT -s SUFFIX --target {pdf,rtf,html} \[--single\] \[--flatten\]

* `-i` input filename or directory (recursive traversal)
* `-o` output path
* `-s` filename suffix to process. Note that certain filenames or suffixes are mapped to `enscript` language for syntax coloring. Note that files like "Dockerfile" and "Makefile" can work here too.
* `--target` output rendering format - supports `pdf`, `rtf` and `html`
* `--single` to process a single file instead of traversing directories
* `--flatten` allows you to map the output path to a prefix on the output filenames. This is useful when you have files with the same names in different subdirectories.


   

