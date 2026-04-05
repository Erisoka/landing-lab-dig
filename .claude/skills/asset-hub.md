# Asset Hub — Project Skill

## Overview

The Asset Hub is an internal service for generating real digital assets using **Gemini 2.5 Flash Image (Image generation 4)** from Google Cloud.

## Location

```
C:\Users\usuario\OneDrive\Documentos\2026\Leo\Proyectos\Asset Hub\cli.js
```

## CLI Command

```bash
node "C:\Users\usuario\OneDrive\Documentos\2026\Leo\Proyectos\Asset Hub\cli.js" image "<PROMPT_EN_INGLES_DETALLADO>" "<NOMBRE_DEL_ARCHIVO>"
```

## Mandatory Workflow

1. **Execute** the CLI command in terminal
2. **Asset Hub saves** image to its internal folder:
   ```
   C:\Users\usuario\OneDrive\Documentos\2026\Leo\Proyectos\Asset Hub\assets\images\<NOMBRE_DEL_ARCHIVO>.png
   ```
3. **Copy/move** the file to the Astro project's `src/assets/` folder using terminal commands
4. **Integrate** the image path in Astro components (use `import` or `astro:assets` for optimization)

## Image Requirements for landing-v1

| Image Name | Purpose | Component |
|------------|---------|-----------|
| `hero-mockup` | Hero section dashboard mockup | Hero.astro |
| `maker-lab-image` | Maker Lab banner image | MakerLab.astro |
| `class-preview-img` | Class preview card visual | ClassPreview.astro |
| `og-image` | Open Graph social sharing image | Layout.astro |

## Notes

- Prompts MUST be in **English** for best results with Gemini
- Be detailed in prompts: style, mood, colors, composition, resolution
- Asset Hub handles Google Cloud authentication internally
- Images are generated in PNG format, optimized at 4K

## Quick Test

```bash
node "C:\Users\usuario\OneDrive\Documentos\2026\Leo\Proyectos\Asset Hub\cli.js" image "A modern hero section background for a digital lab, dark mode, 4k, neon blue accents" "hero-bg"
```
