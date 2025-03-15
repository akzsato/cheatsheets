# cheatsheet: markdown

**Markdown** is a lightweight markup language with plain-text-formatting syntax, created in 2004 by John Gruber and Aaron Swartz. It converts text in a valid HTML code. Markdown is often used for formatting readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.

This cheatsheet supports both [CommonMark](https://commonmark.org/) (John Gruber's caninical description of Markdown's syntax) and [GFM](https://github.github.com/gfm/) (Github Flavored Markdown).

## Basics

### Heading
Headers can be specified by `#`character from H1 to H6.

    # h1
    ## h2
    ### h3
    #### h4
    ##### h5
    ###### h6

### Emphasis
Italic can be achieved using single asterisk or underscore: `*`or `_`  
Bold can be achieved using double asterisk or underscores: `**` or `__`  
Strikethrough can be achieved using double tildes: `˜˜`

    *This text will be italic*
    _This text will also be italic*
    **This text will be bold**
    __This text will also be bold__
    Italic and bold **can be _combined_**
    ˜˜This text will be strikethrough˜˜

### Control Elements

#### Horizontal Rules
To get a single horizontal rule:

    ---

#### Paragraphs and Line breaks

Paragraphs are defined by `<ENTER>` while line breaks are defined by double space at the end of the string.

Example:

This is a paragraph

This is another paragraph

This is a paragraph  
but this is a line break

### Lists

#### Unordered
Unordered lists are set using `* item`

    * item 1
    * item 2
    * item 3
        * nested unordered item
        * nested unordered item

#### Ordered
Ordered lists are set using `1. item``

    1. item 1
    1. item 2
    1. item 3
        1. nested item (3.1)
        1. nested item (3.2)

### Links

### Images
Simple image:

    ![Alternate text](image URL)

Image + Link:

    [![](Image URL)](Link URL)

### Tables


## References used by this document:
[https://en.wikipedia.org/wiki/Markdown](https://en.wikipedia.org/wiki/Markdown)

[Github Flavored Markdown Spec](https://github.github.com/gfm/)

[CommonMark](https://commonmark.org/)

[https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
