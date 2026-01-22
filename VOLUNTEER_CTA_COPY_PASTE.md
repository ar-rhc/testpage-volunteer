# Volunteer CTA Section - Copy & Paste Guide

This document contains the clean, portable code for the volunteer registration call-to-action section.

## Dependencies (Add to `<head>` section)

```html
<!-- Font Awesome for calendar icon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

<!-- Google Fonts (if not already included) -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Raleway:400,500,600,700|Open+Sans:400,600,700">
```

---

## CSS Styles (Add to `<head>` section, inside `<style>` tag or external CSS file)

```css
/* ============================================
   VOLUNTEER CTA CARD STYLES
   ============================================ */

/* Main card container */
.volunteer-cta-card {
    background: #eff6ff !important;
    border: 2px solid #bfdbfe !important;
    border-radius: 12px !important;
    padding: 30px !important;
    text-align: center !important;
    margin: 25px 0 !important;
    box-sizing: border-box !important;
}

/* Card heading */
.volunteer-cta-card h2 {
    color: #1e40af !important;
    margin-bottom: 10px !important;
    font-weight: 700 !important;
    font-size: 24px !important;
    text-align: center !important;
}

/* Card description text */
.volunteer-cta-card p {
    font-size: 16px !important;
    margin-bottom: 25px !important;
    color: #333 !important;
    text-align: center !important;
}

/* Primary button */
.btn-volunteer-primary {
    background-color: #2563eb !important;
    color: #fff !important;
    padding: 12px 35px !important;
    font-size: 18px !important;
    font-weight: 700 !important;
    border-radius: 50px !important;
    text-transform: uppercase !important;
    display: inline-block !important;
    transition: all 0.3s ease !important;
    border: none !important;
    box-shadow: 0 4px 15px rgba(37, 99, 235, 0.2) !important;
    text-decoration: none !important;
    cursor: pointer !important;
    margin: 0 auto !important;
}

/* Button hover state */
.btn-volunteer-primary:hover,
.btn-volunteer-primary:focus {
    background-color: #1d4ed8 !important;
    transform: translateY(-2px) !important;
    box-shadow: 0 6px 20px rgba(37, 99, 235, 0.3) !important;
    text-decoration: none !important;
    color: #fff !important;
}

/* Link to upcoming trips */
.volunteer-cta-card a[href*="upcoming-trips"] {
    font-weight: 600 !important;
    color: #2563eb !important;
    text-decoration: none !important;
    display: inline-block !important;
}

.volunteer-cta-card a[href*="upcoming-trips"]:hover {
    text-decoration: underline !important;
}

/* Container for the link */
.volunteer-cta-card > div {
    text-align: center !important;
    width: 100% !important;
    margin-top: 15px !important;
}

/* Calendar icon styling */
.volunteer-cta-card .fas,
.volunteer-cta-card i.fas {
    margin-right: 8px !important;
    color: #1e40af !important;
}
```

**Note:** If your content is inside a container with class `.entry-content`, you may need to prefix selectors with `.entry-content` (e.g., `.entry-content .volunteer-cta-card`). The `!important` flags ensure styles override existing CSS.

---

## HTML Markup (Paste where you want the section to appear)

```html
<!-- High Visibility Registration Section -->
<div class="volunteer-cta-card">
    <h2>Join a Volunteer Trip</h2>
    <p>
        Ready to help preserve Motuihe Island?
        <br>
        Register now to secure your spot on an upcoming weekend trip.
    </p>
    
    <a href="https://motuihetrust.my.site.com/volunteer/s/weekend-volunteer" class="btn-volunteer-primary">
        Register to Volunteer
    </a>
    
    <div>
        <a href="https://www.motuihe.org.nz/activities/upcoming-trips/">
            <i class="fas fa-calendar-alt"></i> View the full list of upcoming trips
        </a>
    </div>
</div>
```

---

## Color Reference

- **Card Background:** `#eff6ff` (light blue)
- **Card Border:** `#bfdbfe` (blue border)
- **Heading/Icon Color:** `#1e40af` (dark blue)
- **Button Background:** `#2563eb` (blue)
- **Button Hover:** `#1d4ed8` (darker blue)
- **Link Color:** `#2563eb` (blue)
- **Text Color:** `#333` (dark gray)

---

## Customization Notes

1. **Change colors:** Update the hex color values in the CSS (search for `#2563eb`, `#1e40af`, etc.)
2. **Change button text:** Edit the text inside `<a class="btn-volunteer-primary">`
3. **Change links:** Update the `href` attributes in the HTML
4. **Remove icon:** Remove `<i class="fas fa-calendar-alt"></i>` if Font Awesome isn't available
5. **Adjust spacing:** Modify `padding`, `margin`, and `gap` values in CSS

---

## Additional CSS Changes Made to Original Page

These styles were added to make images display in rows of 2 and match the card width:

```css
/* Make images display 2 per row */
.entry-content > p:not(.volunteer-cta-card p) {
    display: flex !important;
    flex-wrap: wrap !important;
    gap: 10px !important;
    width: 100% !important;
    box-sizing: border-box !important;
    margin-bottom: 0 !important;
}

.entry-content p img {
    width: calc(50% - 5px) !important;
    height: auto !important;
    display: block !important;
    max-width: 100% !important;
    box-sizing: border-box !important;
    flex: 0 0 calc(50% - 5px) !important;
}
```

**Note:** These image styles are specific to the original page layout and may need adjustment for your site structure.
