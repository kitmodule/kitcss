# KitCSS

A lightweight, utility-first CSS framework with state-driven styling through data attributes.

## Why KitCSS?

- ✨ **State-Driven** - Style based on states using data attributes
- 🎯 **Responsive** - Built-in responsive modifiers (mobile, tablet, desktop, laptop)
- 🎨 **Interactive** - Hover, focus, and state-based styling
- 📦 **Lightweight** - Pure CSS, no JavaScript required
- 🚀 **Simple** - Intuitive syntax, easy to learn

## Installation

```bash
npm install kitcss
```

Or use CDN:

```html
<link rel="stylesheet" href="https://unpkg.com/kitcss/dist/main.css">
```

## Core Concept: Data Attributes

KitCSS uses **data attributes** to apply styles based on different states and breakpoints. This makes your HTML more semantic and your styling more dynamic.

### Responsive Modifiers

Apply different styles at different screen sizes using data attributes:

```html
<!-- Hide on mobile, show on desktop -->
<div data-mobile-class="display-none" 
     data-desktop-class="display-block">
  Desktop Only Content
</div>

<!-- Different layouts for different screens -->
<div class="row">
  <div data-mobile-class="column-12" 
       data-tablet-class="column-6" 
       data-desktop-class="column-4">
    Responsive Column
  </div>
</div>

<!-- Different padding on different screens -->
<div data-mobile-class="padding-12" 
     data-tablet-class="padding-24" 
     data-desktop-class="padding-36">
  Responsive Padding
</div>
```

**Available Breakpoints:**
- `data-mobile-class` - max-width: 766px
- `data-tablet-class` - min-width: 767px
- `data-laptop-class` - min-width: 992px  
- `data-desktop-class` - min-width: 1280px

### State Modifiers

Apply styles based on user interaction:

```html
<!-- Change color on hover -->
<button data-hover-class="background-primary color-white">
  Hover Me
</button>

<!-- Show/hide on hover -->
<div class="card" data-hover-class="box-shadow-lg">
  Card with hover effect
</div>

<!-- Focus states for forms -->
<input type="text" 
       data-focus-class="border-primary box-shadow-focus">

<!-- Multiple states -->
<div data-hover-class="scale-105" 
     data-focus-class="outline-primary">
  Interactive Element
</div>
```

**Available State Modifiers:**
- `data-hover-class` - Apply on hover
- `data-focus-class` - Apply on focus
- `data-activate-class` - Apply on active
- `data-disable-class` - Apply when disabled
- `data-group-hover-class` - Apply when parent is hovered
- `data-group-focus-class` - Apply when parent is focused

### Combining Modifiers

You can combine multiple data attributes:

```html
<!-- Responsive + Interactive -->
<button class="button-primary"
        data-mobile-class="width-full"
        data-desktop-class="width-auto"
        data-hover-class="background-dark">
  Adaptive Button
</button>

<!-- Complex responsive layout -->
<div class="container">
  <div data-mobile-class="display-block"
       data-tablet-class="display-flex justify-between"
       data-hover-class="background-light">
    <div data-mobile-class="column-12"
         data-tablet-class="column-6"
         data-desktop-class="column-4">
      Item 1
    </div>
    <div data-mobile-class="column-12"
         data-tablet-class="column-6"
         data-desktop-class="column-4">
      Item 2
    </div>
  </div>
</div>
```

## Components

### Buttons

```html
<button class="button-primary">Primary</button>
<button class="button-success">Success</button>
<button class="button-outline" data-hover-class="background-primary color-white">
  Outline with Hover
</button>
```

### Cards

```html
<div class="card padding-24" data-hover-class="shadow-small">
  <h3>Interactive Card</h3>
  <p>Hovers beautifully</p>
</div>
```

### Responsive Navigation

```html
<nav data-mobile-class="display-block" 
     data-desktop-class="display-flex justify-between">
  <a href="#" data-hover-class="color-primary">Home</a>
  <a href="#" data-hover-class="color-primary">About</a>
  <a href="#" data-hover-class="color-primary">Contact</a>
</nav>
```

### Forms

```html
<input type="text" 
       class="padding-12 border-radius-4"
       data-focus-class="border-primary box-shadow-focus"
       data-hover-class="border-gray">

<textarea class="padding-12"
          data-mobile-class="width-full"
          data-desktop-class="width-auto"
          data-focus-class="border-primary"></textarea>
```

## Utility Classes

### Display

```html
<div class="display-flex">Flex container</div>
<div data-mobile-class="display-block" data-desktop-class="display-flex">
  Responsive display
</div>
```

### Spacing

```html
<div class="padding-24">Padded box</div>
<div data-mobile-class="padding-12" data-desktop-class="padding-36">
  Responsive padding
</div>
```

### Layout

```html
<!-- Flexbox -->
<div class="display-flex justify-center items-center">
  Centered content
</div>

<!-- Responsive Grid -->
<div class="display-grid gap-24"
     data-mobile-class="grid-columns-1"
     data-tablet-class="grid-columns-2"
     data-desktop-class="grid-columns-3">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

### Colors

All color utilities work with data attributes:

```html
<div data-hover-class="background-primary color-white">
  Hover to change color
