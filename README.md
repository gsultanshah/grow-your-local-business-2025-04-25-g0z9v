# OneCall Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the OneCall landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu:

```html
<div class="text-2xl font-bold text-blue-600">OneCall</div>
```
To update the company name:
1. Locate this div in the header section
2. Replace "OneCall" with your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Grow Your Local Business
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Discover proven strategies...
</p>
```

To modify:
1. Replace text between the `<h1>` tags for the main headline
2. Update the paragraph text between `<p>` tags
3. Keep the responsive classes (`md:` and `lg:` prefixes) to maintain mobile-friendly design

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-chart-line text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Growth Strategies</h3>
    <p class="text-gray-600">Implement proven strategies...</p>
</div>
```

To customize:
1. Change the icon by updating the `fa-chart-line` class to any [Font Awesome icon](https://fontawesome.com/icons)
2. Modify the heading text between `<h3>` tags
3. Update the description in the `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. The `href="#features"` format links to page sections (internal links)
2. For external links, use complete URLs: `href="https://example.com"`
3. Maintain the same classes for consistent styling

### Call-to-Action Buttons
The main CTA buttons need valid URLs:

```html
<a href="https://www.onecallapp.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Now
</a>
```

Replace `https://www.onecallapp.com` with your actual signup or contact page URL.

## Adding Privacy and Terms Pages

### Step 1: Create Footer Links
Add these links to the Quick Links section in the footer:

```html
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Required Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Add your policy content between them

Example privacy.html structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-sans antialiased bg-gray-50">
    <!-- Copy header section -->
    
    <section class="pt-32 pb-24">
        <div class="container mx-auto px-6">
            <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your privacy policy content here -->
        </div>
    </section>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**: Ensure section IDs match exactly:
   ```html
   <a href="#features">Features</a>
   <section id="features">
   ```

2. **Responsive Design Issues**: Keep these Tailwind prefixes:
   - `sm:` (mobile)
   - `md:` (tablet)
   - `lg:` (desktop)

3. **Icon Not Showing**: Verify Font Awesome inclusion:
   ```html
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
   ```

4. **Styling Inconsistencies**: Copy exact class strings from existing elements when adding new ones

Need help? Contact technical support at support@onecallapp.com

---
Remember to test all changes across different devices and browsers before deploying to production.