# FreeCodeCamp_ResponsiveWebDesign_krishivga
A course that covers the basics and intermediate level HTML and CSS. Great refresher into web development. Course study assisted with Markdown Obsidian notes.
Please contact me at krishiv.agarwal@cgpworldwide.com or vedicseeker (on Discord) to get access to the full Zettlekasten with Obsidian wikilinks enabled.

# HTML Tags Reference

Self-closing tags do not require a `</xyz>` at the end of the tag. e.g. a non-self closing tag, `<html></html>` while a self-closing tag would be, `<meta>`. These tags are signified as **self-closing** in bold.
`<element property="value">` 

## General Properties
`class` - Gives a tag to an element that allows manipulation of elements as a group (usually in CSS).

`id` - Gives an ID to an element for referencing/CSS manipulation

`aria-label` - Labels elements that accessibility systems may have difficulty understanding.

`aria-labelledby` - Labels elements that cannot be labelled directly for accessibility purposes

`role="description"`- Role is a part of the Web Accessibility Initiative that provides a description of each element to accessibility tools to help make websites more accessible for disabled people.

## Basics 
`<!-- -->` - Comment line/block

`<html>` - The main tag of the HTML document, all HTML code must be enclosed within it.

`<head>` - Contains metadata about the document.

`<body>`  - Contains all elements of the HTML document (basically all the stuff that is visible)

`<footer>` - Defines a footer for the HTML document

## MetaData
`<link>` - Defines the relationship between the current document and an external resource. 	
- `rel` - Type of document being linked e.g. 'stylesheet'
- `href` - Link to the document e.g. 'styles.css'

`<meta>` - Defines the metadata in a HTML document. Contained within `<head>`. **Self-Closing.**
- `charset` - Specifies the encoding (type of unicode encoding, each unicode number is related to a short phrase or a letter) of the HTML document.
- `name` -  Gives a name to the meta tag.
- `content` - Specifies values associated with name attribute.

## Basic Content
`<main>` - The content in the main tag is unique to that HTML document; unlike metadata and navbars. It is where most of the content in the HTML document goes.

`<h1>`,`<h2>`...`<h6>` - Heading tag to create large text. Becomes smaller in size as the number increases.

`<p>` - Paragraph tag.

`<a>` - Defines a hyperlink.
- `href` - Specifies the destination of the hyperlink.

`<strong>` - Gives bold effect to enclosed text.

## Images and Media
`<img>` - Displays an image from a referenced location. **Self-closing**.
- `src` - Defines the source for the image
- `alt` - Defines alternative text if the image isn't being displayed

`<figure>` - Contains self-contained content from the document such as images or documents.
- `<figcaption>` - Adds a caption to the image or figure shown in the tag above.

## Sectioning and Boxes
`<header>` - Provides a place to set the introductory information of a page, usually an image and a h1 tag.

`<nav>` - Defines the main navigation links of a document. Usually put in the `<header>`

`<section>` - Creates a section inside the HTML document.

`<div>` - Used to group sections of a web page into one singular block.

`<span>` - Equivalent of div but on the inline level instead of the block level.

`<article>` - Specifies independent, self contained content. Stuff like blogs and articles.

`<label>` - Increases the 'hit' area for certain types of tags. 
- `for` - Specifies the id of the form element that the label should be bound to
 
`<fieldset>` - Draws a box and groups related elements in a form.

`<legend>` - Provides a caption for fieldset.

`<hr>` - Creates a page break. **Self-closing**

## Lists
`<ul>` creates a bulleted list.
- For each bullet point, the point must be enclosed in the `<li>` list item tag. 

```html
<ul>
	<li> Item 1 </li>
	<li> Item 2 </li>
</ul>
```

`<ol>` creates a ordered (numbered) list.
- For each bullet point, the point must be enclosed in the `<li>` list item tag. Similar to `<ul>` in code structure.

## Forms
`<form>` - Creates a HTML form for input
- `action` - Tells the form where to send the form data when it is submitted.
- `method` - Decides how information is sent over. Usually either `get` or `post`

`<input>` -  Specifies input field where users can enter data.
- `type` - Specifies the type of input.
- `id` - ID (usually text) that uniquely identifies this form element
- `name` - Specifies name for input element
- `value` - Specifies a value the element gives when selected.
- `placeholder` - Specifies placeholder text to be put inside input element
- `minlength` - defines the minimum length for a input
- `pattern` - Forces use of certain characters or sets of characters only in a password.`pattern="[a-z0-5]{8,}"`, this results in minimum length of 8, a to z allowed and numbers from 0 to 5 allowed

`<button>` - Creates a clickable button.
- `type` - Defines the type of button (values: `button`,`reset` ,`submit`)

`<select>` - Creates a dropdown that contains options. This element contains option elements within it that describe the possible options in the dropdown.

