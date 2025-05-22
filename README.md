# Texas Web Design Landing Page - Maintenance Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Troubleshooting Tips](#troubleshooting-tips)

---

## Introduction

This guide will help you maintain and customize your Texas Web Design landing page. Even if you're new to HTML and CSS, you'll be able to make common updates by following these step-by-step instructions.

### What You'll Need
- A text editor (like Notepad++, VS Code, or even basic Notepad)
- Your `index.html` file
- Basic understanding of how to save and preview HTML files in a browser

---

## Updating Text Content

Text content in HTML appears between opening and closing tags. For example: `<h1>Your Text Here</h1>`

### Key Sections to Update

#### 1. **Company Name** (appears in multiple places)
Currently shows: "Texas Web Design"

**Location 1 - Navigation Bar (Line 20):**
```html
<a href="#" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition duration-300">Texas Web Design</a>
```
Change to:
```html
<a href="#" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition duration-300">Your Company Name</a>
```

**Location 2 - Footer (Line 255):**
```html
<h3 class="text-xl font-bold mb-4">Texas Web Design</h3>
```

#### 2. **Main Headline** (Line 56)
Currently shows: "Best Websites In Texas"
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Best Websites In Texas
</h1>
```
Change the text between the `<h1>` tags to your desired headline.

#### 3. **Hero Description** (Line 59)
```html
<p class="text-xl md:text-2xl text-gray-600 mb-8 max-w-3xl mx-auto leading-relaxed">
    Professional web design services that deliver stunning results. Transform your online presence with Texas Web Design.
</p>
```

#### 4. **Feature Cards** (Starting at Line 82)
Each feature has a title and description. For example:
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Free Hosting</h3>
<p class="text-gray-600 leading-relaxed">Get started with complimentary hosting services. No hidden fees, no setup costs - just reliable hosting for your website.</p>
```

#### 5. **Contact Information** (Line 240)
```html
<a href="mailto:admin@twd.com" class="text-gray-600 hover:text-blue-600 transition duration-300">admin@twd.com</a>
```
Replace `admin@twd.com` with your actual email address.

---

## Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Each class does one specific thing.

### Understanding Common Classes

#### Text Size Classes:
- `text-sm` = small text
- `text-base` = normal text
- `text-lg` = large text
- `text-xl` = extra large text
- `text-2xl`, `text-3xl`, etc. = progressively larger

#### Color Classes:
- `text-gray-900` = very dark gray text
- `text-blue-600` = blue text
- `bg-white` = white background
- `bg-blue-600` = blue background

#### Spacing Classes:
- `p-4` = padding on all sides
- `px-4` = padding left and right
- `py-4` = padding top and bottom
- `m-4` = margin on all sides
- `mb-4` = margin bottom only

### Common Modifications

#### 1. **Changing Button Colors**
Current button (Line 64):
```html
<a href="https://twd.com" class="bg-blue-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-blue-700 transform hover:scale-105 transition duration-300 shadow-lg">
```

To change to green:
```html
<a href="https://twd.com" class="bg-green-600 text-white px-8 py-4 rounded-lg text-lg font-semibold hover:bg-green-700 transform hover:scale-105 transition duration-300 shadow-lg">
```

#### 2. **Adjusting Section Padding**
Current section (Line 75):
```html
<section id="features" class="py-24 bg-white">
```

To reduce padding:
```html
<section id="features" class="py-12 bg-white">
```

#### 3. **Responsive Design Classes**
Many classes have responsive prefixes:
- No prefix = applies to all screen sizes
- `md:` = applies to medium screens and up
- `lg:` = applies to large screens and up

Example (Line 56):
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
```
This means:
- Mobile: `text-4xl` (smaller)
- Tablet: `text-5xl` (medium)
- Desktop: `text-6xl` (larger)

---

## Fixing Broken Links

Links in HTML use the `<a>` tag with an `href` attribute. Currently, many links point to placeholder destinations.

### Navigation Menu Links (Lines 23-27)

These links use anchors (`#`) to jump to sections on the same page:
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Benefits</a>
<a href="#faq" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Contact</a>
```

These are working correctly and jump to sections with matching IDs.

### External Links to Update

#### 1. **"Get Started" Button** (Multiple locations)
Currently points to: `https://twd.com`

