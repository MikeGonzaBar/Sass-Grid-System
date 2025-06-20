# Sass Grid System

A lightweight, responsive CSS grid system built with Sass that provides flexible column layouts for web projects.

## Features

- **12-column grid system** with flexible column widths
- **Responsive design** with breakpoints for iPad (768px) and phone (414px)
- **Sass-powered** with mixins and variables for easy customization
- **Clean and semantic** HTML structure
- **Cross-browser compatible** with modern CSS features

## About This Project

This Sass Grid System was built as a learning project to understand Sass (Syntactically Awesome Style Sheets) and how modern CSS styling works. It demonstrates key Sass concepts including:

- **Variables** - For consistent theming and easy customization
- **Mixins** - For reusable responsive breakpoints
- **Nesting** - For cleaner, more organized CSS structure
- **Partials** - For modular code organization
- **CSS Grid concepts** - Understanding responsive layouts and flexbox alternatives

The project serves as a practical example of how Sass can simplify CSS development and make stylesheets more maintainable.

## Grid Classes

The grid system provides the following column classes:

| Class | Width | Description |
|-------|-------|-------------|
| `.col-12` | 100% | Full width column |
| `.col-6` | 50% | Half width column |
| `.col-4` | 33.333% | One-third width column |
| `.col-3` | 25% | Quarter width column |
| `.col-2` | 16.667% | One-sixth width column |
| `.col-1_5` | 12.5% | One-eighth width column |
| `.col-1` | 8.333% | One-twelfth width column |

## Responsive Behavior

### iPad (max-width: 768px)
- `.col-2`, `.col-1`, `.col-1_5` columns stack to 33.333%, 33.333%, and 25% respectively

### Phone (max-width: 414px)
- `.col-4` columns: first two become 50%, third becomes 100%
- `.col-3`, `.col-2`, `.col-1_5`, `.col-1` all become 50% width

## Usage

### Basic Structure

```html
<div class="grid">
    <div class="col-6">Column 1</div>
    <div class="col-6">Column 2</div>
</div>
```

### Examples

**12-column layout:**
```html
<div class="grid">
    <div class="col-12">Full width</div>
</div>
```

**6-column layout:**
```html
<div class="grid">
    <div class="col-6">Half width</div>
    <div class="col-6">Half width</div>
</div>
```

**4-column layout:**
```html
<div class="grid">
    <div class="col-4">One-third</div>
    <div class="col-4">One-third</div>
    <div class="col-4">One-third</div>
</div>
```

**Mixed column layout:**
```html
<div class="grid">
    <div class="col-8">Two-thirds</div>
    <div class="col-4">One-third</div>
</div>
```

## Project Structure

```
Sass-Grid-System/
├── frontpage.html          # Demo page showing grid examples
├── sass/
│   ├── _variables.scss     # Sass variables (colors, etc.)
│   ├── _formatGrids.scss   # Grid layout styles
│   └── styles.scss         # Main stylesheet with grid classes
└── styles/
    ├── styles.css          # Compiled CSS
    └── styles.css.map      # Source map for debugging
```

## Setup

1. **Clone or download** the project files
2. **Compile Sass** to CSS:
   ```bash
   sass sass/styles.scss styles/styles.css
   ```
3. **Open** `frontpage.html` in your browser to see the grid system in action

## Customization

### Colors
Edit `sass/_variables.scss` to customize the grid appearance:
```scss
$colorOfBorder: black;
$colorOfBackground: lightblue;
```

### Breakpoints
Modify the responsive breakpoints in `sass/styles.scss`:
```scss
@mixin ipad{
  @media screen and (max-width: 768px) {
    @content;
  }
}

@mixin phone{
  @media screen and (max-width: 414px) {
    @content;
  }
}
```

### Container Width
Change the maximum container width in `sass/_formatGrids.scss`:
```scss
.container {
    max-width: 1024px; // Adjust this value
    margin: 0 auto;
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Internet Explorer 11+

