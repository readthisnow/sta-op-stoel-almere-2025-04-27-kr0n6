# Sta Op Stoel Almere Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Sta Op Stoel Almere landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance below.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo text. To update:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-gray-800">Sta Op Stoel Almere</a>
```
To change the logo text, simply replace "Sta Op Stoel Almere" with your desired text.

#### Navigation Menu Items
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Voordelen</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Aanbod</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```
To modify menu items:
1. Locate the `<a>` tag you want to change
2. Update the text between `>` and `</a>`
3. Keep the existing classes to maintain styling

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8">
    Sta Op Stoel Almere
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting</span>
</h1>
```
To update:
1. Change the main heading text
2. Modify the blue promotional text in the `<span>` tag
3. Keep the responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`)
- `text-[color]`: Controls text color (e.g., `text-gray-900`)
- `bg-[color]`: Controls background color (e.g., `bg-white`)
- `p-[size]`: Controls padding (e.g., `p-8`)
- `m-[size]`: Controls margin (e.g., `mb-8`)

## Fixing Broken Links

### Current Link Structure
The page contains several types of links:

1. Navigation Menu Links (Internal):
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Aanbod</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These link to sections within the page using ID anchors.

2. Call-to-Action Links (External):
```html
<a href="https://sta-opstoelen.nl" class="inline-block bg-blue-600 text-white px-8 py-4">
    Bekijk Aanbod
</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute with the new URL
3. For internal links, ensure the `href` matches the section's `id` attribute
4. For external links, include the complete URL with `https://`

Example:
```html
<!-- Before -->
<a href="https://sta-opstoelen.nl">Bekijk Aanbod</a>

<!-- After -->
<a href="https://your-new-website.com">Bekijk Aanbod</a>
```

## Linking Privacy and Terms Pages

### Current Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match the href attributes
- Ensure IDs are unique across the page
- Verify there are no spaces in ID names

2. **Responsive Design Issues**
- Keep the responsive classes (`md:`, `lg:` prefixes)
- Test on different screen sizes
- Don't remove the viewport meta tag:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Animation Issues**
- Verify AOS script is loaded
- Check data-aos attributes
- Ensure AOS initialization remains:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true,
    });
</script>
```

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Maintain the existing class structure for consistent styling

Remember to always backup your files before making changes, and test all modifications in a development environment first.