# Custom Graphics & Visual Elements Guide

This document provides guidance on creating and customizing visual elements for your GitHub profile landing page.

## Table of Contents
- [Banner Images](#banner-images)
- [Custom Badges](#custom-badges)
- [Progress Bars](#progress-bars)
- [Mermaid Diagrams](#mermaid-diagrams)
- [Using Custom SVGs](#using-custom-svgs)
- [Recommended Tools](#recommended-tools)

## Banner Images

### Using Capsule Render

Your README uses [Capsule Render](https://github.com/kyechan99/capsule-render) for the header and footer banners. You can customize these by modifying the URL parameters:

```markdown
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=200&section=header&text=Your%20Text&fontSize=40&fontAlignY=40&animation=fadeIn" />
```

Parameters you can modify:
- `type`: waving, slice, egg, shark, cylinder, soft, transparent, rect
- `color`: Auto, gradient, timeGradient, or specific colors (0a0c10, f7f9fb)
- `height`: Height in pixels
- `text`: The text to display (use %20 for spaces)
- `animation`: fadeIn, blink, twinkling, scaleIn
- `fontColor`: Text color hex code
- `fontSize`: Text size in pixels

Visit the [Capsule Render GitHub page](https://github.com/kyechan99/capsule-render) for more customization options.

## Custom Badges

### Using Shields.io

Shields.io provides customizable badges for various purposes:

```markdown
![Label](https://img.shields.io/badge/Label-Message-Color?style=style&logo=logoname&logoColor=logoColor)
```

Parameters:
- `Label`: Left side text
- `Message`: Right side text
- `Color`: Background color (e.g., blue, green, red, or hex code like 4c1)
- `style`: plastic, flat, flat-square, for-the-badge, social
- `logo`: Name of a supported logo (see [Simple Icons](https://simpleicons.org/))
- `logoColor`: Color of the logo

### Examples

Technology badge:
```markdown
![Python](https://img.shields.io/badge/Python-Expert-3776AB?style=flat-square&logo=python)
```

Custom status badge:
```markdown
![Status](https://img.shields.io/badge/Status-Available-success)
```

## Progress Bars

### Using progress-bar.dev

Your skills section uses progress bars from progress-bar.dev:

```markdown
<img src="https://progress-bar.dev/95/?width=100&title=Skill" alt="Skill 95%">
```

Parameters:
- The number after the slash is the percentage (0-100)
- `width`: Width in pixels
- `title`: Text displayed before the bar
- `color`: Color (default, red, blue, green, etc.)

## Mermaid Diagrams

GitHub natively supports Mermaid diagrams, which you can use to create visual representations:

### Mindmap Example

```markdown
```mermaid
mindmap
  root((Main Concept))
    Area 1
      Subarea 1
      Subarea 2
    Area 2
      Subarea 3
      Subarea 4
```
```

### Flowchart Example

```markdown
```mermaid
flowchart TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Process]
    B -->|No| D[Skip]
    C --> E[End]
    D --> E
```
```

## Using Custom SVGs

For truly unique visual elements, you can create custom SVGs:

1. Create an SVG file using Inkscape, Adobe Illustrator, or another tool
2. Save it to the `/assets` folder in your repository
3. Reference it in your README:

```markdown
<img src="./assets/your-custom-graphic.svg" width="800" alt="Custom graphic" />
```

For animation effects, you can edit the SVG code directly to add CSS animations.

## Recommended Tools

### Banner Creation
- [Capsule Render](https://github.com/kyechan99/capsule-render) - Dynamic GitHub profile header images
- [Canva](https://www.canva.com/) - Easy design tool for custom graphics

### Badge Creation
- [Shields.io](https://shields.io/) - Concise, consistent, and legible badges
- [Simple Icons](https://simpleicons.org/) - Find icon names for use with Shields.io

### Diagram Creation
- [Mermaid Live Editor](https://mermaid.live/) - Create and test Mermaid diagrams
- [Excalidraw](https://excalidraw.com/) - Hand-drawn style diagrams

### SVG Tools
- [Inkscape](https://inkscape.org/) - Free vector graphics editor
- [SVGOMG](https://jakearchibald.github.io/svgomg/) - Optimize SVGs for web use

### Other Visualization Tools
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats) - Dynamically generated GitHub stats
- [GitHub Profile Trophy](https://github.com/ryo-ma/github-profile-trophy) - Add trophy showcase to GitHub profile

---

Remember that visual elements should enhance your profile's readability and professionalism, not distract from it. Aim for a consistent style that represents your personal brand.
