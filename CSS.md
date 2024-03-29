
# 🎨 CSS Styling Magic: Unleash the Power of Cascading Style Sheets ✨

## Background Magic 🪄

By default, a background-image in CSS is like your favorite song on repeat, playing both vertically and horizontally. But what if you want to change the tune and create a unique background for your web elements? 🎵

### Syntax
```css
background: [background-color] [background-image] [background-repeat] [background-attachment] [background-position];
```
### Example
```css
div {
  background: #ffffff url('path/to/image.jpg') no-repeat fixed center;
}
```

## Border Bonanza 🌈

Borders in CSS are more than just lines; they're your frames! Add a touch of elegance and structure to your web elements with border properties. 🖼️

### Syntax
```css
border: [border-width] [border-style] [border-color];
```
### Example
```css
div {
  border: 1px solid #cccccc;
}
```

## Padding Party 🎉

In CSS, the more padding, the merrier! Add space, comfort, and flair to your web elements with the versatile `padding` property. 🎈

### Syntax
The `padding` property can be specified using one, two, three, or four values, where each value is a length or a percentage. Negative values are invalid.

### Example
```css
div {
  padding: 10px 20px;
}
```

## Marvelous Margins 🌼

In the world of CSS, margins are like the breathing space for your web elements. They provide the perfect balance between elements and create harmonious layouts. 🌆

### Syntax
The `margin` property can be specified using one, two, three, or four values, where each value is a length or a percentage. Negative values are valid.

### Example
```css
div {
  margin: 10px 20px;
}
```

## Text-shadow Secrets 🌟

Enhance your text with a touch of magic using CSS `text-shadow`. It's like giving your words a vibrant personality! 🪄

### Syntax
```css
text-shadow: [horizontal offset] [vertical offset] [blur radius] [color];
```
### Example
```css
h1 {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
```

