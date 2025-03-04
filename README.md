# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-playfair font-bold text-gray-900">Logo</a>
```
- Replace "Logo" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. **Navigation Links:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Keep the `hover:text-gray-900` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-playfair font-bold text-gray-900 leading-tight mb-8">Lorem ipsum dolor</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">Lorem ipsum dolor sit amet...</p>
```
- Replace "Lorem ipsum dolor" with your main headline
- Update paragraph text while maintaining the `<p>` tags
- Class breakdown:
  - `text-4xl`: Base font size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-gray-900 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Feature 1</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet</p>
</div>
```
- Update "Feature 1" with your feature name
- Replace description text in the `<p>` tag
- Keep all classes to maintain styling and hover effects

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Keep the `#` prefix
   - Match the ID of the target section
   - Example: `href="#features"` jumps to `<section id="features">`

2. External links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/page"`

### Call-to-Action (CTA) Buttons
Located in hero and CTA sections:
```html
<a href="#" class="inline-block bg-gray-900 text-white px-8 py-4 rounded-full">Get Started</a>
```
- Replace `#` with your sign-up or product page URL
- Keep all classes to maintain button styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h3 class="text-xl font-bold mb-4">Legal</h3>
        <ul class="space-y-2">
            <!-- Add these lines -->
            <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy header and footer from index.html
3. Add policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in both the link and section ID
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the responsive class chain intact
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Styling Inconsistencies**
   - Copy exact class strings when duplicating elements
   - Maintain spacing in class attributes
   - Keep font family classes (`font-playfair`, `font-inter`)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different screen sizes and browsers before deploying to production.