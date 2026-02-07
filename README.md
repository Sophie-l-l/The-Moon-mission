# The Moon Mission — Animated Narrative Website

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![jQuery](https://img.shields.io/badge/jQuery-3.7-0769AD?style=for-the-badge&logo=jquery&logoColor=white)](https://jquery.com/)

**The Moon Mission** is an animated horror/dream-themed narrative webpage with scroll-triggered animations, interactive SVG graphics (cat with clickable tail, color-changing fire), and dynamic theme switching between cute and dark modes based on scroll direction.

**Related Project:** [Interactive Comic](https://ds7363.github.io/interactivecomic/)

---

## Key Achievements

- **Situation**: Wanted to explore the boundaries of scroll-based storytelling and create an interactive narrative that changes mood dynamically
- **Task**: Build an animated webpage that uses scroll direction to drive theme changes, SVG interactions, and visual storytelling
- **Action**:
  - Created a **dynamic SVG fire graphic** with gradient colors that shift based on scroll position — computed in real-time using RGB interpolation
  - Built a **hand parallax animation** with scroll-linked opacity fading for cinematic depth
  - Implemented **bi-directional scroll detection** for theme switching — scrolling down triggers a dark/horror theme, scrolling up returns to a cute theme
  - Designed an **interactive SVG cat** with clickable tail toggle between two visual states
  - Integrated **AOS (Animate On Scroll)** library for entrance animations and **jQuery** for DOM manipulation
- **Result**: A creative, technically ambitious narrative webpage demonstrating advanced scroll-based interactions, SVG animation, and dynamic theming

---

## Features

- **Scroll-Based Theme Switching** — Dark/horror theme on scroll-down, cute theme on scroll-up
- **Dynamic SVG Fire** — Gradient color changes in real-time based on scroll position (RGB interpolation)
- **Hand Parallax** — Scroll-linked opacity fading with parallax depth effect
- **Interactive SVG Cat** — Clickable tail toggles between two visual states
- **AOS Animations** — Fade-in, slide, and zoom entrance effects triggered by scroll position
- **Responsive Layout** — Adapts to different screen sizes

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Structure** | HTML5, SVG graphics |
| **Styling** | CSS3 (gradients, transitions, transforms) |
| **Interactivity** | JavaScript, jQuery 3.7 |
| **Animations** | AOS (Animate On Scroll) library |
| **SVG** | Hand-crafted SVG with dynamic gradient manipulation |

---

## How It Works

### Dynamic SVG Gradient
The fire's color changes based on scroll position using real-time RGB calculation:

```javascript
function calculateStopColor(scrollRatio) {
    const r = Math.round(255 - scrollRatio * 100);
    const g = Math.round(165 - scrollRatio * 165);
    const b = Math.round(scrollRatio * 50);
    return `rgb(${r}, ${g}, ${b})`;
}
```

### Theme Switching
Scroll direction detection drives CSS class swaps between theme objects:

```javascript
const horrorTheme = { fontFamily: 'Creepster', color: '#8B0000', background: '#1a1a1a' };
const cuteTheme   = { fontFamily: 'Comic Sans MS', color: '#FF69B4', background: '#FFF0F5' };
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/Sophie-l-l/The-Moon-mission.git
cd The-Moon-mission

# Open in browser (no build step required)
open index.html
```

No dependencies to install — jQuery and AOS are loaded via CDN.

---

## Skills Demonstrated

SVG animation and manipulation, scroll-based interactions, dynamic theming, jQuery, CSS transitions and gradients, creative web design, interactive storytelling, real-time color computation

---

## License

This project is licensed under the Unlicense. See the [LICENSE](LICENSE) file for details.
