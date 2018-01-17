# vscode-markdown-imsize

Adds [markdown-it-imsize](https://www.npmjs.com/package/markdown-it-imsize) syntax support to VS Code's built-in Markdown preview. Overloads original markdown-it image renderer.

## Features

Using `markdown-it-imsize` syntax the size of images can be specified in the markdown document. When viewing the document using VS Code's built-in Markdown preview, the image file will be resized accordingly.

### Syntax

#### Using pixel for image size specification

```md
![sample](sample-image.png =200x100)
```

is interpreted as

```html
<p><img src="sample-image.png" alt="sample" width="200" height="100"></p>
```

*Note:* Width or height can be omitted. In this case the aspect ratio is honored during resize.

```md
![sample](sample-image.png =200x)
or  
![sample](sample-image.png =x100)
```

#### Using percentage for image size specification

```md
![sample](sample-image.png =50%x)
```

is interpreted as

```html
<p><img src="sample-image.png" alt="sample" width="50%"></p>
```

### Examples

Playing cat - Resized from 800x600 to fixed size of 200x150 pixel  
`![200x150](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =200x150)`  
![200x150](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =200x150)

Playing cat - Resized from 800x600 to a fixed height of 100 pixel  
`![x100](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =x100)`  
![x100](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =x100)

Playing cat - Resized from 800x600 to a fixed width of 100 pixel  
`![100x](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =100x)`  
![100x](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =100x)

Playing cat - Resized from 800x600 to a variable width of 100%  
`![100%x](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =100%x)`  
![100%x](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG> =100%x)

Playing cat - No image size specified.
`![Default](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG>)`  
![Default](<https://upload.wikimedia.org/wikipedia/commons/thumb/3/33/Spielendes_K%C3%A4tzchen.JPG/800px-Spielendes_K%C3%A4tzchen.JPG>)

## Release Notes

### 0.0.1

Initial release suporting markdown-it-imsize syntax
