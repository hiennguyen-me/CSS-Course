/************ CSS1 ****************/

CSS - Cascading Style Sheets

- Serif typefaces: have small decorative lines: Times New Roman, Georgia, Rockwell
- Sans serif typefaces have no decorative lines: Verdana, Arial, Helvetica
- Use a generic font family as the last option, always declare generic fonts without quotes.
- Box-sizing property: 
	+ content-box: Default. The width and height properties (and min/max properties) includes only the content. Border, padding, or margin are not included
	+ border-box: The width and height properties (and min/max properties) includes content, padding and border, but not the margin
	+ initial:  Sets this property to its default value.
	+ inherit: Inherits this property from its parent element

/************ CSS2 ****************/

## 1. Combination selectors:
- There are four different combinators in CSS3:
	+ descendant selector (space)
	+ child selector (>)
	+ adjacent sibling selector (+)
	+ general sibling selector (~)
- Ex: 
	+ section > a: only a tags that a section's child
	+ h1 + p : one paragraph after h1
	+ h1 ~ p : all paragraph after h1
	+ .one.two : any element with both class name

## 2. Pseudo-class selectors
- `:first-child`: the first child element of its parent
- `:last-child`: the last child element of its parent
- `p:first-of-type`: the first paragraph
- `p:last-of-type`: the last paragraph
- `:nth-child()`: select one or more child elements based on the order within the parent container. Elements are seleccted by passing in an argument in one of three ways: keyword, number, algebraic expression.
- `:nth-of-type`: the same arguments
EX:
	+ :nth-child(odd) / :nth-child(even)
	+ :nth-child(3)
	+ :nth-child(2n+1)

## 3. Pseudo-element selectors
- :before, :after: generate elements that are inserted before or after the selected element.
- Pseudo-element don't become  part of the DOM
- Only used ofr presentational effects.
- Always be used with "content" property
EX: 
	element:before{
		content: "Cotent to be inserted";
	}

## 4. Overflow:
- hidden or scroll

## 5.Position:
- Arrange elements relative to the default page flow or browser vieport
- 5 values: relative, absolute, fixed, static, inherit
	+ Static: default value, elements not positioned at all
	+ Inherit: inherits value from ancestor element
	+ Relative (occupy space): Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.
	+ Absolute (don't occupy space): is positioned relative to the nearest positioned ancestor. However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling. 
	+ Fixed (don't occupy space): is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element.A fixed element does not leave a gap in the page where it would normally have been located.
- Offset properties: top, right, bottom, left

## 6. Overlapping elements:
- When elements are positioned, they can overlap other elements.
- The z-index property specifies the stack order of an element (which element should be placed in front of, or behind, the others).
- An element can have a positive or negative stack order.
- An element with greater stack order is always in front of an element with a lower stack order.

## 7. Float, Display, Position?
- Float: If you have flexible content, like an image surrounded by text, float is a good option.
- Display: used to align blocks on a page similar to floats, but just remember the extra space that shows between elements
- Position: It is also useful for positioning elements that exist outside of the natural page flow, such as a fixed navigation bar, or for aligning elements in a specific spot on the page.

## 8. Icon Fonts
- Fonts Awesome

## 9. CSS Background
- Background-color:
- Background-image: url(image.jpg);
- background-repeat: no-repeat/repeat-x/repeat-y
- background-attachment: scroll/fixed;
- background-position: 0px 0px;
- Can use shorthand 

## 10. Alpha transparency and gradients:
- RGBA and Alpha transparency:
	+ RGBA: specify the opacity of a color 
- Gradients: 2 types:
	+ Linear Gradients (goes down/up/left/right/diagonally). 
		- background: linear-gradient(direction, color-stop1, color-stop2 )
	+ Radial Gradients (Defined by their center)
		- background: radial-gradient(shape size at position, start-color, .., last-color)

## 11. Reset CSS
- Reset.css remove defaults styles
- Normalize.css makes defaults styles more consistent

## 12. Responsive design:
- Website: 1024 x 768; 1280 x 1024
- 2 approaches: 
	+ progressive enhancement
		* Design for modern browsers first
		* Provide fallbacks for unsupported features
		* Ensure basic functionality works for older browsers.
	+ graceful degradation
		* Focus on content and accessibility first
		* Create base-level experience first
		* Add advance features for enhancements.
	
## 13. Creating flexible and fluid layouts:
- Flexible layouts:
	+ Start with fluid Css before adding responsive CSS
	+  Make the content fit relative to its container
	+ Don't rely only  on defined devices sizes
	+ Use percentage-based widths for page components
	+ Use min- or max- widths to add constraints to the layout while maintaining flexibility
	+ Use percentage-based widths and min- /max- values together.
- Fluid layouts: are relative, but teh content and components only wider and narrower
- Media Queries:
	+ Media queries can be used to check many things, such as:
		* width and height of the viewport
		* width and height of the device
		* orientation (is the tablet/phone in landscape or portrait mode?)
		* resolution
  	+ Media syntax: 
  		@media not|only mediatype and (expressions) {
    		CSS-Code;
		}s
		* Can also have different stylesheets for different media: <link rel="stylesheet" media="mediatype and|not|only (expression)" href="mystylesheet.css">
  	+ Media Types:
  		* print: Used for printers
  		* speech: Used for screenreaders that "reads" the page out loud
  		* screens: Used for computer screens, tablets, smart-phones etc
  		* all: Used for all media type devices
  	+ Meddia Features:
	  	* Has the same syntax as CSS properties
	  	* Used to describe the requirements of a device
	  	* Specifies a single feature of the device 

## 14. <Meta> tags:
- Metadata is data (information) about data.
- The <meta> tag provides metadata about the HTML document. Metadata will not be displayed on the page, but will be machine parsable.
- Meta elements are typically used to specify page description, keywords, author of the document, last modified, and other metadata.
- The metadata can be used by browsers (how to display content or reload page), search engines (keywords), or other web services.
<meta name="viewport" content="width=device-width, initial-scale=1.0">
- A <meta> viewport element gives the browser instructions on how to control the page's dimensions and scaling.
- The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).
- The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.

## Others: 
- flex property: Let all the flexible items be the same length, regardless of its content: