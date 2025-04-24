# Albert Park Landing Page Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in header, find this div: -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Albert Park
</div>
```
Simply replace "Albert Park" with your desired company name.

### Hero Section
The main landing section contains your primary headline and call-to-action:

1. **Main Headline**
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Albert Park accounting services
</h1>
```
- Replace the text while keeping the HTML tags intact
- The classes ensure responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-6xl`: Medium screens
  - `lg:text-7xl`: Large screens

2. **Tagline**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Your financial success is our bottom line
</p>
```

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800/50 p-8 rounded-2xl hover:bg-gray-800 transition-all duration-300 transform hover:-translate-y-2 border border-gray-700 hover:border-purple-500/50">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg mb-6 flex items-center justify-center">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```
To modify:
1. Change the heading text in the `<h3>` tag
2. Update the description in the `<p>` tag
3. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
Located in two places due to mobile responsiveness:

1. **Desktop Menu**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

2. **Mobile Menu**
```html
<div x-show="isOpen" class="md:hidden mt-4 space-y-4">
    <a href="#features" class="block text-gray-300 hover:text-white">Features</a>
    <a href="#benefits" class="block text-gray-300 hover:text-white">Benefits</a>
    <a href="#contact" class="block text-gray-300 hover:text-white">Contact</a>
</div>
```

To update links:
1. Identify the `href` attribute
2. Replace the value with your new link
3. Update both desktop and mobile menus to match

### Call-to-Action Buttons
Located in hero and contact sections:
```html
<a href="https://theaccountants.com" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-8 py-4 rounded-lg transform hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-purple-500/25">
    Get Started Today
</a>
```
Replace `https://theaccountants.com` with your desired URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Contact Us</a></li>
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

Common issues and solutions:

1. **Broken Responsive Design**
   - Always maintain both mobile and desktop classes
   - Keep the `md:` and `lg:` prefixed classes when updating
   - Test on different screen sizes after changes

2. **Missing Hover Effects**
   - Ensure you keep the `hover:` classes when updating
   - Common hover classes used:
     - `hover:text-white`
     - `hover:scale-105`
     - `hover:bg-gray-800`

3. **Gradient Text Not Showing**
   - Keep these classes together:
     - `bg-gradient-to-r`
     - `from-purple-400`
     - `to-pink-400`
     - `bg-clip-text`
     - `text-transparent`

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Maintain consistent styling across sections