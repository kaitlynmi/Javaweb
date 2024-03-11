# HTML cheat sheet

# HTML 
## Tags
```HTML
<html>
    <head>
        <title></title>
    </head>
    <body>
    </body>
</html>
```

- Labels are case insensitive
- Attributes can use either '' or "" 
  
### Image `<img>`
#### Attributes
- src: resource url (exact/relative)
  - 绝对路径
    1. 绝对磁盘路径
    2. 绝对网络地址
         - 必须联网
  - 相对路径
    - ./ current folder 
    - ../ 上一级目录
- width (px/percentage)
- height (px/percentage)
- alt: alternative title
- 
### Heading `<h1>`-`<h6>`

### Break `<hr>`

### Span `<span>`
**inline** container used to mark up a part of a text

### `<div>`
A container

### Hyperlink `<a>`
```html
<a href="url" target="_self">link text</a>
```
- href: the link's destination
- target: 
  - _self: default, open on current page
  - _blank: open on a new page
  
### Video `<video>` and Audio `<video>`
- `src` resource url
- `controls` adds video controls, like play, pause, and volume.
- `width` and `height`
  
### Paragraph `<p>`

### Bold `<b>` / `<strong>`

### Table `<table>`
#### `<tr>`
a table column

Attributes:
- border
- width
- cellspacing
  
#### table cell `<td>`
stands for "table data".
table head: `<th>`

### Form `<form>`
a container for different types of input elements
Attributes:
- action: form-handler, where to send data
  - submit to current page on default
- method: GET/POST
  -  `method="GET"` : fetching data 
     -  encoded and **appended to the URL**  in the address bar
        -  `?key=value&key2=value2` format
     -  length of a URL is limited
     -  can be bookmarked and cached
  -  `method="POST"`: submitting data
     -  included in the body of the HTTP request
        -  more secure 
     -  no practical size limit
     -  cannot be bookmarked and aren't cached
     -  used for operations that result in a change on the server
#### Form Elements
  has to include attribute `name` to submit
##### `<input>`

##### `<label>`
##### `<select>`
##### `<textarea>`


# CSS

### Using CSS
- Inline - by using the style attribute inside HTML elements
  - `<p style="color:red;">A red paragraph.</p>`
  - <p style="color:red;">A red paragraph.</p>
- Internal - by using a `<style>` element in the `<head>` section
```HTML
<head>
<style>
    body {background-color: powderblue;}
    h1   {color: blue;}
    p    {color: red;}
</style>
</head>
```
- External - by using a `<link>` element to link to an external CSS file
```HTML
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```
```css
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}z
```

### CSS Selector
- Tag Selector
- ID Selector
  - HTML: `<span id="sid">ID Selector</span>`
  - CSS: `#sid {color: red}`
- Class Selector
  - HTML: `<span class="cls">Class Selector</span>`
  - CSS: `.cls {color: red}`
  
Priority： ID > Class > Tag

### Colors 

#### Color Names
- ex. green, red, blue
#### Color Value
- RGB
  - the value of red, green, blue. each 0 -255
    - ex. rgb(255, 99, 71)
- HEX   
  - \# prefix
  - each pair of number represent a value of RGB in hexadecimal
    - ex. #ff6347

### Box Model
<img src="img/box_model.png">

### Text Attributes

#### `font-size`
- Absolute size:px
  - default is 16px
- Relative size:
  - Sets the size relative to surrounding elements

#### `text-decoration`
The text-decoration property is a shorthand property for:

 - text-decoration-line (required)
   - `none`,`underline`...
 - text-decoration-color (optional)
 - text-decoration-style (optional)
 - text-decoration-thickness (optional)

#### `line-height`
#### `text-indent`
- space token: `&nbsp;`
#### `text-align`