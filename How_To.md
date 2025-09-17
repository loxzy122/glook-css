# Glook 3.0 Framework - Documentation

## Overview

Glook 3.0 is a Google-inspired CSS framework with a comprehensive set of components and utilities for building modern, responsive web applications. It features a clean Material Design aesthetic with a flexible grid system, numerous UI components, and JavaScript interactions.

## Installation

### Option 1: Direct File Inclusion
Include the following files in your HTML project:

```html
<!-- In your head section -->
<link rel="stylesheet" href="path/to/glook3.0.min.css">

<!-- Before closing body tag -->
<script src="path/to/glook.min.js"></script>
```

### Option 2: CDN (if available)
```html
<!-- Replace with your actual CDN links -->
<link rel="stylesheet" href="https://cdn.example.com/glook3.0.min.css">
<script src="https://cdn.example.com/glook.min.js"></script>
```

## Getting Started

### Basic Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glook 3.0 App</title>
    <link rel="stylesheet" href="glook3.0.min.css">
</head>
<body>
    <div class="container">
        <h1>Hello Glook 3.0</h1>
        <button class="btn btn-primary">Click Me</button>
    </div>
    
    <script src="glook.min.js"></script>
</body>
</html>
```

## Core Concepts

### Color System
Glook 3.0 uses CSS custom properties for theming:

```css
:root {
    --primary: #1a73e8;        /* Primary brand color */
    --primary-hover: #1765cc;  /* Primary hover state */
    --secondary: #34a853;      /* Secondary color */
    --danger: #ea4335;         /* Error/danger color */
    --warning: #fbbc04;        /* Warning color */
    --info: #4285f4;           /* Informational color */
    --success: #34a853;        /* Success color */
    --surface: #ffffff;        /* Surface/background for components */
    --background: #f8f9fa;     /* Page background */
    --on-surface: #202124;     /* Text on surfaces */
    --on-surface-variant: #5f6368; /* Secondary text */
    --outline: #dadce0;        /* Borders and dividers */
    --outline-variant: #e8eaed; /* Lighter borders */
    --shadow: rgba(60,64,67,0.3); /* Shadow color */
    --shadow-light: rgba(60,64,67,0.15); /* Light shadow */
}
```

### Typography
Glook provides a typography scale with semantic classes:

```html
<h1 class="h1">Heading 1</h1>
<h2 class="h2">Heading 2</h2>
<h3 class="h3">Heading 3</h3>
<h4 class="h4">Heading 4</h4>
<h5 class="h5">Heading 5</h5>
<h6 class="h6">Heading 6</h6>
<p class="body1">Body text 1</p>
<p class="body2">Body text 2</p>
<p class="caption">Caption text</p>
```

## Layout System

### Containers
```html
<div class="container">Fixed width container</div>
<div class="container-fluid">Full width container</div>
<div class="container-sm">Small container</div>
<div class="container-md">Medium container</div>
<div class="container-lg">Large container</div>
<div class="container-xl">Extra large container</div>
```

### Grid System
Glook uses a 12-column flexbox grid system:

```html
<div class="row">
    <div class="col-6">50% width</div>
    <div class="col-6">50% width</div>
</div>

<div class="row">
    <div class="col-4">33.3% width</div>
    <div class="col-4">33.3% width</div>
    <div class="col-4">33.3% width</div>
</div>
```

Responsive grid classes:
- `col-md-*` for medium screens (≥768px)
- `col-lg-*` for large screens (≥992px)
- `col-xl-*` for extra large screens (≥1200px)

### Flexbox Utilities
```html
<div class="d-flex justify-center align-center">
    <div>Centered content</div>
</div>
```

Available classes:
- Display: `d-flex`, `d-inline-flex`, `d-block`, `d-inline`, `d-inline-block`, `d-none`
- Direction: `flex-row`, `flex-column`
- Wrapping: `flex-wrap`, `flex-nowrap`
- Justify: `justify-start`, `justify-end`, `justify-center`, `justify-between`, `justify-around`, `justify-evenly`
- Align: `align-start`, `align-end`, `align-center`, `align-baseline`, `align-stretch`
- Flex properties: `flex-grow-0`, `flex-grow-1`, `flex-shrink-0`, `flex-shrink-1`

### Spacing Utilities
Margin and padding utilities using the spacing scale:

```html
<div class="m-3 p-3">Medium margin and padding</div>
<div class="mx-auto my-4">Auto horizontal margins, large vertical margins</div>
<div class="px-2 py-3">Horizontal small padding, vertical medium padding</div>
```

Spacing scale:
- `--spacing-xs`: 4px
- `--spacing-sm`: 8px
- `--spacing-md`: 16px
- `--spacing-lg`: 24px
- `--spacing-xl`: 32px

## Components

### Buttons
```html
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
<button class="btn btn-outline">Outline Button</button>
<button class="btn btn-text">Text Button</button>

