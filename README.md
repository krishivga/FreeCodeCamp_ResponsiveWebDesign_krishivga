# FreeCodeCamp_ResponsiveWebDesign_krishivga
A course that covers the basics and intermediate level HTML and CSS. Great refresher into web development. Course study assisted with Markdown Obsidian notes.

# HTML Tags reference
Most tags require a closing tag, e.g. `<html>` requires `</html>`. If **self-closing** is mentioned, the tag does not require a closing tag.

- `<!DOCTYPE html>` - At the start of the document, this declares that the document is a HTML document. **Self-closing**.
- `<html>` - The main tag of the HTML document, all HTML code must be enclosed within it.
- `<head>` - Contains metadata about the document, comes after `<html>` and before `<body>`
- `<meta>` - Defines the metadata in a HTML document. Contained within `<head>`. **Self-Closing.**
	- `charset` - Specifies the encoding (type of unicode encoding, each unicode number is related to a short phrase or a letter) of the HTML document.
	- `name` -  Gives a name to the meta tag
		- `viewport` - Allows for control over the viewport aka the area that the website is displayed in
			- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` is a great setting to create basic dynamic design for websites.
	- `content` - Specifies values associated with name attribute
- `<title>` - Text enclosed becomes the title of the webpage in the tab bar.
- `<body>`  - Contains all elements of the HTML document (basically all the stuff that is visible)
- `<main>` - The content in the main tag is unique to that HTML document; unlike metadata and navbars. It is where most of the content in the HTML document goes.
- `<h1>,<h2>,<h3>...<h6>` - Heading tag to create large text. Becomes smaller in size as the number increases.
- `<!-- -->` - Comment line/block
- `<p>` - Paragraph tag.
- `<a>` - Defines a hyperlink.
	- `href` - Specifies the destination of the hyperlink.
- `<section>` - Creates a section inside the HTML document
- `<ul>` creates a bulleted list.
	- For each bullet point, the point must be enclosed in the `<li>` list item tag. 
```html
<ul>
	<li> Item 1 </li>
	<li> Item 2 </li>
</ul>
```
- `<figure>` - Contains self-contained content from the document such as images or documents.
	- `<figcaption>` - Adds a caption to the image or figure shown in the tag above.
- `<img>` - Displays an image from a referenced location. **Self-closing**.
	- `src` - Defines the source for the image
	- `alt` - Defines alternative text if the image isn't being displayed
- `<ul>` creates a ordered (numbered) list.
	- For each bullet point, the point must be enclosed in the `<li>` list item tag. Similar to `<ul>` in code structure.
- `<strong>` - Gives bold effect to enclosed text.
- `<form>` - Creates a HTML form for input
	- `action` - Tells the form where to send the form data when it is submitted.
	- `method` - Decides how information is sent over. Usually either `get` or `post`
- `<label>` - Increases the 'hit' area for certain types of tags. 
	- `for` - Specifies the id of the form element that the label should be bound to
- `<fieldset>` - Draws a box and groups related elements in a form.
- `<legend>` - Provides a caption for fieldset.
- `<input>` -  Specifies input field where users can enter data.
	- `type` - Specifies the type of input.
	- `id` - ID (usually text) that uniquely identifies this form element
	- `name` - Specifies name for input element
	- `value` - Specifies a value the element gives when selected.
	- `placeholder` - Specifies placeholder text to be put inside input element
	- `minlength` - defines the minimum length for a input
	- `pattern` - Forces use of certain characters or sets of characters only in a password.`pattern="[a-z0-5]{8,}"`, this results in minimum length of 8, a to z allowed and numbers from 0 to 5 allowed
- `<button>` - Creates a clickable button.
- `<footer>` - Defines a footer for the HTML document
- `<link>` - Defines the relationship between the current document and an external resource.
- `<div>` - Used to group sections of a web page into one singular block.
	- `id` - ID that uniquely identifies this element
- `<article>` - Specifies independent, self contained content. Stuff like blogs and articles.
- `<hr>` - Creates a page break. **Self-closing**
- `<select>` - Creates a dropdown that contains options. This element contains option elements within it that describe the possible options in the dropdown
	- `<option>` - Displays an option in a dropdown.
		- `value` - Determines the value that the option sends back to the server when selected
- `<textarea>` - Provides the user with an area of text to type long answers in.
	- `rows` and `cols` - Increase the vertical and horizontal area of textarea

# CSS Tags reference
- `background-color` - Sets the background colour
- `text-align` - Aligns the text to left, right or center.
- `width` - Defines the width that the element takes.
- `margin-left`/`margin-right` -  Sets the margin on each side of the block. Generally recommended to set it to `auto`.
- `background-image` - Defines a background image. Usually formatted as `background-image: url(url-link)`
- `background` - Accepts both image and color.
- `display` - Decides the rendering (display) behavior of a element
	- `inline-block` - Keeps elements within this setting in the same line
- `padding` - Provides padding (distance from the edges of the box) to an element
- `max-width`/`min-width` - Provides a maximum/minimum width for an element
- `font-family` - Sets a font family type for text (serif etc)
- `font-style` -  Sets a font style for text (bold, italic, underline etc)
- `font-size` - Sets the font size
- `height` - Set the height for a block
- `border-color` - Sets the border color for a block
- `margin-top`, `margin-bottom` - Sets the margin for a block
- `color` - Sets color for text
- `margin`, `padding` - Shorthand to apply margin and padding to all sides respectively.
	- You can also set one value for top bottom and one value for left and right `padding: 10px 15px;` puts 10 pixels of padding on the top and bottom and 15 pixels on the left and right. Also, for all margin and padding you can set it to auto.
- `opacity` - Controls how transparent an element is (1 to 100)
- `border-left-width`,`border-right-width`, `border-top-width`, `border-bottom-width`, `border-width`: Define the width of the borders of an element
- `border-style`, `border-left-style`,`border-right-style`, `border-top-style`, `border-bottom-style` : Define the type of border (solid, dotted, dashed etc)
- `border-left`, `border-right`,`border-top`, `border-bottom` and `border` - Let you set width style and color at the same time; `border-left: width style color;`
- `box-shadow: offsetx offsety blurRadius(optional) color;` - Creates a shadow for the block/box of the element.
	- both `offsetX` and `offsetY` accept number values in `px` and other CSS units
	- a positive `offsetX` value moves the shadow right and a negative value moves it left
	- a positive `offsetY` value moves the shadow down and a negative value moves it up
	- if you want a value of zero (`0`) for any or both `offsetX` and `offsetY`, you don't need to add a unit. Every browser understands that zero means no change.
	- The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional `spreadRadius` value to spread out the reach of the shadow.
	- Blur radius creates a blur on the shadow to avoid sharp edges
	- `spreadRadius (optional)` - allows the shadow to be expanded out further

## Units
Instead of using percents for area, you can also use viewport height (abbreviated as vh) of which 1% is equal to 1% of the viewport height.
`rem` determines size of things relative to font size of HTML document

## Psuedo-Selectors
- `a:visited` - If the link has been clicked
- `type selector:hover` - If the element has been hovered on
- `a:active` - If the link is actively being clicked on

## Colors
For colour manipulation, you can use the `rgb(r,g,b)` function. You can also use hexadecimal `#00FF00 (Green)` or hue, saturation and lightness `hsl(hue, saturation%, lightness%)` (note, for saturation and lightness the percentage is required).

