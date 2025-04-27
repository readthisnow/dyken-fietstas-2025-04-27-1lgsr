# Dyken Landing Page Maintenance Guide

This guide will help you maintain and customize the Dyken landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold tracking-tight text-gray-900">Dyken</a>
```
- Replace "Dyken" with your desired brand name
- Adjust text size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)

2. **Navigation Links**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- Additional nav items -->
</div>
```
- Change link text between `<a>` tags
- Modify colors using `text-gray-600` and `hover:text-gray-900`

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Dyken Fietstas
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting</span>
</h1>
```
To update:
1. Replace "Dyken Fietstas" with your product name
2. Modify the discount text in the `<span>` tag
3. Adjust text sizes:
   - Mobile: `text-4xl`
   - Tablet: `sm:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl">
    <!-- Icon -->
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```
To modify:
1. Update the title text in `<h3>`
2. Change the description in `<p>`
3. Adjust spacing using `p-8` (padding) and `mb-4` (margin-bottom)

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="https://amzn.to/3YLlDby">Koop Nu</a>
```

To update:
1. Internal links (starting with #):
   - Ensure the `href` matches the `id` of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   ```html
   <!-- Find this line -->
   <a href="https://amzn.to/3YLlDby">Koop Nu</a>
   <!-- Replace with your link -->
   <a href="https://your-store-url.com">Koop Nu</a>
   ```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white">
        <!-- Facebook icon -->
    </a>
    <a href="#" class="hover:text-white">
        <!-- Instagram icon -->
    </a>
</div>
```
To update:
1. Replace `#` with your social media profile URLs
2. Example: `<a href="https://facebook.com/your-page">`

## Linking Privacy and Terms Pages

### Footer Links Section
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms & Conditions</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
   ```html
   <li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white">Terms & Conditions</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section `id` attributes match link `href` values
   - Example: `<a href="#features">` must link to `<section id="features">`

2. **Responsive Design Issues**
   - Look for classes starting with:
     - `sm:` (tablet)
     - `md:` (medium screens)
     - `lg:` (large screens)
   - Don't remove these prefixes as they control responsive behavior

3. **Missing Styles**
   - Ensure the Tailwind CSS link is present in the `<head>`:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

Remember to:
- Test all links after updating
- Preview changes on multiple screen sizes
- Keep the original class structure for consistent styling
- Make backups before major changes

Need more help? Refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) for detailed style information.