`<option>` - Displays an option in a dropdown.
- `value` - Determines the value that the option sends back to the server when selected

`<textarea>` - Provides the user with an area of text to type long answers in.
- `rows` and `cols` - Increase the vertical and horizontal area of textarea

## Additional Tips
You can group multiple input elements (for example, if you want to only make one radio button selectable out of a set) by giving all of them the same name.

You can link internally by linking the ID of an element in the `href` section of an `<a>` link. e.g. `<a href="#Homepage">Go to Homepage</a>`

# CSS Styling Reference

## Measurements
`percent` - Uses percentage of parent block, if there is no parent then it's the HTML document. e.g. `55%`

`vw`/`vh` - Uses percentage of the entire viewport/viewable space. e.g. `55wv` is 55%

`rem` - Compares in ratios to the font size of the HTML document. For example, if the font is 10 and the size is set as `0.8rem`, that means the size of the font will actually be 8. 

`em` - Compares in ratios to the current font size of the HTML document. Functions very similar to `rem`.

For most margins, padding and borders, you can remove them by putting a 0 (no need for units).

## Sizing and Font
`width` - Defines the width that the element takes.

`height` - Set the height for a block

`max-width`/`min-width`,`max-height/min-height` - Provides a maximum/minimum width/height for an element

`aspect-ratio`: Sets the aspect ratio for the element.

`font-family` - Sets a font family type for text (serif etc)

`font-style` -  Sets a font style for text (bold, italic, underline etc)

`font-size` - Sets the font size

`text-transform`: Changes property of text, such as making it all uppercase using (`uppercase`)

`font-weight`: Determines how bold the text is.

`letter-spacing`: Changes the spacing of letters in an element

`content` - Adds text, usually in specific cases with advanced selectors.

## Colours and Display
`background-color` - Sets the background colour

`background` - Accepts both image and color.

`background-image` - Defines a background image. Usually formatted as `background-image: url(url-link)`

`color` - Sets color for text

`opacity` - Controls how transparent an element is (1 to 100)

`display` - Decides the rendering (display) behavior of a element 
- `inline-block` - Keeps elements within this setting in the same line
- `flex` - Enables CSS Flexbox

## Marigns, Padding and Alignment
`margin-left`,`margin-right`,`margin-top`,`margin-bottom` -  Sets the margin on each side of the block. Generally recommended to set it to `auto`.

`margin`, `padding` - Shorthand to apply margin and padding to all sides respectively.
There are three ways to write `margin` and `padding` shorthand:
1. One value for all, `margin: 5px;`, which applies a 5px margin on all sides. Format: `margin: all_value;`
2. One value for top and bottom, one value for left and right, `margin: 3px 0;`. Format: `margin: top_bottom left_right;`
3. One value for top, one for right, one for bottom and one for left, `margin: 3px 5px 10px 0;`. Format: `margin: top_value right_value bottom_value left_value;`

`text-align` - Aligns the text to left, right or center.

## Borders and Other
`border-left-width`,`border-right-width`, `border-top-width`, `border-bottom-width`, `border-width`: Define the width of the borders of an element

`border-style`, `border-left-style`,`border-right-style`, `border-top-style`, `border-bottom-style` : Define the type of border (solid, dotted, dashed etc)

`border-left`, `border-right`,`border-top`, `border-bottom` and `border` - Allows for shorthand by setting boder width, style and colour at the same time. E.g. `border: 5px dotted black;`. Format: `border: border_width border_style border_colour;`

`border-radius` - Smoothens out edges of border.

`filter` - Adds a visual filter to change how the website looks.
- `blur(px)` - Creates a blur effect on the specified element

## Boxes
`box-shadow: offsetx offsety blurRadius(optional) color;` - Creates a shadow for the block/box of the element.
- Both `offsetX` and `offsetY` accept number values in `px` and other CSS units
- A positive `offsetX` value moves the shadow right and a negative value moves it left
- A positive `offsetY` value moves the shadow down and a negative value moves it up
- If you want a value of zero (`0`) for any or both `offsetX` and `offsetY`, you don't need to add a unit. Every browser understands that zero means no change.
- The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional `spreadRadius` value to spread out the reach of the shadow.
- Blur radius creates a blur on the shadow to avoid sharp edges
- `spreadRadius (optional)` - allows the shadow to be expanded out further

`transform` - Moves an element in a way
- `rotate(deg)` - Rotates an element

`box-sizing`: Decides the setting for the arrangement and sizing of boxes (`border-box`, `content-box`).

## Flexbox
`flex-direction`: Determines the direction of the main and cross axiom for the flexbox (Values: `row`, `row-reverse`, `column`, `column-reverse`)

`flex-wrap`:  Determines whether children of the flexbox wrap or not to the next row/column.

