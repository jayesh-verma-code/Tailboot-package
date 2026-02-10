# Tailboot-lite

**🔗 Website [tailboot.jayyu.in](https://tailboot.jayyu.in/) | NPM [tailboot-lite](https://www.npmjs.com/package/tailboot-lite)** 

![Tailboot Interface](https://res.cloudinary.com/dzhczzqwf/image/upload/v1770687303/Screenshot_2026-02-10_070225_dx85nn.png)

**Tailboot-lite** is a lightweight utility package that brings a Bootstrap-style 12-column grid system to Tailwind CSS while also enabling automatic responsiveness across all components.

##  Features

- Bootstrap 12-column-grid layout in tailwind (`col-lg-x`, `col-md-x`, etc.)
- Auto Responsiveness with the`.responsive` Class
- Simple setup, fast loading

##  Installation

You can include the library in your project like this:

- `npm i tailboot-lite`

### For HTML
- `<link rel="stylesheet" href="tailboot-lite/css/responsive.css" />`

### For Bundler like React/Vite or Webpack:
- `import 'tailboot-lite/css/responsive.css';`

### Visit official docs/website:
- [Tailboot](https://tailboot.netlify.app/)

## 1. 12-Column Grid System (Tailwind-Compatible)
Ever loved how easy layout design is with Bootstrap’s grid system, but found it incompatible with Tailwind CSS?

Tailboot-lite solves this problem by offering the same familiar 12-column grid layout you know from Bootstrap — but in a way that’s fully compatible with Tailwind. No more conflicts, no more compromises.

### 🔹 Why it matters:
- Bootstrap’s grid system is a powerful tool for responsive design
- But using both Bootstrap and Tailwind together can cause conflicts
- Tailboot-lite lets you enjoy Bootstrap-style layout logic directly within Tailwind projects

### 🔹 How it works:
- Use the row class to create a horizontal layout section
- Use col-x-y classes to define width across breakpoints

`<div className="row">`
  `<div className="box col-lg-6 col-md-12"></div>`
  `<div className="box col-lg-6 col-md-12"></div>`
`</div>`
In the above example:

- On large screens (≥1000px): Both boxes occupy 50% width (6 of 12 columns)
-  On medium screens (750px to 1000px): Each box spans full width (12 of 12), stacking vertically

###  Supported Breakpoints:
- **Class Prefix	Screen Width Range**
- `col-lg-x`	≥ 1000px
- `col-md-x`	1000px to 750px
- `col-sm-x`	750px to 500px
- `col-x`   	< 500px (default mobile)

`x` can be any even number from 2 to 12 to represent how many columns out of 12 the element should span.

## 2. Auto Responsiveness with the responsive Class
Responsive design isn’t just about layout — it’s about dynamic resizing of all design properties, including:

- Font sizes
- Widths & heights
- Spacings
- Component dimensions

With Tailboot-lite, simply add a single class to your root element and let it handle responsiveness across your entire app.

###  How to enable:
- `<html class="responsive">`
Once added:

- All REM-based units dynamically scale down as screen size reduces
- No need to manually write multiple responsive utility classes for common sizing
- Works beautifully with Tailwind’s utility-first approach

###  Note:
Tailboot-lite assumes 1rem = 10px instead of the traditional 1rem = 16px, making it easier to calculate spacing and sizing mentally.

#### Example:
Instead of calculating 52px = 3.25rem, just use 5.2rem (since 10px = 1rem)

####  Manual overrides still possible:
Want to override for a specific breakpoint? Just use Tailwind’s built-in responsive utilities:
- `<div className="w-[20rem] sm:w-[10rem]">Hello</div>`


## 📄 License
Free to use 😉✌️. Give credit if you like it!

Made with ❤️ by **Jayesh Verma [NIT R]**.