For opacity control in your colour selection, you may use RGBA which is the same except it has an extra argument for opacity `background-color: rgba(255,255,255,.5); (White)`. HSLA for hsl and you can add another two character set setting for hex (#00FF00FF (last two fs are the alpha))

`linear-gradient(angle_direction deg,colour1 stop1, colour2 stop2, colourn stopn)` is a function that allows you to create linear gradients in CSS. The angle direction determines the angle in which the gradient will switch to another colour, and must be defined with a `deg` afterwards such as `90deg`. Colours can be defined in any viable CSS method such as rgb, hsl or hex and stops can be added to determine how much of the gradient is being used up by one colour. More than two colours can be added, but two is the minimum.

# CSS Styling reference
Most tags require a closing tag, e.g. `<html>` requires `</html>`. If **self-closing** is mentioned, the tag does not require a closing tag.
- `<style>` - Creates a stylesheet for CSS styling. Not necessary if doing CSS on a separate CSS only file.
- `/* */` - Comment
To create styling for a specific tag:
```CSS
element {
	property: value;
}
```
Note: Instead of selecting all versions of a element, if you only want to select a specific one you can refer to its ID using the `#idname` instead of `element` in the type selector. 
Additionally, you can select the class by `.classname` instead of IDname or element. A class is basically a grouped set of elements.
E.g.
To align all H1 text to the center, we can:
```CSS
h1 {
	text-align: center;
}
```
This method of styling HTML documents uses something called *type selectors* that choose the element type and provide formatting instructions.
Additionally, type selectors can format multiple types at the same time.
```CSS
element1, element2, element3 {
	property: value;
}
```
This property will get this value across all the selected types.

When adding values to properties of elements, you can add alternative values if the original isn't found.
```CSS
h1, h2 {

font-family: Impact, serif;

}
<!-- Here, Serif is the fallback -->
```

You can also create pseudo-selectors that only activate in certain cases, such as when a link is clicked.
```CSS
a:visited {

color: grey;

}
```
For advanced colour manipulation, you can use the `rgb(r,g,b)` function. You can also use hexadecimal `#00FF00 (Green)` or hue, saturation and lightness `hsl(hue, saturation%, lightness%)` (note, for saturation and lightness the percentage is required).

You can also create 'type' selectors that only affect one type of an element. For example, if we want to customize all submit buttons we can select:
```CSS
input[type="submit"] {

}
```

You can select a 'class' of elements using:
```CSS
.classname {
property: value;
}
```

You can select an id with:
```CSS
#ID {
property: value;
}
```
