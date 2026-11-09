# Session-07
# Session 07 – CSS Practice Project

A beginner-friendly practice project designed to apply different CSS properties used to style HTML elements, control backgrounds, customize text, and manage element dimensions.

The main goal is to understand how CSS properties work, explore their available values, and observe how they affect HTML elements.

---

## 📌 Project Overview

This project uses HTML to create a simple webpage containing headings and text elements, while CSS is used to control their appearance and layout.

### Topics Covered
- CSS Colors
- Height
- Background Properties
- Text Properties
- Font Properties
- Text Shadow

---

## 📁 Project Structure

```text
Session 07/
│
├── index.html
│
└── CSS/
    └── Style.css
```

---

# 1. HTML Structure

HTML is used to build the webpage structure, while an external CSS file is linked to control its appearance.

### Linking an External CSS File

```html
<link rel="stylesheet" href="CSS/Style.css">
```

- `rel="stylesheet"` specifies that the linked file is a CSS stylesheet.
- `href` specifies the file path.

### HTML Elements Used

| Element | Function |
|---|---|
| `<h2>` | Defines a level-two heading |
| `<h3>` | Defines a level-three heading |
| `<div>` | Groups HTML elements together |
| `<br>` | Inserts a line break |
| `<link>` | Links an external resource |

### Class Attribute

The `class` attribute is used to identify HTML elements so they can be styled using CSS.

HTML:

```html
<h2 class="demo">Lorem ipsum dolor sit amet</h2>

<div class="span">
    <h2>Hello</h2>
    <h3>Lorem ipsum dolor</h3>
</div>
```

CSS:

```css
.demo {
    color: blue;
}

.span {
    color: red;
}
```

In CSS, a class selector starts with a dot (`.`).

---

# 2. CSS Colors

The `color` property changes the text color of an element.

### Available Color Formats

**1. Color Names**

Using predefined color names:

```css
color: blue;
```

**2. HEX**

Using hexadecimal color codes:

```css
color: #f0ff00;
```

**3. RGB**

RGB stands for Red, Green, and Blue.

```css
color: rgb(255, 0, 0);
```

Each color component usually ranges from 0 to 255.

**4. RGBA**

RGBA adds an Alpha channel to control transparency.

```css
color: rgba(255, 0, 0, 0.5);
```

The last value (`0.5`) represents 50% opacity.

> Note: `rgba(red, green, blue, alpha)` is a descriptive placeholder, not valid CSS color syntax.

---

# 3. Height

The `height` property controls the height of an element.

### Example

```css
height: 3000px;
```

### Common Values

| Value | Description |
|---|---|
| `auto` | Default value; height is generally determined by content and layout |
| `100px` | Sets a fixed height |
| `50%` | Sets height relative to the containing block's height, when that height is definite |
| `fit-content` | Sizes the element according to its content and available space |

### Important Note

```css
height: 3000px;
```

Sets the element's height to exactly 3000 pixels.

On the other hand:

```css
height: fit-content;
```

Allows the element's height to fit its content according to CSS sizing rules.

---

# 4. Background Properties

Background properties control the background appearance of HTML elements.

## 4.1 background-image

Adds an image as an element's background.

```css
background-image: url("../image/image1 (1).webp");
```

- `url()` specifies the image path.
- `../` means going up one directory.
- The path is relative to the CSS file's location.

## 4.2 background-color

Sets the background color of an element.

```css
background-color: greenyellow;
```

Color names, HEX, RGB, and other supported color formats can be used.

## 4.3 background-repeat

Controls whether and how a background image repeats.

```css
background-repeat: no-repeat;
```

### Available Values

| Value | Function |
|---|---|
| `repeat` | Repeats the image horizontally and vertically |
| `repeat-x` | Repeats the image horizontally |
| `repeat-y` | Repeats the image vertically |
| `no-repeat` | Prevents the image from repeating |
| `space` | Distributes repeated images with spaces between them |
| `round` | Adjusts image sizes to fit the available space |

## 4.4 background-size

Controls the size of the background image.

```css
background-size: cover;
```

| Value | Function |
|---|---|
| `auto` | Uses the image's intrinsic dimensions |
| `cover` | Covers the entire element; parts of the image may be cropped |
| `contain` | Displays the entire image; empty space may remain |
| `100% 100%` | Stretches the image to fill the specified width and height |

## 4.5 background-position

Controls the position of the background image.

```css
background-position: top;
```

Examples:

