# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
The company name "WebAgency" appears in the header. To change it:
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-white">WebAgency</div>
```
Simply replace "WebAgency" with your company name.

#### Hero Section
To update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Sydney  <!-- Replace this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks  <!-- Replace this text -->
</p>
```

#### Features Section
Each feature card contains three elements:
1. Icon
2. Heading
3. Description

To update a feature card:
```html
<div class="bg-gray-700 rounded-2xl p-8 transform hover:scale-105 transition-all duration-300">
    <div class="text-blue-500 text-4xl mb-6">
        <i class="fas fa-mouse-pointer"></i>  <!-- Change icon class here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>  <!-- Change heading -->
    <p class="text-gray-300">Intuitive interfaces and smooth user experience...</p>  <!-- Change description -->
</div>
```

### Tailwind CSS Classes Explained

#### Common Class Patterns
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-{size}`: Adds margin bottom (4, 6, 8, etc.)
- `py-{size}`: Adds padding top and bottom
- `px-{size}`: Adds padding left and right
- `bg-{color}-{shade}`: Sets background color
- `text-{color}-{shade}`: Sets text color

#### Responsive Design Classes
The page uses these breakpoints:
- `md:`: Applied at medium screens (768px+)
- `lg:`: Applied at large screens (1024px+)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- Text is: -->
<!-- - 4xl on mobile -->
<!-- - 5xl on medium screens -->
<!-- - 6xl on large screens -->
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these:
1. For internal sections: Use `#section-id`
2. For external pages: Use full URL
```html
<!-- Example external link -->
<a href="https://your-domain.com/features">Features</a>
```

### Call-to-Action Links
The page has multiple "Get Started" buttons pointing to "https://fixrr.online". Update these:
```html
<!-- Find all instances of -->
<a href="https://fixrr.online"
<!-- Replace with your target URL -->
<a href="https://your-domain.com/start"
```

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<!-- For privacy policy -->
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>

<!-- For terms of service -->
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure the Tailwind CDN link is working

2. **Links Not Working**
   - For internal links (#features, etc.), ensure IDs match exactly
   - For external links, verify the full URL including https://
   - Test all links in different browsers

3. **Icons Not Showing**
   - Verify the Font Awesome CDN is loading
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

### Need Help?
If you encounter issues:
1. Use browser developer tools (F12) to inspect elements
2. Check the console for error messages
3. Verify all CDN links are accessible
4. Compare your changes against the original code
5. Test the page in multiple browsers

Remember to always backup your code before making changes!