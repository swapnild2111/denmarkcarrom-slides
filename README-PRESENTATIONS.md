# Denmark Carrom Federation - Presentation Setup Guide

## 📁 Project Structure

```
denmarkcarrom-slides/
├── index.html                 # Main landing page
├── css/
│   ├── styles.css            # Landing page styles
│   └── reveal-responsive.css # Shared responsive styles for all presentations
├── assets/
│   ├── favicon-32x32.svg     # Favicon
│   ├── dkcf-logo.png         # DKCF logo
│   └── carrom_bw.jpeg        # Carrom image
├── slides/
│   ├── dkcf-intro/           # DKCF introduction presentation
│   └── carrom-beginner/      # Carrom beginner guide presentation
└── templates/
    ├── presentation-template.html # HTML template for new presentations
    └── presentation-template.md   # Markdown template for content
```

## 🆕 Creating a New Presentation

### Step 1: Set Up New Presentation

```bash
# From the project root, create your presentation folder:
mkdir slides/your-new-presentation
mkdir slides/your-new-presentation/slides

# Copy the HTML template:
cp templates/presentation-template.html slides/your-new-presentation/index.html

# Copy the Markdown template:
cp templates/presentation-template.md slides/your-new-presentation/slides/intro.md
```

### Step 2: Customize HTML File

1. Open `slides/your-new-presentation/index.html`
2. Change the title: `<title>Your Title - Denmark Carrom Federation</title>`
3. The shared responsive styles are automatically included
4. No other changes needed - the HTML is ready to use!

### Step 3: Create Your Content

1. Edit `slides/your-new-presentation/slides/intro.md` with your presentation content
2. Use `---` for horizontal slides (main sections)
3. Use `--` for vertical slides (subsections within a topic)
4. Follow the template structure for consistency

### Step 4: Add to Main Page

Update the main `index.html` to include your new presentation card.

## 🎨 Shared Responsive Styles

All presentations automatically inherit these responsive behaviors:

### 📱 Mobile Devices (≤ 768px)

- H1: 1.6em
- H2: 1.2em
- H3: 1.0em
- P/Li: 0.7em with 1.4 line-height
- 20px padding, 95% max-width for lists

### 📱 Small Mobile (≤ 480px)

- H1: 1.5em
- P/Li: 0.8em (slightly larger for readability)
- 15px padding

### 📱 Ultra-Small (≤ 460px)

- Base font-size: 28px
- Full width/height slides
- 10px padding
- 3px progress bar height

## ✨ Features Included

- ✅ **Responsive design** for all screen sizes
- ✅ **Touch navigation** for mobile devices
- ✅ **Consistent serif theme** across all presentations
- ✅ **Favicon** integration
- ✅ **Vertical slides** support with `--` separators
- ✅ **Navigation arrows** optimized for different devices
- ✅ **Progress bar** and controls

## 🛠️ Customization

### Adding Presentation-Specific Styles

Add custom styles in the `<style>` section of your presentation's `index.html`:

```css
<style>
/* Add any custom styles specific to this presentation here */
.custom-class {
    color: red;
}
</style>
```

### Modifying Shared Styles

Edit `/css/reveal-responsive.css` to change styles that affect ALL presentations.

## 📋 Best Practices

1. **Use the Markdown template** - start with `templates/presentation-template.md`
2. **Keep presentations consistent** - follow the template structure
3. **Test on multiple devices** - especially mobile
4. **Keep slide content concise** for mobile readability
5. **Use vertical slides (`--`)** to organize related content
6. **Include emojis** to make content more engaging
7. **Test navigation** - both horizontal and vertical slides

## 🔧 Troubleshooting

- **Styles not loading?** Check the path to `../../css/reveal-responsive.css`
- **Mobile issues?** Ensure viewport meta tag is correct
- **Navigation problems?** Verify reveal.js configuration settings
- **Font too large/small?** Check the responsive breakpoints in shared CSS

---

_This structure ensures all DKCF presentations maintain consistency while being easy to maintain and extend._