```css
background-position: center;
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
```

Percentage values and pixel values can also be used.

## 4.6 background-attachment

Controls how the background image behaves when the page or element is scrolled.

```css
background-attachment: fixed;
```

| Value | Function |
|---|---|
| `scroll` | Background scrolls with the page; default value |
| `fixed` | Background stays fixed relative to the viewport in typical cases |
| `local` | Background scrolls with the element's content |

---

# 5. Text Properties

These properties control text direction, spacing, alignment, and decoration.

## 5.1 direction

Controls the direction of text.

```css
direction: rtl;
```

| Value | Function |
|---|---|
| `ltr` | Left to Right |
| `rtl` | Right to Left |

This property is useful when working with Arabic and English content.

> Tip: For document-level direction, using the HTML `dir` attribute is often preferable.

Example:

```html
<html lang="ar" dir="rtl">
```

## 5.2 letter-spacing

Controls the space between individual characters.

```css
letter-spacing: 20px;
```

Another example:

```css
letter-spacing: normal;
```

Positive values increase character spacing, while negative values decrease it.

## 5.3 word-spacing

Controls the space between words.

```css
word-spacing: -5px;
```

Positive values increase the spacing between words, while negative values decrease it.

## 5.4 line-height

Controls the height of a line box and the vertical spacing between lines of text.

```css
line-height: 50px;
```

Other examples:

```css
line-height: normal;
line-height: 1.5;
line-height: 50px;
```

The value `1.5` means the line height is 1.5 times the element's font size.

## 5.5 text-align

Controls the horizontal alignment of text.

```css
text-align: center;
```

| Value | Function |
|---|---|
| `left` | Aligns text to the left |
| `right` | Aligns text to the right |
| `center` | Centers the text |
| `justify` | Distributes text across the available line width |
| `start` | Aligns text to the start of the writing direction |
| `end` | Aligns text to the end of the writing direction |

## 5.6 text-transform

Controls the capitalization of displayed text.

```css
text-transform: capitalize;
```

| Value | Function |
|---|---|
| `uppercase` | Converts letters to uppercase |
| `lowercase` | Converts letters to lowercase |
| `capitalize` | Capitalizes the first letter of each word |
| `none` | Applies no transformation |

## 5.7 text-decoration

Adds decorative lines to text.

```css
text-decoration: line-through underline;
```

| Value | Function |
|---|---|
| `underline` | Adds a line below the text |
| `overline` | Adds a line above the text |
| `line-through` | Adds a line through the text |
| `none` | Removes text decoration |

Multiple values can be combined in the same declaration.

---

# 6. Font Properties

The following properties were included in the CSS comments for experimentation.

## 6.1 font-size

Controls the size of the text.

```css
font-size: 20px;
```

## 6.2 font-family

Specifies the font used to display text.

```css
font-family: Arial, Helvetica, sans-serif;
```

The browser tries the fonts in order and uses the first available one.

## 6.3 font-style

Controls the style of the font.

```css
font-style: italic;
```

Common values:

- `normal`
- `italic`
- `oblique`

## 6.4 font-weight

Controls the thickness of the text.

```css
font-weight: bold;
```

Common values:

- `normal`
- `bold`
- `100` to `900`

## 6.5 text-shadow

Adds a shadow effect to text.

```css
text-shadow: 2px 2px 5px gray;
```

The values represent:

1. Horizontal Offset
2. Vertical Offset
3. Blur Radius
4. Shadow Color

---

# 7. Important Notes

- CSS declarations written inside `/* ... */` are comments and are not executed.
- Multiple values can be used with `text-decoration`.
- `letter-spacing` controls the space between characters, while `word-spacing` controls the space between words.
- `background-size: cover` may crop parts of the image.
- `background-size: contain` displays the entire image.
- `text-transform` changes how text is displayed, not the original HTML content.
- `direction` and `text-align` are different properties: one controls writing direction, while the other controls text alignment.

---

# 8. What I Learned

Through this project, I practiced:

1. Using different color formats in CSS.
2. Controlling element dimensions with `height`.
3. Adding background images and colors.
4. Controlling background image size, position, repetition, and attachment.
5. Managing text direction and spacing.
6. Formatting text using `text-align`, `text-transform`, and `text-decoration`.
7. Changing font family, size, style, and weight.
8. Adding shadow effects to text.
9. Using CSS comments to temporarily disable declarations during experimentation.
10. Linking an external CSS file to an HTML document.

---
Thank you
