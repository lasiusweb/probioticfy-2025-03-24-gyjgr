# Probioticfy Landing Page Maintenance Guide

This guide will help you maintain and customize the Probioticfy landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing and Managing Links](#fixing-and-managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-green-700">Probioticfy</div>
```
- Replace "Probioticfy" with your desired company name
- Adjust text size using Tailwind classes:
  - `text-xl` (smaller)
  - `text-2xl` (current)
  - `text-3xl` (larger)

### Hero Section
Located at the top of the page with a background image:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">Probioticfy</h1>
```
- Replace the heading text
- `md:text-6xl` means the text becomes larger on medium screens
- `leading-tight` controls line spacing

2. **Hero Image:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Fertile soil with growing plants" 
     class="w-full h-full object-cover">
```
- Replace the `src` with your image URL
- Always update the `alt` text to match your new image

### Tailwind CSS Tips for Beginners
- Colors use format: `text-{color}-{shade}` (e.g., `text-green-600`)
- Spacing uses format: `p-{number}` for padding, `m-{number}` for margin
- Responsive prefixes: `md:`, `lg:`, `xl:` apply styles at different screen sizes

## Fixing and Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-green-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-green-600">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-green-600">FAQ</a>
    <a href="https://probioticfy.com/checkout" class="bg-green-600 text-white px-6 py-2">Shop Now</a>
</div>
```

To update:
1. Internal links (starting with #) connect to page sections
2. Replace `https://probioticfy.com/checkout` with your actual checkout URL
3. Ensure section IDs match your href values:
   ```html
   <section id="features"> <!-- matches href="#features" -->
   ```

### Footer Links
Located at the bottom of the page:

```html
<div class="text-lg font-semibold mb-4">Quick Links</div>
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

To update:
1. Match href values with page sections
2. Add new links by copying the `<li>` format
3. Maintain consistent styling using the same classes

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the footer:

```html
<!-- Original code -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- Updated code -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check that href values exactly match section IDs
   - Ensure file names are correct and in the same directory
   - Verify that URLs start with `http://` or `https://`

2. **Responsive Design Issues**
   - Check mobile menu functionality
   - Verify responsive classes (md:, lg:, xl:) are correct
   - Test on different screen sizes

3. **Images Not Loading**
   - Verify image URLs are accessible
   - Check file paths for local images
   - Ensure proper image formats (jpg, png, etc.)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different devices and browsers before publishing updates to your live site.