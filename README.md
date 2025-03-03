# SkillForge Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SkillForge landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">SkillForge</a>
```
- Replace "SkillForge" with your desired company name
- The `text-2xl` class controls text size
- `font-bold` makes the text bold

2. **Navigation Menu Items**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Common classes explained:
  - `text-gray-600`: Default text color
  - `hover:text-gray-900`: Color on mouse hover
  - `transition duration-300`: Smooth color transition

### Hero Section
The main banner section with background image:

```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    SkillForge: Discover Your Perfect Learning Path
</h1>
```
- Update heading text between the `<h1>` tags
- Important classes:
  - `text-4xl`: Text size on mobile
  - `md:text-6xl`: Larger text on medium screens
  - `mb-6`: Bottom margin spacing

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 transform hover:scale-105 transition duration-300">
    <h3 class="text-xl font-bold mb-4">Expert Reviews</h3>
    <p class="text-gray-600">Get detailed insights from industry experts...</p>
</div>
```
- Update text in `<h3>` and `<p>` tags
- Key styling classes:
  - `rounded-xl`: Rounded corners
  - `shadow-lg`: Box shadow effect
  - `hover:scale-105`: Slight zoom on hover

## Fixing Broken Links

### Navigation Links
Current navigation links in the header:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://skillforge/checkout">Get Started</a>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. Replace `https://skillforge/checkout` with your actual checkout URL
3. Ensure section IDs match exactly:
```html
<!-- Example: Features section must have matching ID -->
<section id="features" class="py-24 bg-gray-50">
```

### Call-to-Action (CTA) Links
Multiple CTAs throughout the page need updating:
```html
<a href="https://skillforge/checkout" 
   class="inline-block bg-indigo-600 text-white px-8 py-4 rounded-full">
    Start Learning Today
</a>
```
- Replace all instances of `https://skillforge/checkout` with your actual URL
- Maintain consistent styling classes for visual harmony

## Linking Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To update:
1. Replace `href="#"` with actual page links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```
2. Create corresponding privacy.html and terms.html files
3. Maintain consistent styling classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Verify that section IDs match exactly (case-sensitive)
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Check mobile classes (default) vs. desktop classes (starting with `md:`)
- Example: `class="text-4xl md:text-6xl"` means:
  - Mobile: text-4xl
  - Desktop: text-6xl

3. **Image Loading Problems**
- Verify image URLs in src attributes
- Ensure images are in the correct directory
- Check file permissions

4. **Style Inconsistencies**
- Copy exact Tailwind classes from existing elements
- Use browser inspector to identify current styles
- Test on multiple screen sizes

Remember to always test changes across different devices and browsers before deploying to production.

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Alpine.js Documentation](https://alpinejs.dev/docs) for interactive elements