<!-- Sizes -->
<button class="btn btn-primary btn-sm">Small Button</button>
<button class="btn btn-primary btn-lg">Large Button</button>

<!-- Disabled state -->
<button class="btn btn-primary" disabled>Disabled Button</button>
```

### Cards
```html
<div class="card">
    <div class="card-header">
        <h3 class="card-title">Card Title</h3>
        <p class="card-subtitle">Card subtitle</p>
    </div>
    <p>Card content goes here</p>
</div>
```

### Forms
```html
<div class="form-group">
    <label class="form-label">Email address</label>
    <input type="email" class="form-control" placeholder="Enter email">
</div>

<div class="form-group">
    <label class="form-label required">Required Field</label>
    <input type="text" class="form-control" required>
</div>

<!-- Material Design Input -->
<div class="input-group">
    <input type="text" class="input-material" placeholder=" ">
    <label class="input-label">Material Input</label>
</div>

<!-- Checkboxes and Radios -->
<div class="form-check">
    <input type="checkbox" class="form-check-input" id="checkbox1">
    <label class="form-check-label" for="checkbox1">Checkbox</label>
</div>

<!-- Switch -->
<div class="form-switch">
    <input type="checkbox" class="switch-input" id="switch1">
    <label class="switch" for="switch1"></label>
    <label for="switch1">Toggle switch</label>
</div>

<!-- File Input -->
<div class="file-input">
    <input type="file" id="file1">
    <label class="file-input-label" for="file1">
        <span>📁</span> Choose a file
    </label>
</div>
```

### Tables
```html
<div class="table-container">
    <table class="table">
        <thead>
            <tr>
                <th>Name</th>
                <th>Email</th>
                <th>Status</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>John Doe</td>
                <td>john@example.com</td>
                <td><span class="table-status status-active">Active</span></td>
            </tr>
        </tbody>
    </table>
</div>

<!-- Table variants -->
<table class="table table-striped">Striped rows</table>
<table class="table table-bordered">Bordered table</table>
<table class="table table-sm">Small table</table>
<table class="table table-lg">Large table</table>

<!-- Sortable table -->
<table class="table table-sortable">
    <thead>
        <th data-sort="name">Name ↕</th>
        <!-- Becomes ↑ or ↓ when sorted -->
    </thead>
</table>

<!-- Responsive table -->
<div class="table-responsive">
    <table class="table">...</table>
</div>
```

### Alerts
```html
<div class="alert alert-info">
    <div class="alert-icon">ℹ️</div>
    <div class="alert-content">
        <h4 class="alert-title">Information</h4>
        <p class="alert-message">This is an info alert.</p>
    </div>
    <button class="alert-dismiss">×</button>
</div>

<!-- Alert variants -->
<div class="alert alert-success">Success alert</div>
<div class="alert alert-warning">Warning alert</div>
<div class="alert alert-danger">Danger alert</div>
```

### Badges
```html
<span class="badge badge-primary">Primary</span>
<span class="badge badge-secondary">Secondary</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-danger">Danger</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-info">Info</span>
<span class="badge badge-light">Light</span>
<span class="badge badge-outline">Outline</span>

<!-- Sizes -->
<span class="badge badge-primary badge-sm">Small</span>
<span class="badge badge-primary badge-lg">Large</span>

<!-- Pill style -->
<span class="badge badge-primary badge-pill">Pill</span>
```

### Tooltips
```html
<div class="tooltip tooltip-top">
    Hover me
    <span class="tooltip-text">Tooltip text</span>
</div>

<!-- Positions -->
<div class="tooltip tooltip-bottom">Bottom tooltip</div>
<div class="tooltip tooltip-left">Left tooltip</div>
<div class="tooltip tooltip-right">Right tooltip</div>
```

### Modals
```html
<!-- Modal trigger -->
<button onclick="openModal('exampleModal')">Open Modal</button>

<!-- Modal structure -->
<div class="modal" id="exampleModal">
    <div class="modal-content">
        <div class="modal-header">
            <h3 class="modal-title">Modal Title</h3>
            <button class="modal-close" onclick="closeModal('exampleModal')">×</button>
        </div>
        <div class="modal-body">
            <p>Modal content goes here</p>
        </div>
        <div class="modal-footer">
            <button class="btn btn-text" onclick="closeModal('exampleModal')">Cancel</button>
            <button class="btn btn-primary">Save</button>
        </div>
    </div>
</div>

