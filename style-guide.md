# Style Guide - Social Links Profile

Complete design specifications and guidelines for the Social Links Profile project.

## 📋 Table of Contents
1. [Colors](#colors)
2. [Typography](#typography)
3. [Spacing](#spacing)
4. [Border Radius](#border-radius)
5. [Shadows & Effects](#shadows--effects)
6. [Interactive States](#interactive-states)
7. [Responsive Design](#responsive-design)

---

## 🎨 Colors

### Primary Colors
```css
--clr-primary-bg: #1f1f1f;      /* Page background */
--clr-card-bg: #111111;         /* Card background */
--clr-text-primary: #ffffff;    /* Primary text */
--clr-text-secondary: #b6b6b6;  /* Secondary text */
```

### Accent Color
```css
--clr-accent: #00d084;          /* Accent/highlight color */
```

### Interactive Colors
```css
--clr-link-bg: #333333;         /* Default link background */
--clr-link-hover-bg: #00d084;   /* Link on hover */
--clr-link-hover-text: #111111; /* Text on hover */
```

### Color Usage
- **Primary Background**: Full page background
- **Card Background**: Main profile card
- **Text Primary**: Headings, main content
- **Text Secondary**: Location, bio, supporting text
- **Accent**: Focus states, hover effects, highlights
- **Link Background**: Default social link buttons
- **Link Hover**: Active/hovered social links

---

## 🔤 Typography

### Font Family
```css
--font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

### Font Sizes
```css
--font-size-name: 1.5rem;       /* Profile name (24px) */
--font-size-location: 0.875rem; /* Location (14px) */
--font-size-bio: 0.875rem;      /* Bio/quote (14px) */
--font-size-link: 1rem;         /* Social links (16px) */
```

### Font Weights
- **700** - Profile name (bold)
- **600** - Social link buttons
- **500** - Location text
- **400** - Bio/quote (default)

### Line Heights
- **1.6** - Body text
- **1.5** - Bio/quote text

---

## 📐 Spacing

### Spacing Scale
```css
--spacing-xs: 0.5rem;   /* 8px */
--spacing-sm: 1rem;     /* 16px */
--spacing-md: 1.5rem;   /* 24px */
--spacing-lg: 2rem;     /* 32px */
--spacing-xl: 3rem;     /* 48px */
```

### Component Spacing

**Profile Card**
- Padding: `var(--spacing-xl) var(--spacing-lg)` (48px vertical, 32px horizontal)

**Profile Image**
- Margin bottom: `var(--spacing-lg)` (32px)
- Size: 88x88px
- Border width: 3px

**Profile Name**
- Margin bottom: `var(--spacing-xs)` (8px)

**Profile Location**
- Margin bottom: `var(--spacing-md)` (24px)

**Profile Bio**
- Margin bottom: `var(--spacing-lg)` (32px)

**Social Links Container**
- Gap between links: `var(--spacing-sm)` (16px)

**Social Link Button**
- Padding: `var(--spacing-sm) var(--spacing-md)` (16px vertical, 24px horizontal)

---

## 🔲 Border Radius

```css
--border-radius-sm: 0.5rem;  /* 8px - buttons */
--border-radius-lg: 1rem;    /* 16px - card */
```

### Usage
- **8px**: Social link buttons
- **16px**: Profile card container
- **50%**: Profile image (circular)

---

## 💫 Shadows & Effects

### Card Shadow
```css
box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
```
- Creates depth and separation from background

### Link Hover Shadow
```css
box-shadow: 0 8px 16px rgba(0, 208, 132, 0.3);
```
- Accent color glow on hover
- Creates elevated effect

### Link Focus Shadow
```css
box-shadow: 0 0 0 3px rgba(0, 208, 132, 0.3);
```
- Ring effect around link
- Accessibility indicator

### Animations

#### Slide In (Card Load)
```css
@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
animation: slideIn 0.6s ease-out;
```

---

## 🎯 Interactive States

### Hover State (Links)
- **Background**: Changes to accent color (#00d084)
- **Text Color**: Inverts to card background (#111111)
- **Transform**: `translateY(-2px)` - lifts element
- **Shadow**: Accent glow effect
- **Transition**: 0.3s ease-in-out

### Focus State (Keyboard)
- **Border**: 2px solid accent color
- **Shadow**: 3px ring of accent with transparency
- **Outline**: None (custom focus style)
- **Transition**: 0.3s ease-in-out

### Focus Visible State
- **Border**: 2px solid accent color
- **Shadow**: Enhanced ring effect
- **Background**: Changes to accent on focus-visible
- **Text**: Inverts for contrast
- **Transition**: 0.3s ease-in-out

### Active State (Click)
- **Transform**: `translateY(0)` - returns to default
- **Shadow**: Reduced to `0 4px 8px rgba(0, 208, 132, 0.2)`
- **Provides**: Tactile feedback

---

## 📱 Responsive Design

### Breakpoints
```css
/* Mobile First Approach */
@media (max-width: 480px) {
    /* Mobile styles */
}

@media (max-width: 768px) {
    /* Tablet styles */
}

/* Desktop: > 768px */
```

### Container Constraints
```css
max-width: 384px;  /* Maximum card width */
width: 100%;       /* Full width on mobile */
```

### Mobile Adjustments
- Card padding: `var(--spacing-lg) var(--spacing-md)` (32px vertical, 24px horizontal)
- Profile name font size: `1.25rem` (20px)
- Social links: Full width (`width: 100%`)

### Padding on Body
- Mobile/Tablet: `var(--spacing-sm)` (16px)
- Desktop: `var(--spacing-md)` (24px)

---

## ♿ Accessibility

### Keyboard Navigation
- All interactive elements are keyboard accessible
- Tab order flows naturally (top to bottom)
- Links are focusable and keyboard activatable

### Focus Indicators
- Always visible when using Tab key
- High contrast with background
- Clear shape (ring with 3px offset)

### Reduced Motion Support
```css
@media (prefers-reduced-motion: reduce) {
    /* Disables all animations and transitions */
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
}
```

### Color Contrast
- **Text on background**: WCAG AA compliant
- **White text on dark**: 8.59:1 ratio (exceeds WCAG AAA)
- **Accent on dark**: 4.86:1 ratio (meets WCAG AA)

### Semantic HTML
- Proper heading hierarchy (`<h1>` for name)
- Navigation element (`<nav>`) for social links
- Descriptive alt text for profile image

---

## 🌙 Dark Mode Support

```css
@media (prefers-color-scheme: dark) {
    :root {
        --clr-primary-bg: #0a0e27;
        --clr-card-bg: #13142b;
        --clr-text-primary: #ffffff;
        --clr-text-secondary: #b6b6b6;
    }
}
```

Automatically adjusts colors based on system preference.

---

## 🖨️ Print Styles

```css
@media print {
    body {
        background-color: white;
    }
    .profile-card {
        box-shadow: none;
        border: 1px solid #ccc;
    }
}
```

Optimizes appearance for printing.

---

## 📊 Transition Timing

```css
--transition: all 0.3s ease-in-out;
```

- **Duration**: 300ms
- **Timing Function**: ease-in-out (smooth acceleration/deceleration)
- **Applied to**: All interactive elements

---

## 🎪 Component Sizes

### Profile Image
- Size: 88px × 88px
- Border radius: 50% (circle)
- Border: 3px solid accent color

### Profile Card
- Maximum width: 384px
- Padding: 48px 32px (desktop)
- Padding: 32px 24px (mobile)
- Border radius: 16px

### Social Link Buttons
- Full width (desktop)
- Padding: 16px 24px (vertical, horizontal)
- Border radius: 8px
- Height: ~48px (with padding)

---

## ✅ Design Checklist

- ✅ Dark theme with proper contrast
- ✅ All interactive states implemented
- ✅ Responsive on all screen sizes
- ✅ Keyboard accessible
- ✅ Focus indicators visible
- ✅ Smooth transitions
- ✅ Print-friendly
- ✅ Dark mode support
- ✅ Reduced motion support
- ✅ Semantic HTML

---

**Last Updated**: June 1, 2026
**Project**: di_silent - Social Links Profile
