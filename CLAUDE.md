# luiz-website

Personal website for Luiz Chagas — a new version of luizchagas.com.

## Tech Stack

- Plain HTML + CSS, no build tools, no frameworks, no JavaScript (unless minimal)
- Deployed via GitHub Pages from the `main` branch root
- `.nojekyll` present to skip Jekyll processing

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
luiz-website/
├── index.html          # Desktop + all content windows
├── css/
│   └── style.css       # Windows 98/XP theme
├── assets/
│   └── icons/          # Window/desktop icons (SVG or PNG)
├── CLAUDE.md           # This file
└── .nojekyll           # GitHub Pages: skip Jekyll
```

## Content (sourced from luizchagas.com)
- **Bio**: Software developer, ~7 years experience, full-stack JavaScript, functional programming focus
- **Work**: Crema (Sr. App Dev Dec 2019–, App Dev Nov 2018–Dec 2019), Self-Employed (Jan 2017–Nov 2018)
- **Projects**: Vera Plant Care App, Stock Info NPM package
- **Education**: Computer Engineering CEFET-MG, Exchange Kansas State, Associate's CEFET-MG
- **Contact**: luiz@luizchagas.com, GitHub, LinkedIn, Twitter

## Deployment
Push to `main` branch. Enable GitHub Pages in repo Settings > Pages > Source: main branch / root.
Site will be available at `https://luiz-chagas.github.io/luiz-website/` (or custom domain).
