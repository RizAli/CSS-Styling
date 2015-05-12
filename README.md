CSS Styling
------------

Resources:

```
Mozilla Developer Network
https://developer.mozilla.org/en-US/

WebPlatform
https://www.webplatform.org/

W3.org
http://www.w3.org/TR/css3-color/

for up-to-date browser support
http://caniuse.com/
```

Methods of applying css
--------------------------
author styles
Three methods to add author styles to a page

Inline styles
-------------
good for mocking and debugging only

```
e.g <body style= "background-color: orange;">
```

we write directly inside an elemet tag using style attribute.
body element style attribute



Internal styles
------------------
sometimes used just for feature testing but not for big websites because we will endup duplicating lots of styling on several pages, which is not a good practice. it can make maintence and development fairly difficult.

a tag inside html file such as
```
 <title>Lake Tahoe</title>
    <style>
    p {
      font-size: 20px;
      font-weight: bold;
    }

    h1 {
      font-size: 50px;
      color: firebrick;
    }

   header {
      background-color: orange;
    }

    body {
      background-color: white;
    }

    </style>

```

External stylesheets
---------------------
It is most the effecient method for styling. We can change the look of our website just by changing one file.

Create style.css file in the css folder

In your html head tag link your stylesheet
example: <link rel="stylesheet" href='css/style.css'>


CSS import statement
--------------------
another method of using external stylesheets


one way we can import file in our html document.

after title and link add the style tag in your html file........
----------------------------------------------------------------
note: import-styles.css file has been created and saved in the css folder.

```
<title> Lake Tahoe</title>
  <link rel="stylesheet" href="css/style.css">
  <style>
      @import "import-styles.css";
  </style>
```
or completely remove the style tag and add import statement at the top of css file.
-----------------------------------------------------------------------------------
@import "import-styles.css";


CSS Rules or Rules Set
----------------------
it is made of two things Selector and a declaration block

Declaration is defined in curley braces and is consist of property name and a value

```
selector {
  property: value;
}
```

Defining Universal Selectors
----------------------------

```
/* defining Universal selector*/

* {
  margin: 0;
  padding: 0;
  color: green;
}

```
Defining Element Selectors
---------------------------

```
/* defining element selector*/
/* Any html tag can be used as selectors in css */
p {
  color: white;
  background-color: lightblue;
}

header {
  background-color: orange;
}

```

Defining ID Selector:
---------------------

To declare the id symbole we will use "#" key. ID name could be anything but it's important and good practice to give meaningful names to the id's.
'An element can only have one ID and a page can have only one element with the same id name'


ID's also have browser's functionality they can be used as 'fragment identifiers' for creating landmarks and anchors on pages.

```
'#primary-content {
  border: 3px solid red;
}'

and in html file
<div ='primary-content'>

```

Defining Class Selector:
-----------------------
ID's are unique and are used to identify one element on the page whereas Class can be used to classify and targe more than one element on the page.
In other words multiple elements can share the same class. This ability of classes makes it more flexible than ID's.

An important point to note that ID carry more weight then class, it can overwrite the styles defined because the ID are more specific to the element.
hence it is important not to share the same properties between class and ID's.

to define class selector instead '#'' we use '.' for example

```
css file

.primary-content {
  border: 3px solid red;
}

in html file instead

<div class='primary-content'>
```

Descendent Selectors
---------------------
CSS allows us target elements based on their relationship in the html document. Descendent selectors makes our selector more specific.
In the following example notice span element is nested inside header element. This means span element is descendent of the header element.
To select the descended element we will need to use two or more selectors seperated by white space.

```
  html file

  <header id="top" class="main-header">
    <span>Journey through the Sierra Nevada Mountains</span>
    <h1>Lake Tahoe, California</h1>
  </header>


  css file
...
  header span {
   color: white;
   font-size: 26px;
}
...

```
Descendent selectors are not limited to the type selectors only. We can be pretty specific with class and id selectors.

```
for the same example above the header element can be swaped with the class

in css file

.main-header {
  background-color: orange;
}

.main-header span{
  color: white;
  font-size: 26px;
}

```

Pseudo Classes:
--------------
Pseudo-classes are similar to classes. But they are not explicitly defined in an elements class attribute. Unlike type, ID and class selectors, pseudo-classes can target elements dynamically based on user interaction, an element state or more. for example visited link

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

```
selector:pseudo-class {
  property: value;
}

example:

a:hover {
  color: forestgreen;
}

a:link {
  color: orange;
}

a:visited {
  color: lightblue;
}

a:hover {
  color: forestgreen;
}

a:active {
  color: lightcoral;
}

a:focus{
  color: white;
  background-color: orange;
}



```

CSS Data Types
---------------:
Mozilla Developer Network
resource: https://developer.mozilla.org/en-US/docs/tag/CSS%20Data%20Type


CSS datatypes simply means a type of CSS value
Example:
Color values, integers, numbers, percentages etc.
Images, gradient, uri datatype



CSS px is an Angular Measurement
----------------------------------

css pixels units in css doesn't have anything to do with screen pixels. The pixel in css is more about pixel density of the viewing device.
It is actually a non-linear angular measurement. To read more click link: http://inamidst.com/stuff/notes/csspx

css percentage unit are commonly used since they allow fluid sizing of elements relative to their container.

```
https://developer.mozilla.org/en-US/docs/tag/CSS%20Data%20Type

resource: https://developer.mozilla.org/en-US/docs/Web/CSS/percentage
```
### Relative Length Units:
The Default font size for many browsers is 16px.
1em value is equal to the font size value of the parent element.

```
https://developer.mozilla.org/en/docs/Web/CSS/length#Relative_length_units


body {
  font-size: 1em;
}

this is same as

body {
  font-size: 16px;
}

```

### Conversion of Pixel value to em value. We can use a simple formulae

em sizes are very useful because it can adapt the other font sizes. This way child elements are able to resize proportinally based on the parent font size.

```
h1 {
  font-size: 5.625em; /*  90px / 16px */
  color: white;
}

```

Colors in CSS
--------------

colors in css can be defined as keywords, hexadecimal value and RGB values.

resource: https://developer.mozilla.org/en-US/docs/Web/CSS/color_value

Hex values are defined by # sign followed by six hexadecimal characters.

```
#main-footer {
  padding-top: 60px;
  padding-bottom: 60px;
  border-bottom: solid 10px #ffa949;
}

to define as rgb

a:link {
  color: rgb(255,169,73)
}

```

Text and css
------------
css has several properties for defining text.
```
source: https://developer.mozilla.org/en-US/docs/Web/CSS/text-align
```

Font Family
-----------
It is always good to use web safe font as they are installed in any computer.
font stack can be defined, browsers goes through all the fonts and checks if the end user has the font installed.
```
source: https://developer.mozilla.org/en-US/docs/Web/CSS/font-family
http://www.cssfontstack.com/


body {
  color: #878787;
  margin: 0px;
  font-size: 1em;
  font-family: Helvetica, Arial, sans-serif;  /* Font stack defined */
}

```

CSS line Height
---------------
Line height defines the vertical spacing of the paragraphs. We can increase or decrease the line height.


The box Model
--------------

The box model defines the amount of space each element takes upon the page.


content area
padding area -
border area - the outer most part of the box
margin area - margin area exits out side the box




