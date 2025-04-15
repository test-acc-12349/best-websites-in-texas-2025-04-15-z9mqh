# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your Texas Web landing page. Follow these step-by-step instructions to make common updates while preserving the page's design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```
- Replace "Texas Web" with your desired text
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. **Navigation Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional nav items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the class structure for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Keep responsive classes (`md:` and `lg:` prefixes) for proper scaling

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless navigation and management.</p>
</div>
```
To modify:
1. Update heading text between `<h3>` tags
2. Change description text between `<p>` tags
3. Maintain padding (`p-8`) and shadow classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Replace `#section-name` with your desired anchor
2. Ensure corresponding sections have matching IDs
3. For external links, use complete URLs:
```html
<a href="https://your-website.com/page">Page Name</a>
```

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white">Start Your Project</a>
```
To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link before deploying

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout:**
- Check that all Tailwind classes remain intact
- Verify the Tailwind CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

2. **Non-Working Links:**
- Ensure all `href` attributes start with either:
  - `#` for internal section links
  - `https://` for external links
  - Relative paths (`./`) for local pages

3. **Missing Styles:**
- Confirm the Inter font link is present:
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

### Need Help?
- Double-check all changes against the original HTML
- Test the page in multiple browsers
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Keep a backup of the original file before making changes

Remember to test all changes in a development environment before pushing to production.