-->text-shadow: [horizontal offset] [vertical offset] [blur radius] [color];
eg:h1 {
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

-->box-shadow: [horizontal offset] [vertical offset] [blur radius] [spread radius] [color] [inset];
eg:div {
  box-shadow: 2px 2px 4px #cccccc;
}

-->List of several CSS text effect properties:word-break, text-overflow, word-wrap, writing-mode

-->An inline element does not start on a new line and only takes up as much width as necessary.eg:(<a>, <img> , <span>....)

-->display:table => Setting display to table makes the element behave like a table. So you can make a replica of an HTML table without using the table element and corresponding elements such as tr and td.

-->The flex-flow property is a shorthand property in CSS that combines the flex-direction and flex-wrap properties. It specifies the direction and wrapping behavior of the flex container items. flex-flow: <flex-direction> <flex-wrap>;

-->justify-content:Aligns flex items along the main axis(horizontally) of the current line of the flex container.

-->align-items:Aligns flex items along the cross axis(vertically) of the current line of the flex container.

--> CSS treats every element as a box.

-->Negative margins are used to remove unwanted margins, e.g: applying negative margin to a parent element to cancel out unwanted margin.

-->Does the margin collapse horizontally?
Ans:	No, margins never collapse horizontally, because it simply does not satisfy the conditions which make a margin collapse horizontally. Only vertical margins get collapsed.

-->What causes Margin collapsing?
Ans: Collapsing of margins happen when two vertical margins come in contact with one another. The greater margin overrides the smaller, leaving out one single margin value which is the greater one.

-->float:left,right,initial,inherit,none
-->clear:left,right,both,none,inerit
-->Giving float and clear property together inside an element is not a desirable approach. When you float an element & clear a direction, you are simply adding a page break to the document flow.

-->How can you control the behavior of floated elements?
Ans:If you don't give the "clear" property then the elements will overlap or clutter up with the existing floating elements.

------------------------------------------------------------------------------------------------
================
	SASS
================
SASS --> Syntactically Awesome StyleSheets

--> It is a platform independent CSS preprocessor language
--> Same properties with same values can be defined with variables in SASS
--> SASS is considered to be as Advanced CSS.
--> SASS Features: Variables, Mixins, Nesting, Partials, Operators, Inheritance, @rules, and more...
--> The browsers cannot read the Sass files, it can only read the CSS files.
--> Variables can be defined anywhere, but generally they are defined at the top of the styles page.
--> Sass variables can be defined for every property available in CSS.
--> With Sass, nesting of selectors that follows the same visual hierarchy of HTML is possible.
--> Overuse of nesting rules will result in overqualified CSS, that could be hard to maintain.

@import Vs @use
================
--> The @import statement makes all the variables, functions etc. globally available.
--> Same variables get overridden from the last imported file
--> Diffficult to find where the variable or function was defined
--> An alternative approach is to define a module with the @use rule
--> The namespace and the variable is separated by a "dot(.)".
--> The default namespace can be replaced with any name prefixed by 'as' keyword.

--> Some built-in modules that can be imported explicitly are:
@use 'sass:math', @use 'sass:color, @use 'sass:string' @use 'sass:list' @use 'sass:map', @use 'sass:selector', @use 'sass:meta'.

--> The @use rule is similar to the @import rule with some noticeable differences:
@use rule
============
--> Makes the variables & the functions availble within the scope of current file.
--> Avoids adding the variables & the functions to the global scope.
--> Easy to figure out where each name of the Sass file references comes from.
--> Lets you add shorter names without any risk of collision.
--> Lets you load your files only once to end up duplicating dependencies.
--> It must appear at the beginning of your file, and cannot be nested in style rules.
--> Completely deprecate the use of @import
--> Better alternative as compared to @import rule

@mixins
=========
--> By using mixins, repeatation of writing the same code lines can be reduced.
--> As a standard practice, mixins are created in a separate file, and then imported in the main Sass file.
--> It is important to remove the namespace from the mixins file, as it allows you to include them in Sass without giving any namespace.
--> Mixins help to group different styling options for re-using them in a stylesheets.
--> @mixin mixin-name($var1, $var2, ...)
--> Include the mixin file in main Sass with @include rule with mixin-name.

Sass partials rules:
====================
--> 1. The filename must start with an underscore(_).
--> 2. The filename must have the extension of ".scss/.sass"
--> 3. The file must be saved in the same path of root stylesheet.
--> It's possible to place partials in subfolders as well though.

Inheritance with Sass:
=========================
--> With the use of @extend rule, you can inherit the styles from one class to another.
--> To inherit any class properties, it's not a necessity to have a parent-child relationship.
--> Properties can be overridden & new properties can be added to the inherited class.
--> The placeholder selector(%) is used specifically with the @extend rule.
--> In Sass, the selector denoted by "&" symbol is mainly used in nested selectors in which it is defined.
--> Any complex selector, that even contains a placeholder selector isn't included in the CSS.
--> Placeholders don't clutter up the CSS, if they aren't extended.
--> Placeholders are very useful when writing a Sass library where each style rule may or may not be used.


Sass Operators:
====================
--> Different units cannot be compiled;
--> values inside the brackets are evaluated first as they have greater priority then rest.
--> With operators in Sass precise values can be defined by calculations.

--> "&" in Sass is used for nesting, to avoid repetition of code.
--> "&" allows to place the parent selector inside the child selector.
--> "user-select" specifies whether the text of an element can be selected or not.
-->"@content" rule simple way to reduce the repetitive code lines & allows an easier way for reusing & applying the changes throughout the codebase.
--> @content rule mostly used in media queries and keyframes.
--> @content rule can set any properties and as many as we want for the media rule. 
--> @content rule set the properties inside, without any clutter.

Q. Why do we need SASS?
A. With Sass you can write a clean code which is easy to understand and less CSS in a programming construct. It contains fewer code lines, is more powerful and stable, as it is an extension of CSS, making it efficient and quick for designing and development.

Q. What are modules in Sass?
A. Sass modules system or Sass module is a feature which lets you import the Sass file to main scss file, by using the @use statement.
By importing the file with @use, you are importing the file as a module, to which you have access & can be used anywhere inside the stylesheet. It does share similar functionality when compared with @import statement, but is a much better alternative than @import.

Q. What are mixins?
A. mixins are basically functions like facility in CSS, where you define a process with a name & you can pass arguments to those mixins.

----------------------------------------------------------------------------------------------
======================
BOOTSTRAP
======================
--> Bootstrap is a open source framework
--> Bootstrap is a popular front-end framework that allows you to build responsive and mobile-first websites. It provides a collection of pre-designed CSS and Javascript components that you can use to create a visually appealing and functional website quickly.

--> Different ways to implement Bootstrap:
	1. CDN link directly
	2. Download the bootstrap zip file
	3. Using Node Package Manager(npm)

--> When you are working with frameworks, we generally have the npm install command. At the same time, we see that the bootstrap files are downloaded & ther are used at the development server. But when it goes to the productions server, it is always the cdn, which works in the best way.

--> Bootstrap classes for styling container elements.

--> Use the "container" class when you want a fixed-width container that provides a responsive layout. It's suitable for most standard website layouts, where you want the content to be centered and have consistent margins on the sides.

-->Use the "container-fluid" class when you want a full-width container that expands to fill the entire viewport. It's useful for creating designs that require a full-width background, full-width images, or when you want to maximize the content's width without any margins on the sides.

--> For customizing & giving specific CSS, Bootstrap has got it all.
--> Helper class is a new concept in Bootstrap 5.
	p - padding, m - margin, h - height, w - width
	t - top, r - right, b - bottom, l - left
	y - top-bottom(y-axis), x - left-right(x-axis)

--> Values from 0-5 defined as default values in Bootstrap.
--> w-0, w-25, w-50, w-75 & w-100 are predefined width in Bootstrap.

Q. Why use Bootstrap?
A. 	1. Increase development speed
	2. Assure responsiveness
	3. Prevent repetition between projects
	4. Add consistency
	5. Ensure cross browser compatibility
	6. Large community
	7. Customizable


 

---------------------------------------------------------------------------