<!-- Modal sizes -->
<div class="modal modal-sm">Small modal</div>
<div class="modal modal-lg">Large modal</div>
<div class="modal modal-xl">Extra large modal</div>
```

JavaScript functions for modal control:
```js
function openModal(id) {
    document.getElementById(id).classList.add('open');
}

function closeModal(id) {
    document.getElementById(id).classList.remove('open');
}
```

### Dropdowns
```html
<div class="dropdown">
    <button class="dropdown-toggle btn btn-primary">
        Dropdown
    </button>
    <div class="dropdown-menu">
        <a href="#" class="dropdown-item">Action 1</a>
        <a href="#" class="dropdown-item">Action 2</a>
        <div class="dropdown-divider"></div>
        <a href="#" class="dropdown-item">Separated action</a>
    </div>
</div>

<!-- Dropdown positions -->
<div class="dropdown">
    <button class="dropdown-toggle">Right dropdown</button>
    <div class="dropdown-menu dropdown-menu-right">...</div>
</div>

<div class="dropdown">
    <button class="dropdown-toggle">Upward dropdown</button>
    <div class="dropdown-menu dropdown-menu-up">...</div>
</div>
```

### Progress Bars
```html
<div class="progress">
    <div class="progress-bar" style="width: 50%"></div>
</div>

<!-- Sizes -->
<div class="progress progress-sm">Small progress</div>
<div class="progress progress-lg">Large progress</div>

<!-- Variants -->
<div class="progress">
    <div class="progress-bar progress-bar-success" style="width: 30%"></div>
</div>
<div class="progress">
    <div class="progress-bar progress-bar-danger" style="width: 30%"></div>
</div>
<div class="progress">
    <div class="progress-bar progress-bar-warning" style="width: 30%"></div>
</div>
<div class="progress">
    <div class="progress-bar progress-bar-info" style="width: 30%"></div>
</div>

<!-- Animated -->
<div class="progress">
    <div class="progress-bar progress-animated" style="width: 50%"></div>
</div>

<!-- With label -->
<div class="progress progress-labeled">
    <div class="progress-bar" style="width: 75%"></div>
    <span class="progress-label">75%</span>
</div>
```

### Spinners
```html
<div class="spinner"></div>

<!-- Sizes -->
<div class="spinner spinner-sm"></div>
<div class="spinner spinner-lg"></div>

<!-- Variants -->
<div class="spinner spinner-primary"></div>
<div class="spinner spinner-secondary"></div>
<div class="spinner spinner-success"></div>
<div class="spinner spinner-danger"></div>
<div class="spinner spinner-warning"></div>
<div class="spinner spinner-light"></div>
```

### Pagination
```html
<div class="pagination">
    <a href="#" class="pagination-item">Previous</a>
    <a href="#" class="pagination-item">1</a>
    <a href="#" class="pagination-item active">2</a>
    <a href="#" class="pagination-item">3</a>
    <a href="#" class="pagination-item">Next</a>
</div>

<!-- Sizes -->
<div class="pagination pagination-sm">Small pagination</div>
<div class="pagination pagination-lg">Large pagination</div>
```

## Navigation Components

### Navbar
```html
<nav class="navbar">
    <a href="#" class="navbar-brand">My App</a>
    
    <button class="menu-toggle" onclick="toggleMobileMenu()">
        <span></span>
        <span></span>
        <span></span>
    </button>
    
    <ul class="navbar-nav" id="mobile-menu">
        <li class="nav-item">
            <a href="#" class="nav-link active">Home</a>
        </li>
        <li class="nav-item">
            <a href="#" class="nav-link">About</a>
        </li>
        <li class="nav-item">
            <a href="#" class="nav-link">Contact</a>
        </li>
    </ul>
</nav>
```

### Sidebar Navigation
```html
<button onclick="toggleSidebar()">Toggle Sidebar</button>

<div class="sidebar" id="sidebar">
    <a href="#" class="navbar-brand">My App</a>
    
    <ul class="navbar-nav vertical">
        <li class="nav-item">
            <a href="#" class="nav-link active">
                <span class="nav-icon">🏠</span>
                Home
            </a>
        </li>
        <li class="nav-item">
            <a href="#" class="nav-link">
                <span class="nav-icon">📊</span>
                Dashboard
            </a>
        </li>
    </ul>
</div>

<div class="sidebar-overlay" id="sidebar-overlay" onclick="toggleSidebar()"></div>
```

### Tabs
```html
<ul class="nav-tabs">
    <li><a href="#" class="nav-link active">Tab 1</a></li>
    <li><a href="#" class="nav-link">Tab 2</a></li>
    <li><a href="#" class="nav-link">Tab 3</a></li>
</ul>
```

### Breadcrumb
```html
<nav class="breadcrumb">
    <div class="breadcrumb-item">
        <a href="#" class="breadcrumb-link">Home</a>
    </div>
    <div class="breadcrumb-item">
        <a href="#" class="breadcrumb-link">Library</a>
    </div>
    <div class="breadcrumb-item">Data</div>
