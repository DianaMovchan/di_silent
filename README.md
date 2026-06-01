# Social Links Profile - di_silent

A modern, responsive social links profile card built with HTML and CSS. This project showcases a clean, dark-themed profile design with interactive social media links featuring smooth hover and focus states for accessibility.

## 🎯 Project Overview

The **Social Links Profile** is a Frontend Mentor challenge designed to practice:
- Semantic HTML structure
- Modern CSS styling and animations
- Accessibility best practices (hover and focus states)
- Responsive design for all screen sizes
- User interaction feedback

## ✨ Features

✅ **Responsive Design** - Works seamlessly on mobile, tablet, and desktop
✅ **Interactive Elements** - Smooth hover and focus states on all links
✅ **Accessibility First** - Keyboard navigation and focus indicators
✅ **Dark Mode Support** - Follows system preferences
✅ **Performance Optimized** - Minimal CSS, no JavaScript required
✅ **Reduced Motion Support** - Respects user's motion preferences
✅ **SEO Friendly** - Semantic HTML markup

## 🚀 Quick Start

1. **Clone the Repository**
   ```bash
   git clone https://github.com/DianaMovchan/di_silent.git
   cd di_silent
   ```

2. **Open in Browser**
   - Simply open `index.html` in your favorite browser
   - Or use a local server:
     ```bash
     npx http-server
     # or
     python -m http.server 8000
     ```

3. **Customize**
   - Edit `index.html` to add your information
   - Modify `styles.css` to match your brand colors
   - Replace profile image at `./assets/avatar.jpg`

## 📁 Project Structure

```
di_silent/
├── index.html          # Main HTML file
├── styles.css          # CSS styling with animations
├── style-guide.md      # Design specifications
├── README.md           # This file
└── assets/
    └── avatar.jpg      # Profile image
```

## 🎨 Customization

### Update Profile Information

Edit the following in `index.html`:
```html
<h1 class="profile-name">Your Name</h1>
<p class="profile-location">Your Location</p>
<p class="profile-bio">Your Bio or Quote</p>
```

### Update Social Links

Modify the links to point to your profiles:
```html
<a href="your-github-url" class="social-link">GitHub</a>
<a href="your-linkedin-url" class="social-link">LinkedIn</a>
```

### Customize Colors

Edit CSS variables in `styles.css`:
```css
:root {
    --clr-accent: #00d084;
    --clr-card-bg: #111111;
    --clr-text-primary: #ffffff;
    /* ... more colors */
}
```

## 📱 Responsive Breakpoints

- **Mobile**: < 480px
- **Tablet**: 480px - 768px
- **Desktop**: > 768px

The card maintains a max-width of 384px for optimal readability.

## ♿ Accessibility Features

- **Keyboard Navigation**: All links are fully keyboard accessible
- **Focus Indicators**: Clear visual feedback when using Tab key
- **Focus Visible**: Enhanced focus styling for keyboard users
- **Semantic HTML**: Proper heading hierarchy and nav elements
- **Reduced Motion**: Respects `prefers-reduced-motion` setting
- **Color Contrast**: WCAG AA compliant contrast ratios

## 🎮 Interactive States

### Hover State
- Background color changes to accent color
- Text color inverts for contrast
- Subtle elevation effect (translateY)
- Glow shadow effect

### Focus State
- Clear 3px outline in accent color
- Background and text color transitions
- Works with keyboard navigation (Tab key)

### Active State
- Quick, responsive button press effect
- Reduced shadow for tactile feedback

## 🖼️ Design Specifications

See `style-guide.md` for:
- Color palette
- Typography
- Spacing system
- Border radius values
- Transition timings

## 🔧 Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with variables and media queries
- **No Dependencies** - Pure HTML and CSS, no frameworks or libraries

## 📊 Browser Support

- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🚢 Deployment

Deploy to any static hosting service:

### GitHub Pages
```bash
# Push to main branch, then enable GitHub Pages in repository settings
```

### Vercel
```bash
vercel
```

### Netlify
```bash
netlify deploy --prod --dir=.
```

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Frontend Mentor** - Original challenge design and specifications
- Icons and design inspiration from the Frontend Mentor community

## 💬 Feedback & Support

Have suggestions or found a bug? Open an issue on GitHub!

---

**Happy coding! 🎉**

Made with ❤️ by Diana Movchan
