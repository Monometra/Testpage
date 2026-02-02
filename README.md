# KARIO Media - Panel Digital

A complete, responsive **pure HTML and CSS** web application that reproduces the KARIO Media interface with animated intro sequence and interactive dashboard.

## Features

- **No JavaScript** - All animations, transitions, and page navigation are done purely with CSS
- **Animated Intro Sequence** - Logo animations, login page, and welcome card transitions
- **Interactive Dashboard** - Clickable navigation using CSS `:checked` and `:target` selectors
- **Responsive Design** - Works on desktop, tablet, and mobile devices
- **Modern UI** - Clean design with white cards, shadows, and orange accent color

## Animation Flow

1. **First Logo** - KARIO logo fades in on dark stadium background
2. **Fade Out** - Logo fades to black
3. **Second Logo** - Logo reappears
4. **Login Page** - Login card with username/password fields
5. **Welcome Card** - User profile welcome screen after login
6. **Third Logo** - Final logo transition
7. **Dashboard** - Main application dashboard appears

## Pages & Interactions

- **Dashboard** - Main indicators panel with data table
- **Añadir** - Form to add new indicators
- **Refrescar** - Shows refresh confirmation message
- **Eliminar** - Toggle delete mode (changes row icons to red X)
- **Reportar** - Reports page with CSS-only bar charts
- **Ayuda** - FAQ page with expandable `<details>` elements
- **Configuración** - Settings page with toggle switches
- **Notificaciones** - Dropdown notification panel

## Project Structure

```
PageTest/
├── index.html          # Main HTML file
├── README.md           # This file
├── css/
│   ├── styles.css      # Base styles, variables, typography
│   ├── animations.css  # Keyframes and intro sequence
│   ├── dashboard.css   # Navbar, table, dashboard layout
│   └── pages.css       # Add, Report, Help, Settings pages
└── media/
    ├── icon-kairo.svg          # Main logo
    ├── background.png          # Stadium background
    ├── background@2.png        # Alt background
    ├── pfp.png                 # Small profile picture
    ├── pfp@2x.png              # Large profile picture
    ├── add_icon.svg            # Add icon
    ├── refresh-icon.svg        # Refresh icon
    ├── delete-icon.svg         # Delete icon
    ├── reportar-icon.svg       # Report icon
    ├── notifications.icon.svg  # Bell icon
    ├── settings.icon.svg       # Gear icon
    ├── move-grab.svg           # Move/grab icon
    ├── move-grab2.svg          # Alt move icon
    └── X-red-icon.png          # Red X delete icon
```

## How It Works

### Navigation (CSS-only)
Hidden radio buttons control which page is visible:
```css
#nav-dashboard:checked ~ .dashboard-wrapper .page-dashboard { display: block; }
#nav-add:checked ~ .dashboard-wrapper .page-add { display: block; }
```

### Delete Mode
A hidden checkbox toggles delete mode styling:
```css
#delete-mode:checked ~ .dashboard-wrapper .action-delete { display: inline-block; }
#delete-mode:checked ~ .dashboard-wrapper .action-move { display: none; }
```

### Intro Animation Timing
CSS `animation-delay` creates the sequential intro:
```css
.intro-logo-1 { animation: fadeInScale 0.8s ease-out 0.3s forwards; }
.intro-login { animation: fadeIn 0.6s ease-out 4.5s forwards; }
.app-container { animation: fadeIn 0.8s ease-out 12s forwards; }
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Usage

Simply open `index.html` in a web browser. No build process or server required.

## License

© KARIO Media - All Rights Reserved