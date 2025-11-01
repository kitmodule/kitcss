# KitCSS - Complete AI Assistant Guide

This is a comprehensive guide for AI assistants to understand and effectively use KitCSS framework.

## 🎯 Core Philosophy

KitCSS is a **data-attribute driven CSS framework** that enables:
- **State-based styling** through data attributes
- **Responsive design** without media query classes
- **Pure CSS** implementation (no JavaScript required)
- **SSR-friendly** architecture

## 📋 Quick Reference

### Basic Structure

```html
<!-- Standard utility class -->
<div class="padding-24 margin-12">Content</div>

<!-- Data-attribute for responsive -->
<div data-mobile-class="padding-12" 
     data-desktop-class="padding-48">
  Responsive Content
</div>

<!-- Data-attribute for states -->
<button data-hover-class="background-primary color-white">
  Hover Me
</button>
```

## 🎨 Available Data Attributes

### 1. Responsive Breakpoints

| Attribute | Media Query | Usage |
|-----------|-------------|-------|
| `data-mobile-class` | `@media (max-width: 766px)` | Mobile-only styles |
| `data-tablet-class` | `@media (min-width: 767px)` | Tablet and up |
| `data-laptop-class` | `@media (min-width: 992px)` | Laptop and up |
| `data-desktop-class` | `@media (min-width: 1280px)` | Desktop and up |

### 2. Interactive States

| Attribute | Trigger | Usage |
|-----------|---------|-------|
| `data-hover-class` | `:hover` | Mouse hover effects |
| `data-focus-class` | `:focus` | Focus states for inputs |
| `data-activate-class` | `:active` | Click/press states |
| `data-disable-class` | `:disabled` | Disabled states |
| `data-group-hover-class` | Parent `:hover` | Child reacts to parent hover |
| `data-group-focus-class` | Parent `:focus` | Child reacts to parent focus |

## 🔧 Complete Utility Classes Reference

### Display

```
display-none, display-block, display-inline, display-inline-block
display-flex, display-inline-flex, display-grid, display-inline-grid
display-table, display-table-row, display-table-cell, display-contents
```

### Flexbox

```
flex-row, flex-column, flex-row-reverse, flex-column-reverse
flex-wrap, flex-nowrap, flex-wrap-reverse
justify-start, justify-end, justify-center, justify-between, justify-around, justify-evenly
items-start, items-end, items-center, items-baseline, items-stretch
self-start, self-end, self-center, self-baseline, self-stretch, self-auto
flex-1, flex-auto, flex-initial, flex-none
flex-grow, flex-grow-0, flex-grow-1
flex-shrink, flex-shrink-0, flex-shrink-1
```

### Grid

```
grid-columns-1, grid-columns-2, ..., grid-columns-12
grid-rows-1, grid-rows-2, ..., grid-rows-6
gap-0, gap-1, gap-2, gap-3, gap-4, gap-5, gap-6, gap-7, gap-8, gap-9, gap-12, gap-24, gap-36, gap-48, gap-60, gap-72, gap-96
column-span-1, ..., column-span-12, column-span-full
row-span-1, ..., row-span-6, row-span-full
```

### Spacing (Padding & Margin)

**Pattern:** `padding-{size}`, `margin-{size}`, `padding-x-{size}`, `padding-y-{size}`, `margin-x-{size}`, `margin-y-{size}`

**Available sizes:**
```
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 12, 14, 16, 18, 20, 22, 24, 30, 36, 48, 50, 56, 60, 72, 80, 96, 120, 180, 240, 320, 360
```

**Examples:**
```html
<div class="padding-24">All sides padding</div>
<div class="padding-x-12 padding-y-24">Horizontal and vertical</div>
<div class="margin-top-12 margin-bottom-24">Individual sides</div>
```

### Positioning

```
position-relative, position-absolute, position-fixed, position-sticky
top-0, right-0, bottom-0, left-0
top-12, top-24, top-36, ... (same sizes as spacing)
top-50-percent, left-50-percent, top-full, left-full
inset-0 (shorthand for top-0 right-0 bottom-0 left-0)
```

### Sizing

```
width-full, width-auto, width-screen
height-full, height-auto, height-screen
width-1/2, width-1/3, width-2/3, width-1/4, width-3/4
width-25-percent, width-50-percent, width-75-percent, width-100-percent
```

### Typography

