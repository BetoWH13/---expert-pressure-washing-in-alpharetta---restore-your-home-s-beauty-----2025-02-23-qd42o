# AlphaWash Landing Page - Maintenance Guide

This guide will help you maintain and customize the AlphaWash pressure washing landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    AlphaWash  <!-- Change company name here -->
</div>
```

To modify:
1. Locate this section at the top of the page
2. Replace "AlphaWash" with your company name
3. Keep the surrounding div and classes to maintain the gradient effect

### Hero Section Text
Update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    ✨ Expert Pressure Washing in Alpharetta  <!-- Main headline -->
    <span class="block text-blue-400">Restore Your Home's Beauty!</span>  <!-- Subheading -->
</h1>
```

The classes explain:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-900 rounded-xl p-8 hover:transform hover:scale-105 transition-transform duration-300 shadow-xl">
    <div class="text-blue-400 text-4xl mb-4">🏠</div>  <!-- Change emoji -->
    <h3 class="text-xl font-semibold mb-4">Deep Clean for Homes</h3>  <!-- Change title -->
    <p class="text-gray-400">Professional exterior cleaning...</p>  <!-- Change description -->
</div>
```

To modify:
1. Locate the features section (identified by id="features")
2. Change emoji, title, and description text as needed
3. Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. The `#` symbol indicates an internal page link
2. Match the href value to the section id you're linking to
3. For external links, use the full URL: `href="https://example.com"`

### Quote Button Links
The quote buttons use this URL structure:

```html
<a href="https://leads.leadsmartinc.com/?api_key=eccf565586cda416df8b89f66df641fee9a1bcb8&affiliate_source=albertowaizel1&category=&funnel=3&buttons=btn-success&step=1">
```

To update:
1. Locate all quote button links (there are multiple throughout the page)
2. Replace the entire URL with your new quote system link
3. Keep the surrounding classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="text-gray-400 space-y-2">
        <li>Privacy Policy</li>  <!-- Convert to link -->
        <li>Terms of Service</li>  <!-- Convert to link -->
    </ul>
</div>
```

To add proper links:
1. Modify the list items to include anchor tags:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

2. Create matching HTML files (privacy.html and terms.html) in the same directory
3. Add the hover effect class for consistency

## Troubleshooting

Common issues and solutions:

### Broken Internal Links
- Ensure section IDs match exactly with href values
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

### Responsive Design Issues
If elements look wrong on mobile:
1. Check for responsive classes (md:, lg:)
2. Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Animation Problems
If animations aren't working:
1. Verify AOS script is loaded
2. Check data-aos attributes are spelled correctly
3. Ensure AOS is initialized:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true
    });
</script>
```

Remember to test all changes across different devices and browsers to ensure consistency.

Need more help? Feel free to reference the Tailwind CSS documentation or contact technical support.