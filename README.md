# Tailboot

**Bootstrap-style grid system for Tailwind CSS — without conflicts**

**🔗 Website: [tailboot.jayyu.in](https://tailboot.jayyu.in)
| NPM: [tailboot-lite](https://www.npmjs.com/package/tailboot-lite)**

![](https://res.cloudinary.com/dzhczzqwf/image/upload/v1770687303/Screenshot_2026-02-10_070225_dx85nn.png)

Tailboot-lite is a lightweight utility package that brings Bootstrap’s familiar **12-column grid system** to **Tailwind CSS**, along with **automatic responsiveness** for sizing, spacing, and typography. It is designed to work seamlessly with Tailwind without introducing Bootstrap or causing style conflicts.

---

## Features

### 1. Bootstrap-like 12-Column Grid (Tailwind-Compatible)

* Familiar `col-lg-x`, `col-md-x`, `col-sm-x` syntax
* No Bootstrap dependency
* No Tailwind conflicts
* Clean and readable layout structure

### 2. Automatic Responsiveness

* Enable responsiveness with a single `.responsive` class
* Automatically scales:

  * Font sizes
  * Widths and heights
  * Spacing and component dimensions
* Reduces the need for repetitive responsive utility classes

---

## Installation

Install via npm:

```bash
npm install tailboot-lite
```

### Usage in HTML

```html
<link rel="stylesheet" href="tailboot-lite/css/responsive.css" />
```

### Usage with Bundlers (React, Vite, Webpack)

```js
import 'tailboot-lite/css/responsive.css';
```

---

## 12-Column Grid System

Tailboot-lite replicates Bootstrap’s grid behavior while remaining fully compatible with Tailwind CSS.

### Basic Usage

```html
<div class="row">
  <div class="col-lg-6 col-md-12">Content</div>
  <div class="col-lg-6 col-md-12">Content</div>
</div>
```

### Behavior

* Large screens (≥ 1000px): Each column occupies 6 of 12 columns (50% width)
* Medium screens (750px – 1000px): Each column spans full width (12 of 12)
* Smaller screens: Columns stack vertically by default

---

## Supported Breakpoints

| Class Prefix | Screen Width      |
| ------------ | ----------------- |
| `col-lg-x`   | ≥ 1000px          |
| `col-md-x`   | 750px – 1000px    |
| `col-sm-x`   | 500px – 750px     |
| `col-x`      | < 500px (default) |

`x` can be any even number between `2` and `12`, representing the number of columns out of 12.

---

## Automatic Responsiveness

Responsive design in Tailboot-lite goes beyond layout. It automatically scales all REM-based values across screen sizes.

### Enable Auto Responsiveness

Add the `responsive` class to your root element:

```html
<html class="responsive">
```

### How It Works

* Assumes `1rem = 10px` instead of the default `16px`
* Makes spacing and sizing calculations easier
* Automatically scales UI elements as screen size changes

### Example

Instead of:

```css
52px = 3.25rem
```

You can use:

```css
5.2rem
```

### Manual Overrides

You can still use Tailwind’s responsive utilities when needed:

```html
<div class="w-[20rem] sm:w-[10rem]">
  Hello
</div>
```

---

## License

Free to use. Attribution is appreciated 😊.

---

## Author

Made with 💓 by **Jayesh Verma  (NIT R)**

---