```
text-left, text-center, text-right, text-justify
font-size-12, font-size-14, font-size-16, font-size-18, font-size-20, font-size-24, font-size-32, font-size-36, font-size-48
font-weight-light, font-weight-normal, font-weight-medium, font-weight-bold
```

### Colors

**Background Colors:**
```
background-white, background-black, background-primary, background-success
background-danger, background-warning, background-info
background-dark, background-light, background-ghost
```

**Text Colors:**
```
color-white, color-black, color-primary, color-success
color-danger, color-warning, color-info
color-dark, color-light, color-gray
```

### Borders

```
border-0, border-1, border-2, border-4
border-radius-0, border-radius-2, border-radius-4, border-radius-8, border-radius-12
border-primary, border-success, border-danger, border-gray
```

### Order (Flexbox/Grid)

```
order-0, order-1, order-2, ..., order-12
order-first, order-last
```

## 📦 Pre-built Components

### Buttons

```html
<!-- Solid buttons -->
<button class="button-flat">Flat</button>
<button class="button-raised">Raised</button>

<!-- Outlined buttons -->
<button class="button-outline">Outline</button>
<button class="button-stroked">Stroked</button>

<!-- Color variants -->
<button class="button-primary">Primary</button>
<button class="button-success">Success</button>
<button class="button-danger">Danger</button>
<button class="button-warning">Warning</button>
<button class="button-info">Info</button>
```

### Cards

```html
<div class="card padding-24">
  <h3>Card Title</h3>
  <p>Card content</p>
</div>

<div class="card-outline padding-24">
  <h3>Outlined Card</h3>
</div>

<div class="card-flat padding-24">
  <h3>Flat Card</h3>
</div>
```

### Grid System

```html
<!-- Container -->
<div class="container">
  <!-- 12-column row -->
  <div class="row">
    <div class="column-6">Half</div>
    <div class="column-6">Half</div>
  </div>
  
  <!-- Auto columns -->
  <div class="row row-columns-3">
    <div>Auto 1/3</div>
    <div>Auto 1/3</div>
    <div>Auto 1/3</div>
  </div>
</div>
```

### Forms

```html
<!-- Checkbox -->
<input type="checkbox" class="checkbox checkbox-primary">

<!-- Radio -->
<input type="radio" class="radio radio-success">

<!-- Switch -->
<input type="checkbox" class="checkbox switch">

<!-- Progress -->
<progress class="progress-bar progress-primary" value="70" max="100"></progress>
<progress class="progress-spinner progress-info"></progress>
```

### Badges

```html
<span class="badge" data-badge="5">Notifications</span>
<span class="badge-dot badge-top-right" data-badge="">Status</span>
<span class="badge-electron badge-top-right" data-badge="NEW">Feature</span>
```

### Dropdown

```html
<div class="dropdown">
  <button class="dropdown-button">Menu</button>
  <div class="dropdown-menu">
    <a href="#">Option 1</a>
    <a href="#">Option 2</a>
  </div>
</div>
```

### Tabs

```html
<div class="tab">
  <input type="radio" name="tabs" id="tab1" checked>
  <label for="tab1">Tab 1</label>
  <div class="tab-content">Content 1</div>

  <input type="radio" name="tabs" id="tab2">
  <label for="tab2">Tab 2</label>
  <div class="tab-content">Content 2</div>
</div>
```

## 🎓 AI Assistant Usage Patterns

### Pattern 1: Mobile-First Responsive Design

**Rule:** Always start with mobile base classes, then add data attributes for larger screens.

```html
<!-- ✅ CORRECT: Mobile-first approach -->
<div class="padding-12 display-block"
     data-tablet-class="padding-24"
     data-desktop-class="padding-48 display-flex">
  Content
</div>

<!-- ❌ WRONG: Don't use only desktop classes -->
<div data-desktop-class="padding-48 display-flex">
  Content
</div>
```

### Pattern 2: Interactive States

**Rule:** Use data-hover-class and data-focus-class for interactive feedback.

```html
<!-- ✅ CORRECT: Clear hover states -->
<button class="button-primary"
        data-hover-class="background-dark transform-scale-105">
  Click Me
</button>

<!-- ✅ CORRECT: Form focus states -->
<input type="text" 
       class="padding-12 border-radius-4"
       data-focus-class="border-primary box-shadow-focus">
```

### Pattern 3: Responsive Layouts

**Rule:** Combine grid/flexbox with responsive data attributes.

