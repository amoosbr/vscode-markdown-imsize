# vscode-markdown-imsize

[![](https://vsmarketplacebadge.apphb.com/version/amoosbr.markdown-imsize.svg)](https://vsmarketplacebadge.apphb.com/version/amoosbr.markdown-imsize.svg)

Adds [markdown-it-imsize](https://www.npmjs.com/package/markdown-it-imsize) syntax support to VS Code's built-in Markdown preview. Overloads original markdown-it image renderer.

## Features

Using `markdown-it-imsize` syntax the size of images can be specified in the markdown document. When viewing the document using VS Code's built-in Markdown preview, the image file will be resized accordingly.

### Syntax

#### Using pixel for image size specification

```markdown
![sample](sample-image.png =200x100)
```

is interpreted as

```html
<p><img src="sample-image.png" alt="sample" width="200" height="100"></p>
```

*Note:* Width or height can be omitted. In this case the aspect ratio is honored during resize.

```markdown
![sample](sample-image.png =200x)
or  
![sample](sample-image.png =x100)
```

#### Using percentage for image size specification

```markdown
![sample](sample-image.png =50%x)
```

is interpreted as

```html
<p><img src="sample-image.png" alt="sample" width="50%"></p>
```

### Examples

![](https://raw.githubusercontent.com/amoosbr/vscode-markdown-imsize/master/docs/playing-cat-example1.png)
![](https://raw.githubusercontent.com/amoosbr/vscode-markdown-imsize/master/docs/playing-cat-example2.png)

## Release Notes

### 0.0.2

Added example images

### 0.0.1

Initial release suporting markdown-it-imsize syntax
