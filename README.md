# Spring Hill Festival Coffee Cart - Landing Page Maintenance Guide

This guide will help you maintain and customize the Spring Hill Festival Coffee Cart landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<span class="font-bold text-xl">Delightful Bean</span>
```
Simply replace "Delightful Bean" with your desired name.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-amber-700 transition-colors duration-300">Features</a>
```
- Replace text between `>` and `</a>` to change menu items
- Keep the `class` attributes to maintain styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-6">Spring Hill Festival Coffee Cart</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Artisan coffee experiences for Spring Hill event attendees</p>
```
- Update the h1 text to change your main headline
- Modify the paragraph text for your subheading
- The `md:` and `lg:` prefixes control responsive text sizes - keep these intact

### Understanding Tailwind Classes
Common classes used throughout:
- `text-{size}`: Controls text size (xl, 2xl, etc.)
- `bg-{color}-{shade}`: Sets background color
- `p-{number}`: Sets padding
- `m-{number}`: Sets margin
- `rounded-{size}`: Controls border radius

Example:
```html
<div class="bg-white rounded-xl p-8 shadow-lg">
```
This creates a white background with rounded corners, padding of 8 units, and a large shadow.

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.delightfulbean.com/">Book Now</a>
```

To update:
1. Internal links (starting with #) connect to page sections
2. External links (starting with http) go to other websites
3. Replace `https://www.delightfulbean.com/` with your booking URL

### Social Media Links
Located in the footer:
```html
<a href="#" class="hover:text-white transition-colors duration-300">
    <i class='bx bxl-facebook text-2xl'></i>
</a>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert this code in the Quick Links section of the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between them

Example structure for privacy.html:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header section -->
    
    <section class="pt-32 pb-24">
        <div class="container mx-auto px-4">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your privacy policy content here -->
        </div>
    </section>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout:**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all `div` tags are properly closed
   - Maintain the responsive classes (sm:, md:, lg: prefixes)

2. **Links Not Working:**
   - For section links (#features, etc.), ensure the ID exists in the HTML
   - Check for typos in URLs
   - Verify file names match exactly for privacy.html and terms.html

3. **Icons Not Showing:**
   - Confirm the Boxicons CDN link is present in the head section
   - Check icon class names match the Boxicons documentation

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always make a backup of your files before making significant changes.