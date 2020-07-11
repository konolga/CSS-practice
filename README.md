# CSS-practice and my comments for the course:
[udemy] CSS - The Complete Guide 2020 (incl. Flexbox, Grid &amp; Sass)



### Combinators

`+` Second element comes immediately after first element and share the same parent

`~` Second element comes anywhere after first element and share the same parent

`>` Second element is a direct child of first element

` (space)` Second element is a descendant of the first element




### Block-level vs Inline Elements

Block-level elements are rendered as a block and hence take up all the available horizontal space: `<div> , <section> , <article> , <nav>, <h1>, <p>`

Inline elements on the other hand only take up the space they require to fit their content in. Setting a width  or height, margin-top  and margin-bottom  on an inline element also has no effect

You can set display: inline-block  to merge behaviors:` <a> , <span> , <img>`




### Pseudo classes and elements
`:` pseudo-class => special state of an element
`::` pseudo-name => specific part of an element

box-sizing : https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing
More on height & width: https://www.w3schools.com/css/css_dimension.asp

The display  Property: https://developer.mozilla.org/en-US/docs/Web/CSS/display



### Positioning
Positioning Context (anchor):

`static` is default, remains in document flow.

`fixed` relates to viewport. Convenient for navigation bar. To fix border outside viewport: `box-sizing: border-box`. Excluded from document flow.

`absolute` relates to  another element: `html` or closest with position ancestor applied. Excluded from document flow.

`relative` relates to itself, partly remains in document flow.

`sticky` relates to viewport and another element, combination of `relative` and `fixed`, but is partly supported but browsers.


Flow: `absolute` and `fixed` value take the element the value is applied to out of the document flow.

Z-index default is 0 or auto. To use z-index must apply `position`.

Stacking Context: defines stacking behavior of child elements, created when applying fixed/ sticky or absolute/ relative in combination with `z-index`. When we apply position we change stacking context from viewport to parent's stacking context. So other element with `z-index` 2, can still be on the top, because our parent's position 1, even if our element is 100, but inside parent and have position applied.

The “position” properties: `top`,  `bottom`,  `left`  or `right` can be used only after we add `position` different than `static`. 

Positioning theory: https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning

More about the "position" property: https://developer.mozilla.org/en-US/docs/Web/CSS/position

The z-index: https://developer.mozilla.org/en-US/docs/Web/CSS/z-index




### Units
Rules:

1.  `position:fixed` + % = % of `viewport`

2. If `position:absolute` + % = % of the closest `Ancestor` with `padding`.

2. If `position:static` or  `position:relative`  + % = % of the closest  `Ancestor`.
`px`

`%` 

`em` multiply browser default font size (ex 16px), can be overridden by parent elements (H1, body, html)

`rem` root, adjust to font init html element size, better than `em`

`vh` viewport height

`vw` viewport width

`vmin` viewport min (detect what is smaller: height or width)

`vmax` viewport max (detect what is bigger: height or width)

Hiding Vertical Scrollbars on Mac and PC => https://web.archive.org/web/20180505112131/https://blogs.msdn.microsoft.com/kurlak/2013/11/03/hiding-vertical-scrollbars-with-pure-css-in-chrome-ie-6-firefox-opera-and-safari/

Recommended units:

`font-size` of root => `%` or nothing

`font-size` of element => `rem` (`em`=> for children only)

`padding` => `rem`

`border` => `px`

`margin` => `rem`

`width`, `height` => `%`, `vw`, `vh`, `vmin`, `vmax`

`top`, `bottom` => `%`



### Mobile first

Media queries go from smaller to bigger 

@media (min-width: 40rem) and (min-height: 40rem) {}

@media (min-width: 40rem), (orientation: landscape) {}

@media (min-width: 40rem), (orientation: portrait) {}

@media (min-width: 60rem) {}

all @media should be in the end of css




### Styling
![Selectors](images/selectors.PNG)

`.class input:not([type="checkbox"])` - select all inputs except checkboxes


### Fonts
`font-variant` - change case

`font-stretch`

`letter-spacing` - space between letters

`white-space` - how white space is treated inside the element, `nowrap` - one line, `pre-line`, `pre-wrap`

`line-height` - font size + 2 * space to border = height of element inside, depends on the font family

`text-decoration` - underline, overline, line-through, dotted, wavy, color

`text-shadow` - toRight; toBottom; Blur; Color;

`font` - font shorthand

`font-display` -strategy how to loaf fonts;

`block period` - invisible fallback, space is reserved;

`swap period` - fallback visible immediately;

strategies: `[ auto | block | swap | fallback | optional ]`