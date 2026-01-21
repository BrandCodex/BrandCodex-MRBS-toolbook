# Incorrect Examples (Anti-Patterns)

This directory contains examples of brand violations with explanations of what's wrong.

## Purpose

These examples help:
- AI agents recognize and avoid common mistakes
- Designers understand what NOT to do
- Validation tools identify violations

## Common Violations

### Color Violations

| Violation | Problem | Correct Approach |
|-----------|---------|------------------|
| Cyan text on white background | Fails contrast (1.4:1) | Use cyan only on dark backgrounds |
| Coral as primary accent | Overuse of secondary color | Coral ≤10% of design, cyan for primary accents |
| Cyan and coral adjacent | Visual clash | Separate with neutral space |
| Purple text on dark gray | Insufficient contrast | Use white or cyan for text on dark |

### Typography Violations

| Violation | Problem | Correct Approach |
|-----------|---------|------------------|
| Clash Display for body text | Display font for heroes only | Use Plus Jakarta Sans for body |
| System fonts | Missing brand personality | Install brand fonts |
| More than 3 font families | Visual noise | Stick to Clash, Plus Jakarta, JetBrains |
| Justified text | Uneven word spacing | Left-align body text |

### Logo Violations

| Violation | Problem | Correct Approach |
|-----------|---------|------------------|
| Logo on busy background | Poor readability | Solid or gradient background only |
| Rotated logo | Logo must be level | No rotation |
| Primary logo on dark | Wrong variant | Use reversed variant on dark backgrounds |
| Logo with added effects | No modifications allowed | Use original files only |

### Layout Violations

| Violation | Problem | Correct Approach |
|-----------|---------|------------------|
| Light theme as default | Brand is dark-first | Dark backgrounds primary |
| No cyan accents | Missing signature element | Include cyan highlights |
| Overcrowded slides | Content limits exceeded | Max 5 bullets, 12 words each |

## Example Metadata Format

Each incorrect example should document:

```yaml
violation:
  type: "color_contrast"
  rule_reference: "rules/accessibility.yaml#color_contrast"
  severity: "critical"
  explanation: "Cyan (#00FFD1) on white fails WCAG AA with only 1.4:1 contrast"
  correct_approach: "Use cyan only on dark backgrounds (primary, neutral-800, neutral-900)"
```

## Validation Mapping

| File Pattern | Rule Reference |
|--------------|----------------|
| `*-contrast-fail.*` | `rules/accessibility.yaml#color_contrast` |
| `*-wrong-font.*` | `rules/constraints.yaml#typography` |
| `*-logo-*` | `rules/constraints.yaml#logo` |
| `*-color-clash.*` | `visual/colors.tokens.json#pairing` |

## Note

These examples exist to teach what to avoid. **Never use these as templates!**
