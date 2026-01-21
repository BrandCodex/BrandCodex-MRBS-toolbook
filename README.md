# Brandcodex Brand System

[![MRBS Version](https://img.shields.io/badge/MRBS-v1.0.0-00FFD1)](https://github.com/MRBSystem/MRBS-Specification)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](./LICENSE)

**The official brand identity for Brandcodex — The Index of Machine-Readable Identities**

This repository contains the complete, MRBS-compliant brand system for Brandcodex. It serves as both the authoritative source of truth for Brandcodex brand identity AND as a reference implementation of the MRBS specification.

---

## Quick Reference

### Brand Essence

**Brandcodex** bridges the ancient concept of a codex (structured knowledge) with modern code (machine-executable instructions). We make brand identity accessible to AI agents.

### Visual Identity at a Glance

| Element | Value | Usage |
|---------|-------|-------|
| **Primary Color** | `#2D1B69` (Codex Purple) | Backgrounds, headers, brand elements |
| **Accent 1** | `#00FFD1` (Code Mint) | Links, highlights, interactive elements |
| **Accent 2** | `#FF7A5C` (Human Coral) | Secondary accents, warmth (≤10%) |
| **Display Font** | Clash Display | Hero headlines only |
| **Heading Font** | Plus Jakarta Sans | Headings, buttons, UI |
| **Body Font** | Plus Jakarta Sans | Body text, descriptions |
| **Code Font** | JetBrains Mono | Code, technical content |

### Voice Quick Guide

- **Authoritative yet accessible** — We're experts who explain clearly
- **Technical yet human** — Code-native but never cold
- **Precise yet engaging** — Exact specifications, readable prose

---

## Repository Structure

```
brandcodex-mrbs/
├── brand.manifest.json          # Entry point — AI reads this first
├── identity/
│   ├── brand-values.yaml        # Mission, vision, personality
│   ├── voice-tone.yaml          # Writing guidelines by context
│   └── naming.yaml              # Naming conventions
├── visual/
│   ├── colors.tokens.json       # Color palette + usage rules
│   ├── typography.tokens.json   # Fonts, scales, rules
│   ├── spacing.tokens.json      # Spacing system
│   └── effects.tokens.json      # Shadows, radius, transitions
├── assets/
│   └── logos/
│       └── manifest.json        # Logo variants + usage rules
├── templates/
│   └── presentation/
│       └── manifest.json        # Slide layouts + constraints
├── rules/
│   ├── constraints.yaml         # Do's and don'ts
│   ├── accessibility.yaml       # WCAG requirements
│   └── legal.yaml               # Trademark, copyright
└── examples/
    ├── correct/                 # Approved examples
    └── incorrect/               # Anti-patterns with explanations
```

---

## For AI Agents

### Quick Integration

```markdown
## Brand Context

Follow Brandcodex brand guidelines:

### Colors
- Primary: #2D1B69 (dark backgrounds, headers)
- Accent: #00FFD1 (links, highlights — dark bg only)
- Secondary: #FF7A5C (warmth accents, ≤10%)

### Typography
- Heroes: Clash Display (600-700)
- Headings: Plus Jakarta Sans (500-800)
- Body: Plus Jakarta Sans (400-600)
- Code: JetBrains Mono

### Voice
- Authoritative yet accessible
- Technical yet human
- Define terms, never assume

### Key Rules
- Dark backgrounds primary
- Cyan never on light backgrounds (fails contrast)
- One idea per slide, max 5 bullets
```

### MCP Access

```typescript
// Resource URIs
"brand://brandcodex.org/manifest"
"brand://brandcodex.org/colors"
"brand://brandcodex.org/typography"
"brand://brandcodex.org/voice/professional"
"brand://brandcodex.org/constraints"
```

### Priority Order

When guidelines conflict, follow this order:
1. **Rules** (constraints, accessibility)
2. **Visual** (colors, typography)
3. **Identity** (voice, values)
4. **Templates** (layouts, zones)

---

## Key Brand Principles

### 1. Dark-First Design

Brandcodex embraces dark themes as primary. The deep Codex Purple creates atmosphere and allows our signature cyan accents to glow.

```
✓ Dark backgrounds (primary, neutral-900)
✓ Light text (#FFFFFF, neutral-100)
✓ Cyan accents that pop
✗ Light backgrounds as default
```

### 2. Precision Through Structure

Like the codex we're named after, everything is organized and intentional. Structured data, clear hierarchies, semantic tokens.

### 3. Bridging Human and Machine

Our coral accent represents the human side of branding — warmth, creativity, approachability. It balances the technical cyan.

### 4. Accessibility as Foundation

We make brand identity accessible to AI agents. That mission starts with making it accessible to humans of all abilities. WCAG AA minimum.

---

## Color Philosophy

| Color | Name | Role | Usage |
|-------|------|------|-------|
| `#2D1B69` | Codex Purple | Brand Identity | Backgrounds, headers, depth |
| `#00FFD1` | Code Mint | Machine Interface | Links, code, highlights, AI elements |
| `#FF7A5C` | Human Coral | Human Warmth | Secondary accents, notifications |

The palette tells our story:
- **Purple** is the binding of the codex — structured, authoritative, deep
- **Cyan** is the code — machine-readable, precise, electric
- **Coral** is the human — warm, creative, approachable

---

## Typography System

### Three-Tier Hierarchy

1. **Display** (Clash Display) — For moments of maximum impact
   - Hero headlines
   - Brand statements
   - Section openers in presentations
   
2. **Heading** (Plus Jakarta Sans, 500-800) — For structure
   - Page titles
   - Section headings
   - Navigation
   - Buttons
   
3. **Body** (Plus Jakarta Sans, 400-600) — For content
   - Paragraphs
   - Descriptions
   - UI text

4. **Code** (JetBrains Mono) — For technical content
   - Code snippets
   - File paths
   - MCP URIs
   - JSON/YAML examples

---

## Usage Guidelines

### Do

- ✓ Use dark backgrounds as primary
- ✓ Let cyan accents glow on dark surfaces
- ✓ Use Clash Display sparingly for impact
- ✓ Define technical terms on first use
- ✓ Validate color contrast (WCAG AA)
- ✓ Use semantic color roles (not just values)

### Don't

- ✗ Use cyan text on light backgrounds (fails contrast)
- ✗ Place coral adjacent to cyan (visual clash)
- ✗ Use Clash Display for body text
- ✗ Use more than 3 font families
- ✗ Justify body text
- ✗ Skip heading hierarchy levels

---

## Files Reference

| File | Purpose |
|------|---------|
| `brand.manifest.json` | Entry point, paths to all components |
| `visual/colors.tokens.json` | Complete color system with usage rules |
| `visual/typography.tokens.json` | Fonts, scales, presentation typography |
| `identity/voice-tone.yaml` | Writing guidelines by context |
| `rules/constraints.yaml` | Visual do's and don'ts |
| `rules/accessibility.yaml` | WCAG compliance requirements |
| `assets/logos/manifest.json` | Logo variants and usage rules |

---

## License

This brand system is licensed under [Apache 2.0](./LICENSE).

The Brandcodex name and logo are trademarks of Brandcodex Foundation. The MRBS specification is open source and free to implement.

---

## About MRBS

This brand system is built on the [Machine-Readable Brand System (MRBS)](https://github.com/MRBSystem/MRBS-Specification) specification — an open standard for AI-ready brand identity systems.

MRBS enables:
- AI agents to create brand-compliant content autonomously
- Validation tools to check compliance programmatically
- Design systems to consume tokens directly
- Multiple platforms to share a single source of truth

---

<p align="center">
  <strong>Brandcodex — The Index of Machine-Readable Identities</strong><br>
  <a href="https://brandcodex.org">brandcodex.org</a>
</p>
