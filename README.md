
<h1 align="center">Complete CSS Notes</h1>

<p align="center">CSS Handbook — Complete Reference & Practical Guide</p>

---

## Table of Contents

1. [Introduction to CSS](#1-introduction-to-css)
2. [Basic CSS Syntax](#2-basic-css-syntax)
3. [Ways to Add CSS](#3-ways-to-add-css)
4. [CSS Selectors](#4-css-selectors)
5. [Pseudo-Classes](#5-pseudo-classes)
6. [Pseudo-Elements](#6-pseudo-elements)
7. [Cascade, Specificity and Inheritance](#7-cascade-specificity-and-inheritance)
8. [CSS Colors](#8-css-colors)
9. [Background Properties](#9-background-properties)
10. [CSS Units and Values](#10-css-units-and-values)
11. [CSS Functions](#11-css-functions)
12. [Width, Height and Sizing](#12-width-height-and-sizing)
13. [CSS Box Model](#13-css-box-model)
14. [Margin Properties](#14-margin-properties)
15. [Padding Properties](#15-padding-properties)
16. [Border and Outline](#16-border-and-outline)
17. [Font Properties](#17-font-properties)
18. [Text Properties](#18-text-properties)
19. [Display, Visibility and Overflow](#19-display-visibility-and-overflow)
20. [CSS Positioning](#20-css-positioning)
21. [Flexbox](#21-flexbox)
22. [CSS Grid](#22-css-grid)
23. [Images and Media](#23-images-and-media)
24. [Lists and Tables](#24-lists-and-tables)
25. [Forms and Controls](#25-forms-and-controls)
26. [Cursor and Interaction](#26-cursor-and-interaction)
27. [Shadows and Visual Effects](#27-shadows-and-visual-effects)
28. [Transform Properties](#28-transform-properties)
29. [Transition Properties](#29-transition-properties)
30. [Animation Properties](#30-animation-properties)
31. [Responsive Design and Media Queries](#31-responsive-design-and-media-queries)
32. [CSS Variables](#32-css-variables)
33. [Logical Properties](#33-logical-properties)
34. [Accessibility and Best Practices](#34-accessibility-and-best-practices)
35. [Practical Project 1 — Product Card](#35-practical-project-1--product-card)
36. [Practical Project 2 — Responsive Navbar](#36-practical-project-2--responsive-navbar)
37. [Quick Reference — Common CSS Properties](#37-quick-reference--common-css-properties)
38. [CSS Learning Checklist](#38-css-learning-checklist)
39. [Useful Resources](#39-useful-resources)

---

# 1. Introduction to CSS

## What is CSS?

CSS stands for **Cascading Style Sheets**.

CSS is a stylesheet language used to control the appearance and layout of HTML documents. It helps us design beautiful and responsive websites.

CSS is used to control:

- Colors and backgrounds
- Fonts and text styling
- Width and height
- Margin and padding
- Borders and shadows
- Element positioning
- Flexbox and Grid layouts
- Transitions and animations
- Responsive website layouts

### HTML, CSS and JavaScript

| Technology | Purpose |
|---|---|
| HTML | Structure of a webpage |
| CSS | Styling and layout of a webpage |
| JavaScript | Behaviour and interactivity of a webpage |

---

# 2. Basic CSS Syntax

CSS rules follow a specific syntax.

### Syntax

```css
selector {
    property: value;
}
```

### Example

```css
h1 {
    color: blue;
    font-size: 32px;
}
```

### Key Components

1. **Selector:** Selects the HTML element that we want to style.
2. **Property:** Defines which style we want to change.
3. **Value:** Defines the setting assigned to a property.
4. **Declaration:** A property and value pair.
5. **Declaration Block:** All declarations written inside curly brackets `{ }`.

### Example Breakdown

```css
p {
    color: red;
    font-size: 18px;
}
```

- `p` — Selector
- `color` — Property
- `red` — Value
- `color: red;` — Declaration
- `{ }` — Declaration block

---

# 3. Ways to Add CSS

There are three main ways to add CSS to an HTML document.

## 1. Inline CSS

CSS is written directly inside an HTML element using the `style` attribute.

### Example

```html
<p style="color: red; font-size: 20px;">
    Hello World
</p>
```

**Use:** For applying a style to a specific HTML element.

## 2. Internal CSS

CSS is written inside the `<style>` element in the HTML document.

### Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Internal CSS</title>

    <style>
        p {
            color: red;
            font-size: 20px;
        }
    </style>
</head>
<body>

    <p>Hello World</p>

</body>
</html>
```

**Use:** When styling a single HTML page.

## 3. External CSS (Recommended)

CSS is written in a separate file, usually named `style.css`, and connected to the HTML document.

### HTML File

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>External CSS</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>Hello World</h1>

</body>
</html>
```

### CSS File (style.css)

```css
h1 {
    color: blue;
    font-size: 32px;
}
```

**Use:** Best for websites with multiple pages because one CSS file can style many HTML pages.

---

# 4. CSS Selectors

CSS selectors are used to select HTML elements that we want to style.

## 1. Universal Selector (`*`)

Selects all HTML elements.

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```

## 2. Element Selector

Selects all elements of a particular HTML tag.

```css
p {
    color: #333;
    font-size: 18px;
}
```

## 3. Class Selector (`.`)

Selects all HTML elements having a specific class name.

```css
.card {
    background-color: white;
    padding: 20px;
}
```

### HTML

```html
<div class="card">
    This is a card.
</div>
```

## 4. ID Selector (`#`)

Selects the element having a specific ID.

```css
#header {
    background-color: black;
    color: white;
}
```

### HTML

```html
<header id="header">
    Website Header
</header>
```

## 5. Grouping Selector (`,`)

Applies the same CSS properties to multiple selectors.

```css
h1, h2, p {
    font-family: Arial, sans-serif;
    color: #333;
}
```

## 6. Descendant Selector (Space)

Selects matching elements located anywhere inside another element.

```css
.card p {
    color: gray;
}
```

This selects all `<p>` elements inside `.card`, including nested descendants.

## 7. Child Selector (`>`)

Selects only the direct children of an element.

```css
nav > a {
    text-decoration: none;
    color: black;
}
```

## 8. Adjacent Sibling Selector (`+`)

Selects the first matching element immediately after another element.

```css
h2 + p {
    margin-top: 0;
}
```

## 9. General Sibling Selector (`~`)

Selects matching sibling elements that appear after another element.

```css
h2 ~ p {
    color: gray;
}
```

## 10. Attribute Selector (`[]`)

Selects elements based on their attributes or attribute values.

```css
input[type="email"] {
    border: 1px solid gray;
}
```

```css
a[target="_blank"] {
    color: purple;
}
```

### Quick Selector Reference

| Selector | Meaning |
|---|---|
| `*` | All elements |
| `p` | All paragraph elements |
| `.box` | Elements with class box |
| `#header` | Element with ID header |
| `h1, p` | Grouping selector |
| `.card p` | Descendant selector |
| `.card > p` | Direct child selector |
| `h2 + p` | Adjacent sibling |
| `h2 ~ p` | General sibling |
| `input[type="text"]` | Attribute selector |

---

# 5. Pseudo-Classes

Pseudo-classes select HTML elements based on their state, position or condition.

### Syntax

```css
selector:pseudo-class {
    property: value;
}
```

### Example

```css
a:hover {
    color: red;
}
```

When the mouse pointer moves over the link, its color changes to red.

## Common Pseudo-Classes

| Pseudo-Class | Use |
|---|---|
| `:hover` | When mouse pointer is over an element |
| `:focus` | When an element receives focus |
| `:focus-visible` | Shows focus indicator when appropriate |
| `:active` | When an element is being activated |
| `:visited` | Visited links |
| `:link` | Unvisited links |
| `:checked` | Checked checkbox or radio button |
| `:disabled` | Disabled form control |
| `:enabled` | Enabled form control |
| `:required` | Required input field |
| `:valid` | Input passes validation |
| `:invalid` | Input fails validation |
| `:first-child` | First child of its parent |
| `:last-child` | Last child of its parent |
| `:nth-child(n)` | Child at a particular position |
| `:not()` | Elements that do not match a selector |
| `:is()` | Matches any selector in a list |
| `:where()` | Similar to `:is()` with zero specificity |
| `:root` | Root HTML element |
| `:empty` | Element with no children |

### Example 1 — Hover

```css
button:hover {
    background-color: blue;
    color: white;
}
```

### Example 2 — First Child

```css
li:first-child {
    color: red;
}
```

### Example 3 — Last Child

```css
li:last-child {
    color: green;
}
```

### Example 4 — Odd and Even Children

```css
li:nth-child(odd) {
    background-color: #f2f2f2;
}

li:nth-child(even) {
    background-color: #ddd;
}
```

### Example 5 — Disabled Button

```css
button:disabled {
    cursor: not-allowed;
    opacity: 0.5;
}
```

---

# 6. Pseudo-Elements

Pseudo-elements style a specific part of an HTML element or create decorative content.

### Syntax

```css
selector::pseudo-element {
    property: value;
}
```

### Example

```css
p::first-letter {
    font-size: 32px;
    color: red;
}
```

## Common Pseudo-Elements

| Pseudo-Element | Use |
|---|---|
| `::before` | Inserts generated content before an element's content |
| `::after` | Inserts generated content after an element's content |
| `::first-letter` | Styles the first letter |
| `::first-line` | Styles the first line |
| `::selection` | Styles selected text |
| `::placeholder` | Styles placeholder text |
| `::marker` | Styles list markers |
| `::file-selector-button` | Styles file input button |

### Example 1 — Before

```css
.heading::before {
    content: "★ ";
    color: orange;
}
```

### Example 2 — After

```css
.button::after {
    content: " →";
}
```

### Example 3 — Placeholder

```css
input::placeholder {
    color: gray;
    font-size: 14px;
}
```

### Example 4 — Selection

```css
::selection {
    background-color: yellow;
    color: black;
}
```

**Note:** `::before` and `::after` usually need the `content` property to display generated content.

---

# 7. Cascade, Specificity and Inheritance

These three concepts determine how CSS styles are applied to HTML elements.

## 1. Cascade

Cascade is the process through which the browser decides which CSS declaration wins when multiple rules apply to the same element.

## 2. Specificity

Specificity is the weight of a selector used to resolve conflicting CSS rules.

### General Specificity Order

1. Inline styles
2. ID selectors
3. Class, attribute and pseudo-class selectors
4. Element and pseudo-element selectors

## 3. Inheritance

Inheritance means some CSS properties automatically pass from a parent element to its children.

For example, `color` and `font-family` are commonly inherited.

## 4. Source Order

If two declarations have the same priority and specificity, the later declaration generally wins.

## 5. !important

The `!important` rule gives a declaration higher priority within the cascade.

```css
p {
    color: red !important;
}
```

Avoid using `!important` unnecessarily.

### Specificity Example

```css
p {
    color: blue;
}

.note {
    color: green;
}

#intro {
    color: red;
}
```

If the same paragraph matches all three selectors, the ID selector normally wins among these declarations.

---

# 8. CSS Colors

CSS provides different ways to define colors for text, backgrounds, borders and other elements.

## 1. Named Colors

```css
h1 {
    color: red;
}
```

Examples:

- red
- blue
- black
- white
- green
- yellow
- purple

## 2. HEX Colors

HEX is a hexadecimal color format.

```css
p {
    color: #ff6600;
}
```

## 3. RGB Colors

RGB stands for Red, Green and Blue.

```css
div {
    color: rgb(255, 100, 0);
}
```

## 4. RGBA Colors

RGBA adds an alpha channel for transparency.

```css
section {
    background-color: rgba(0, 0, 0, 0.5);
}
```

## 5. HSL Colors

HSL stands for Hue, Saturation and Lightness.

```css
h2 {
    color: hsl(20, 100%, 50%);
}
```

## 6. Transparent

Makes the color completely transparent.

```css
.box {
    background-color: transparent;
}
```

### Common Color Formats

| Format | Example |
|---|---|
| Named | `red` |
| HEX | `#ff0000` |
| RGB | `rgb(255, 0, 0)` |
| RGBA | `rgba(255, 0, 0, 0.5)` |
| HSL | `hsl(0, 100%, 50%)` |
| Transparent | `transparent` |

## Related Color Properties

| Property | Use |
|---|---|
| `color` | Sets foreground or text color |
| `opacity` | Sets transparency of the entire element |
| `accent-color` | Sets accent color of supported controls |
| `caret-color` | Sets text cursor color in inputs |
| `color-scheme` | Indicates support for light and dark color schemes |

### Example

```css
:root {
    accent-color: #2563eb;
    color-scheme: light;
}
```

---

# 9. Background Properties

Background properties control an element's background color, image, position, size and display.

### Example

```css
body {
    background-color: #f5f7fb;
    background-image: url("background.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
}
```

## Background Properties

| Property | Use |
|---|---|
| `background` | Shorthand for background settings |
| `background-color` | Sets background color |
| `background-image` | Adds an image or gradient |
| `background-repeat` | Controls image repetition |
| `background-position` | Sets background image position |
| `background-size` | Sets background image size |
| `background-attachment` | Controls scrolling attachment |
| `background-origin` | Sets the box used to position the background |
| `background-clip` | Defines the area painted by the background |
| `background-blend-mode` | Blends background layers |

## Background Gradient

A gradient creates a smooth transition between two or more colors.

### Linear Gradient

```css
.hero {
    background: linear-gradient(135deg, #2563eb, #9333ea);
}
```

### Radial Gradient

```css
.box {
    background: radial-gradient(circle, #ffffff, #2563eb);
}
```

### Conic Gradient

```css
.box {
    background: conic-gradient(red, yellow, green, blue);
}
```

## Useful Background Values

### Background Size

```css
background-size: cover;
background-size: contain;
background-size: auto;
```

- `cover` — Covers the complete background area.
- `contain` — Shows the complete image inside the area.
- `auto` — Uses the original image size where applicable.

### Background Repeat

```css
background-repeat: no-repeat;
background-repeat: repeat;
background-repeat: repeat-x;
background-repeat: repeat-y;
```

### Background Position

```css
background-position: center;
background-position: top right;
background-position: bottom left;
```

---

# 10. CSS Units and Values

CSS units define the size, spacing and dimensions of HTML elements.

## 1. Absolute Unit

Absolute units have fixed reference sizes.

| Unit | Meaning |
|---|---|
| `px` | CSS pixel |
| `cm` | Centimeter |
| `mm` | Millimeter |
| `in` | Inch |
| `pt` | Point |
| `pc` | Pica |

For normal web layouts, `px` is commonly used.

## 2. Relative Units

Relative units depend on another size or the viewport.

| Unit | Meaning |
|---|---|
| `%` | Percentage relative to a relevant containing size |
| `em` | Relative to the element's font size |
| `rem` | Relative to the root element's font size |
| `vw` | 1% of viewport width |
| `vh` | 1% of viewport height |
| `dvw` | 1% of dynamic viewport width |
| `dvh` | 1% of dynamic viewport height |
| `vmin` | 1% of smaller viewport dimension |
| `vmax` | 1% of larger viewport dimension |
| `ch` | Based on the width of the 0 character |
| `fr` | Fraction of available space in CSS Grid |

### Example 1 — REM

```css
h1 {
    font-size: 2rem;
}
```

### Example 2 — Percentage

```css
.container {
    width: 80%;
}
```

### Example 3 — Viewport Width

```css
.box {
    width: 50vw;
}
```

### Example 4 — Viewport Height

```css
.hero {
    min-height: 100vh;
}
```

---

# 11. CSS Functions

CSS functions are used to calculate values, define sizes, create gradients and reuse values.

## 1. calc()

Performs mathematical calculations.

```css
.container {
    width: calc(100% - 40px);
}
```

## 2. min()

Selects the smaller value.

```css
.container {
    width: min(100%, 1200px);
}
```

## 3. max()

Selects the larger value.

```css
.heading {
    font-size: max(16px, 2vw);
}
```

## 4. clamp()

Keeps a value between a minimum and maximum.

```css
h1 {
    font-size: clamp(24px, 4vw, 48px);
}
```

## 5. var()

Uses a CSS custom property.

```css
.box {
    color: var(--primary-color);
}
```

## 6. minmax()

Defines minimum and maximum sizes, commonly used in CSS Grid.

```css
.grid {
    grid-template-columns: repeat(3, minmax(200px, 1fr));
}
```

## 7. repeat()

Repeats Grid track definitions.

```css
.grid {
    grid-template-columns: repeat(3, 1fr);
}
```

## 8. url()

References an external resource.

```css
.box {
    background-image: url("image.jpg");
}
```

### Common Gradient Functions

```css
background: linear-gradient(to right, red, blue);

background: radial-gradient(circle, red, blue);

background: conic-gradient(red, yellow, green);
```

### Responsive Container Example

```css
.container {
    width: min(100% - 32px, 1200px);
    margin-inline: auto;
}
```

---

# 12. Width, Height and Sizing

Sizing properties control the dimensions of HTML elements.

## Common Sizing Properties

| Property | Use |
|---|---|
| `width` | Sets width |
| `min-width` | Sets minimum width |
| `max-width` | Sets maximum width |
| `height` | Sets height |
| `min-height` | Sets minimum height |
| `max-height` | Sets maximum height |
| `inline-size` | Sets logical width |
| `block-size` | Sets logical height |
| `min-inline-size` | Sets minimum logical width |
| `max-inline-size` | Sets maximum logical width |
| `min-block-size` | Sets minimum logical height |
| `max-block-size` | Sets maximum logical height |
| `aspect-ratio` | Sets preferred width-to-height ratio |
| `box-sizing` | Controls how dimensions are calculated |
| `object-fit` | Controls how image/video fits its box |
| `object-position` | Controls image/video position inside its box |
| `overflow` | Controls content outside an element's box |

### Example

```css
img {
    width: 100%;
    max-width: 400px;
    aspect-ratio: 4 / 3;
    object-fit: cover;
}
```

### Min and Max Width

```css
.container {
    width: 100%;
    max-width: 1200px;
    min-width: 300px;
}
```

### Min and Max Height

```css
.box {
    min-height: 200px;
    max-height: 500px;
}
```

---

# 13. CSS Box Model

Every HTML element is represented as a rectangular box in CSS.

The CSS Box Model consists of four main parts:

1. Content
2. Padding
3. Border
4. Margin

## 1. Content

The actual text, image or other content inside the element.

## 2. Padding

Space between the content and the border.

## 3. Border

The line surrounding the padding and content.

## 4. Margin

Space outside the border.

### Box Model Structure

```text
+----------------------------------+
|              Margin              |
|   +--------------------------+   |
|   |          Border          |   |
|   |   +------------------+   |   |
|   |   |     Padding      |   |   |
|   |   |  +------------+  |   |   |
|   |   |  |  Content   |  |   |   |
|   |   |  +------------+  |   |   |
|   |   +------------------+   |   |
|   +--------------------------+   |
+----------------------------------+
```

## box-sizing Property

The `box-sizing` property controls how the width and height of an element are calculated.

### content-box

Default value. Padding and border are added outside the declared width and height.

```css
.box {
    box-sizing: content-box;
}
```

### border-box

Declared width and height include padding and border.

```css
* {
    box-sizing: border-box;
}
```

### Complete Example

```css
.card {
    width: 300px;
    padding: 20px;
    border: 1px solid #ddd;
    margin: 16px;
    box-sizing: border-box;
}
```

---

# 14. Margin Properties

Margin creates space outside an element's border.

## Margin Properties

| Property | Use |
|---|---|
| `margin` | Shorthand for all sides |
| `margin-top` | Top margin |
| `margin-right` | Right margin |
| `margin-bottom` | Bottom margin |
| `margin-left` | Left margin |
| `margin-inline` | Inline-start and inline-end margin |
| `margin-block` | Block-start and block-end margin |
| `margin-inline-start` | Inline-start margin |
| `margin-inline-end` | Inline-end margin |
| `margin-block-start` | Block-start margin |
| `margin-block-end` | Block-end margin |

## 1. Margin on All Sides

```css
.box {
    margin: 20px;
}
```

## 2. Margin on Top/Bottom and Left/Right

```css
.box {
    margin: 10px 20px;
}
```

- `10px` — Top and bottom
- `20px` — Left and right

## 3. Different Margin on Each Side

```css
.box {
    margin: 10px 15px 20px 25px;
}
```

Order:

1. Top
2. Right
3. Bottom
4. Left

## 4. Individual Margin Properties

```css
.box {
    margin-top: 10px;
    margin-right: 20px;
    margin-bottom: 30px;
    margin-left: 40px;
}
```

## 5. Centering a Block Element

```css
.container {
    max-width: 1000px;
    margin-inline: auto;
}
```

`auto` distributes the available inline space equally when the element has a constrained width.

---

# 15. Padding Properties

Padding creates space inside an element's border, around its content.

## Padding Properties

| Property | Use |
|---|---|
| `padding` | Shorthand for all sides |
| `padding-top` | Top padding |
| `padding-right` | Right padding |
| `padding-bottom` | Bottom padding |
| `padding-left` | Left padding |
| `padding-inline` | Inline-start and inline-end padding |
| `padding-block` | Block-start and block-end padding |
| `padding-inline-start` | Inline-start padding |
| `padding-inline-end` | Inline-end padding |
| `padding-block-start` | Block-start padding |
| `padding-block-end` | Block-end padding |

## 1. Padding on All Sides

```css
.box {
    padding: 20px;
}
```

## 2. Padding on Top/Bottom and Left/Right

```css
.box {
    padding: 10px 20px;
}
```

## 3. Different Padding on Each Side

```css
.box {
    padding: 10px 15px 20px 25px;
}
```

Order:

1. Top
2. Right
3. Bottom
4. Left

## 4. Individual Padding Properties

```css
.box {
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 30px;
    padding-left: 40px;
}
```

### Button Example

```css
.button {
    padding: 10px 18px;
}
```

---

# 16. Border and Outline

Border creates a visible boundary around an element.

Outline draws a line outside the border.

## Border Properties

| Property | Use |
|---|---|
| `border` | Shorthand for border width, style and color |
| `border-width` | Sets border thickness |
| `border-style` | Sets border style |
| `border-color` | Sets border color |
| `border-top` | Sets top border |
| `border-right` | Sets right border |
| `border-bottom` | Sets bottom border |
| `border-left` | Sets left border |
| `border-radius` | Rounds the corners |
| `border-top-left-radius` | Rounds top-left corner |
| `border-top-right-radius` | Rounds top-right corner |
| `border-bottom-left-radius` | Rounds bottom-left corner |
| `border-bottom-right-radius` | Rounds bottom-right corner |

## Border Style Values

```css
border-style: solid;
border-style: dashed;
border-style: dotted;
border-style: double;
border-style: groove;
border-style: ridge;
border-style: inset;
border-style: outset;
border-style: none;
```

### Border Example

```css
.box {
    border: 2px solid black;
}
```

### Border Radius

```css
.card {
    border-radius: 12px;
}
```

### Individual Border Example

```css
.box {
    border-top: 2px solid red;
    border-right: 2px solid blue;
    border-bottom: 2px solid green;
    border-left: 2px solid orange;
}
```

## Outline Properties

| Property | Use |
|---|---|
| `outline` | Shorthand for outline settings |
| `outline-width` | Sets outline thickness |
| `outline-style` | Sets outline style |
| `outline-color` | Sets outline color |
| `outline-offset` | Sets gap between border and outline |

### Example

```css
button {
    border: 0;
    border-radius: 8px;
    outline: 2px solid blue;
    outline-offset: 3px;
}
```

**Note:** Outline does not take up space in the element's box model. Avoid removing keyboard focus outlines without providing a visible replacement.

---

# 17. Font Properties

Font properties control the appearance of text.

## Font Properties

| Property | Use |
|---|---|
| `font-family` | Sets the font typeface |
| `font-size` | Sets text size |
| `font-weight` | Sets text thickness |
| `font-style` | Sets normal, italic or oblique style |
| `font-stretch` | Controls font width when supported |
| `font-variant` | Controls alternate glyph forms |
| `font` | Shorthand for several font settings |
| `line-height` | Controls line spacing |
| `letter-spacing` | Controls spacing between characters |
| `word-spacing` | Controls spacing between words |
| `font-kerning` | Controls spacing adjustments between letter pairs |
| `font-optical-sizing` | Controls optical sizing for variable fonts |
| `font-feature-settings` | Controls low-level font features |
| `font-variation-settings` | Controls low-level variable font settings |

## 1. Font Family

Defines which font should be used.

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

## 2. Font Size

Controls the size of text.

```css
h1 {
    font-size: 32px;
}
```

## 3. Font Weight

Controls the thickness of text.

```css
p {
    font-weight: 400;
}

h1 {
    font-weight: 700;
}
```

Common values:

- `100` — Thin
- `200` — Extra Light
- `300` — Light
- `400` — Normal
- `500` — Medium
- `600` — Semi Bold
- `700` — Bold
- `800` — Extra Bold
- `900` — Black

## 4. Font Style

```css
p {
    font-style: normal;
}

.italic {
    font-style: italic;
}

.oblique {
    font-style: oblique;
}
```

## 5. Line Height

Controls the vertical spacing between lines.

```css
p {
    line-height: 1.6;
}
```

## 6. Letter Spacing

Controls the space between characters.

```css
h1 {
    letter-spacing: 2px;
}
```

## 7. Word Spacing

Controls the space between words.

```css
p {
    word-spacing: 5px;
}
```

## 8. Font Shorthand

```css
p {
    font: italic 700 18px/1.5 Arial, sans-serif;
}
```

---

# 18. Text Properties

Text properties control the alignment, decoration, spacing and appearance of text.

## Text Properties

| Property | Use |
|---|---|
| `text-align` | Aligns text horizontally |
| `text-align-last` | Aligns the last line of text |
| `text-decoration` | Adds or removes text decoration |
| `text-decoration-line` | Sets underline, overline or line-through |
| `text-decoration-color` | Sets decoration color |
| `text-decoration-style` | Sets decoration style |
| `text-decoration-thickness` | Sets decoration thickness |
| `text-underline-offset` | Sets distance between text and underline |
| `text-transform` | Converts text to uppercase, lowercase or capitalize |
| `text-indent` | Indents the first line |
| `text-overflow` | Controls how clipped overflowing text appears |
| `text-shadow` | Adds a shadow behind text |
| `text-wrap` | Controls text wrapping behaviour |
| `white-space` | Controls spaces and line breaks |
| `overflow-wrap` | Allows long words to wrap |
| `word-break` | Controls word-breaking rules |
| `hyphens` | Controls hyphenation |
| `direction` | Sets text direction |
| `writing-mode` | Sets horizontal or vertical text flow |
| `vertical-align` | Aligns inline or table-cell content vertically |
| `user-select` | Controls whether text can be selected |

## 1. Text Alignment

```css
h1 {
    text-align: center;
}
```

Common values:

```css
text-align: left;
text-align: right;
text-align: center;
text-align: justify;
```

## 2. Text Transform

```css
.uppercase {
    text-transform: uppercase;
}

.lowercase {
    text-transform: lowercase;
}

.capitalize {
    text-transform: capitalize;
}
```

## 3. Text Decoration

```css
a {
    text-decoration: none;
}

.underline {
    text-decoration: underline;
}

.overline {
    text-decoration: overline;
}

.line-through {
    text-decoration: line-through;
}
```

## 4. Text Shadow

```css
h1 {
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
```

## 5. Text Indent

```css
p {
    text-indent: 30px;
}
```

## 6. White Space

```css
.text {
    white-space: normal;
}
```

Common values:

```css
white-space: normal;
white-space: nowrap;
white-space: pre;
white-space: pre-wrap;
white-space: pre-line;
```

## 7. Word Break

```css
.text {
    word-break: break-all;
}
```

## 8. Text Overflow

Controls how text appears when it overflows its available space.

```css
.text {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
```

## Single-Line Ellipsis

Used when you want to display `...` at the end of text that does not fit.

```css
.ellipsis {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
```

---

# 19. Display, Visibility and Overflow

The `display` property controls how an element participates in the layout.

## Display Properties

| Value | Use |
|---|---|
| `block` | Starts on a new line and usually fills available width |
| `inline` | Flows within text |
| `inline-block` | Flows inline but supports width and height |
| `none` | Removes element from the layout |
| `flex` | Creates a Flexbox container |
| `inline-flex` | Creates an inline-level Flexbox container |
| `grid` | Creates a Grid container |
| `inline-grid` | Creates an inline-level Grid container |
| `flow-root` | Creates a block formatting context |
| `contents` | Removes the element's own layout box |
| `list-item` | Displays an element like a list item |

### 1. Display Block

```css
.box {
    display: block;
}
```

### 2. Display Inline

```css
span {
    display: inline;
}
```

### 3. Display Inline-Block

```css
.box {
    display: inline-block;
    width: 150px;
    height: 100px;
}
```

### 4. Display None

```css
.menu {
    display: none;
}
```

The element is removed from the layout.

### 5. Display Flex

```css
.container {
    display: flex;
}
```

### 6. Display Grid

```css
.container {
    display: grid;
}
```

## Other Properties

| Property | Use |
|---|---|
| `visibility` | Shows or hides an element |
| `opacity` | Controls transparency |
| `overflow` | Controls overflowing content |
| `overflow-x` | Controls horizontal overflow |
| `overflow-y` | Controls vertical overflow |
| `overflow-wrap` | Allows long words to wrap |
| `clip-path` | Clips an element to a shape |
| `contain` | Limits certain layout, paint and other effects |
| `content-visibility` | Allows rendering optimizations |

## Visibility

```css
.hidden {
    visibility: hidden;
}
```

The element becomes invisible but keeps its layout space.

## Opacity

```css
.box {
    opacity: 0.5;
}
```

Value range:

- `0` — Completely transparent
- `0.5` — 50% opacity
- `1` — Fully visible

## Overflow

```css
.box {
    width: 200px;
    height: 100px;
    overflow: auto;
}
```

Common values:

```css
overflow: visible;
overflow: hidden;
overflow: scroll;
overflow: auto;
```

---

# 20. CSS Positioning

The `position` property controls how an element is positioned in a document.

## Position Values

| Value | Use |
|---|---|
| `static` | Default position in normal document flow |
| `relative` | Stays in normal flow but can be offset |
| `absolute` | Positioned relative to its containing block |
| `fixed` | Usually positioned relative to the viewport |
| `sticky` | Behaves relatively until it reaches a scroll threshold |

## 1. Static Position

Default positioning of HTML elements.

```css
.box {
    position: static;
}
```

## 2. Relative Position

Element stays in its normal document flow but can be moved from its original position.

```css
.box {
    position: relative;
    top: 20px;
    left: 30px;
}
```

## 3. Absolute Position

Element is positioned relative to its nearest positioned containing block.

```css
.parent {
    position: relative;
}

.child {
    position: absolute;
    top: 10px;
    right: 10px;
}
```

## 4. Fixed Position

Element is positioned relative to the viewport in typical cases and stays in place while scrolling.

```css
.button {
    position: fixed;
    bottom: 20px;
    right: 20px;
}
```

## 5. Sticky Position

Element behaves like a relatively positioned element until it reaches the specified scroll position.

```css
.header {
    position: sticky;
    top: 0;
}
```

## Offset Properties

| Property | Use |
|---|---|
| `top` | Distance from top |
| `right` | Distance from right |
| `bottom` | Distance from bottom |
| `left` | Distance from left |
| `inset` | Shorthand for top, right, bottom and left |
| `inset-block` | Logical block-axis offsets |
| `inset-inline` | Logical inline-axis offsets |
| `z-index` | Controls stacking order within stacking-context rules |

### Z-Index Example

```css
.card {
    position: relative;
    z-index: 1;
}

.badge {
    position: absolute;
    top: 10px;
    right: 10px;
    z-index: 2;
}
```

**Note:** `z-index` works according to stacking-context rules. A larger number does not always place an element above every other element.

---

# 21. Flexbox

Flexbox is a one-dimensional layout system used to arrange elements in a row or column.

It is useful for:

- Centering elements
- Creating navigation bars
- Aligning images
- Creating card layouts
- Managing spacing between elements

## Basic Flexbox Example

```css
.container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 16px;
    flex-wrap: wrap;
}
```

## Flexbox Container Properties

| Property | Use |
|---|---|
| `display` | Creates a Flexbox container |
| `flex-direction` | Sets direction of items |
| `flex-wrap` | Controls item wrapping |
| `flex-flow` | Shorthand for direction and wrapping |
| `justify-content` | Aligns items along the main axis |
| `align-items` | Aligns items along the cross axis |
| `align-content` | Controls spacing between flex lines |
| `gap` | Sets row and column gaps |
| `row-gap` | Sets gaps between rows |
| `column-gap` | Sets gaps between columns |

## 1. Flex Direction

Controls the direction of flex items.

```css
.container {
    display: flex;
    flex-direction: row;
}
```

Common values:

```css
flex-direction: row;
flex-direction: row-reverse;
flex-direction: column;
flex-direction: column-reverse;
```

## 2. Justify Content

Aligns items along the main axis.

```css
.container {
    display: flex;
    justify-content: center;
}
```

Common values:

```css
justify-content: flex-start;
justify-content: flex-end;
justify-content: center;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;
```

## 3. Align Items

Aligns items along the cross axis.

```css
.container {
    display: flex;
    align-items: center;
}
```

Common values:

```css
align-items: stretch;
align-items: flex-start;
align-items: flex-end;
align-items: center;
align-items: baseline;
```

## 4. Flex Wrap

Controls whether flex items stay on one line or move to another line.

```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

Common values:

```css
flex-wrap: nowrap;
flex-wrap: wrap;
flex-wrap: wrap-reverse;
```

## 5. Flex Flow

Shorthand for `flex-direction` and `flex-wrap`.

```css
.container {
    flex-flow: row wrap;
}
```

## 6. Align Content

Controls spacing between multiple flex lines when there is extra cross-axis space.

```css
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
}
```

## Flex Item Properties

| Property | Use |
|---|---|
| `order` | Changes visual order of an item |
| `flex` | Shorthand for grow, shrink and basis |
| `flex-grow` | Controls how an item can grow |
| `flex-shrink` | Controls how an item can shrink |
| `flex-basis` | Sets initial main size |
| `align-self` | Overrides cross-axis alignment for an individual item |

### Flex Grow

```css
.item {
    flex-grow: 1;
}
```

### Flex Shrink

```css
.item {
    flex-shrink: 1;
}
```

### Flex Basis

```css
.item {
    flex-basis: 200px;
}
```

### Flex Shorthand

```css
.item {
    flex: 1;
}
```

## Center an Element Using Flexbox

```css
.parent {
    min-height: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

## Gap Example

```css
.container {
    display: flex;
    gap: 20px;
}
```

**Remember:**

- `justify-content` — Main axis
- `align-items` — Cross axis
- `flex-direction` — Direction of items
- `gap` — Space between items

---

# 22. CSS Grid

CSS Grid is a two-dimensional layout system used to arrange items in rows and columns.

It is useful for:

- Product grids
- Image galleries
- Dashboard layouts
- Website sections
- Responsive card layouts

## Basic Grid Example

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

## Grid Container Properties

| Property | Use |
|---|---|
| `grid-template-columns` | Defines column sizes |
| `grid-template-rows` | Defines row sizes |
| `grid-template-areas` | Defines named layout areas |
| `grid-template` | Shorthand for explicit grid definitions |
| `grid-auto-columns` | Sets sizes of implicit columns |
| `grid-auto-rows` | Sets sizes of implicit rows |
| `grid-auto-flow` | Controls automatic item placement |
| `gap` | Sets gaps between rows and columns |
| `row-gap` | Sets gaps between rows |
| `column-gap` | Sets gaps between columns |
| `justify-items` | Aligns items along the inline axis |
| `align-items` | Aligns items along the block axis |
| `place-items` | Shorthand for align-items and justify-items |
| `justify-content` | Aligns grid content along the inline axis |
| `align-content` | Aligns grid content along the block axis |
| `place-content` | Shorthand for content alignment |

## 1. Grid Template Columns

Defines the number and size of columns.

```css
.container {
    display: grid;
    grid-template-columns: 200px 200px 200px;
}
```

### Using Fraction Unit

```css
.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}
```

### Using Repeat

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}
```

## 2. Grid Template Rows

Defines the height of rows.

```css
.container {
    display: grid;
    grid-template-rows: 100px 200px;
}
```

## 3. Gap

Creates space between rows and columns.

```css
.container {
    display: grid;
    gap: 20px;
}
```

Separate row and column gaps:

```css
.container {
    row-gap: 20px;
    column-gap: 30px;
}
```

## 4. Grid Template Areas

Defines named areas inside a grid.

```css
.container {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar content"
        "footer footer";
    grid-template-columns: 200px 1fr;
}

.header {
    grid-area: header;
}

.sidebar {
    grid-area: sidebar;
}

.content {
    grid-area: content;
}

.footer {
    grid-area: footer;
}
```

## Grid Item Properties

| Property | Use |
|---|---|
| `grid-column` | Sets column start/end placement |
| `grid-row` | Sets row start/end placement |
| `grid-area` | Sets placement or a named area |
| `justify-self` | Aligns an individual item along the inline axis |
| `align-self` | Aligns an individual item along the block axis |
| `place-self` | Shorthand for individual item alignment |

### Grid Column

```css
.item {
    grid-column: 1 / 3;
}
```

### Grid Row

```css
.item {
    grid-row: 1 / 3;
}
```

## Responsive Grid

```css
.products {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
}
```

This automatically adjusts the number of columns according to the available space.

---

# 23. Images and Media

CSS provides properties to control how images and videos appear on a webpage.

### Responsive Image and Video

```css
img,
video {
    max-width: 100%;
    height: auto;
}
```

## Image Properties

| Property | Use |
|---|---|
| `object-fit` | Controls how image/video fits its box |
| `object-position` | Sets content position inside its box |
| `aspect-ratio` | Sets preferred width-to-height ratio |
| `image-rendering` | Controls image scaling preferences |
| `vertical-align` | Aligns inline images vertically |

## Object Fit

Controls how an image or video fits inside its container.

### Common Values

```css
object-fit: fill;
object-fit: contain;
object-fit: cover;
object-fit: none;
object-fit: scale-down;
```

### Object Fit Example

```css
.product-image {
    width: 100%;
    height: 220px;
    object-fit: cover;
    border-radius: 12px;
}
```

## Object Position

Controls the position of the image inside its container.

```css
img {
    object-fit: cover;
    object-position: center;
}
```

Other values:

```css
object-position: top;
object-position: bottom;
object-position: left;
object-position: right;
```

## Aspect Ratio

Defines the preferred width-to-height ratio.

```css
.image {
    aspect-ratio: 16 / 9;
}
```

---

# 24. Lists and Tables

CSS provides properties to style HTML lists and tables.

## 1. List Properties

| Property | Use |
|---|---|
| `list-style` | Shorthand for list marker settings |
| `list-style-type` | Sets marker type |
| `list-style-position` | Sets marker position |
| `list-style-image` | Uses an image as a list marker |

### List Style Type

```css
ul {
    list-style-type: square;
}

ol {
    list-style-type: upper-roman;
}
```

Common values:

```css
list-style-type: disc;
list-style-type: circle;
list-style-type: square;
list-style-type: decimal;
list-style-type: lower-alpha;
list-style-type: upper-alpha;
list-style-type: lower-roman;
list-style-type: upper-roman;
list-style-type: none;
```

### List Style Position

```css
ul {
    list-style-position: inside;
}
```

Values:

```css
list-style-position: inside;
list-style-position: outside;
```

### Remove List Markers

```css
ul {
    list-style: none;
    padding: 0;
    margin: 0;
}
```

## 2. Table Properties

| Property | Use |
|---|---|
| `border-collapse` | Controls whether table borders collapse or remain separate |
| `border-spacing` | Sets spacing between cell borders |
| `table-layout` | Controls table column sizing behaviour |
| `caption-side` | Sets caption placement |
| `empty-cells` | Controls borders/backgrounds of empty cells |

### Example

```css
table {
    width: 100%;
    border-collapse: collapse;
}

th,
td {
    padding: 12px;
    border: 1px solid #ddd;
    text-align: left;
}
```

### Border Collapse

```css
table {
    border-collapse: collapse;
}
```

### Border Spacing

```css
table {
    border-collapse: separate;
    border-spacing: 10px;
}
```

### Table Layout

```css
table {
    table-layout: fixed;
    width: 100%;
}
```

---

# 25. Forms and Controls

CSS can style text fields, dropdowns, buttons, checkboxes, radio buttons and other form controls.

## Common Properties and Selectors

| Property / Selector | Use |
|---|---|
| `accent-color` | Sets accent color of supported controls |
| `appearance` | Controls native appearance of a control |
| `caret-color` | Sets input text cursor color |
| `resize` | Controls whether an element can be resized |
| `field-sizing` | Controls content-based sizing where supported |
| `::placeholder` | Styles placeholder text |
| `:focus` | Selects an element when it has focus |
| `:disabled` | Selects disabled controls |
| `:checked` | Selects checked checkboxes and radio buttons |

## 1. Input Styling

```css
input {
    width: 100%;
    padding: 10px 12px;
    border: 1px solid #cbd5e1;
    border-radius: 6px;
    font-size: 16px;
}
```

## 2. Textarea Styling

```css
textarea {
    width: 100%;
    padding: 12px;
    resize: vertical;
}
```

## 3. Placeholder Styling

```css
input::placeholder {
    color: gray;
    font-size: 14px;
}
```

## 4. Focus Styling

```css
input:focus {
    outline: 2px solid #2563eb;
    outline-offset: 2px;
}
```

## 5. Disabled Control

```css
input:disabled {
    background-color: #eee;
    cursor: not-allowed;
}
```

## 6. Checked Checkbox

```css
input:checked {
    accent-color: blue;
}
```

## 7. Button Styling

```css
button {
    padding: 10px 18px;
    border: none;
    border-radius: 6px;
    background-color: #2563eb;
    color: white;
    cursor: pointer;
}
```

---

# 26. Cursor and Interaction

These properties control how users interact with elements using a mouse, keyboard or touch input.

## Common Properties

| Property | Use |
|---|---|
| `cursor` | Controls cursor appearance |
| `pointer-events` | Controls whether an element can be a pointer target |
| `user-select` | Controls whether text can be selected |
| `touch-action` | Controls touch gesture handling |
| `scroll-behavior` | Sets scrolling behaviour |
| `scroll-margin` | Sets space around a target when scrolling to it |
| `scroll-padding` | Sets inset of a scroll container |
| `overscroll-behavior` | Controls scroll chaining and overscroll behaviour |
| `resize` | Allows resizing where supported |

## Common Cursor Values

```css
cursor: pointer;
cursor: default;
cursor: text;
cursor: move;
cursor: not-allowed;
cursor: grab;
cursor: grabbing;
cursor: wait;
cursor: help;
cursor: crosshair;
```

## Example — Pointer Cursor

```css
button {
    cursor: pointer;
}
```

## Pointer Events

```css
.disabled {
    pointer-events: none;
}
```

## User Select

```css
.text {
    user-select: none;
}
```

## Smooth Scrolling

```css
html {
    scroll-behavior: smooth;
}
```

## Scroll Margin

```css
section {
    scroll-margin-top: 80px;
}
```

## Overscroll Behaviour

```css
.container {
    overscroll-behavior: contain;
}
```

---

# 27. Shadows and Visual Effects

CSS provides different properties to create shadows, filters, transparency and visual effects.

## Common Properties

| Property | Use |
|---|---|
| `box-shadow` | Adds shadow around an element's box |
| `text-shadow` | Adds shadow behind text |
| `filter` | Applies effects such as blur, grayscale or brightness |
| `backdrop-filter` | Applies effects to content behind a translucent element |
| `mix-blend-mode` | Controls how an element blends with its background |
| `background-blend-mode` | Controls blending between background layers |
| `opacity` | Sets element transparency |
| `clip-path` | Clips an element to a shape |
| `mask` | Masks visible areas where supported |

## 1. Box Shadow

Adds a shadow around an element.

### Syntax

```css
box-shadow: horizontal vertical blur spread color;
```

### Example

```css
.card {
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
}
```

## 2. Text Shadow

Adds a shadow behind text.

```css
h1 {
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
```

## 3. Filter

Applies visual effects to an element.

### Grayscale

```css
img {
    filter: grayscale(100%);
}
```

### Blur

```css
.blur {
    filter: blur(3px);
}
```

### Brightness

```css
.dark {
    filter: brightness(70%);
}
```

### Other Filter Functions

```css
filter: contrast(150%);
filter: sepia(100%);
filter: saturate(200%);
filter: invert(100%);
filter: opacity(50%);
```

## 4. Backdrop Filter

Applies effects to the area behind an element.

```css
.glass {
    background: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
}
```

## 5. Clip Path

Clips an element into a particular shape.

```css
.circle {
    clip-path: circle(50%);
}
```

---

# 28. Transform Properties

Transforms are used to move, rotate, scale or skew an element without changing the normal document flow.

## Transform Properties

| Property | Use |
|---|---|
| `transform` | Applies transformations |
| `transform-origin` | Sets point around which transformation occurs |
| `transform-style` | Controls 3D child rendering |
| `perspective` | Sets perspective depth for 3D transformations |
| `perspective-origin` | Sets viewer position for perspective |
| `backface-visibility` | Controls whether an element's back face is visible |
| `translate` | Moves an element |
| `rotate` | Rotates an element |
| `scale` | Scales an element |

## Common Transform Functions

### 1. Translate

Moves an element.

```css
.box {
    transform: translate(20px, 10px);
}
```

### 2. Translate X

Moves an element horizontally.

```css
.box {
    transform: translateX(20px);
}
```

### 3. Translate Y

Moves an element vertically.

```css
.box {
    transform: translateY(-10px);
}
```

### 4. Rotate

Rotates an element.

```css
.box {
    transform: rotate(45deg);
}
```

### 5. Scale

Changes the size of an element.

```css
.box {
    transform: scale(1.2);
}
```

### 6. Skew

Slants an element.

```css
.box {
    transform: skew(10deg);
}
```

## Transform Origin

Controls the point around which an element rotates or scales.

```css
.box {
    transform-origin: center;
}
```

Other values:

```css
transform-origin: top left;
transform-origin: top right;
transform-origin: bottom left;
transform-origin: bottom right;
```

### Practical Hover Example

```css
.card {
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-4px);
}
```

---

# 29. Transition Properties

Transitions make changes between CSS states appear smooth over a period of time.

## Transition Properties

| Property | Use |
|---|---|
| `transition-property` | Selects the property to transition |
| `transition-duration` | Sets transition duration |
| `transition-timing-function` | Controls speed curve |
| `transition-delay` | Sets delay before transition starts |
| `transition` | Shorthand for transition settings |

## 1. Transition Property

Defines which CSS property should change smoothly.

```css
button {
    transition-property: background-color;
}
```

## 2. Transition Duration

Defines how long the transition takes.

```css
button {
    transition-duration: 0.3s;
}
```

## 3. Transition Timing Function

Controls the speed curve of the transition.

```css
transition-timing-function: ease;
```

Common values:

```css
ease;
linear;
ease-in;
ease-out;
ease-in-out;
```

## 4. Transition Delay

Defines how long the browser waits before starting the transition.

```css
button {
    transition-delay: 0.2s;
}
```

## 5. Transition Shorthand

```css
.button {
    background-color: #2563eb;
    transition: background-color 0.2s ease, transform 0.2s ease;
}

.button:hover {
    background-color: #1d4ed8;
    transform: translateY(-2px);
}
```

---

# 30. Animation Properties

CSS animations allow elements to change their styles over time using `@keyframes`.

Unlike transitions, animations can run automatically and can have multiple stages.

## Keyframes Example

```css
@keyframes slide-in {
    from {
        opacity: 0;
        transform: translateX(-12px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.panel {
    animation: slide-in 0.4s ease both;
}
```

## Animation Properties

| Property | Use |
|---|---|
| `animation-name` | Sets keyframe name |
| `animation-duration` | Sets animation duration |
| `animation-timing-function` | Sets speed curve |
| `animation-delay` | Sets delay |
| `animation-iteration-count` | Sets how many times animation runs |
| `animation-direction` | Sets animation direction |
| `animation-fill-mode` | Controls styles before and after animation |
| `animation-play-state` | Sets running or paused state |
| `animation` | Shorthand for animation settings |

## 1. Animation Name

```css
.box {
    animation-name: bounce;
}
```

## 2. Animation Duration

```css
.box {
    animation-duration: 2s;
}
```

## 3. Animation Iteration Count

```css
.box {
    animation-iteration-count: infinite;
}
```

## 4. Animation Direction

```css
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;
```

## 5. Animation Fill Mode

```css
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;
```

## 6. Animation Play State

```css
animation-play-state: running;
animation-play-state: paused;
```

## Common Animation Timing Functions

```css
animation-timing-function: ease;
animation-timing-function: linear;
animation-timing-function: ease-in;
animation-timing-function: ease-out;
animation-timing-function: ease-in-out;
```

## Complete Bounce Animation

```css
@keyframes bounce {
    0% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-15px);
    }

    100% {
        transform: translateY(0);
    }
}

.box {
    animation: bounce 1s ease infinite;
}
```

---

# 31. Responsive Design and Media Queries

Responsive design makes a website adapt to different screen sizes such as mobile, tablet and desktop.

## What is a Media Query?

A media query allows CSS rules to apply only when specific conditions are true.

### Syntax

```css
@media (condition) {
    selector {
        property: value;
    }
}
```

### Example

```css
@media (max-width: 768px) {
    .navigation {
        flex-direction: column;
    }

    .products {
        grid-template-columns: 1fr;
    }
}
```

## Common Media Features

| Feature | Use |
|---|---|
| `min-width` | Applies styles at or above a viewport width |
| `max-width` | Applies styles at or below a viewport width |
| `orientation` | Detects portrait or landscape orientation |
| `prefers-color-scheme` | Detects light or dark preference |
| `prefers-reduced-motion` | Detects reduced motion preference |
| `hover` | Checks whether primary input can hover |
| `pointer` | Detects pointer accuracy, such as coarse or fine |

## 1. Max Width

Applies styles when the viewport is at or below a specified width.

```css
@media (max-width: 768px) {
    body {
        background-color: lightgray;
    }
}
```

## 2. Min Width

Applies styles when the viewport is at or above a specified width.

```css
@media (min-width: 768px) {
    body {
        background-color: white;
    }
}
```

## 3. Orientation

```css
@media (orientation: landscape) {
    body {
        background-color: lightblue;
    }
}
```

## 4. Dark Mode Preference

```css
@media (prefers-color-scheme: dark) {
    body {
        background-color: #111;
        color: white;
    }
}
```

## 5. Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms;
        transition-duration: 0.01ms;
    }
}
```

## Mobile-First Design

Mobile-first means designing for smaller screens first and then adding styles for larger screens.

### Example

```css
.container {
    width: min(100% - 32px, 1200px);
    margin-inline: auto;
}

.grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
}

@media (min-width: 700px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 1000px) {
    .grid {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

---

# 32. CSS Variables

CSS variables are also called **CSS Custom Properties**.

They store reusable values such as colors, spacing, font sizes and border radius.

## Defining Variables

Variables are commonly defined inside the `:root` selector.

```css
:root {
    --primary-color: #2563eb;
    --text-color: #1f2937;
    --radius: 10px;
    --space: 16px;
}
```

## Using Variables

Use the `var()` function to access a variable.

```css
.button {
    background: var(--primary-color);
    border-radius: var(--radius);
    padding: var(--space);
    color: white;
}
```

## Variable with Fallback Value

```css
.box {
    color: var(--secondary-color, black);
}
```

If `--secondary-color` is not defined, the fallback value `black` is used.

## Variables Inside a Selector

```css
.card {
    --card-padding: 20px;
    padding: var(--card-padding);
}
```

**Note:** CSS custom properties follow the cascade and inheritance rules.

---

# 33. Logical Properties

Logical properties follow the writing direction instead of fixed left/right or top/bottom directions.

They are useful for supporting different languages and writing modes.

## Common Logical Properties

| Property | Use |
|---|---|
| `margin-inline` | Inline-start/end outer spacing |
| `padding-inline` | Inline-start/end inner spacing |
| `margin-block` | Block-start/end outer spacing |
| `padding-block` | Block-start/end inner spacing |
| `border-inline` | Inline-start/end borders |
| `inset-inline` | Logical inline positioning |
| `inset-block` | Logical block positioning |
| `inline-size` | Logical width |
| `block-size` | Logical height |

## Example

```css
.card {
    padding-inline: 20px;
    padding-block: 16px;
    margin-inline: auto;
}
```

### Physical vs Logical Properties

| Physical Property | Logical Property |
|---|---|
| `margin-left` | `margin-inline-start` |
| `margin-right` | `margin-inline-end` |
| `padding-left` | `padding-inline-start` |
| `padding-right` | `padding-inline-end` |
| `width` | `inline-size` |
| `height` | `block-size` |

---

# 34. Accessibility and Best Practices

Writing good CSS is not only about making a website beautiful. It is also important to make it usable and accessible.

## Do's

- Use external CSS for most project styles.
- Prefer reusable classes and meaningful names.
- Organize CSS by component or section.
- Test layouts at different screen sizes.
- Keep keyboard focus visible.
- Ensure sufficient text and background contrast.
- Respect `prefers-reduced-motion` for non-essential animations.
- Add meaningful alt text in HTML for images.
- Use consistent spacing and typography.
- Use flexible layouts instead of fixed widths where possible.

## Don'ts

- Don't memorize every property before building projects.
- Don't use `!important` everywhere.
- Don't remove focus outlines without providing a replacement.
- Don't rely only on color to communicate meaning.
- Don't use fixed widths that break small screens.
- Don't use CSS as a replacement for semantic HTML.
- Don't overuse animations and visual effects.

## Reduced Motion Example

```css
@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        scroll-behavior: auto !important;
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
    }
}
```

---

# 35. Practical Project 1 — Product Card

In this project, we will create a simple product card using HTML and CSS.

## HTML

```html
<div class="product-card">

    <img src="product.jpg" alt="A simple product">

    <div class="product-info">

        <p class="category">HOME ESSENTIALS</p>

        <h2>Product Name</h2>

        <p class="description">
            A useful product for everyday life.
        </p>

        <div class="product-bottom">

            <strong>₹499</strong>

            <button type="button">Add to Cart</button>

        </div>

    </div>

</div>
```

## CSS

```css
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 24px;
    font-family: Arial, sans-serif;
    background: #f3f4f6;
    color: #1f2937;
}

.product-card {
    width: 100%;
    max-width: 320px;
    overflow: hidden;
    background: white;
    border-radius: 14px;
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
}

.product-card img {
    display: block;
    width: 100%;
    height: 210px;
    object-fit: cover;
}

.product-info {
    padding: 18px;
}

.category {
    color: #64748b;
    font-size: 12px;
    letter-spacing: 1px;
}

.description {
    line-height: 1.5;
    color: #475569;
}

.product-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
}

button {
    padding: 10px 14px;
    color: white;
    background: #2563eb;
    border: 0;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background: #1d4ed8;
}
```

### Output Screenshot

<!-- Add your output screenshot here. Recommended size: 600 × 450 px -->

---

# 36. Practical Project 2 — Responsive Navbar

In this project, we will create a responsive navigation bar using Flexbox and Media Queries.

## HTML

```html
<nav class="navbar">

    <a class="logo" href="#">MySite</a>

    <div class="nav-links">

        <a href="#home">Home</a>

        <a href="#about">About</a>

        <a href="#services">Services</a>

        <a href="#contact">Contact</a>

    </div>

</nav>
```

## CSS

```css
* {
    box-sizing: border-box;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    padding: 16px 24px;
    background: #111827;
}

.logo {
    color: white;
    font-size: 22px;
    font-weight: 700;
    text-decoration: none;
}

.nav-links {
    display: flex;
    flex-wrap: wrap;
    gap: 18px;
}

.nav-links a {
    color: #e5e7eb;
    text-decoration: none;
}

.nav-links a:hover {
    color: white;
}

@media (max-width: 600px) {

    .navbar {
        align-items: flex-start;
        flex-direction: column;
    }

    .nav-links {
        flex-direction: column;
        gap: 12px;
    }

}
```

### Output Screenshot

<!-- Add your output screenshot here. Recommended size: 600 × 350 px -->

---

# 37. Quick Reference — Common CSS Properties

| Property | Use |
|---|---|
| `color` | Text color |
| `background` | Background shorthand |
| `font-family` | Typeface |
| `font-size` | Text size |
| `font-weight` | Text thickness |
| `line-height` | Line spacing |
| `text-align` | Text alignment |
| `width` | Element width |
| `height` | Element height |
| `max-width` | Maximum width |
| `margin` | Outer spacing |
| `padding` | Inner spacing |
| `border` | Border |
| `border-radius` | Rounded corners |
| `box-shadow` | Shadow |
| `display` | Layout behaviour |
| `position` | Positioning mode |
| `top` | Top position offset |
| `right` | Right position offset |
| `bottom` | Bottom position offset |
| `left` | Left position offset |
| `z-index` | Stacking order |
| `overflow` | Overflow handling |
| `gap` | Layout gaps |
| `flex` | Flex item sizing |
| `justify-content` | Main-axis/content alignment |
| `align-items` | Item alignment |
| `grid-template-columns` | Grid columns |
| `object-fit` | Image/video fitting |
| `opacity` | Transparency |
| `cursor` | Cursor appearance |
| `transition` | Smooth state change |
| `transform` | Move, rotate, scale and skew |
| `animation` | Keyframe animation |
| `@media` | Responsive styles |
| `var()` | Uses a CSS variable |

---

# 38. CSS Learning Checklist

Use this checklist to track your CSS learning progress.

## CSS Fundamentals

- [ ] Understand CSS syntax.
- [ ] Understand inline, internal and external CSS.
- [ ] Practise element, class and ID selectors.
- [ ] Understand pseudo-classes and pseudo-elements.
- [ ] Understand cascade, specificity and inheritance.

## Styling Fundamentals

- [ ] Practise CSS colors.
- [ ] Understand background properties.
- [ ] Practise CSS units.
- [ ] Understand width and height.
- [ ] Understand the CSS Box Model.
- [ ] Practise margin and padding.
- [ ] Practise borders and outlines.

## Text and Layout

- [ ] Understand font properties.
- [ ] Practise text properties.
- [ ] Understand display properties.
- [ ] Practise visibility and overflow.
- [ ] Understand CSS positioning.
- [ ] Build layouts using Flexbox.
- [ ] Build layouts using CSS Grid.

## Advanced CSS

- [ ] Practise image and media properties.
- [ ] Style lists and tables.
- [ ] Style forms and controls.
- [ ] Practise cursor and interaction properties.
- [ ] Understand shadows and filters.
- [ ] Practise transforms.
- [ ] Understand transitions.
- [ ] Create animations using keyframes.
- [ ] Make websites responsive.
- [ ] Understand CSS variables.
- [ ] Practise logical properties.

## Practical Skills

- [ ] Build a product card.
- [ ] Build a responsive navbar.
- [ ] Create a responsive image gallery.
- [ ] Create a login form.
- [ ] Build a responsive landing page.
- [ ] Practise without copying every line.
- [ ] Learn to use CSS documentation.

---

# 39. Useful Resources

Use these official resources when you want to understand a CSS property in more detail.

1. **MDN CSS Reference:**  
   https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

2. **MDN CSS Guides:**  
   https://developer.mozilla.org/en-US/docs/Web/CSS

3. **CSS Flexbox Guide:**  
   https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout

4. **CSS Grid Guide:**  
   https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout

5. **W3C CSS Validator:**  
   https://jigsaw.w3.org/css-validator/

---

<p align="center"><strong>END OF CSS NOTES</strong></p>
<p align="center">Keep Practising. Keep Building. Keep Improving.</p>
