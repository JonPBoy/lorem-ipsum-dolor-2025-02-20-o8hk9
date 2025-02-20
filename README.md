# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<span class="text-2xl font-['Playfair_Display'] font-bold text-gray-900">Logo</span>
```
To update the logo text, replace "Logo" with your company name. This appears in both the header and footer.

#### Hero Section
Located in the first `<section>` after `<main>`, update these elements:
```html
<h1 class="font-['Playfair_Display'] text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Lorem ipsum dolor
</h1>
<p class="max-w-2xl mx-auto text-xl text-gray-600 mb-10">
    Lorem ipsum dolor
</p>
```
Replace "Lorem ipsum dolor" with your actual headline and subheading text.

### Tailwind CSS Modifications

#### Understanding Responsive Classes
The landing page uses these breakpoints:
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

Example:
```html
text-4xl md:text-5xl lg:text-6xl
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Style Classes
- Text Colors: `text-gray-900`, `text-gray-600`, `text-white`
- Background Colors: `bg-white`, `bg-gray-50`, `bg-gradient-to-r`
- Spacing: `px-4`, `py-24`, `mb-6`, `mt-4`
- Font Families: `font-['Playfair_Display']`, `font-['Inter']`

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="Lorem ipsum dolor">Get Started</a>
```

To update:
1. Internal links (starting with #) connect to sections with matching IDs
2. Replace "Lorem ipsum dolor" in the Get Started button with your actual URL
3. Example of a proper external link:
```html
<a href="https://your-website.com/signup">Get Started</a>
```

### Call-to-Action Buttons
There are three CTA buttons to update:
1. Header "Get Started"
2. Hero section "Get Started Now"
3. Contact section "Contact Us"

Update each `href="Lorem ipsum dolor"` with your actual URLs.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer grid:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <!-- Existing content -->
    <div>
        <h3 class="text-lg font-semibold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in ID names
   - IDs are case-sensitive

2. **Responsive Design Problems**
   - Test all screen sizes using browser dev tools
   - Verify media query classes (md:, lg:) are properly ordered
   - Check for overflow issues on mobile screens

3. **Font Loading Issues**
   - Confirm the Google Fonts link is working
   - Verify font family names match exactly in classes
   - Check for proper fallback fonts

### Getting Help
- Inspect elements using browser developer tools (F12)
- Check the Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different devices and browsers before deploying to production.