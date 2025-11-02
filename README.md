# Emet Media House Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Emet Media House landing page. This document provides step-by-step instructions for developers of all skill levels.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Customizing Colors and Styling](#customizing-colors-and-styling)
8. [Common Issues and Troubleshooting](#common-issues-and-troubleshooting)
9. [Best Practices](#best-practices)

---

## Quick Start Overview

### What You Have

Your landing page (`index.html`) is a fully functional, responsive website built with:
- **Tailwind CSS**: A utility-first CSS framework for styling
- **Font Awesome Icons**: Professional icons throughout the page
- **Vanilla JavaScript**: Interactive features like mobile menu and FAQ toggles
- **Responsive Design**: Automatically adapts to desktop, tablet, and mobile devices

### Key Features of This Page

- **Announcement bar** at the top with shipping information
- **Sticky navigation header** that stays visible while scrolling
- **Hero section** with large background image and call-to-action
- **Feature cards** showcasing core capabilities
- **Benefit sections** highlighting business advantages
- **Testimonials** from satisfied clients
- **FAQ section** with expandable questions
- **Contact form** for lead generation
- **Footer** with links and social media

---

## Understanding the Page Structure

### File Organization

```
Your Project Folder
├── index.html              (Main landing page)
├── privacy.html            (To be created)
├── terms.html              (To be created)
├── blog.html               (Referenced in footer)
├── /services               (Referenced in buttons)
└── /css or /styles         (Optional: custom CSS file)
```

### Key Sections in Your HTML

Each section of your page is clearly marked with ID attributes:

| Section ID | Location | Purpose |
|-----------|----------|---------|
| `#home` | Hero section | Main landing area with headline |
| `#features` | Features section | Three core capabilities |
| `#benefits` | Multiple sections | Boost Visibility, Build Trust, Grow Sales |
| `#about` | About section | Company story and mission |
| `#testimonials` | Testimonials section | Client success stories |
| `#faq` | FAQ section | Frequently asked questions |
| `#contact` | Contact section | Contact form and information |

### Understanding Tailwind CSS

Tailwind CSS uses **utility classes** instead of traditional CSS. Each class does one specific thing:

```html
<!-- Example: Creating a blue button -->
<button class="bg-blue-500 text-white px-4 py-2 rounded-lg">Click Me</button>

<!-- Breaking down the classes: -->
<!-- bg-blue-500 = blue background -->
<!-- text-white = white text -->
<!-- px-4 = horizontal padding -->
<!-- py-2 = vertical padding -->
<!-- rounded-lg = rounded corners -->
```

---

## Updating Text Content

### Section 1: Announcement Bar

**Location**: Top of the page, immediately after the opening `<body>` tag

**Current Code**:
```html
<div class="bg-gray-900 text-white py-3 px-4 md:px-0">
    <div class="max-w-7xl mx-auto text-center">
        <p class="text-sm md:text-base flex items-center justify-center gap-2">
            <i class="fas fa-truck text-yellow-400"></i>
            Fast Worldwide Shipping (5 days delivery)
        </p>
    </div>
</div>
```

**How to Update**:
1. Find the text `Fast Worldwide Shipping (5 days delivery)`
2. Replace it with your announcement text
3. Keep the `<i class="fas fa-truck text-yellow-400"></i>` if you want the truck icon, or change it to another icon

**Example Change**:
```html
<!-- Change from: -->
Fast Worldwide Shipping (5 days delivery)

<!-- Change to: -->
Limited Time Offer: 20% Off All Services This Month!
```

**Icon Options**: Visit [Font Awesome Icons](https://fontawesome.com/icons) and replace `fa-truck` with any icon name (e.g., `fa-star`, `fa-gift`, `fa-fire`)

---

### Section 2: Logo and Company Name

**Location**: Header section, top left

**Current Code**:
```html
<div class="flex items-center gap-2">
    <div class="w-10 h-10 bg-gray-900 rounded-lg flex items-center justify-center">
        <span class="text-white font-bold text-lg">EM</span>
    </div>
    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Emet</span>
</div>
```

**How to Update**:
1. Replace `EM` with your company initials or logo text
2. Replace `Emet` with your company name
3. The `hidden sm:inline` means it only shows on small screens and above

**Example Change**:
```html
<!-- Change from: -->
<span class="text-white font-bold text-lg">EM</span>
<span class="font-bold text-xl text-gray-900 hidden sm:inline">Emet</span>

<!-- Change to: -->
<span class="text-white font-bold text-lg">AB</span>
<span class="font-bold text-xl text-gray-900 hidden sm:inline">Acme Brand</span>
```

---

### Section 3: Hero Section (Main Headline)

**Location**: Large section with background image

**Current Code**:
```html
<section id="home" class="relative h-screen md:h-[600px] flex items-center justify-center overflow-hidden">
    <div class="absolute inset-0">
        <img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
             alt="Brand amplification" class="w-full h-full object-cover">
        <div class="hero-overlay absolute inset-0"></div>
    </div>

    <div class="relative z-10 max-w-4xl mx-auto px-4 md:px-6 lg:px-8 text-center">
        <h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight tracking-tight">
            Your Brand. Amplified.
        </h1>
        <p class="text-xl md:text-2xl lg:text-3xl text-gray-100 mb-8 leading-relaxed font-light">
            Make your message impossible to ignore.
        </p>
        <a href="/services" class="btn-primary inline-block bg-yellow-400 text-gray-900 px-8 md:px-12 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 shadow-lg hover:shadow-xl">
            Start Your Journey <i class="fas fa-arrow-right ml-2"></i>
        </a>
    </div>
</section>
```

**How to Update**:

**Update the Main Headline (h1)**:
```html
<!-- Find this line: -->
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight tracking-tight">
    Your Brand. Amplified.
</h1>

<!-- Change "Your Brand. Amplified." to your headline, for example: -->
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold text-white mb-6 leading-tight tracking-tight">
    Grow Your Business Today
</h1>
```

**Update the Subheadline (p tag)**:
```html
<!-- Find this line: -->
<p class="text-xl md:text-2xl lg:text-3xl text-gray-100 mb-8 leading-relaxed font-light">
    Make your message impossible to ignore.
</p>

<!-- Change to: -->
<p class="text-xl md:text-2xl lg:text-3xl text-gray-100 mb-8 leading-relaxed font-light">
    Professional services to boost your brand visibility
</p>
```

**Update the Button Text**:
```html
<!-- Find this line: -->
<a href="/services" class="btn-primary inline-block bg-yellow-400 text-gray-900 px-8 md:px-12 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 shadow-lg hover:shadow-xl">
    Start Your Journey <i class="fas fa-arrow-right ml-2"></i>
</a>

<!-- Change "Start Your Journey" to: -->
<a href="/services" class="btn-primary inline-block bg-yellow-400 text-gray-900 px-8 md:px-12 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 shadow-lg hover:shadow-xl">
    Get Started Now <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**Update the Background Image**:
```html
<!-- Find this line: -->
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Brand amplification" class="w-full h-full object-cover">

<!-- Change the src URL to a different image from Unsplash or your own URL: -->
<img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=1600&h=900&fit=crop&q=80" 
     alt="Your new description" class="w-full h-full object-cover">
```

> **💡 Tip**: Find free images at [Unsplash.com](https://unsplash.com) or [Pexels.com](https://pexels.com)

---

### Section 4: Features Section

**Location**: Three cards showing "Brand Strategy," "Media Content," and "Audience Reach"

**Current Code for First Feature Card**:
```html
<div class="feature-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl hover:border-gray-300">
    <div class="w-14 h-14 bg-gray-900 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-lightbulb text-yellow-400 text-2xl"></i>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">Brand Strategy</h3>
    <p class="text-gray-600 leading-relaxed mb-6">
        Develop a comprehensive brand strategy that resonates with your target audience...
    </p>
    <ul class="space-y-3">
        <li class="flex items-center gap-3 text-gray-700">
            <i class="fas fa-check text-yellow-400 font-bold"></i>
            Market positioning
        </li>
        <!-- More list items... -->
    </ul>
</div>
```

**How to Update Feature Cards**:

**Update Feature Title**:
```html
<!-- Find: -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">Brand Strategy</h3>

<!-- Change to: -->
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">Your New Feature Name</h3>
```

**Update Feature Description**:
```html
<!-- Find: -->
<p class="text-gray-600 leading-relaxed mb-6">
    Develop a comprehensive brand strategy that resonates with your target audience, 
    differentiates you from competitors, and creates lasting emotional connections with your customers.
</p>

<!-- Change to: -->
<p class="text-gray-600 leading-relaxed mb-6">
    Your new description here. Explain what this feature does and why it matters to your customers.
</p>
```

**Update Feature Icon**:
```html
<!-- Find: -->
<i class="fas fa-lightbulb text-yellow-400 text-2xl"></i>

<!-- Change to any Font Awesome icon, for example: -->
<i class="fas fa-star text-yellow-400 text-2xl"></i>
<!-- Or: -->
<i class="fas fa-rocket text-yellow-400 text-2xl"></i>
```

**Update Feature List Items**:
```html
<!-- Find: -->
<ul class="space-y-3">
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Market positioning
    </li>
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Competitive analysis
    </li>
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Brand guidelines
    </li>
</ul>

<!-- Change the list items to: -->
<ul class="space-y-3">
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Your first benefit
    </li>
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Your second benefit
    </li>
    <li class="flex items-center gap-3 text-gray-700">
        <i class="fas fa-check text-yellow-400 font-bold"></i>
        Your third benefit
    </li>
</ul>
```

> **Note**: There are THREE feature cards. Find and update all three in the Features Section.

---

### Section 5: Benefits Sections (Boost Visibility, Build Trust, Grow Sales)

**Location**: Three large sections with images and text

**Example - "Boost Visibility" Section**:

```html
<section id="benefits" class="py-16 md:py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-24">
            <div class="order-2 md:order-1">
                <img src="https://images.unsplash.com/photo-1556740714-a8395b3bf30f?w=800&h=600&fit=crop&q=80" 
                     alt="Boost visibility" class="w-full h-auto rounded-xl shadow-lg object-cover">
            </div>
            <div class="order-1 md:order-2">
                <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
                    Boost Visibility
                </h2>
                <p class="text-lg text-gray-600 mb-6 leading-relaxed">
                    Stand out in a crowded marketplace with strategic brand amplification...
                </p>
                <!-- Bullet points list -->
            </div>
        </div>
    </div>
</section>
```

**How to Update**:

**Update Section Heading**:
```html
<!-- Find: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
    Boost Visibility
</h2>

<!-- Change to: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
    Your New Section Title
</h2>
```

**Update Section Description**:
```html
<!-- Find: -->
<p class="text-lg text-gray-600 mb-6 leading-relaxed">
    Stand out in a crowded marketplace with strategic brand amplification. 
    Our proven methods ensure your message reaches the right people...
</p>

<!-- Change to: -->
<p class="text-lg text-gray-600 mb-6 leading-relaxed">
    Your new description explaining this benefit to customers.
</p>
```

**Update Benefit List Items**:
```html
<!-- Find a list item like: -->
<li class="flex items-start gap-4">
    <div class="w-6 h-6 bg-yellow-400 rounded-full flex items-center justify-center flex-shrink-0 mt-1">
        <i class="fas fa-check text-gray-900 text-sm font-bold"></i>
    </div>
    <div>
        <h4 class="font-bold text-gray-900 mb-1">Multi-channel presence</h4>
        <p class="text-gray-600">Consistent brand messaging across all platforms</p>
    </div>
</li>

<!-- Change to: -->
<li class="flex items-start gap-4">
    <div class="w-6 h-6 bg-yellow-400 rounded-full flex items-center justify-center flex-shrink-0 mt-1">
        <i class="fas fa-check text-gray-900 text-sm font-bold"></i>
    </div>
    <div>
        <h4 class="font-bold text-gray-900 mb-1">Your benefit title</h4>
        <p class="text-gray-600">Your benefit description</p>
    </div>
</li>
```

**Update Section Image**:
```html
<!-- Find: -->
<img src="https://images.unsplash.com/photo-1556740714-a8395b3bf30f?w=800&h=600&fit=crop&q=80" 
     alt="Boost visibility" class="w-full h-auto rounded-xl shadow-lg object-cover">

<!-- Change to: -->
<img src="YOUR_NEW_IMAGE_URL_HERE" 
     alt="Your new description" class="w-full h-auto rounded-xl shadow-lg object-cover">
```

---

### Section 6: About Section

**Location**: Mid-page, "About Emet Media House"

**Current Code**:
```html
<section id="about" class="py-16 md:py-24 bg-gray-50">
    <div class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8">
        <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
                About Emet Media House
            </h2>
            <p class="text-lg text-gray-600">
                Pioneering brand amplification since our founding
            </p>
        </div>

        <div class="bg-white rounded-xl p-8 md:p-12 shadow-md">
            <div class="mb-8">
                <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Story</h3>
                <p class="text-lg text-gray-700 leading-relaxed mb-4">
                    Founded with a passion for transforming brands...
                </p>
            </div>

            <div>
                <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Mission & Vision</h3>
                <p class="text-lg text-gray-700 leading-relaxed">
                    Our mission is to empower businesses...
                </p>
            </div>
        </div>
    </div>
</section>
```

**How to Update**:

**Update Main Heading**:
```html
<!-- Find: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Emet Media House
</h2>

<!-- Change to: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Your Company Name
</h2>
```

**Update Subheading**:
```html
<!-- Find: -->
<p class="text-lg text-gray-600">
    Pioneering brand amplification since our founding
</p>

<!-- Change to: -->
<p class="text-lg text-gray-600">
    Your company tagline or description
</p>
```

**Update "Our Story" Section**:
```html
<!-- Find: -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Our Story</h3>
<p class="text-lg text-gray-700 leading-relaxed mb-4">
    Founded with a passion for transforming brands, 
    Emet Media House emerged from the recognition that businesses needed more than traditional marketing services...
</p>

<!-- Change to: -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Our Story</h3>
<p class="text-lg text-gray-700 leading-relaxed mb-4">
    Your company's origin story and background. 
    Explain how you got started and what drives your business...
</p>
```

**Update "Our Mission & Vision" Section**:
```html
<!-- Find: -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Our Mission & Vision</h3>
<p class="text-lg text-gray-700 leading-relaxed">
    Our mission is to empower businesses by creating authentic, compelling brand narratives...
</p>

<!-- Change to: -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Our Mission & Vision</h3>
<p class="text-lg text-gray-700 leading-relaxed">
    Your company's mission statement and vision for the future...
</p>
```

---

### Section 7: Testimonials Section

**Location**: Customer success stories with 5-star ratings

**Current Code for One Testimonial**:
```html
<div class="testimonial-card bg-white border border-gray-200 rounded-xl p-8 hover:shadow-xl hover:border-gray-300">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Emet Media House completely transformed how we present our brand..."
    </p>
    <div class="flex items-center gap-4">
        <div class="w-12 h-12 bg-gradient-to-br from-yellow-400 to-yellow-500 rounded-full flex items-center justify-center text-white font-bold">
            JM
        </div>
        <div>
            <p class="font-bold text-gray-900">Jessica Martinez</p>
            <p class="text-sm text-gray-600">Marketing Director, TechStart Inc.</p>
        </div>
    </div>
</div>
```

**How to Update**:

**Update Testimonial Quote**:
```html
<!-- Find: -->
<p class="text-gray-700 leading-relaxed mb-6">
    "Emet Media House completely transformed how we present our brand. 
    Their strategic approach to brand positioning..."
</p>

<!-- Change to: -->
<p class="text-gray-700 leading-relaxed mb-6">
    "Your client's testimonial goes here. Keep the quotes and make it authentic 
    to your real customer's experience..."
</p>
```

**Update Client Name and Title**:
```html
<!-- Find: -->
<p class="font-bold text-gray-900">Jessica Martinez</p>
<p class="text-sm text-gray-600">Marketing Director, TechStart Inc.</p>

<!-- Change to: -->
<p class="font-bold text-gray-900">Your Client Name</p>
<p class="text-sm text-gray-600">Their Title, Their Company</p>
```

**Update Client Avatar Initials**:
```html
<!-- Find: -->
<div class="w-12 h-12 bg-gradient-to-br from-yellow-400 to-yellow-500 rounded-full flex items-center justify-center text-white font-bold">
    JM
</div>

<!-- Change to (using your client's initials): -->
<div class="w-12 h-12 bg-gradient-to-br from-yellow-400 to-yellow-500 rounded-full flex items-center justify-center text-white font-bold">
    AB
</div>
```

**Change Star Rating** (if needed):
```html
<!-- To show 4 stars instead of 5, change from: -->
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>

<!-- To: -->
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star star-rating"></i>
<i class="fas fa-star-half-alt star-rating"></i>
```

> **Note**: There are FOUR testimonial cards. Update all of them with your real client testimonials.

---

### Section 8: FAQ Section

**Location**: Frequently Asked Questions with expandable answers

**Current Code for One FAQ Item**:
```html
<div class="faq-item bg-white border border-gray-200 rounded-xl overflow-hidden hover:border-gray-300 transition-all duration-300">
    <button class="faq-toggle w-full px-8 py-6 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-300" onclick="toggleFAQ(this)">
        <h3 class="text-lg font-bold text-gray-900">
            What services does Emet Media House offer?
        </h3>
        <i class="fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-content max-h-0 overflow-hidden transition-all duration-300">
        <div class="px-8 py-6 border-t border-gray-200 bg-gray-50">
            <p class="text-gray-700 leading-relaxed">
                Emet Media House provides comprehensive brand and media solutions...
            </p>
        </div>
    </div>
</div>
```

**How to Update**:

**Update FAQ Question**:
```html
<!-- Find: -->
<h3 class="text-lg font-bold text-gray-900">
    What services does Emet Media House offer?
</h3>

<!-- Change to: -->
<h3 class="text-lg font-bold text-gray-900">
    Your new FAQ question?
</h3>
```

**Update FAQ Answer**:
```html
<!-- Find: -->
<p class="text-gray-700 leading-relaxed">
    Emet Media House provides comprehensive brand and media solutions 
    including brand strategy development, media content creation...
</p>

<!-- Change to: -->
<p class="text-gray-700 leading-relaxed">
    Your detailed answer to the FAQ question goes here. 
    Make it clear and helpful for your customers.
</p>
```

> **Note**: There are FOUR FAQ items. Update all of them with your most common questions and answers.

---

### Section 9: Contact Section

**Location**: Contact form and information

**Current Code**:
```html
<section id="contact" class="py-16 md:py-24 bg-white">
    <div class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8">
        <div class="text-center mb-12">
            <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
                Get In Touch
            </h2>
            <p class="text-lg text-gray-600">
                Ready to amplify your brand? Contact us today.
            </p>
        </div>
        <!-- Contact form and info -->
    </div>
</section>
```

**How to Update**:

**Update Section Heading**:
```html
<!-- Find: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Get In Touch
</h2>

<!-- Change to: -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Contact Us Today
</h2>
```

**Update Email Address**:
```html
<!-- Find: -->
<a href="mailto:info@emetmediahouse.co.za" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    info@emetmediahouse.co.za
</a>

<!-- Change to: -->
<a href="mailto:your-email@yourcompany.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    your-email@yourcompany.com
</a>
```

**Update Location**:
```html
<!-- Find: -->
<h4 class="font-bold text-gray-900 mb-1">Location</h4>
<p class="text-gray-600">
    South Africa
</p>

<!-- Change to: -->
<h4 class="font-bold text-gray-900 mb-1">Location</h4>
<p class="text-gray-600">
    Your City, Your Country
</p>
```

**Update Response Time**:
```html
<!-- Find: -->
<h4 class="font-bold text-gray-900 mb-1">Response Time</h4>
<p class="text-gray-600">
    We typically respond within 24 hours
</p>

<!-- Change to: -->
<h4 class="font-bold text-gray-900 mb-1">Response Time</h4>
<p class="text-gray-600">
    We respond within 2 business hours
</p>
```

---

### Section 10: Footer

**Location**: Bottom of the page

**Current Code**:
```html
<footer class="bg-gray-900 text-gray-300 py-16 md:py-24">
    <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
        <!-- Footer content with company info and links -->
    </div>
</footer>
```

**How to Update**:

**Update Company Name in Footer**:
```html
<!-- Find: -->
<span class="font-bold text-xl text-white">Emet Media House</span>

<!-- Change to: -->
<span class="font-bold text-xl text-white">Your Company Name</span>
```

**Update Company Description**:
```html
<!-- Find: -->
<p class="text-gray-400 leading-relaxed mb-6">
    Amplifying brands and driving growth through strategic media and content solutions.
</p>

<!-- Change to: -->
<p class="text-gray-400 leading-relaxed mb-6">
    Your company's brief description or tagline.
</p>
```

**Update Copyright Year**:
```html
<!-- Find: -->
<p class="text-sm text-gray-500">
    © 2024 Emet Media House. All rights reserved.
</p>

<!-- Change to: -->
<p class="text-sm text-gray-500">
    © 2024 Your Company Name. All rights reserved.
</p>
```

---

## Modifying Tailwind CSS Classes

### Understanding Responsive Design

Your page uses Tailwind's responsive prefixes to adapt to different screen sizes:

```html
<!-- Example: -->
<h1 class="text-4xl md:text-6xl lg:text-7xl">
    Responsive Heading
</h1>

<!-- Breaking it down: -->
<!-- text-4xl = Size on mobile (default) -->
<!-- md:text-6xl = Size on medium screens (768px+) -->
<!-- lg:text-7xl = Size on large screens (1024px+) -->
```

### Common Tailwind Classes Used in Your Page

#### Text Sizes
```
text-sm    = Small text (12px)
text-base  = Normal text (16px)
text-lg    = Large text (18px)
text-xl    = Extra large (20px)
text-2xl   = 24px
text-3xl   = 30px
text-4xl   = 36px
text-5xl   = 48px
text-6xl   = 60px
text-7xl   = 72px
```

#### Colors
```
text-white     = White text
text-gray-900  = Dark gray text
text-gray-600  = Medium gray text
text-yellow-400 = Yellow text (accent color)

bg-white       = White background
bg-gray-900    = Dark gray background
bg-gray-50     = Light gray background
bg-yellow-400  = Yellow background
```

#### Spacing (Padding & Margin)
```
px-4 = Horizontal padding (left and right)
py-3 = Vertical padding (top and bottom)
mb-6 = Margin bottom
mt-4 = Margin top
gap-2 = Space between items
```

#### Common Modifications

**Change Text Color**:
```html
<!-- Current: -->
<h2 class="text-gray-900">Heading</h2>

<!-- Change to blue: -->
<h2 class="text-blue-900">Heading</h2>

<!-- Change to green: -->
<h2 class="text-green-900">Heading</h2>
```

**Change Background Color**:
```html
<!-- Current: -->
<div class="bg-gray-50">Content</div>

<!-- Change to blue: -->
<div class="bg-blue-50">Content</div>
```

**Change Button Color**:
```html
<!-- Current primary button (gray): -->
<a href="#" class="bg-gray-900 text-white px-6 py-3 rounded-lg">Button</a>

<!-- Change to blue: -->
<a href="#" class="bg-blue-600 text-white px-6 py-3 rounded-lg">Button</a>

<!-- Change to green: -->
<a href="#" class="bg-green-600 text-white px-6 py-3 rounded-lg">Button</a>
```

**Change Accent Color (Currently Yellow)**:

If you want to change the accent color throughout the page from yellow to another color:

1. Find all instances of `bg-yellow-400` or `text-yellow-400`
2. Replace with your new color

```html
<!-- Find all: -->
<i class="fas fa-check text-yellow-400 font-bold"></i>

<!-- Replace with: -->
<i class="fas fa-check text-blue-400 font-bold"></i>
```

**Increase or Decrease Padding**:
```html
<!-- Current: -->
<div class="px-4 py-3">Content</div>

<!-- More padding: -->
<div class="px-8 py-6">Content</div>

<!-- Less padding: -->
<div class="px-2 py-1">Content</div>
```

**Increase or Decrease Text Size**:
```html
<!-- Current: -->
<p class="text-lg">Paragraph</p>

<!-- Smaller: -->
<p class="text-base">Paragraph</p>

<!-- Larger: -->
<p class="text-xl">Paragraph</p>
```

### Common Tailwind Classes Reference

| Class | Purpose | Examples |
|-------|---------|----------|
| `text-*` | Text color | `text-white`, `text-gray-900`, `text-yellow-400` |
| `bg-*` | Background color | `bg-white`, `bg-gray-50`, `bg-gray-900` |
| `text-*xl` | Font size | `text-sm`, `text-lg`, `text-2xl` |
| `font-bold` | Bold text | Makes text heavier/darker |
| `px-*` | Horizontal padding | `px-4`, `px-8`, `px-12` |
| `py-*` | Vertical padding | `py-3`, `py-6`, `py-12` |
| `mb-*` | Margin bottom | `mb-4`, `mb-6`, `mb-8` |
| `mt-*` | Margin top | `mt-2`, `mt-4`, `mt-6` |
| `gap-*` | Space between items | `gap-2`, `gap-4`, `gap-8` |
| `rounded-lg` | Rounded corners | `rounded-lg`, `rounded-xl` |
| `shadow-lg` | Drop shadow | `shadow-md`, `shadow-lg`, `shadow-xl` |
| `hover:*` | Hover effect | `hover:bg-gray-800`, `hover:text-white` |
| `transition-*` | Smooth animation | `transition-colors`, `transition-all` |

---

## Fixing and Managing Links

### Understanding Links in Your Page

Your page has several types of links:

1. **Internal Navigation Links** (jump to sections on same page)
2. **External Links** (go to other pages or websites)
3. **Button Links** (styled as buttons)
4. **Social Media Links**

### Where Links Are Located

#### 1. Navigation Menu (Header)

**Location**: Inside the `<header>` section

**Current Code**:
```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Home</a>
    <a href="#features" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Benefits</a>
    <a href="#about" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">About</a>
    <a href="#testimonials" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Testimonials</a>
    <a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Contact</a>
</nav>
```

**What These Links Do**:
- `href="#home"` = Jumps to section with `id="home"`
- `href="#features"` = Jumps to section with `id="features"`
- And so on for each section

**These links are working correctly** if you haven't changed the section IDs.

---

#### 2. "Get Started" Buttons

**Location**: Multiple places throughout the page

**Current Code**:
```html
<a href="/services" class="btn-primary inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
    Get Started
</a>
```

**What This Link Does**:
- `href="/services"` = Goes to a page at `/services`

**To Change This**:

If you don't have a `/services` page yet, change the link to:

```html
<!-- Option 1: Link to a contact form -->
<a href="#contact" class="btn-primary inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
    Get Started
</a>

<!-- Option 2: Link to an external URL -->
<a href="https://yourwebsite.com/services" class="btn-primary inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
    Get Started
</a>

<!-- Option 3: Link to a services.html file in your project -->
<a href="services.html" class="btn-primary inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
    Get Started
</a>
```

**Find All "Get Started" Buttons**:

Search for `href="/services"` in your HTML file. There should be multiple instances:
- One in the hero section
- One in the CTA section
- One in the footer
- One in the mobile menu

**Replace All Instances**:

Use your code editor's "Find and Replace" feature:
1. Press `Ctrl+H` (or `Cmd+H` on Mac)
2. Find: `/services`
3. Replace with: `#contact` (or your desired link)
4. Click "Replace All"

---

#### 3. Contact Email Link

**Location**: Contact section and footer

**Current Code**:
```html
<a href="mailto:info@emetmediahouse.co.za" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    info@emetmediahouse.co.za
</a>
```

**What This Link Does**:
- Opens the user's default email client to compose an email to this address

**To Change This**:
```html
<!-- Find: -->
<a href="mailto:info@emetmediahouse.co.za">

<!-- Replace with: -->
<a href="mailto:your-email@yourcompany.com">
```

**Find All Email Links**:

Search for `mailto:` in your HTML. Replace all instances with your email.

---

#### 4. Social Media Links

**Location**: Contact section and footer

**Current Code**:
```html
<a href="#" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**What This Link Does**:
- Currently does nothing (link to `#`)

**To Change This**:
```html
<!-- Facebook - Find: -->
<a href="#" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Replace with: -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Twitter - Change: -->
<a href="https://twitter.com/yourprofile" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-twitter"></i>
</a>

<!-- Instagram - Change: -->
<a href="https://instagram.com/yourprofile" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-instagram"></i>
</a>

<!-- LinkedIn - Change: -->
<a href="https://linkedin.com/company/yourcompany" class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center hover:bg-gray-900 hover:text-white transition-all duration-300">
    <i class="fab fa-linkedin-in"></i>
</a>
```

**Find Your Social Media URLs**:

1. Go to your Facebook page and copy the URL
2. Go to your Twitter profile and copy the URL
3. Do the same for Instagram and LinkedIn

---

#### 5. Footer Links

**Location**: Bottom of the page in the `<footer>`

**Current Code**:
```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
```

**What These Links Do**:
- `href="privacy.html"` = Goes to a file called `privacy.html`
- `href="terms.html"` = Goes to a file called `terms.html`
- `href="blog.html"` = Goes to a file called `blog.html`

**Status**: These files don't exist yet. See the next section for how to create them.

---

### Link Checklist

Use this checklist to verify all your links are working:

- [ ] Navigation menu links jump to correct sections
- [ ] All "Get Started" buttons go to the right page
- [ ] Email link has your correct email address
- [ ] Social media links go to your actual profiles
- [ ] Privacy and Terms links are set up (see next section)
- [ ] Blog link is set up (if you have a blog)

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy Policy and Terms of Service pages are:
- **Legal requirements** for most websites
- **Build trust** with visitors
- **Protect your business** legally

### Step-by-Step: Creating Privacy.html

#### Step 1: Create a New File

1. Open your code editor
2. Create a new file named `privacy.html`
3. Save it in the same folder as `index.html`

#### Step 2: Add Basic Structure

Copy and paste this template into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Emet Media House">
    <title>Privacy Policy | Emet Media House</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation (copy from index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center gap-2">
                    <div class="w-10 h-10 bg-gray-900 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-lg">EM</span>
                    </div>
                    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Emet</span>
                </div>

                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Home</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Contact</a>
                </nav>

                <div class="flex items-center gap-4">
                    <a href="index.html" class="btn-primary hidden sm:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
                        Back Home
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700">
            <p class="mb-6 leading-relaxed">
                Last updated: January 2024
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
            <p class="mb-6 leading-relaxed">
                Emet Media House ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you 
                visit our website.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
            <p class="mb-4 leading-relaxed">
                We may collect information about you in a variety of ways. The information we may collect on the site includes:
            </p>
            <ul class="list-disc list-inside mb-6 space-y-2">
                <li>Personal Data: Name, email address, phone number, company name, and other information you voluntarily provide</li>
                <li>Device Information: Browser type, IP address, operating system</li>
                <li>Usage Data: Pages visited, time spent on pages, links clicked</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
            <p class="mb-6 leading-relaxed">
                We use the information we collect for the following purposes:
            </p>
            <ul class="list-disc list-inside mb-6 space-y-2">
                <li>To provide and maintain our services</li>
                <li>To respond to your inquiries and support requests</li>
                <li>To send marketing and promotional communications (with your consent)</li>
                <li>To improve our website and services</li>
                <li>To comply with legal obligations</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Sharing Your Information</h2>
            <p class="mb-6 leading-relaxed">
                We do not sell, trade, or rent your personal information to third parties. We may share your information 
                only in the following circumstances:
            </p>
            <ul class="list-disc list-inside mb-6 space-y-2">
                <li>With your explicit consent</li>
                <li>To comply with legal requirements</li>
                <li>To protect our rights and safety</li>
                <li>With service providers who assist us in operating our website</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Data Security</h2>
            <p class="mb-6 leading-relaxed">
                We implement appropriate technical and organizational measures to protect your personal information 
                against unauthorized access, alteration, disclosure, or destruction.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Your Rights</h2>
            <p class="mb-6 leading-relaxed">
                You have the right to:
            </p>
            <ul class="list-disc list-inside mb-6 space-y-2">
                <li>Access your personal data</li>
                <li>Correct inaccurate data</li>
                <li>Request deletion of your data</li>
                <li>Opt-out of marketing communications</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Contact Us</h2>
            <p class="mb-6 leading-relaxed">
                If you have questions about this Privacy Policy or our privacy practices, please contact us at:
            </p>
            <p class="mb-6">
                Email: <a href="mailto:info@emetmediahouse.co.za" class="text-blue-600 hover:text-blue-800">info@emetmediahouse.co.za</a>
            </p>
        </div>
    </main>

    <!-- Footer (copy from index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-24 mt-16">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center gap-2 mb-4">
                        <div class="w-10 h-10 bg-yellow-400 rounded-lg flex items-center justify-center">
                            <span class="text-gray-900 font-bold text-lg">EM</span>
                        </div>
                        <span class="font-bold text-xl text-white">Emet Media House</span>
                    </div>
                    <p class="text-sm text-gray-500">
                        © 2024 Emet Media House. All rights reserved.
                    </p>
                </div>

                <div>
                    <h4 class="font-bold text-white mb-6 text-lg">Quick Links</h4>
                    <ul class="space-y-3">
                        <li>
                            <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                        </li>
                        <li>
                            <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
                        </li>
                        <li>
                            <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-500 text-sm text-center">
                    © 2024 Emet Media House. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

#### Step 3: Customize Privacy Policy

Replace the placeholder text with your actual privacy policy:

```html
<!-- Change the company name from "Emet Media House" to your company name -->
<!-- Change the email from "info@emetmediahouse.co.za" to your email -->
<!-- Update the "Last updated" date to today's date -->
<!-- Customize the sections to match your actual practices -->
```

---

### Step-by-Step: Creating Terms.html

#### Step 1: Create a New File

1. Create a new file named `terms.html`
2. Save it in the same folder as `index.html`

#### Step 2: Add Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Emet Media House">
    <title>Terms of Service | Emet Media House</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex items-center gap-2">
                    <div class="w-10 h-10 bg-gray-900 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-lg">EM</span>
                    </div>
                    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Emet</span>
                </div>

                <nav class="hidden md:flex items-center gap-8">
                    <a href="index.html" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Home</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium text-sm transition-colors duration-300">Contact</a>
                </nav>

                <div class="flex items-center gap-4">
                    <a href="index.html" class="btn-primary hidden sm:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-medium text-sm hover:bg-gray-800">
                        Back Home
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 md:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg max-w-none text-gray-700">
            <p class="mb-6 leading-relaxed">
                Last updated: January 2024
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
            <p class="mb-6 leading-relaxed">
                By accessing and using this website, you accept and agree to be bound by the terms and provision 
                of this agreement. If you do not agree to abide by the above, please do not use this service.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
            <p class="mb-6 leading-relaxed">
                Permission is granted to temporarily download one copy of the materials (information or software) 
                on Emet Media House's website for personal, non-commercial transitory viewing only. This is the grant 
                of a license, not a transfer of title, and under this license you may not:
            </p>
            <ul class="list-disc list-inside mb-6 space-y-2">
                <li>Modify or copy the materials</li>
                <li>Use the materials for any commercial purpose or for any public display</li>
                <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                <li>Remove any copyright or other proprietary notations from the materials</li>
                <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
            </ul>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
            <p class="mb-6 leading-relaxed">
                The materials on Emet Media House's website are provided on an 'as is' basis. Emet Media House makes 
                no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, 
                without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, 
                or non-infringement of intellectual property or other violation of rights.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
            <p class="mb-6 leading-relaxed">
                In no event shall Emet Media House or its suppliers be liable for any damages (including, without limitation, 
                damages for loss of data or profit, or due to business interruption) arising out of the use or inability 
                to use the materials on Emet Media House's website.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
            <p class="mb-6 leading-relaxed">
                The materials appearing on Emet Media House's website could include technical, typographical, or 
                photographic errors. Emet Media House does not warrant that any of the materials on the website are 
                accurate, complete, or current. Emet Media House may make changes to the materials contained on its 
                website at any time without notice.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
            <p class="mb-6 leading-relaxed">
                Emet Media House has not reviewed all of the sites linked to its website and is not responsible for 
                the contents of any such linked site. The inclusion of any link does not imply endorsement by Emet Media House 
                of the site. Use of any such linked website is at the user's own risk.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
            <p class="mb-6 leading-relaxed">
                Emet Media House may revise these terms of service for its website at any time without notice. 
                By using this website, you are agreeing to be bound by the then current version of these terms of service.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
            <p class="mb-6 leading-relaxed">
                These terms and conditions are governed by and construed in accordance with the laws of South Africa 
                and you irrevocably submit to the exclusive jurisdiction of the courts located in that location.
            </p>

            <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Us</h2>
            <p class="mb-6 leading-relaxed">
                If you have any questions about these Terms of Service, please contact us at:
            </p>
            <p class="mb-6">
                Email: <a href="mailto:info@emetmediahouse.co.za" class="text-blue-600 hover:text-blue-800">info@emetmediahouse.co.za</a>
            </p>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-24 mt-16">
        <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center gap-2 mb-4">
                        <div class="w-10 h-10 bg-yellow-400 rounded-lg flex items-center justify-center">
                            <span class="text-gray-900 font-bold text-lg">EM</span>
                        </div>
                        <span class="font-bold text-xl text-white">Emet Media House</span>
                    </div>
                    <p class="text-sm text-gray-500">
                        © 2024 Emet Media House. All rights reserved.
                    </p>
                </div>

                <div>
                    <h4 class="font-bold text-white mb-6 text-lg">Quick Links</h4>
                    <ul class="space-y-3">
                        <li>
                            <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
                        </li>
                        <li>
                            <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
                        </li>
                        <li>
                            <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-500 text-sm text-center">
                    © 2024 Emet Media House. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Verify Links in Index.html

Your `index.html` already has the correct links to these pages in the footer:

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

**These links should now work!**

---

### Customization Checklist for Policy Pages

- [ ] Update company name from "Emet Media House" to your company name
- [ ] Update email from "info@emetmediahouse.co.za" to your email
- [ ] Update "Last updated" date to today's date
- [ ] Update copyright year to current year
- [ ] Customize the policy content to match your actual practices
- [ ] Update "Governing Law" section to match your location
- [ ] Review and ensure accuracy of all information

---

## Customizing Colors and Styling

### Current Color Scheme

Your page uses these main colors:

| Color | Usage | Tailwind Class |
|-------|-------|-----------------|
| Dark Gray | Primary text, backgrounds | `gray-900`, `text-gray-900` |
| Light Gray | Secondary text, backgrounds | `gray-600`, `bg-gray-50` |
| Yellow | Accents, highlights | `yellow-400` |
| White | Text on dark backgrounds | `text-white`, `bg-white` |

### How to Change the Primary Color

The primary color (currently dark gray) is used for:
- Main headings
- Buttons
- Navigation

**To change from dark gray to blue:**

1. Find all instances of `bg-gray-900` (button backgrounds)
2. Replace with `bg-blue-600` or `bg-blue-700`

```html
<!-- Find: -->
<a href="#" class="bg-gray-900 text-white px-6 py-3 rounded-lg">Button</a>

<!-- Replace with: -->
<a href="#" class="bg-blue-600 text-white px-6 py-3 rounded-lg">Button</a>
```

3. Also update hover states:
```html
<!-- Find: -->
hover:bg-gray-800

<!-- Replace with: -->
hover:bg-blue-700
```

### How to Change the Accent Color (Yellow)

The accent color is currently yellow and used for:
- Icons in feature cards
- Check marks in lists
- Button accents

**To change from yellow to green:**

1. Use Find and Replace to change all `yellow-400` to `green-400`

```
Find: text-yellow-400
Replace with: text-green-400

Find: bg-yellow-400
Replace with: bg-green-400
```

2. Also update hover states:
```
Find: hover:bg-yellow-300
Replace with: hover:bg-green-300
```

### Tailwind Color Options

Here are common Tailwind colors you can use:

```
Blue:     blue-400, blue-500, blue-600, blue-700
Green:    green-400, green-500, green-600, green-700
Red:      red-400, red-500, red-600, red-700
Purple:   purple-400, purple-500, purple-600, purple-700
Pink:     pink-400, pink-500, pink-600, pink-700
Orange:   orange-400, orange-500, orange-600, orange-700
```

### Custom CSS (Advanced)

If you want to add custom styling beyond Tailwind, add a `<style>` section in the `<head>`:

```html
<head>
    <!-- Existing code -->
    <style>
        /* Your custom CSS here */
        .my-custom-class {
            color: #your-color;
            background: #your-background;
        }
    </style>
</head>
```

---

## Common Issues and Troubleshooting

### Issue 1: Links Not Working

**Problem**: Clicking a link doesn't go anywhere

**Solutions**:

1. **Check the href attribute**:
```html
<!-- Wrong: -->
<a href="services">Page</a>

<!-- Correct: -->
<a href="services.html">Page</a>
<!-- Or: -->
<a href="/services">Page</a>
<!-- Or: -->
<a href="https://example.com/services">Page</a>
```

2. **For internal section links, verify the section ID exists**:
```html
<!-- Link: -->
<a href="#features">Features</a>

<!-- Must have matching section: -->
<section id="features">...</section>
```

3. **Check file paths**:
   - Files in the same folder: `privacy.html`
   - Files in subfolders: `pages/privacy.html`
   - Absolute URLs: `https://example.com/privacy`

---

### Issue 2: Text Not Changing When You Edit

**Problem**: You edit text in the HTML, but it doesn't appear on the website

**Solutions**:

1. **Save the file** (Ctrl+S or Cmd+S)
2. **Refresh the browser** (F5 or Cmd+R)
3. **Clear browser cache**:
   - Chrome: Ctrl+Shift+Delete
   - Safari: Cmd+Shift+Delete
4. **Check you edited the right file** (verify file name is `index.html`)

---

### Issue 3: Styling Looks Wrong

**Problem**: Colors, spacing, or layout looks different than expected

**Solutions**:

1. **Check Tailwind CSS is loading**:
   - Look for this line in the `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - If missing, add it

2. **Verify class names are correct**:
```html
<!-- Wrong: -->
<div class="text-larg">Text</div>

<!-- Correct: -->
<div class="text-lg">Text</div>
```

3. **Check for typos in color names**:
```html
<!-- Wrong: -->
<div class="bg-gra-900">Text</div>

<!-- Correct: -->
<div class="bg-gray-900">Text</div>
```

---

### Issue 4: Mobile Menu Not Working

**Problem**: Mobile menu doesn't open on small screens

**Solutions**:

1. **Check JavaScript is enabled** in your browser
2. **Verify the toggleMobileMenu function exists**:
```html
<!-- Should be in <script> section at bottom: -->
<script>
    function toggleMobileMenu() {
        const mobileMenu = document.querySelector('.mobile-menu');
        mobileMenu.classList.toggle('active');
    }
</script>
```

3. **Test on actual mobile device or browser developer tools**:
   - Press F12 to open developer tools
   - Click the mobile device icon to view mobile version

---

### Issue 5: Images Not Showing

**Problem**: Images from Unsplash or other sources don't display

**Solutions**:

1. **Check image URL is correct**:
```html
<!-- Wrong: -->
<img src="htp://images.unsplash.com/...">

<!-- Correct: -->
<img src="https://images.unsplash.com/...">
```

2. **Check internet connection** - Unsplash images require internet

3. **Use local images instead**:
```html
<!-- Instead of Unsplash URL: -->
<img src="https://images.unsplash.com/photo-123456?w=800">

<!-- Use local file: -->
<img src="images/my-image.jpg">
```

---

### Issue 6: Form Not Submitting

**Problem**: Contact form doesn't send messages

**Solutions**:

1. **The form is not connected to a backend service**. You need to:
   - Set up a form submission service like Formspree, Netlify Forms, or EmailJS
   - Or create a backend script to handle submissions

2. **Quick fix with Formspree** (free):
```html
<!-- Find the form tag: -->
<form class="space-y-4">

<!-- Change to: -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-4">
```

3. **To get a Formspree form ID**:
   - Go to formspree.io
   - Sign up
   - Create a new form
   - Copy the form ID
   - Replace `YOUR_FORM_ID` above

---

### Issue 7: Responsive Design Broken

**Problem**: Page doesn't look right on mobile or tablet

**Solutions**:

1. **Check viewport meta tag exists**:
```html
<!-- Should be in <head>: -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. **Don't remove responsive classes**:
```html
<!-- Wrong - removes responsive design: -->
<div class="text-4xl">Text</div>

<!-- Correct - keeps responsive design: -->
<div class="text-4xl md:text-6xl lg:text-7xl">Text</div>
```

3. **Test on mobile**:
   - Use browser developer tools (F12)
   - Click mobile device icon
   - Test on actual phone

---

## Best Practices

### 1. Always Back Up Your Files

Before making major changes:
```
1. Copy your index.html to index.html.backup
2. Or use version control (Git)
3. Or save to cloud storage
```

### 2. Use Meaningful File Names

```
✅ Good names:
- privacy.html
- terms.html
- services.html
- about-us.html

❌ Bad names:
- page1.html
- new-file.html
- copy.html
```

### 3. Keep Consistent Styling

```html
<!-- Use the same color throughout: -->
<!-- Good: -->
<button class="bg-blue-600">Button 1</button>
<button class="bg-blue-600">Button 2</button>

<!-- Bad: -->
<button class="bg-blue-600">Button 1</button>
<button class="bg-green-600">Button 2</button>
```

### 4. Test on Multiple Devices

Always test your changes on:
- Desktop (1920px width)
- Tablet (768px width)
- Mobile (375px width)

Use browser developer tools to simulate different screen sizes.

### 5. Keep Images Optimized

```html
<!-- Use appropriate image sizes: -->
<!-- Good: -->
<img src="image.jpg?w=800&h=600&fit=crop&q=80">

<!-- Bad: -->
<img src="image-4000x3000.jpg">
```

### 6. Use Semantic HTML

```html
<!-- Good: -->
<section id="features">Features</section>
<h1>Main Heading</h1>
<h2>Subheading</h2>

<!-- Bad: -->
<div id="features">Features</div>
<div class="heading">Main Heading</div>
<div class="heading">Subheading</div>
```

### 7. Comment Your Changes

```html
<!-- Add comments to help future you understand changes -->
<!-- Updated email to new support address - Jan 2024 -->
<a href="mailto:support@newaddress.com">Email</a>
```

### 8. Test All Links

Before publishing, verify:
- [ ] All navigation links work
- [ ] All buttons go to correct pages
- [ ] Email links open email client
- [ ] Social media links go to your profiles
- [ ] External links open in new tab (if desired)

### 9. Keep Code Organized

```html
<!-- Group related content: -->
<section id="features">
    <!-- All feature cards together -->
</section>

<section id="testimonials">
    <!-- All testimonials together -->
</section>
```

### 10. Use Consistent Spacing

```html
<!-- Use consistent margin/padding classes: -->
<!-- Good: -->
<h2 class="text-3xl font-bold mb-6">Heading</h2>
<p class="text-lg mb-6">Paragraph</p>

<!-- Bad: -->
<h2 class="text-3xl font-bold mb-2">Heading</h2>
<p class="text-lg mb-10">Paragraph</p>
```

---

## Quick Reference: Common Tasks

### Change Company Name
Search for "Emet" and replace with your company name (appears in header, footer, and multiple places)

### Change Email Address
Search for "info@emetmediahouse.co.za" and replace with your email

### Change Button Links
Search for `href="/services"` and replace with your desired link

### Change Accent Color
Search for "yellow-400" and replace with your desired color (e.g., "blue-400")

### Change Primary Color
Search for "gray-900" and replace with your desired color (e.g., "blue-700")

### Add New Section
1. Copy an existing section
2. Paste it in desired location
3. Update the ID attribute (e.g., `id="new-section"`)
4. Update all content
5. Add link to navigation menu

### Update Hero Image
Find the `<img>` tag in the hero section and change the `src` URL

### Add Social Media Links
Find the social media icons in the contact section and footer, update the `href` attributes with your profile URLs

---

## Resources

### Learning Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

### Tools
- [Unsplash Images](https://unsplash.com) - Free stock photos
- [Pexels Images](https://pexels.com) - Free stock photos
- [Formspree](https://formspree.io) - Form submissions
- [VS Code](https://code.visualstudio.com) - Code editor
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/) - Browser testing

### Color Tools
- [Tailwind Color Palette](https://tailwindcss.com/docs/customizing-colors)
- [Color Hunt](https://colorhunt.co) - Color palettes
- [Coolors.co](https://coolors.co) - Color generator

---

## Support & Next Steps

### Common Next Steps

1. **Add more pages**:
   - Create services.html
   - Create blog.html
   - Create case-studies.html

2. **Set up form submission**:
   - Use Formspree for simple forms
   - Use Netlify Forms for hosted sites
   - Use EmailJS for JavaScript-based forms

3. **Add analytics**:
   - Google Analytics
   - Hotjar for user behavior

4. **Optimize for search engines (SEO)**:
   - Update meta descriptions
   - Add structured data
   - Optimize images

5. **Deploy your website**:
   - Netlify (free)
   - Vercel (free)
   - GitHub Pages (free)
   - Traditional hosting provider

### Getting Help

If you encounter issues:

1. **Check this guide** - Most common issues are covered above
2. **Check the HTML** - Look for typos or missing tags
3. **Use browser developer tools** - Press F12 to inspect elements
4. **Search online** - Google the error message
5. **Ask in communities** - Stack Overflow, Reddit, web development forums

---

## Final Checklist Before Launch

- [ ] All text content is updated with your information
- [ ] Company name, email, and contact info are correct
- [ ] All links are working and go to correct pages
- [ ] Images are loading correctly
- [ ] Mobile menu works on small screens
- [ ] Page looks good on desktop, tablet, and mobile
- [ ] Privacy and Terms pages are created and linked
- [ ] Form submission is set up (if needed)
- [ ] All social media links are correct
- [ ] No broken links or 404 errors
- [ ] Page loads quickly
- [ ] All text is spelled correctly
- [ ] Colors and styling are consistent
- [ ] Testimonials are updated with real clients
- [ ] FAQ questions and answers are relevant
- [ ] CTA buttons are prominent and working

---

**Congratulations!** You now have a comprehensive guide to maintaining and customizing your Emet Media House landing page. Start with small changes, test thoroughly, and don't hesitate to refer back to this guide as needed.