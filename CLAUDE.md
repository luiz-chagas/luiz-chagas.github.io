# luiz-website

Personal website for Luiz Chagas — luizchagas.com.

## Tech Stack

- Plain HTML + CSS, minimal JavaScript (clock, window close easter eggs)
- Deployed via GitHub Pages from the `main` branch root
- Custom domain via `CNAME`

## Design System: Windows 98/XP Theme

### Colors
| Token | Value | Usage |
|---|---|---|
| `--desktop-bg` | `#008080` | Teal desktop background |
| `--window-bg` | `#c0c0c0` | Window and button face |
| `--titlebar-start` | `#000080` | Title bar gradient start |
| `--titlebar-end` | `#1084d0` | Title bar gradient end |
| `--titlebar-text` | `#ffffff` | Title bar text/icons |
| `--window-body-bg` | `#ffffff` | Window content area |
| `--border-light` | `#ffffff` | 3D border highlight (top/left) |
| `--border-dark` | `#808080` | 3D border shadow (bottom/right) |
| `--border-darker` | `#404040` | Outer shadow border |
| `--text` | `#000000` | Body text |

### Typography
- Font family: `Tahoma, Arial, sans-serif`
- Base size: `11px` (Win98/XP default UI size)
- Window title: `12px bold`

### Component Classes
| Class | Description |
|---|---|
| `.desktop` | Full-viewport teal background; contains windows and taskbar |
| `.window` | Raised 3D box with classic Win9x border styling |
| `.title-bar` | Window title bar with gradient, icon, title text, control buttons |
| `.title-bar-controls` | Container for min/max/close buttons |
| `.window-body` | White content area inside a window |
| `.taskbar` | Fixed bottom bar with Start button |
| `.field-row` | Label + input row inside windows |
| `.tree-view` | Explorer-style list with indentation |

### 3D Border Technique
Win98-style raised border uses 4 border colors:
```css
border-top: 2px solid #ffffff;
border-left: 2px solid #ffffff;
border-bottom: 2px solid #404040;
border-right: 2px solid #404040;
outline: 1px solid #808080; /* inner shadow */
```

## File Structure
```
├── index.html          # Desktop + all content windows
├── css/style.css       # Windows 98/XP theme
├── assets/             # Images (luiz.png, bliss.png)
├── CNAME               # luizchagas.com
├── sitemap.xml
├── robots.txt
└── CLAUDE.md
```

## Content

All copy lives in `index.html` (no build step, no CMS).

- **Bio**: Staff Engineer at Crema, 10+ years, AWS SAA, technical leadership + hands-on dev
- **Work**: Crema (Staff Engineer, DoE, Sr. App Dev, App Dev), Freelance, RHI Magnesita, CEFET-MG
- **Projects**: Vera Plant Care App, Stock Info NPM package
- **Education**: B.S. Computer Engineering CEFET-MG, Exchange Kansas State, Associate's CEFET-MG
- **Certifications**: AWS Certified Solutions Architect (2024)
- **Contact**: luiz@luizchagas.com, GitHub, LinkedIn

## Deployment

Push to `main`. GitHub Pages serves the repo root. Site: https://luizchagas.com

After deploy, submit the sitemap in [Google Search Console](https://search.google.com/search-console) (property: `luizchagas.com`, sitemap URL: `https://luizchagas.com/sitemap.xml`).
