# Hawthorn Web Design Landing Page - Maintenance Guide

## Table of Contents
- [Text and Styling Updates](#text-and-styling-updates)
- [Link Management](#link-management)
- [Legal Pages Integration](#legal-pages-integration)
- [Troubleshooting](#troubleshooting)

## Text and Styling Updates

### Header Section
The header contains the logo and navigation menu. To update:

```html
<!-- Logo Text (Line 19) -->
<a href="/" class="text-2xl font-bold text-gray-800">
    HWD  <!-- Update this text for logo changes -->
</a>

<!-- Navigation Items (Lines 22-25) -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update navigation labels here -->
</div>
```

**Styling Tips:**
- Maintain the `hidden md:flex` class for responsive mobile behavior
- The `space-x-8` class controls navigation item spacing
- `hover:text-purple-600` provides the purple hover effect

### Hero Section
Located at the top of the page with main headline and CTA:

```html
<!-- Main Headline (Lines 37-39) -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold">
    Transform Your Online Presence  <!-- Update main headline here -->
</h1>

<!-- Subheading (Lines 40-42) -->
<p class="text-2xl md:text-3xl text-gray-600">
    Melbourne's Premier Web Design Studio  <!-- Update subheading here -->
</p>
```

**Important Classes:**
- Responsive text sizing: `text-5xl md:text-6xl lg:text-7xl`
- Gradient background: `bg-gradient-to-br from-gray-50 to-white`

### Features & Benefits Sections
Each feature card follows this structure:

```html
<div class="group p-8 bg-white rounded-2xl shadow-lg">
    <div class="w-14 h-14 bg-purple-100 rounded-xl">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold">Title</h3>
    <p class="text-gray-600">Description</p>
</div>
```

**Styling Notes:**
- Use `group` class for hover effects
- Maintain consistent padding (`p-8`) and rounded corners (`rounded-2xl`)
- Keep icon containers at `w-14 h-14`

## Link Management

### Current Link Structure
```html
<!-- Primary Navigation Links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- CTA Button Links -->
<a href="https://hwd.com">Get Started</a>  <!-- Update with actual URL -->
```

### Updating Links
1. Internal Links (Sections):
   - Keep the `#` prefix for smooth scrolling
   - Ensure IDs match in the corresponding sections
   - Example: `<a href="#features">` matches `<section id="features">`

2. External Links:
   ```html
   <!-- Replace placeholder URLs -->
   <a href="https://hwd.com" class="inline-flex items-center">
   ```
   - Update all instances of `https://hwd.com`
   - Maintain the `inline-flex` class for button styling

3. Email Links:
   ```html
   <!-- Update email address -->
   <p class="text-sm">boss@hwd.com</p>
   ```

## Legal Pages Integration

### Footer Legal Section
```html
<!-- Legal Links Section in Footer -->
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-sm">
        <li><a href="/privacy.html" class="hover:text-white hover:translate-x-2">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white hover:translate-x-2">Terms of Service</a></li>
    </ul>
</div>
```

To add new legal pages:
1. Create `privacy.html` and `terms.html` in the root directory
2. Update href attributes with correct paths
3. Maintain consistent styling classes
4. Consider adding relative paths: `./privacy.html`

## Troubleshooting

### Common Issues

1. Broken Responsive Layout
   - Verify all `md:` and `lg:` prefixed classes are intact
   - Check container classes: `container mx-auto px-6`
   - Ensure `hidden md:flex` is present on mobile menu

2. Hover Effects Not Working
   - Confirm `group` class on parent elements
   - Check `hover:` classes are properly chained
   - Verify `transition-all duration-300` is present

3. Gradient Issues
   - Ensure proper format: `bg-gradient-to-br from-{color} to-{color}`
   - Check color classes match Tailwind's color palette

### Style Maintenance Tips
- Keep consistent spacing using Tailwind's spacing scale
- Maintain the purple/indigo color scheme for brand consistency
- Preserve responsive classes for mobile-first design
- Test all interactive elements after updates

For additional support or questions, contact the development team or refer to the Tailwind CSS documentation.