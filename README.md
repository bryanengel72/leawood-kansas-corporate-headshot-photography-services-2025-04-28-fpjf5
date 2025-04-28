# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page consists of these key sections:
- Header/Navigation (fixed at top)
- Hero Section (full-screen welcome area)
- Services Section
- Contact Section
- Footer

### Updating Text Content

#### Hero Section
Located in the first `<section>` tag, update the main heading:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Leawood, Kansas Corporate Headshot Photography Services</h1>

<!-- To update, replace the text between the h1 tags -->
```

#### Services Section
Find the three service cards in the grid:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <!-- Each card follows this pattern -->
    <div class="bg-gray-800 rounded-2xl p-8">
        <h3 class="text-xl font-semibold mb-4">Pro Gear</h3>
        <p class="text-gray-400">Industry-leading cameras...</p>
    </div>
```

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The site uses these breakpoints:
- `md:` (768px and up)
- `lg:` (1024px and up)

Example:
```html
<div class="text-xl md:text-2xl">
<!-- text-xl on mobile, text-2xl on medium screens and up -->
```

#### Common Style Classes
- Background colors: `bg-gray-900`, `bg-gray-800`
- Text colors: `text-gray-100`, `text-gray-300`, `text-gray-400`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom)
- Gradients: `bg-gradient-to-r from-purple-500 to-pink-500`

## Managing Links

### Navigation Menu Links
Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
    <!-- Update the booking link URL -->
    <a href="https://www.101headshots.com">Book Now</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with new URL or section ID
3. For internal links, use `#section-id`
4. For external links, use full URL including `https://`

### Call-to-Action Links
Main booking buttons throughout the page:
```html
<!-- Hero section button -->
<a href="https://www.101headshots.com" class="inline-block px-8 py-4...">
    Schedule Your Session
</a>
```

### Email Links
Update email addresses in contact section and footer:
```html
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```

## Adding Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match link hrefs
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify breakpoint classes (md:, lg:) are correct
   - Test all screen sizes

3. **Gradient Text Not Showing**
   - Ensure these classes are present:
     ```html
     bg-gradient-to-r from-[color] to-[color] bg-clip-text text-transparent
     ```

### Need Help?
If you encounter issues:
1. Check browser console for errors
2. Verify all files are in correct directories
3. Ensure Tailwind CSS CDN link is working
4. Test all links in multiple browsers

Remember to always backup your files before making changes, and test thoroughly on multiple devices and browsers after updates.