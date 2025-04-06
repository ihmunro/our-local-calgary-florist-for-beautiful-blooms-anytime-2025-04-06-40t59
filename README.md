# Landing Page Maintenance Guide
## Bloom & Co. Florist Website

This guide provides detailed instructions for maintaining and customizing the Bloom & Co. landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-['Playfair_Display'] font-bold text-emerald-800">Bloom & Co.</a>
```
- Replace "Bloom & Co." with your company name
- Keep the existing classes to maintain styling

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-emerald-700 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` for each menu item
- Maintain the `class` attributes to preserve styling and hover effects

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900">
    Your Local Calgary Florist for Beautiful Blooms Anytime
</h1>
```
- Update the text between the `<h1>` tags
- The classes control:
  - `text-4xl/5xl/6xl`: Text size at different screen sizes
  - `leading-tight`: Line height
  - `text-gray-900`: Text color

### Tailwind CSS Class Modifications

When updating classes, remember:
- Keep responsive classes (starting with `md:` or `lg:`)
- Maintain spacing classes (like `px-6`, `py-4`)
- Don't remove transition classes (`transition-all`, `duration-300`)

Example of modifying button colors:
```html
<!-- Original -->
<a href="#" class="px-8 py-4 bg-emerald-600 text-white rounded-full">

<!-- To change to blue -->
<a href="#" class="px-8 py-4 bg-blue-600 text-white rounded-full">
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://yourwebsite.com" class="...">Order Now</a>
```

### Updating Links Step-by-Step

1. **Internal Links** (sections on the same page):
- Keep the `#` symbol
- Match the `id` of the target section
```html
<!-- Link in navigation -->
<a href="#features">Services</a>

<!-- Corresponding section -->
<section id="features" class="py-24 px-6 bg-white">
```

2. **External Links** (Order Now buttons):
```html
<!-- Find all instances of -->
href="https://yourwebsite.com"

<!-- Replace with your actual order page URL -->
href="https://your-actual-store.com/order"
```

## Linking Privacy and Terms Pages

### Adding Footer Links
Locate the footer section and add privacy/terms links:

```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Bloom & Co. All rights reserved.</p>
    <!-- Add these lines -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Link back to the main page:
```html
<a href="/" class="text-emerald-600 hover:text-emerald-700">Return to Home</a>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Verify that section `id` attributes match the href values
- IDs are case-sensitive
- Remove any spaces in ID names

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixed classes
- Test on multiple screen sizes
- Use browser dev tools to check responsive breakpoints

3. **Style Inconsistencies**
- Keep consistent color classes (e.g., `emerald-600`)
- Maintain font family classes
- Preserve spacing classes (`px-`, `py-`, `m-`, etc.)

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- Check the browser console for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.