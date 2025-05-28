# MigrateHost Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the MigrateHost landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<div class="text-2xl font-bold text-blue-600">MigrateHost</div>
```
- Replace "MigrateHost" with your desired brand name
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional nav items -->
</div>
```
- Update link text between `<a>` tags
- Maintain the `hidden md:flex` class for proper mobile responsiveness

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight text-gray-900 mb-6">
    Migrate from Shared Hosting Without Losing Traffic, Rankings, or Sleep
</h1>
```
- Update heading text while keeping the classes intact
- Text sizes are responsive:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Step-by-Step Guides</h3>
    <p class="text-gray-600">Detailed instructions for every stage...</p>
</div>
```

To modify:
1. Update the `<h3>` text for the feature title
2. Change the description in the `<p>` tag
3. Keep the styling classes to maintain consistent design

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Ensure section IDs match these href values
2. For external links, use full URLs:
```html
<a href="https://example.com/page">External Page</a>
```

### Call-to-Action Buttons
The main CTA buttons use this format:

```html
<a href="https://www.cloudways.com/en/?id=1384181" class="inline-block px-8 py-4 bg-blue-600 text-white text-lg font-semibold rounded-full hover:bg-blue-700">
    Start Your Migration
</a>
```

To update:
1. Replace the href attribute with your desired URL
2. Update the button text between the tags
3. Maintain the classes for consistent styling

## Adding Legal Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design:**
- Check that you haven't removed important responsive classes (md:, lg:, sm:)
- Verify all container classes remain: `container mx-auto px-6`

2. **Misaligned Elements:**
- Ensure flex classes remain intact: `flex items-center justify-between`
- Check spacing utilities: `space-x-8`, `mb-6`, etc.

3. **Missing Styles:**
- Verify the Tailwind CDN link remains in the head:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Need Help?
If you encounter issues:
1. Compare your changes against the original HTML
2. Check the browser console for errors
3. Verify all classes match the original styling
4. Ensure all closing tags are present

Remember to test all changes across different screen sizes using browser developer tools.