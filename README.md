# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "TWD":
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```

2. **Navigation Menu Items**: Located in the `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
Located right after the header, update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-6`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right

To modify responsive design:
- `md:`: Applies styles on medium screens and up
- `lg:`: Applies styles on large screens and up

Example of changing text size and color:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">Free Hosting</h3>

<!-- Modified for larger text and different color -->
<h3 class="text-2xl font-bold mb-4 text-blue-700">Free Hosting</h3>
```

## Fixing Broken Links

### Current Link Structure
1. **Navigation Links**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links**:
Replace all instances of `https://twd.com` with your actual website URL:
```html
<!-- Find and replace this -->
<a href="https://twd.com" class="px-6 py-2 bg-blue-600 text-white rounded-full">Get Started</a>
```

3. **Email Links**:
Update the email address in the contact section:
```html
<!-- Change admin@twd.com to your email -->
<a href="mailto:admin@twd.com">Contact Us</a>
```

### Step-by-Step Link Update Process
1. Open the HTML file in a text editor
2. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
3. Search for "twd.com"
4. Replace with your actual domain
5. Search for "admin@twd.com"
6. Replace with your contact email

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Locate the footer section and update these links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues
1. **Broken Internal Links**
   - Ensure all section IDs match their corresponding links
   - Check for typos in href attributes
   - Verify file names match exactly

2. **Responsive Design Problems**
   - Check mobile view using browser developer tools
   - Ensure `md:` and `lg:` classes are properly set
   - Verify the viewport meta tag is present

3. **Style Inconsistencies**
   - Confirm Tailwind CDN link is working
   - Check for missing closing tags
   - Verify class names are spelled correctly

### Need Help?
If you encounter issues:
1. Use browser developer tools (F12) to inspect elements
2. Check the console for error messages
3. Verify all files are in the correct directory
4. Ensure all links point to existing files

Remember to test all changes across different devices and browsers before publishing updates to your live site.