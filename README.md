# Melbourne AI Automation Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your Melbourne AI Automation landing page. Whether you're updating text, fixing links, or adding new pages, we'll walk you through each step with clear instructions and examples.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Issues and Troubleshooting](#common-issues-and-troubleshooting)
7. [Best Practices](#best-practices)

---

## Getting Started

### What You Need to Know

This landing page is built with:
- **HTML**: The structure and content of the page
- **Tailwind CSS**: A utility-first framework that handles all styling and responsive design
- **Font Awesome**: Icons used throughout the page
- **Vanilla JavaScript**: Simple interactivity like mobile menu toggle and FAQ accordion

### How to Edit This File

1. **Open the file** in a text editor (VS Code, Notepad++, Sublime Text, etc.)
2. **Make your changes** following the instructions in this guide
3. **Save the file** (Ctrl+S or Cmd+S)
4. **View in browser** by opening the HTML file in your web browser
5. **Refresh the page** (F5 or Cmd+R) to see your changes

### File Structure Overview

```
Your Project Folder/
├── index.html (the main landing page - this file)
├── privacy.html (to be created)
├── terms.html (to be created)
└── blog.html (optional)
```

---

## Updating Text Content

### Understanding the Page Sections

Your landing page is organized into distinct sections. Here's where to find and update each one:

#### 1. **Header Navigation** (Lines 38-65)

**Location**: Top of the page with "MAI" logo and navigation menu

**Current Content**:
```html
<h1 class="text-2xl font-bold gradient-text">MAI</h1>
```

**How to Change the Logo Text**:
1. Find the line with `<h1 class="text-2xl font-bold gradient-text">MAI</h1>`
2. Replace `MAI` with your preferred text (e.g., `MELBOURNE AI`)
3. Save and refresh your browser

**Navigation Menu Links** (Lines 51-56):
These are the menu items: Features, Benefits, About, Testimonials, FAQ

```html
<a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
```

The text between `>` and `</a>` is what displays. To change "Features" to something else:
1. Locate the line with `>Features</a>`
2. Replace `Features` with your new text
3. **Important**: Keep the `href="#features"` unchanged (this links to sections below)

#### 2. **Hero Section** (Lines 68-112)

**Location**: Large banner at the top with "Melbourne AI Automation" heading

**Main Heading** (Line 80):
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    <span class="gradient-text">Melbourne AI Automation</span>
</h1>
```

**To update the main heading**:
1. Find the line with `<span class="gradient-text">Melbourne AI Automation</span>`
2. Replace `Melbourne AI Automation` with your desired text
3. This text will appear in the blue gradient color

**Subheading** (Line 83):
```html
<p class="text-xl md:text-2xl text-gray-700 mb-8 leading-relaxed max-w-3xl mx-auto">
    AI Automation For Small Business
</p>
```

**To update the subheading**:
1. Find the line with `AI Automation For Small Business`
2. Replace with your new text
3. Save and refresh

**Description Paragraph** (Lines 85-89):
```html
<p class="text-lg text-gray-600 mb-10 leading-relaxed max-w-2xl mx-auto">
    Transform your business operations with intelligent automation solutions...
</p>
```

**To update the description**:
1. Find the paragraph starting with `Transform your business operations...`
2. Replace the entire text between `>` and `</p>` with your new content
3. You can write multiple sentences

**Button Text** (Lines 91-92 and 95-96):
```html
<a href="https://mai.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all duration-300 hover:shadow-lg hover:scale-105 font-bold text-lg">
    Start Your Automation Journey
</a>
```

**To change button text**:
1. Find the button text (e.g., `Start Your Automation Journey`)
2. Replace with your desired button text
3. The URL `https://mai.com` can be updated separately (see [Fixing Links](#fixing-and-managing-links) section)

#### 3. **Features Section** (Lines 115-175)

**Location**: Three-column section with icons showing "Low Cost Solutions," "Self-Hosted Infrastructure," and "Unlimited Updates"

**Feature Card Title** (Line 128):
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Low Cost Solutions</h3>
```

**To update a feature title**:
1. Find the feature title you want to change
2. Replace the text between `>` and `</h3>`
3. Example: Change `Low Cost Solutions` to `Affordable Pricing`

**Feature Description** (Lines 129-132):
```html
<p class="text-gray-700 leading-relaxed mb-4">
    Eliminate expensive enterprise automation platforms. Our affordable pricing model means...
</p>
```

**To update feature description**:
1. Find the description paragraph under the title
2. Replace the text between `>` and `</p>`
3. Keep paragraphs concise (2-3 sentences)

**Feature Bullet Points** (Lines 133-137):
```html
<ul class="space-y-2 text-gray-600">
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> Transparent pricing</li>
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> No hidden fees</li>
    <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> Flexible plans</li>
</ul>
```

**To update bullet points**:
1. Find the `<li>` tags (each one is a bullet point)
2. Replace the text after `mr-3"></i> ` with your new bullet point
3. To add more bullets, copy an entire `<li>` line and paste it below
4. To remove bullets, delete the entire `<li>` line

**Example - Adding a new bullet point**:
```html
<li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> Transparent pricing</li>
<li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> No hidden fees</li>
<li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> Flexible plans</li>
<!-- New bullet point -->
<li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i> Your new feature here</li>
```

#### 4. **Benefits Section** (Lines 178-267)

**Location**: Section with "Why Choose Melbourne AI Automation?" heading

**Main Section Heading** (Line 186):
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
    Why Choose Melbourne AI Automation?
</h2>
```

**To update**:
1. Replace the text between `>` and `</h2>`
2. This is the main heading for the entire benefits section

**Benefit Card Titles** (Lines 199, 218, 237):
```html
<h3 class="text-xl font-bold text-gray-900">Fast Implementation</h3>
```

**To update benefit titles**:
1. Find each benefit title (Fast Implementation, Powered by n8n, Infinitely Scalable)
2. Replace with your new title text

**Benefit Descriptions** (Lines 200-204):
```html
<p class="text-gray-600 leading-relaxed">
    Get your automation workflows up and running in days, not months...
</p>
```

**To update descriptions**:
1. Replace the text between `>` and `</p>`
2. Keep descriptions 2-3 sentences for readability

**Additional Benefits (Checkmark Items)** (Lines 256-295):
```html
<h4 class="text-lg font-bold text-gray-900 mb-2">Reduce Manual Work</h4>
<p class="text-gray-600">Eliminate repetitive tasks and free your team...</p>
```

**To update these items**:
1. Find the `<h4>` tag with the benefit title
2. Replace the title text
3. Update the `<p>` tag below it with the new description

#### 5. **About Us Section** (Lines 298-350)

**Location**: Section with company story and statistics

**Main Heading** (Line 305):
```html
<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-8">About Melbourne AI Automation</h2>
```

**Company Story** (Lines 307-311 and 313-317):
```html
<p class="text-lg text-gray-700 leading-relaxed mb-6">
    Founded in 2022 by a team of automation enthusiasts...
</p>
```

**To update the company story**:
1. Find the `<p>` tags in the About section
2. Replace the text between `>` and `</p>`
3. You can have multiple paragraphs

**Statistics Cards** (Lines 320-349):
```html
<div class="bg-gradient-to-br from-blue-500 to-blue-600 rounded-lg p-8 text-white text-center hover-lift">
    <div class="text-4xl font-bold mb-2">500+</div>
    <p class="text-blue-100">Businesses Automated</p>
</div>
```

**To update statistics**:
1. Find the large number (e.g., `500+`)
2. Replace with your statistic
3. Replace the text below it (e.g., `Businesses Automated`)

#### 6. **Testimonials Section** (Lines 353-437)

**Location**: Section with customer quotes and reviews

**Section Heading** (Line 361):
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
    What Our Customers Say
</h2>
```

**Testimonial Quote** (Lines 377-385):
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Melbourne AI Automation has been a game-changer for our accounting firm..."
</p>
```

**To update a testimonial**:
1. Find the quote text between the quotation marks
2. Replace with the new testimonial
3. Keep it in quotation marks

**Testimonial Author** (Lines 387-389):
```html
<p class="font-bold text-gray-900">Sarah Mitchell</p>
<p class="text-gray-600 text-sm">Director, Mitchell & Associates Accounting</p>
```

**To update author information**:
1. Replace the name in the `font-bold` line
2. Replace the title/company in the second `<p>` tag

#### 7. **FAQ Section** (Lines 440-545)

**Location**: Expandable question and answer section

**Section Heading** (Line 448):
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4">
    Frequently Asked Questions
</h2>
```

**FAQ Question** (Line 556):
```html
<span class="text-lg font-bold text-gray-900">What is Melbourne AI Automation and how does it work?</span>
```

**To update a question**:
1. Find the question text
2. Replace between `>` and `</span>`

**FAQ Answer** (Lines 562-564):
```html
<div class="px-6 py-4 text-gray-700 leading-relaxed border-t border-gray-200">
    <p>Melbourne AI Automation is a platform...</p>
</div>
```

**To update an answer**:
1. Find the answer text between `>` and `</p>`
2. Replace with your new answer
3. You can include multiple paragraphs by adding more `<p>` tags

#### 8. **Call-to-Action Section** (Lines 548-571)

**Location**: Blue section with "Ready to Transform Your Business?"

**Heading** (Lines 559-560):
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white mb-6">
    Ready to Transform Your Business?
</h2>
```

**Description** (Lines 561-563):
```html
<p class="text-xl text-blue-100 mb-10 max-w-2xl mx-auto">
    Join hundreds of small businesses already saving time and money...
</p>
```

**Button Text** (Lines 564-566):
```html
<a href="https://mai.com" class="inline-block px-10 py-4 bg-white text-blue-600 rounded-lg hover:bg-blue-50 transition-all duration-300 hover:shadow-lg hover:scale-105 font-bold text-lg">
    Get Started Now
</a>
```

#### 9. **Footer Section** (Lines 574-650)

**Location**: Bottom of the page with company info and links

**Company Description** (Lines 580-582):
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Empowering small businesses with affordable, scalable AI automation solutions.
</p>
```

**Footer Column Headings** (Lines 589, 598, 607):
```html
<h4 class="text-white font-bold mb-6">Product</h4>
```

**Footer Links** (Lines 590-595):
```html
<ul class="space-y-3">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
</ul>
```

**Contact Information** (Lines 619-627):
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-400 mt-1 mr-3"></i>
    <a href="mailto:admin@mai.com" class="text-gray-400 hover:text-white transition-colors duration-300">admin@mai.com</a>
</li>
```

**To update email**:
1. Find `mailto:admin@mai.com`
2. Replace `admin@mai.com` with your email address
3. Also replace the displayed text after it

**Copyright Text** (Line 638):
```html
&copy; 2025 Melbourne AI Automation. All rights reserved.
```

**To update copyright**:
1. Replace `2025` with current year
2. Replace `Melbourne AI Automation` with your company name

---

## Modifying Tailwind CSS Classes

### What Are Tailwind Classes?

Tailwind CSS uses utility classes to style elements. Instead of writing traditional CSS, you add class names directly to HTML elements. For example:

```html
<div class="text-2xl font-bold text-gray-900">
```

This means:
- `text-2xl` = Large text size
- `font-bold` = Bold font weight
- `text-gray-900` = Dark gray text color

### Common Tailwind Classes Used in This Landing Page

#### Text Sizing

| Class | Size |
|-------|------|
| `text-sm` | Small |
| `text-base` | Normal |
| `text-lg` | Large |
| `text-xl` | Extra Large |
| `text-2xl` | 2X Large |
| `text-3xl` | 3X Large |
| `text-4xl` | 4X Large |
| `text-5xl` | 5X Large |
| `text-6xl` | 6X Large |

**Example**: Change a heading from `text-5xl` to `text-4xl`

Original:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900">
```

Modified:
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900">
```

#### Font Weight

| Class | Weight |
|-------|--------|
| `font-light` | Thin |
| `font-normal` | Regular |
| `font-medium` | Medium |
| `font-semibold` | Semi-Bold |
| `font-bold` | Bold |
| `font-extrabold` | Extra Bold |

#### Colors

The page uses these color classes:

**Text Colors**:
- `text-gray-600` = Medium gray text
- `text-gray-700` = Darker gray text
- `text-gray-900` = Very dark text
- `text-white` = White text
- `text-blue-600` = Blue text

**Background Colors**:
- `bg-white` = White background
- `bg-gray-50` = Very light gray background
- `bg-blue-50` = Very light blue background
- `bg-blue-600` = Blue background
- `bg-gray-900` = Dark background

**Example**: Change text color from gray to blue

Original:
```html
<p class="text-gray-700">Your text here</p>
```

Modified:
```html
<p class="text-blue-600">Your text here</p>
```

#### Spacing (Padding and Margins)

| Class | Spacing |
|-------|---------|
| `p-4` | 1rem padding |
| `p-6` | 1.5rem padding |
| `p-8` | 2rem padding |
| `mb-4` | 1rem margin bottom |
| `mb-6` | 1.5rem margin bottom |
| `mb-8` | 2rem margin bottom |
| `px-4` | 1rem padding left & right |
| `px-6` | 1.5rem padding left & right |
| `px-8` | 2rem padding left & right |

**Example**: Add more padding to a card

Original:
```html
<div class="p-6 bg-white rounded-xl">
```

Modified:
```html
<div class="p-8 bg-white rounded-xl">
```

#### Rounded Corners

| Class | Radius |
|-------|--------|
| `rounded` | Small radius |
| `rounded-lg` | Large radius |
| `rounded-xl` | Extra large radius |
| `rounded-full` | Completely circular |

#### Display and Layout

| Class | Purpose |
|-------|---------|
| `flex` | Display as flex container |
| `grid` | Display as grid container |
| `hidden` | Hide element |
| `block` | Display as block |
| `inline-block` | Display inline-block |
| `space-x-4` | Add horizontal spacing between children |
| `space-y-4` | Add vertical spacing between children |

#### Responsive Design

Tailwind uses breakpoints for responsive design:

| Prefix | Screen Size | When to Use |
|--------|-------------|------------|
| (none) | Mobile (default) | Extra small screens |
| `sm:` | 640px and up | Small screens |
| `md:` | 768px and up | Medium screens (tablets) |
| `lg:` | 1024px and up | Large screens (desktops) |

**Example**: Different text sizes on different screens

```html
<h1 class="text-2xl md:text-4xl lg:text-5xl">
```

This means:
- Mobile: `text-2xl` (smaller)
- Tablet (768px+): `text-4xl` (medium)
- Desktop (1024px+): `text-5xl` (larger)

**To make text smaller on all devices**:
```html
<h1 class="text-xl md:text-3xl lg:text-4xl">
```

#### Hover Effects

| Class | Effect |
|-------|--------|
| `hover:bg-blue-700` | Change background on hover |
| `hover:text-white` | Change text color on hover |
| `hover:shadow-lg` | Add shadow on hover |
| `hover:scale-105` | Slightly enlarge on hover |
| `hover:translate-y-2` | Move down on hover |

### Practical Examples for Common Changes

#### Example 1: Make Feature Cards Larger

**Original**:
```html
<div class="hover-lift p-8 bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl border border-blue-100">
```

**Change padding from p-8 to p-12**:
```html
<div class="hover-lift p-12 bg-gradient-to-br from-blue-50 to-indigo-50 rounded-xl border border-blue-100">
```

#### Example 2: Change Button Color

**Original**:
```html
<a href="https://mai.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-lg hover:bg-blue-700">
```

**Change from blue to green**:
```html
<a href="https://mai.com" class="inline-block px-8 py-4 bg-green-600 text-white rounded-lg hover:bg-green-700">
```

#### Example 3: Make Text Bolder

**Original**:
```html
<h2 class="text-3xl md:text-4xl font-bold text-gray-900">
```

**Change from font-bold to font-extrabold**:
```html
<h2 class="text-3xl md:text-4xl font-extrabold text-gray-900">
```

#### Example 4: Adjust Spacing Between Sections

**Original**:
```html
<section class="py-24 md:py-32 bg-white">
```

**Increase vertical padding**:
```html
<section class="py-32 md:py-40 bg-white">
```

This changes the top and bottom padding from 24 (mobile) / 32 (desktop) to 32 (mobile) / 40 (desktop).

### Modifying Gradients

The page uses gradient backgrounds. Here's how to modify them:

**Original gradient**:
```html
<div class="bg-gradient-to-br from-blue-50 to-indigo-50">
```

This creates a gradient from top-left to bottom-right (`to-br`), starting with light blue (`from-blue-50`) and ending with light indigo (`to-indigo-50`).

**Direction options**:
- `to-r` = Left to right
- `to-b` = Top to bottom
- `to-br` = Top-left to bottom-right
- `to-bl` = Top-right to bottom-left

**Example: Change gradient direction**:
```html
<div class="bg-gradient-to-r from-blue-50 to-indigo-50">
```

### Modifying Shadows

**Original**:
```html
<div class="shadow-md hover:shadow-xl">
```

**Shadow options**:
- `shadow-sm` = Small shadow
- `shadow-md` = Medium shadow
- `shadow-lg` = Large shadow
- `shadow-xl` = Extra large shadow

**Example: Increase shadow on cards**:
```html
<div class="shadow-lg hover:shadow-2xl">
```

---

## Fixing and Managing Links

### Understanding Links on Your Page

Your landing page has several types of links:

1. **Internal links** (linking to sections within the same page)
2. **External links** (linking to other websites)
3. **Action links** (like "Get Started" buttons)
4. **Email links**

### Internal Links (Navigation Menu)

These links take you to different sections of the same page.

**Location**: Header navigation (Lines 51-56) and footer (Lines 590-595)

**How Internal Links Work**:
```html
<a href="#features">Features</a>
```

The `href="#features"` tells the browser to scroll to the element with `id="features"`.

**Example**: When you click "Features" in the menu, it jumps to:
```html
<section id="features" class="py-24 md:py-32 bg-white">
```

### Current Internal Links

Here are all the internal section links:

| Link Text | Href | Section ID |
|-----------|------|-----------|
| Features | `#features` | Line 115 |
| Benefits | `#benefits` | Line 178 |
| About | `#about` | Line 298 |
| Testimonials | `#testimonials` | Line 353 |
| FAQ | `#faq` | Line 440 |

**To verify links are working**:
1. Check that the `href` matches the section `id`
2. For example, `href="#features"` should match `id="features"`
3. If they don't match, the link won't work

### External Links (Action Buttons)

These are links that take you to external websites.

**Location**: Throughout the page (buttons and CTAs)

**Current External Links**:
```html
<a href="https://mai.com">Get Started</a>
```

This link appears multiple times:
- Line 62 (Header "Get Started" button)
- Line 92 (Hero section primary button)
- Line 102 (Hero section secondary button)
- Line 565 (CTA section button)

### Updating External Links

**To change where the "Get Started" button links to**:

1. Find all instances of `href="https://mai.com"`
2. Replace `https://mai.com` with your desired URL
3. For example: `href="https://yourwebsite.com/contact"`

**Example**: Change to a contact form page
```html
<!-- Original -->
<a href="https://mai.com" class="inline-block px-8 py-4 bg-blue-600 text-white">
    Get Started
</a>

<!-- Updated -->
<a href="https://yourwebsite.com/contact-us" class="inline-block px-8 py-4 bg-blue-600 text-white">
    Get Started
</a>
```

### Email Links

**Location**: Footer contact section (Line 621)

**Current Email Link**:
```html
<a href="mailto:admin@mai.com" class="text-gray-400 hover:text-white">admin@mai.com</a>
```

**To update the email address**:

1. Find the line with `mailto:admin@mai.com`
2. Replace `admin@mai.com` with your email address (both places)

**Example**:
```html
<!-- Original -->
<a href="mailto:admin@mai.com">admin@mai.com</a>

<!-- Updated -->
<a href="mailto:contact@yourcompany.com">contact@yourcompany.com</a>
```

### Social Media Links

**Location**: Footer (Lines 586-593)

**Current Social Links**:
```html
<a href="#" aria-label="Facebook" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**To add your social media URLs**:

1. Find `href="#"` in each social link
2. Replace with your social media profile URL

**Example**:
```html
<!-- Original (Facebook) -->
<a href="#" aria-label="Facebook">

<!-- Updated (Facebook) -->
<a href="https://facebook.com/yourpage" aria-label="Facebook">
```

**Social Media URL Examples**:
- Facebook: `https://facebook.com/yourpage`
- Twitter: `https://twitter.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Instagram: `https://instagram.com/yourhandle`

### Website URL

**Location**: Footer (Line 627)

**Current Website Link**:
```html
<a href="https://mai.com">https://mai.com</a>
```

**To update**:
1. Replace both instances of `https://mai.com`
2. First one in `href="..."`
3. Second one in the displayed text

**Example**:
```html
<!-- Original -->
<a href="https://mai.com">https://mai.com</a>

<!-- Updated -->
<a href="https://yourwebsite.com">https://yourwebsite.com</a>
```

### Footer Navigation Links

**Location**: Footer columns (Lines 590-615)

**Current Links**:
```html
<ul class="space-y-3">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#about">About Us</a></li>
    <li><a href="#testimonials">Testimonials</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

These are internal links. They're already set up correctly and link to sections on this page.

**Special Footer Links**:
```html
<li><a href="blog.html">Blog</a></li>
<li><a href="privacy.html">Privacy Policy</a></li>
<li><a href="terms.html">Terms of Service</a></li>
```

These link to separate pages. See the next section for how to set these up.

### Link Best Practices

✅ **Do**:
- Always use `https://` for external URLs (not just `http://`)
- Match `href` attributes with section `id` attributes
- Test links after making changes
- Use descriptive link text (not "click here")

❌ **Don't**:
- Leave `href="#"` (this does nothing)
- Use spaces in URLs
- Mix up internal (`#`) and external links
- Forget to update both the `href` and displayed text

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy and Terms pages are important for:
- **Legal compliance** (especially with customer data)
- **Building trust** with visitors
- **Protecting your business** legally
- **SEO** (search engines like sites with proper policies)

### Step 1: Create the Privacy Page

**Step 1a: Create a new file**
1. Open your text editor
2. Create a new blank file
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 1b: Add basic HTML structure**

Copy and paste this template into your `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Melbourne AI Automation">
    <title>Privacy Policy - Melbourne AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-blue-600">MAI</a>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Benefits</a>
                    <a href="index.html#about" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">About</a>
                </div>
                <div class="hidden md:block">
                    <a href="https://mai.com" class="inline-block px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all font-medium">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="leading-relaxed">
                        Melbourne AI Automation ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p class="leading-relaxed mb-4">We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you provide.</li>
                        <li><strong>Automatically Collected Information:</strong> Browser type, IP address, pages visited, and time spent on pages.</li>
                        <li><strong>Cookies:</strong> We use cookies to enhance your experience and analyze site usage.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Your Information</h2>
                    <p class="leading-relaxed mb-4">Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Generate a personal profile about you so that future visits to the Site will be personalized</li>
                        <li>Increase the efficiency and operation of the Site</li>
                        <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                        <li>Notify you of updates to the Site</li>
                        <li>Offer new products, services, and/or recommendations to you</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Disclosure of Your Information</h2>
                    <p class="leading-relaxed">
                        We may share your information with third parties only in the ways that are described in this privacy policy. We do not sell, trade, or rent your personal information to third parties. We may disclose your information when required to do so by law or when we believe in good faith that such disclosure is necessary to protect our rights or the rights of others.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Security of Your Information</h2>
                    <p class="leading-relaxed">
                        We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your personal information, we cannot guarantee its absolute security.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
                    <p class="leading-relaxed">
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Melbourne AI Automation</strong><br>
                        Email: <a href="mailto:admin@mai.com" class="text-blue-600 hover:text-blue-700">admin@mai.com</a><br>
                        Address: Melbourne, Australia
                    </p>
                </div>

                <div class="bg-gray-50 p-6 rounded-lg border border-gray-200">
                    <p class="text-sm text-gray-600">
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>

            <!-- Back to Home Link -->
            <div class="mt-12">
                <a href="index.html" class="inline-block px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all font-medium">
                    Back to Home
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 text-sm mb-4 md:mb-0">
                        &copy; 2025 Melbourne AI Automation. All rights reserved.
                    </p>
                    <div class="flex space-x-6">
                        <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors text-sm">Privacy Policy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-white transition-colors text-sm">Terms of Service</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms Page

**Step 2a: Create a new file**
1. Open your text editor
2. Create a new blank file
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2b: Add basic HTML structure**

Copy and paste this template into your `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Melbourne AI Automation">
    <title>Terms of Service - Melbourne AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Inter', sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-blue-600">MAI</a>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">Benefits</a>
                    <a href="index.html#about" class="text-gray-700 hover:text-blue-600 transition-colors font-medium">About</a>
                </div>
                <div class="hidden md:block">
                    <a href="https://mai.com" class="inline-block px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all font-medium">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p class="leading-relaxed">
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="leading-relaxed mb-4">Permission is granted to temporarily download one copy of the materials (information or software) on Melbourne AI Automation's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="leading-relaxed">
                        The materials on Melbourne AI Automation's website are provided on an 'as is' basis. Melbourne AI Automation makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="leading-relaxed">
                        In no event shall Melbourne AI Automation or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Melbourne AI Automation's website, even if Melbourne AI Automation or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="leading-relaxed">
                        The materials appearing on Melbourne AI Automation's website could include technical, typographical, or photographic errors. Melbourne AI Automation does not warrant that any of the materials on its website are accurate, complete, or current. Melbourne AI Automation may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p class="leading-relaxed">
                        Melbourne AI Automation has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Melbourne AI Automation of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="leading-relaxed">
                        Melbourne AI Automation may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of Australia, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Information</h2>
                    <p class="leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Melbourne AI Automation</strong><br>
                        Email: <a href="mailto:admin@mai.com" class="text-blue-600 hover:text-blue-700">admin@mai.com</a><br>
                        Address: Melbourne, Australia
                    </p>
                </div>

                <div class="bg-gray-50 p-6 rounded-lg border border-gray-200">
                    <p class="text-sm text-gray-600">
                        <strong>Last Updated:</strong> January 2025
                    </p>
                </div>
            </div>

            <!-- Back to Home Link -->
            <div class="mt-12">
                <a href="index.html" class="inline-block px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-all font-medium">
                    Back to Home
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 text-sm mb-4 md:mb-0">
                        &copy; 2025 Melbourne AI Automation. All rights reserved.
                    </p>
                    <div class="flex space-x-6">
                        <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors text-sm">Privacy Policy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-white transition-colors text-sm">Terms of Service</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Verify Links Are Working

**Check that your files are in the correct location**:
```
Your Project Folder/
├── index.html
├── privacy.html (newly created)
└── terms.html (newly created)
```

**Test the links**:
1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should take you to `privacy.html`
4. Click on "Terms of Service" - should take you to `terms.html`
5. Click "Back to Home" on either page - should return to `index.html`

### Customizing Privacy and Terms Content

The templates provided are generic. You should customize them with your specific information:

**In privacy.html**, update:
- Email address (search for `admin@mai.com`)
- Company name (search for `Melbourne AI Automation`)
- Location (search for `Melbourne, Australia`)
- Specific data collection practices
- Last Updated date

**In terms.html**, update:
- Email address (search for `admin@mai.com`)
- Company name (search for `Melbourne AI Automation`)
- Location (search for `Melbourne, Australia`)
- Your specific terms and conditions
- Last Updated date

**Example - Updating email in privacy.html**:

Original:
```html
Email: <a href="mailto:admin@mai.com" class="text-blue-600 hover:text-blue-700">admin@mai.com</a>
```

Updated:
```html
Email: <a href="mailto:your-email@yourcompany.com" class="text-blue-600 hover:text-blue-700">your-email@yourcompany.com</a>
```

### Adding a Blog Page (Optional)

Your footer already has a link to `blog.html`. To create it:

1. Create a new file named `blog.html`
2. Copy the structure from `privacy.html` or `terms.html`
3. Replace the content with your blog posts
4. Update the title and headings

---

## Common Issues and Troubleshooting

### Issue 1: Links Not Working

**Problem**: You click a link but nothing happens or it goes to the wrong page

**Solution**:
1. Check the `href` attribute matches the section `id`
   ```html
   <!-- Link -->
   <a href="#features">Features</a>
   
   <!-- Section -->
   <section id="features">
   ```
   These should match exactly (both say "features")

2. Make sure there are no typos
   - `#feature` ≠ `#features`
   - `#Benefits` ≠ `#benefits`

3. Check file names match exactly
   - `privacy.html` ≠ `Privacy.html`
   - File names are case-sensitive on some systems

### Issue 2: Page Looks Broken or Styling is Wrong

**Problem**: Text is too large/small, colors are wrong, or layout is broken

**Solution**:
1. **Did you accidentally delete a class?**
   - Check that all class names are intact
   - Example: `class="text-2xl font-bold"` not `class="text-2xl font-"`

2. **Did you miss a closing tag?**
   - Every `<div>` needs a `</div>`
   - Every `<a>` needs a `</a>`
   - Check that tags match

3. **Clear your browser cache**:
   - Press Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
   - This forces the browser to reload the page fresh

### Issue 3: Mobile Menu Not Working

**Problem**: The hamburger menu on mobile doesn't open/close

**Solution**:
1. Check that the JavaScript at the bottom of the page is intact
2. Make sure you didn't accidentally delete the `<script>` tag
3. Verify the menu toggle button exists:
   ```html
   <button class="menu-toggle md:hidden" id="menuToggle">
   ```

### Issue 4: Buttons Are Wrong Color

**Problem**: A button appears in the wrong color after you made changes

**Solution**:
1. Check the background color class
   - `bg-blue-600` = Blue button
   - `bg-white` = White button
   - `bg-green-600` = Green button

2. Check the text color class
   - `text-white` = White text
   - `text-blue-600` = Blue text

3. Example fix:
   ```html
   <!-- Wrong -->
   <button class="bg-red-600 text-white">Submit</button>
   
   <!-- Correct -->
   <button class="bg-blue-600 text-white">Submit</button>
   ```

### Issue 5: Text Content Appears But Styling is Missing

**Problem**: You updated text but lost formatting (bold, colors, etc.)

**Solution**:
1. Don't delete the surrounding HTML tags
2. Only replace the text content, not the tags

**Example - WRONG**:
```html
<!-- Original -->
<h2 class="text-3xl font-bold text-gray-900">Features</h2>

<!-- WRONG - Deleted the tags -->
New Features
```

**Example - CORRECT**:
```html
<!-- Original -->
<h2 class="text-3xl font-bold text-gray-900">Features</h2>

<!-- CORRECT - Kept the tags -->
<h2 class="text-3xl font-bold text-gray-900">New Features</h2>
```

### Issue 6: Page Won't Load

**Problem**: Browser shows error or blank page

**Solution**:
1. **Check for HTML syntax errors**:
   - Use an online HTML validator (search "HTML validator")
   - Paste your code to find errors

2. **Check file is saved**:
   - Make sure you saved the file (Ctrl+S or Cmd+S)
   - Check file extension is `.html` not `.txt`

3. **Check file location**:
   - Make sure `index.html` is in the correct folder
   - Make sure you're opening the right file

### Issue 7: FAQ Accordion Not Opening

**Problem**: Clicking FAQ questions doesn't expand them

**Solution**:
1. Check JavaScript is intact at bottom of page
2. Verify the accordion structure matches:
   ```html
   <div class="accordion-item">
       <button class="faq-toggle">
           <span>Question text</span>
       </button>
       <div class="accordion-content">
           <div>Answer text</div>
       </div>
   </div>
   ```

3. Check that you didn't accidentally delete the `<script>` section

### Issue 8: Images Not Showing

**Problem**: Image placeholders appear instead of actual images

**Solution**:
1. The page uses placeholder images from Unsplash (free image service)
2. These should work automatically
3. If they don't load, check your internet connection
4. To use your own images, replace the image URLs:
   ```html
   <!-- Original -->
   <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=1200&h=600&fit=crop">
   
   <!-- Your image -->
   <img src="your-image.jpg">
   ```

### Issue 9: Email Link Not Working

**Problem**: Clicking email link doesn't open email client

**Solution**:
1. Verify the email link format:
   ```html
   <a href="mailto:your-email@example.com">your-email@example.com</a>
   ```

2. Check email address is valid (no spaces or special characters)

3. Note: This requires the user to have an email client set up on their computer

### Issue 10: Footer Links Go to Wrong Page

**Problem**: Footer links don't go where expected

**Solution**:
1. Check file names are correct:
   - `privacy.html` (not `Privacy.html` or `privacy.HTML`)
   - `terms.html` (not `Terms.html` or `terms.HTML`)
   - `blog.html` (not `Blog.html` or `blog.HTML`)

2. Check files exist in same folder as `index.html`

3. Verify href attributes match file names exactly:
   ```html
   <a href="privacy.html">Privacy Policy</a>
   <!-- File must be named privacy.html -->
   ```

---

## Best Practices

### 1. **Always Back Up Your Files**

Before making major changes:
1. Make a copy of `index.html` and name it `index-backup.html`
2. Keep this as a safety copy
3. If something breaks, you can reference the backup

**How to backup**:
1. Right-click on `index.html`
2. Select "Copy"
3. Right-click in the same folder
4. Select "Paste"
5. Rename to `index-backup.html`

### 2. **Test Changes in Your Browser**

After every change:
1. Save the file (Ctrl+S)
2. Refresh your browser (F5 or Cmd+R)
3. Check that everything looks correct
4. Test all interactive elements (buttons, links, menus)

### 3. **Use Consistent Formatting**

Keep your HTML organized:
- Use proper indentation (spaces or tabs)
- Keep related elements together
- Add comments for sections

**Example**:
```html
<!-- Hero Section -->
<section id="hero" class="py-24">
    <div class="container">
        <h1>Your heading</h1>
        <p>Your paragraph</p>
    </div>
</section>
```

### 4. **Keep URLs Updated**

When you change your website URL:
1. Update `https://mai.com` everywhere it appears
2. Use Find & Replace (Ctrl+H) to change all at once
3. Test all links after changing

### 5. **Maintain Consistent Branding**

Use the same:
- Colors (blue-600 for primary, gray-900 for text)
- Font sizes (text-lg for body, text-3xl for headings)
- Spacing (mb-4, mb-6, mb-8)
- Button styles

### 6. **Mobile Responsive Design**

Always test on:
- Desktop (1024px+)
- Tablet (768px - 1023px)
- Mobile (320px - 767px)

The page uses responsive classes:
```html
<h1 class="text-2xl md:text-4xl lg:text-5xl">
```
- Mobile: `text-2xl`
- Tablet: `text-4xl` (768px+)
- Desktop: `text-5xl` (1024px+)

### 7. **Test All Links Regularly**

Create a checklist:
- [ ] All navigation links work
- [ ] All buttons go to correct URLs
- [ ] Email links open email client
- [ ] Social media links go to profiles
- [ ] Footer links work

### 8. **Keep Content Updated**

Regularly check and update:
- Statistics (customers, tasks automated)
- Testimonials (add new ones)
- Contact information
- Links (especially external URLs)
- Last updated dates

### 9. **Use Semantic HTML**

Use proper HTML elements:
- `<h1>` for main heading
- `<h2>` for section headings
- `<p>` for paragraphs
- `<button>` for buttons
- `<a>` for links
- `<nav>` for navigation

### 10. **Document Your Changes**

Keep track of what you've changed:

**Example change log**:
```
## Changes Made

### January 15, 2025
- Updated company email from admin@mai.com to contact@mai.com
- Changed hero section heading from "Melbourne AI Automation" to "AI Solutions for Your Business"
- Added new testimonial from Jane Smith

### January 10, 2025
- Fixed broken link to privacy policy
- Updated "Get Started" button URL
```

### 11. **Security Best Practices**

- Don't put sensitive information (passwords, API keys) in HTML
- Keep your website files in a secure location
- Use HTTPS when deploying your website
- Regularly update contact information
- Keep backups of important files

### 12. **Performance Tips**

- Minimize large images (they slow down the page)
- Use the CDN links for external libraries (Tailwind, Font Awesome)
- Test page load speed
- Remove unused CSS classes

---

## Quick Reference Guide

### Common Tailwind Classes

```html
<!-- Text Sizing -->
<p class="text-sm">Small text</p>
<p class="text-base">Normal text</p>
<p class="text-lg">Large text</p>
<p class="text-xl">Extra large</p>
<p class="text-2xl">2X large</p>

<!-- Font Weight -->
<p class="font-light">Light</p>
<p class="font-normal">Normal</p>
<p class="font-bold">Bold</p>
<p class="font-extrabold">Extra bold</p>

<!-- Colors -->
<p class="text-gray-600">Gray text</p>
<p class="text-blue-600">Blue text</p>
<p class="bg-blue-600">Blue background</p>

<!-- Spacing -->
<div class="p-4">Padding</div>
<div class="m-4">Margin</div>
<div class="mb-8">Margin bottom</div>
<div class="px-6">Horizontal padding</div>

<!-- Responsive -->
<div class="text-sm md:text-lg lg:text-xl">
    Responsive text
</div>
```

### Common Link Patterns

```html
<!-- Internal link -->
<a href="#features">Features</a>

<!-- External link -->
<a href="https://example.com">External Site</a>

<!-- Email link -->
<a href="mailto:email@example.com">Email Us</a>

<!-- File link -->
<a href="privacy.html">Privacy Policy</a>

<!-- Button-style link -->
<a href="#" class="px-6 py-2 bg-blue-600 text-white rounded-lg">
    Click Me
</a>
```

### Common Section Structure

```html
<section id="section-name" class="py-24 md:py-32 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section heading -->
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-8">
            Section Title
        </h2>
        
        <!-- Section content -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Card/item -->
            <div class="p-6 bg-white rounded-lg shadow-md">
                <h3 class="text-xl font-bold mb-4">Item Title</h3>
                <p class="text-gray-600">Item description</p>
            </div>
        </div>
    </div>
</section>
```

---

## Additional Resources

### Learning Resources

- **Tailwind CSS Documentation**: https://tailwindcss.com/docs
- **HTML Tutorial**: https://www.w3schools.com/html/
- **Font Awesome Icons**: https://fontawesome.com/icons
- **MDN Web Docs**: https://developer.mozilla.org/

### Tools

- **HTML Validator**: https://validator.w3.org/
- **Responsive Design Tester**: https://responsively.app/
- **Color Picker**: https://htmlcolorcodes.com/
- **Image Optimizer**: https://tinypng.com/

### Getting Help

If you encounter issues:
1. Check this troubleshooting guide
2. Search the error message online
3. Use the HTML validator to find syntax errors
4. Check browser developer tools (F12)

---

## Final Checklist

Before launching your website:

- [ ] All text content updated
- [ ] All links tested and working
- [ ] Email address updated
- [ ] Social media links added
- [ ] Company information correct
- [ ] Privacy policy page created
- [ ] Terms of service page created
- [ ] Mobile menu works
- [ ] FAQ accordion works
- [ ] All buttons functional
- [ ] Page loads quickly
- [ ] No broken images
- [ ] Responsive on mobile/tablet/desktop
- [ ] Spelling and grammar checked
- [ ] Backup copy created

---

## Conclusion

Congratulations! You now have the knowledge to maintain and customize your Melbourne AI Automation landing page. Remember:

1. **Start small** - Make one change at a time
2. **Test often** - Refresh your browser after each change
3. **Backup regularly** - Keep copies of working versions
4. **Read carefully** - Pay attention to HTML structure
5. **Ask for help** - Don't hesitate to search for solutions

For ongoing maintenance, regularly:
- Update content and statistics
- Check all links
- Review and update policies
- Test on different devices
- Keep backups

Good luck with your landing page! 🚀