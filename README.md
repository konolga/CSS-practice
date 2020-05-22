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