</div>
```

## Real-World Examples

### Responsive Hero Section

```html
<section class="container"
         data-mobile-class="padding-24 text-center"
         data-desktop-class="padding-72 text-left">
  <h1 data-mobile-class="font-size-32"
      data-desktop-class="font-size-56">
    Welcome to KitCSS
  </h1>
  <button class="button-primary"
          data-mobile-class="width-full"
          data-desktop-class="width-auto"
          data-hover-class="background-dark">
    Get Started
  </button>
</section>
```

### Product Card Grid

```html
<div class="display-grid gap-24"
     data-mobile-class="grid-columns-1"
     data-tablet-class="grid-columns-2"
     data-desktop-class="grid-columns-4">
  
  <div class="card padding-24"
       data-hover-class="box-shadow-xl transform-scale-105">
    <img src="product.jpg" class="width-full">
    <h3>Product Name</h3>
    <p>$29.99</p>
    <button class="button-primary width-full"
            data-hover-class="background-dark">
      Add to Cart
    </button>
  </div>
  
</div>
```

### Navigation Menu

```html
<nav class="container display-flex justify-between items-center"
     data-mobile-class="flex-column"
     data-desktop-class="flex-row">
  
  <div class="logo" data-mobile-class="margin-bottom-24" data-desktop-class="margin-bottom-0">
    Logo
  </div>
  
  <div class="menu"
       data-mobile-class="display-block width-full"
       data-desktop-class="display-flex gap-36">
    <a href="#" data-hover-class="color-primary transform-translate-y--2">Home</a>
    <a href="#" data-hover-class="color-primary transform-translate-y--2">Products</a>
    <a href="#" data-hover-class="color-primary transform-translate-y--2">About</a>
    <a href="#" data-hover-class="color-primary transform-translate-y--2">Contact</a>
  </div>
  
</nav>
```

### Form with Validation States

```html
<form class="card padding-36"
      data-mobile-class="width-full"
      data-desktop-class="width-50-percent margin-x-auto">
  
  <input type="email" 
         class="width-full padding-12 margin-bottom-12"
         data-focus-class="border-primary box-shadow-focus"
         data-hover-class="border-gray"
         placeholder="Email">
  
  <input type="password" 
         class="width-full padding-12 margin-bottom-24"
         data-focus-class="border-primary box-shadow-focus"
         data-hover-class="border-gray"
         placeholder="Password">
  
  <button class="button-primary width-full"
          data-hover-class="background-dark transform-scale-102"
          data-activate-class="background-darker">
    Sign In
  </button>
  
</form>
```

### Dashboard Layout

```html
<div class="container">
  <div class="display-grid gap-24"
       data-mobile-class="grid-columns-1"
       data-tablet-class="grid-columns-2"
       data-desktop-class="grid-columns-4">
    
    <div class="card padding-24"
         data-hover-class="box-shadow-lg border-primary">
      <h3 data-mobile-class="font-size-18" data-desktop-class="font-size-24">
        Users
      </h3>
      <p class="font-size-36 font-weight-bold">1,234</p>
      <span class="color-success">+12%</span>
    </div>
    
    <div class="card padding-24"
         data-hover-class="box-shadow-lg border-success">
      <h3 data-mobile-class="font-size-18" data-desktop-class="font-size-24">
        Revenue
      </h3>
      <p class="font-size-36 font-weight-bold">$12,345</p>
      <span class="color-success">+23%</span>
    </div>
    
  </div>
</div>
```

## Advanced Patterns

### Group Hover Effects

```html
<div class="card padding-24 group">
  <img src="image.jpg" 
       class="width-full"
       data-group-hover-class="transform-scale-110">
  <h3 data-group-hover-class="color-primary">Title</h3>
  <p data-group-hover-class="color-gray">Description</p>
</div>
```

### Conditional Visibility

```html
<!-- Show different content on different devices -->
<div data-mobile-class="display-block" data-desktop-class="display-none">
  Mobile Menu
</div>

<div data-mobile-class="display-none" data-desktop-class="display-block">
  Desktop Menu
</div>
```

### Dynamic Spacing

```html
<section data-mobile-class="padding-24 margin-y-24"
         data-tablet-class="padding-48 margin-y-48"
         data-desktop-class="padding-72 margin-y-72">
  Content with responsive spacing
</section>
```

## Customization

Override CSS variables:

```css
:root {
  --color-brand-rgb: 66, 66, 255;
  --root-sizing: 0.0625rem;
}
```

## Browser Support

Works on all modern browsers (Chrome, Firefox, Safari, Edge).

## Tips & Best Practices

1. **Start Mobile First** - Use base classes for mobile, then add data attributes for larger screens
2. **Combine Wisely** - You can use multiple data attributes on the same element
3. **Keep it Semantic** - Data attributes make your HTML more readable and maintainable
4. **Test Interactions** - Always test hover, focus states on real devices

## Contributing

We welcome contributions! Feel free to:

- 🐛 Report bugs
- 💡 Suggest features  
- 🔧 Submit pull requests
- 📖 Improve documentation

## License

MIT License

## Links

- [GitHub Repository](https://github.com/kitmodule/kitcss)
- [Guide](https://github.com/kitmodule/kitcss/blob/master/guide.md)

---

Made with ❤️ by the KitModule team