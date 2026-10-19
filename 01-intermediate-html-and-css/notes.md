# Intermediate HTML and CSS

## SVG

A very common image format on the web.

### What are SVGs?

SVGs are a scalable image format, which means they will easily scale to any size and retain their quality without increasing their filesize.

SVGS are used for 

1. Icons
2. Graphs/Charts
3. Large, simple images
4. Patterened backgrounds
5. Applying effects to other elements via SVG filters

SVG - Stands for Scablable Vector Graphics, defined by math for their shape and allow to scale proportionally with whatever size you want it. To create SVG, you'll be using XML ("Extensible Markup Language").

The benefit to it being XML is that the image will be human readable, while a normal image like jpeg if opened in a text editor is not understandable.

Example

```html

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
  <rect x=0 y=0 width=100 height=50 />
  <circle class="svg-circle" cx="50" cy="50" r="10"/>
</svg>

```

You can use that code shown above anywhere in the body of HTML and will display the same image because SVG is designed to be interoperable with HTML.

### Drawbacks

They're good for simple images but because every single bit of detail needs to be written in XML it become inefficient and you're better of using any of the binary images mentioned previous for more detailed images. So SVG's are a good option but it shouldn't be used to replace all image formats on a webpage.

### Anatomy of an SVG

```html

<div class="container">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
    <rect x=0 y=0 width=100 height=100 fill="burlywood"/>
    <path d="M 10 10 H 90 V 90 L 10 60" fill="transparent" stroke="black" stroke-width="3"/>
  <circle cx=50 cy=50 r=20 class="svg-circle"/>
    <g class="svg-text-group">
      <text x="20" y="25" rotate="10" id="hello-text">Hello!</text>
      <use href="#hello-text" x="-10" y="65" fill="white"/>
    </g>
</svg>
</div>

```

1. xmlns - stands for “XML NameSpace”. This specifies what dialect of XML you’re using. In our case, that dialect is the SVG language spec. Without it, some browsers will not render your image or will render it incorrectly.
2. viewBox - defines the bounds of your SVG. When you have to define the positions of different points of the elements in your SVG, this is what that’s referencing. It also defines the aspect ratio and the origin of your SVG. So it’s doing quite a lot! Be sure to play around with different values in the example above to get a feel for how it affects the shapes.
3. class, id
4. Elements such as <circle>, <rect>, <path>, and <text> are defined by the SVG namespace. These are our basic building-blocks. Although you can make extremely complex images with SVG, they are mostly created with just a dozen or so of these basic elements.
5. Many SVG attributes, such as fill and stroke, can be changed in your CSS.

## Tables

### HTML Tables

You can create tables by using the <table></table> tags and build the the content of tables by using elements like tr, td, etc.