Line 28:
```html
<a href="https://twd.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transform hover:scale-105 transition duration-300 font-medium">Get Started</a>
```

Replace `https://twd.com` with your actual website URL or contact form.

#### 2. **Logo Link** (Line 20)
Currently: `href="#"`
```html
<a href="#" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition duration-300">Texas Web Design</a>
```

Change to:
```html
<a href="index.html" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition duration-300">Texas Web Design</a>
```

#### 3. **Footer Service Links** (Lines 268-273)
Currently all point to `#`:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Web Design</a></li>
```

Update with actual page URLs:
```html
<li><a href="services/web-design.html" class="text-gray-400 hover:text-white transition duration-300">Web Design</a></li>
```

#### 4. **Social Media Links** (Lines 278-281)
```html
<a href="#" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-facebook-f text-xl"></i></a>
```

Replace with actual social media URLs:
```html
<a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-white transition duration-300"><i class="fab fa-facebook-f text-xl"></i></a>
```

---

## Adding Privacy and Terms Pages

### Step 1: Create the Policy Pages

First, create two new files in the same folder as your `index.html`:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links

The footer already has placeholder links for these pages (Line 288):

```html
<p class="text-gray-400">&copy; 2024 Texas Web Design. All rights reserved. | <a href="#" class="hover:text-white transition duration-300">Privacy Policy</a> | <a href="#" class="hover:text-white transition duration-300">Terms of Service</a></p>
```

Update to:
```html
<p class="text-gray-400">&copy; 2024 Texas Web Design. All rights reserved. | <a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a> | <a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></p>
```

### Step 3: Add to Navigation (Optional)

To add these links to the main navigation menu, insert after line 26:

```html
<a href="privacy.html" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Privacy</a>
<a href="terms.html" class="text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Terms</a>
```

Don't forget to also add them to the mobile menu (after line 39):
```html
<a href="privacy.html" class="block px-3 py-2 text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Privacy</a>
<a href="terms.html" class="block px-3 py-2 text-gray-700 hover:text-blue-600 transition duration-300 font-medium">Terms</a>
```

### Step 4: Basic Template for Policy Pages

Here's a simple template for your privacy.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Texas Web Design</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900">
    <!-- Copy the header from index.html here -->
    
    <section class="py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            <div class="prose prose-lg">
                <!-- Add your privacy policy content here -->
            </div>
        </div>
    </section>
    
    <!-- Copy the footer from index.html here -->
</body>
</html>
```

---

## Troubleshooting Tips

### Common Issues and Solutions

#### 1. **Changes Not Showing**
- **Solution**: Clear your browser cache (Ctrl+F5 on Windows, Cmd+Shift+R on Mac)
- Make sure you saved the file
- Check you're viewing the correct file in your browser

#### 2. **Broken Layout After Changes**
- **Solution**: Check that you didn't accidentally delete a closing tag (`</div>`, `</a>`, etc.)
- Make sure quotes around classes are intact: `class="..."` not `class=..."`
- Verify you didn't remove important Tailwind classes

#### 3. **Links Not Working**
- **Solution**: Check the file path is correct
- For external links, include `https://`
- For internal links, ensure the file exists in the correct location

#### 4. **Mobile Menu Not Working**
- **Solution**: The JavaScript at the bottom of the file controls this
- Make sure the script section (lines 291-315) is intact
- Check that IDs match: `mobile-menu-button` and `mobile-menu`

### Best Practices

1. **Always Keep a Backup**: Before making changes, save a copy of your working file
2. **Test on Multiple Devices**: Use your browser's responsive design mode
3. **Validate Your HTML**: Use an online HTML validator to check for errors
4. **Make One Change at a Time**: This makes it easier to identify what caused any issues

### Getting Help

If you encounter issues:
1. Check that all opening tags have closing tags
2. Ensure all quotation marks are paired
3. Verify file paths are correct
4. Test in different browsers

Remember: HTML is forgiving, but small syntax errors can cause unexpected results. Take your time and double-check your changes.