`justify-content`: Determines how content is aligned along the main axis (values: Center)

`align-items`: Determines how content is aligned across the cross axis (values: Center, flex-end)

`object-fit`: Modifies items in flex box to fit through stretching or cropping (value: `cover` - crops img).

`gap`: Referred to as gutter, provides a gap between each element in the flexbox (values: row-gap, column-gap)

To gain an basic understanding of flexbox: https://www.youtube.com/watch?v=K74l26pE4YA

## Functions
### Color-codes
There are three main ways to define colour in CSS:
1. Red Green Blue (RGB) - Uses the function `rgb(red,green,blue)` to set the colour values based on Red, Green and Blue. Each value is from 0 to 255.
2. Hue, Saturation and Lightness (HSL) - Uses the function `hsl(hue, saturation%, lightness%)` to set the colour based on HSL values. Hue is from 0 to 360 with 0 is Red, 120 is Green and 240 is Blue. Saturation and Lightness are in percentages of 100.
3. Hexadecimal - Uses the function `#000000` where each pair of zeroes represents Red, Green and Blue (equivalent of `#RRGGBB`). Each Hexadecimal value is between 0 to F (which means 0 to 9 and then A to F).

Opacity control can be added using alpha values.
1. Red, Green, Blue and Alpha (RGBA) - Uses `rgba(r,g,b,a)` to set opacity and colour values. Alpha values are from 0 to 1.
2. Hue, Saturation, Lightness and Alpha (HSLA) - Uses `hsla(hue, saturation%, lightness%, alpha%)` where alpha is from 0 to 100.
3. Hexadecimal - Uses two more values to represent the alpha values `#FFFFFFFF` or `#RRGGBBAA`.
### Color-gradients
`linear-gradient(angle_direction deg, colour1 stop1%, colour2 stop2%, colourx stopx%)` is a function that allows you to create linear gradients in CSS. 
- `angle_direction` - Describes the degree at which the gradient 'curves' or changes. Must have a deg after the numbers to signify being a degree e.g. `95deg`
- `colour1 stop1%`,`colour2 stop2%`...`colourx stopx%` - Determine the colour of that segment of the gradient and at what 'part' of the gradient does it stop showing the colour and focuses on the next. For example, if `red 50%` is the value, that means the colour red will be shown by the gradient until 50% of the space is covered, then it will blend into the other colour.  
- `angle_direction deg`, and two colours are necessary (the stops aren't). The rest of the specifications are optional.
- Colours can be defined by any of the [[CSS Styling Reference#Functions|colour functions]] in CSS.

### Other Functions
`rotate(deg)` - Provides degrees for rotation.

`property: max(value1, value2)...` - A CSS function that allows you to set the largest value from a set of values.

`property: min(value1, value2...)` - A CSS function that allows you to set the smallest value from a set of values.

# CSS Selectors

For more case-specific/advanced forms of selection, you may want to use [[Psuedo-classes in CSS|psuedo-classes]].
The most basic format for a CSS 'styling' is selecting an element, selecting a property of that element and giving it a value.
```CSS
element {
	property: value;
}
```

We can select multiple elements using commas.
```CSS
element1, element2, element3 {
	property: value;
}
```

We can select elements that are *children* (inside another element) by using > operator or by simply referencing them as sub-elements. The program below only targets elements of type C which are within elements of type B which are in elements of type A. Multiple elements can still be listed out as shown in the second example.
```CSS
element_a > element_b > element_c {
	property: value;
}
```

This is easily explained with an example.
```CSS
form > label > p {
	color: black;
}
```

## Advanced selectors
We can select the IDs and the classes of specific elements by referencing them.
```CSS
#ID {
	property: value;
}

.class {
	property: value;
}
```

Additionally, we can also filter our selection by a certain element property.
```CSS
input[type="submit"] {
	property: value;
}
```

You can also decide to select *everything* using the * selector.
```CSS
* {
	property: value
}
```

A few more advanced selectors include `::before` and `::after` that add content before and after each `<p>` element.
```CSS
p::before {
	property: value;
}
```
# CSS Psuedo-Classes
For more Pseudo-Classes, you may want to look at https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes#user_action_pseudo-classes.

## Anchor Psuedo-Classes
You can target different states of a HTML link.
```CSS
/* unvisited link */  
a:link {
	color: #FF0000;
}  
  
/* visited link */  
a:visited {
	color: #00FF00;
}  
  
/* mouse over link */  
a:hover {
	color: #FF00FF;
}  
  
/* selected link */  
a:active {
	color: #0000FF;
}
```

## Advanced Psuedo-Classes
You can create special interactions on hover by creating, for example, a `<p>` element as a tooltip each time someone hovers over another element.
```CSS
div:hover p {
	display: block;
}
```