```html
<!-- ✅ CORRECT: Responsive grid -->
<div class="display-grid gap-24"
     data-mobile-class="grid-columns-1"
     data-tablet-class="grid-columns-2"
     data-desktop-class="grid-columns-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
  <div>Item 4</div>
</div>
```

### Pattern 4: Component with Multiple States

**Rule:** Combine multiple data attributes for rich interactions.

```html
<!-- ✅ CORRECT: Rich interactive card -->
<div class="card padding-24"
     data-mobile-class="margin-12"
     data-desktop-class="margin-24"
     data-hover-class="box-shadow-xl transform-scale-102"
     data-group-hover-class="background-light">
  <img src="image.jpg" 
       class="width-full"
       data-group-hover-class="transform-scale-110">
  <h3 data-group-hover-class="color-primary">Title</h3>
</div>
```

## 🏗️ Common Layouts for AI to Generate

### 1. Hero Section

```html
<section class="container"
         data-mobile-class="padding-24 text-center"
         data-desktop-class="padding-72 text-left">
  <h1 data-mobile-class="font-size-32"
      data-desktop-class="font-size-56">
    Hero Title
  </h1>
  <p data-mobile-class="font-size-16"
     data-desktop-class="font-size-20">
    Hero description text goes here
  </p>
  <button class="button-primary"
          data-mobile-class="width-full margin-top-24"
          data-desktop-class="width-auto margin-top-36"
          data-hover-class="background-dark">
    Call to Action
  </button>
</section>
```

### 2. Navigation Bar

```html
<nav class="container display-flex items-center"
     data-mobile-class="flex-column padding-y-12"
     data-desktop-class="flex-row justify-between padding-y-24">
  
  <div class="logo" 
       data-mobile-class="margin-bottom-12" 
       data-desktop-class="margin-bottom-0">
    <h1>Logo</h1>
  </div>
  
  <div class="menu"
       data-mobile-class="display-block width-full text-center"
       data-desktop-class="display-flex gap-36">
    <a href="#" 
       class="padding-12"
       data-hover-class="color-primary">Home</a>
    <a href="#" 
       class="padding-12"
       data-hover-class="color-primary">Products</a>
    <a href="#" 
       class="padding-12"
       data-hover-class="color-primary">About</a>
    <a href="#" 
       class="padding-12"
       data-hover-class="color-primary">Contact</a>
  </div>
</nav>
```

### 3. Product Grid

```html
<div class="container">
  <div class="display-grid gap-24"
       data-mobile-class="grid-columns-1"
       data-tablet-class="grid-columns-2"
       data-desktop-class="grid-columns-4">
    
    <!-- Product Card -->
    <div class="card padding-24"
         data-hover-class="box-shadow-xl transform-scale-105">
      <img src="product.jpg" 
           class="width-full border-radius-8 margin-bottom-12">
      <h3 class="margin-bottom-8">Product Name</h3>
      <p class="color-gray margin-bottom-12">Product description</p>
      <p class="font-size-24 font-weight-bold margin-bottom-12">$29.99</p>
      <button class="button-primary width-full"
              data-hover-class="background-dark">
        Add to Cart
      </button>
    </div>
    
  </div>
</div>
```

### 4. Form Layout

```html
<form class="card padding-36"
      data-mobile-class="width-full"
      data-desktop-class="width-50-percent margin-x-auto">
  
  <h2 class="margin-bottom-24">Sign In</h2>
  
  <div class="margin-bottom-12">
    <label class="display-block margin-bottom-4">Email</label>
    <input type="email" 
           class="width-full padding-12 border-radius-4"
           data-focus-class="border-primary box-shadow-focus"
           data-hover-class="border-gray">
  </div>
  
  <div class="margin-bottom-24">
    <label class="display-block margin-bottom-4">Password</label>
    <input type="password" 
           class="width-full padding-12 border-radius-4"
           data-focus-class="border-primary box-shadow-focus"
           data-hover-class="border-gray">
  </div>
  
  <button class="button-primary width-full"
          data-hover-class="background-dark"
          data-activate-class="background-darker">
    Sign In
  </button>
</form>
```

### 5. Dashboard Cards