</nav>
```

## Layout Components

### Hero Section
```html
<section class="hero">
    <div class="container">
        <h1>Welcome to our service</h1>
        <p>A catchy subtitle that describes your offering</p>
        <button class="btn btn-primary">Get Started</button>
    </div>
</section>
```

### Section Spacing
```html
<section class="section">Standard section spacing</section>
<section class="section-sm">Small section spacing</section>
<section class="section-lg">Large section spacing</section>
```

### Layout Patterns
```html
<!-- Sidebar layout -->
<div class="sidebar-layout">
    <aside class="sidebar-content">
        <!-- Sidebar content -->
    </aside>
    <main class="main-content">
        <!-- Main content -->
    </main>
</div>

<!-- Header layout -->
<div class="header-layout">
    <header class="header">
        <!-- Header content -->
    </header>
    <main class="main">
        <!-- Main content -->
    </main>
</div>

<!-- Centered content -->
<div class="center-content">
    <div>Vertically and horizontally centered</div>
</div>

<!-- Split layout -->
<div class="split-layout">
    <div>Left side</div>
    <div>Right side</div>
</div>
```

## JavaScript Interactions

The included JavaScript file provides basic functionality for:

1. **Mobile menu toggle** - `toggleMobileMenu()`
2. **Sidebar toggle** - `toggleSidebar()`
3. **Tab navigation** - Automatic activation on click
4. **File input interactions** - Drag and drop support, file name display
5. **Click outside to close** - Mobile menu closes when clicking outside

## Utility Classes

### Text Utilities
```html
<p class="text-primary">Primary colored text</p>
<p class="text-secondary">Secondary colored text</p>
<p class="text-success">Success colored text</p>
<p class="text-danger">Danger colored text</p>
<p class="text-warning">Warning colored text</p>
<p class="text-info">Info colored text</p>
<p class="text-muted">Muted text</p>
<p class="text-center">Centered text</p>
<p class="text-right">Right-aligned text</p>
```

### Margin and Padding Utilities
```html
<div class="mt-3">Top margin</div>
<div class="mb-3">Bottom margin</div>
<div class="m-3">All margins</div>
<div class="mx-auto">Auto horizontal margins</div>
```

### Display Utilities
```html
<div class="d-none">Hidden</div>
<div class="d-block">Block</div>
<div class="d-flex">Flex</div>

<!-- Responsive display -->
<div class="d-none d-md-block">Hidden on mobile, visible on medium+</div>
<div class="d-block d-md-none">Visible on mobile, hidden on medium+</div>
```

### Animation Utilities
```html
<div class="fade-in">Fades in</div>
<div class="fade-out">Fades out</div>
<div class="slide-in-left">Slides in from left</div>
<div class="slide-in-right">Slides in from right</div>
<div class="slide-up">Slides up</div>
<div class="slide-down">Slides down</div>
```

## Responsive Design

Glook 3.0 is mobile-first and includes responsive utilities:

### Breakpoints
- Extra small: < 576px
- Small: ≥576px
- Medium: ≥768px
- Large: ≥992px
- Extra large: ≥1200px

### Responsive Classes
```html
<!-- Responsive grid -->
<div class="col-12 col-md-6 col-lg-4">Responsive column</div>

<!-- Responsive display -->
<div class="d-none d-md-block">Hidden on mobile</div>

<!-- Responsive text alignment -->
<div class="text-center-mobile">Centered on mobile</div>
```

## Customization

### Overriding Variables
You can override the CSS custom properties to customize the theme:

```css
:root {
    --primary: #your-color;
    --radius: 8px;
    /* Add other customizations */
}
```

### Adding Custom Styles
Create a separate CSS file to add your custom styles:

```css
/* custom.css */
.my-custom-component {
    /* Your styles */
}
```

## Browser Support

Glook 3.0 supports all modern browsers:
- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)

## Troubleshooting

1. **Components not working**: Ensure you've included both CSS and JS files
2. **JavaScript not working**: Check browser console for errors
3. **Styles not applying**: Verify CSS file path is correct
4. **Grid not working**: Ensure you're using the row/column structure correctly

## License

Glook 3.0 is available under the MIT License.

## Changelog

### Version 3.0
- Added comprehensive component library
- Enhanced grid system with responsive breakpoints
- Improved JavaScript interactions
- Added Material Design input styles
- Expanded utility classes

## Support

For issues and questions, please check the documentation first. If you need further assistance, please contact support.

---

*This documentation covers the core features of Glook 3.0. For more advanced usage, refer to the source code comments and experiment with the various components and utilities.*