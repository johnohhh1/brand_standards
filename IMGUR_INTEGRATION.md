# Imgur Image Integration Guide

This document explains how to integrate your decorative images with the Chili's Brand Standards web page using Imgur.

## Current Status

The HTML file (`index.html`) now includes placeholder Imgur URLs for decorative pattern images. These images appear:
- In the header section (4 larger decorative images)
- Between major sections as dividers (6 smaller pattern images)

## How to Update with Your Imgur URLs

### Step 1: Upload Images to Imgur

1. Go to [imgur.com](https://imgur.com)
2. Upload your decorative pattern images (image1.png through image27.png)
3. For each uploaded image, copy the direct image URL (ends with .png or .jpg)

### Step 2: Replace Placeholder URLs in index.html

Find and replace the placeholder URLs with your actual Imgur URLs:

**Header Pattern Images (lines ~332-336):**
```html
<img src="https://i.imgur.com/placeholder1.png" alt="Chili Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/placeholder2.png" alt="Chili Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/placeholder3.png" alt="Chili Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/placeholder4.png" alt="Chili Pattern" onerror="this.style.display='none'">
```

**Section Divider Patterns (appears 5 times throughout the file):**
```html
<img src="https://i.imgur.com/pattern1.png" alt="Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/pattern2.png" alt="Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/pattern3.png" alt="Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/pattern4.png" alt="Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/pattern5.png" alt="Pattern" onerror="this.style.display='none'">
<img src="https://i.imgur.com/pattern6.png" alt="Pattern" onerror="this.style.display='none'">
```

### Step 3: Example Replacement

Replace placeholder URLs with your actual Imgur URLs. For example:

**Before:**
```html
<img src="https://i.imgur.com/placeholder1.png" alt="Chili Pattern" onerror="this.style.display='none'">
```

**After:**
```html
<img src="https://i.imgur.com/ABC123.png" alt="Chili Pattern" onerror="this.style.display='none'">
```

Where `ABC123` is your actual Imgur image ID.

## Image Specifications

- **Header Pattern Images**: Displayed at 80px × 80px
- **Section Divider Patterns**: Displayed at 60px × 60px
- Recommended upload size: 200px × 200px (will scale down automatically)
- Supported formats: PNG, JPG

## Error Handling

The `onerror="this.style.display='none'"` attribute ensures that if an image fails to load, it will be hidden rather than showing a broken image icon.

## Questions or Issues?

If images aren't displaying correctly:
1. Verify the Imgur URLs are direct image links (end with .png or .jpg)
2. Check that the URLs are publicly accessible
3. Ensure you're using the direct link, not the Imgur page link