```html
<div class="container">
  <div class="display-grid gap-24"
       data-mobile-class="grid-columns-1"
       data-tablet-class="grid-columns-2"
       data-desktop-class="grid-columns-4">
    
    <div class="card padding-24"
         data-hover-class="box-shadow-lg border-primary">
      <h3 class="color-gray margin-bottom-8"
          data-mobile-class="font-size-16"
          data-desktop-class="font-size-18">
        Total Users
      </h3>
      <p class="font-size-36 font-weight-bold margin-bottom-4">1,234</p>
      <span class="color-success font-size-14">+12% from last month</span>
    </div>
    
    <div class="card padding-24"
         data-hover-class="box-shadow-lg border-success">
      <h3 class="color-gray margin-bottom-8"
          data-mobile-class="font-size-16"
          data-desktop-class="font-size-18">
        Revenue
      </h3>
      <p class="font-size-36 font-weight-bold margin-bottom-4">$12,345</p>
      <span class="color-success font-size-14">+23% from last month</span>
    </div>
    
  </div>
</div>
```

## 🚫 Common Mistakes to Avoid

### ❌ Mistake 1: Using responsive classes instead of data attributes

```html
<!-- WRONG: Using md:, lg: style classes -->
<div class="padding-12 md:padding-24 lg:padding-48">

<!-- CORRECT: Using data attributes -->
<div class="padding-12"
     data-tablet-class="padding-24"
     data-desktop-class="padding-48">
```

### ❌ Mistake 2: Forgetting mobile-first base classes

```html
<!-- WRONG: Only desktop styling -->
<div data-desktop-class="display-flex padding-48">

<!-- CORRECT: Mobile base + desktop override -->
<div class="display-block padding-24"
     data-desktop-class="display-flex padding-48">
```

### ❌ Mistake 3: Over-nesting data attributes

```html
<!-- WRONG: Too complex -->
<div data-mobile-class="display-block padding-12 margin-12 font-size-14 color-primary background-white border-radius-4">

<!-- CORRECT: Split into base + override -->
<div class="display-block padding-12 color-primary background-white border-radius-4"
     data-desktop-class="padding-24 font-size-16">
```

### ❌ Mistake 4: Not using component classes

```html
<!-- WRONG: Recreating button styles -->
<button class="padding-12 border-radius-4 background-primary color-white"
        data-hover-class="background-dark">

<!-- CORRECT: Using button component -->
<button class="button-primary"
        data-hover-class="background-dark">
```

## 📝 Decision Tree for AI Assistants

```
When styling an element:

1. Is it a common component? (button, card, form input)
   YES → Use component class (button-primary, card, checkbox)
   NO → Continue to 2

2. Does it need responsive behavior?
   YES → Use base class + data-{breakpoint}-class
   NO → Continue to 3

3. Does it need interactive states?
   YES → Add data-hover-class or data-focus-class
   NO → Continue to 4

4. Use standard utility classes
   (display-flex, padding-24, margin-12, etc.)
```

## 🎯 Best Practices Summary

1. **Always start mobile-first**: Base classes for mobile, data attributes for larger screens
2. **Use component classes when available**: button-primary, card, checkbox, etc.
3. **Combine data attributes freely**: An element can have multiple data-{state}-class
4. **Keep base classes simple**: Don't overload with too many classes
5. **Use semantic grouping**: Group related responsive/state changes
6. **Test states**: Always include hover and focus states for interactive elements
7. **Maintain consistency**: Use the same breakpoint pattern across the project

## 🔍 Quick Troubleshooting

**Issue:** Styles not applying
- ✓ Check if using correct data attribute name (data-mobile-class, not data-mobile)
- ✓ Verify class name exists in utility list
- ✓ Ensure proper spacing in class names

**Issue:** Responsive not working
- ✓ Always include base class for mobile
- ✓ Check breakpoint order (mobile < tablet < laptop < desktop)
- ✓ Test in browser dev tools at correct widths

**Issue:** Hover states not working
- ✓ Use data-hover-class, not :hover pseudo-class
- ✓ Check if element is interactive (button, a, input)
- ✓ Verify class name is correct

## 📚 Additional Resources

- KitCSS is designed to work with SSR (Server-Side Rendering)
- All styles are pure CSS, no JavaScript runtime required
- Data attributes are parsed at build time
- Compatible with modern browsers (Chrome, Firefox, Safari, Edge)

---

**For AI Assistants:** When generating KitCSS code:
1. Always use data attributes for responsive and state styling
2. Prefer component classes over custom utility combinations
3. Follow mobile-first approach
4. Include interactive states (hover, focus) for better UX
5. Keep markup clean and semantic