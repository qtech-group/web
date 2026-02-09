# QTech Group Email Signature Design System

## Version 1.0 | February 2025

---

## Table of Contents

1. [Design Principles](#1-design-principles)
2. [Visual Identity](#2-visual-identity)
3. [Typography](#3-typography)
4. [Layout & Spacing](#4-layout--spacing)
5. [Color System](#5-color-system)
6. [Logo Usage](#6-logo-usage)
7. [Iconography](#7-iconography)
8. [Content Guidelines](#8-content-guidelines)
9. [Legal & Compliance](#9-legal--compliance)
10. [Technical Specifications](#10-technical-specifications)
11. [Implementation](#11-implementation)
12. [Version Control](#12-version-control)

---

## 1. Design Principles

### Core Philosophy

| Principle | Application |
|-----------|-------------|
| **Legibility First** | All text must be readable at default email client zoom levels |
| **Legal Defensibility** | Every element serves compliance or risk mitigation |
| **Scalability** | System works for 1 or 100 staff without degradation |
| **Client Confidence** | Professional appearance builds construction sector trust |
| **Technical Resilience** | Renders correctly across all major email platforms |

### Design Constraints

```
Constraint: Email clients strip CSS
Response: Use table-based layouts with inline styles

Constraint: Dark mode inversion
Response: Tested white-background variant with dark accents

Constraint: Mobile viewport limitations
Response: Max-width 600px, single-column stacking ready

Constraint: Image blocking
Response: Critical information in HTML text, images decorative only

Constraint: Legal liability exposure
Response: Comprehensive disclaimer architecture
```

---

## 2. Visual Identity

### Signature Architecture

```
┌─────────────────────────────────────────────────────────┐
│  ┌─────────┐  ┌──────────────────────────────────────┐  │
│  │         │  │  QTECH GROUP                         │  │
│  │  LOGO   │  │  ───────────                         │  │
│  │  160px  │  │  Full Name                           │  │
│  │  square │  │  Job Title                           │  │
│  │         │  │                                      │  │
│  │ #0D0D0D │  │  Services Line                       │  │
│  │ bg      │  │                                      │  │
│  │         │  │  📞 Phone                            │  │
│  │         │  │  ✉ Email                             │  │
│  │         │  │  🌐 Website                          │  │
│  │         │  │  📍 Location                         │  │
│  └─────────┘  └──────────────────────────────────────┘  │
│  ↑ Dark panel    ↑ White content area                   │
│       ↑ 3px gold divider                               │
├─────────────────────────────────────────────────────────┤
│  Legal disclaimer (9px, justified, muted)               │
└─────────────────────────────────────────────────────────┘
        ↓ Max 600px total width
```

### Signature Variants

| Variant | Use Case | Complexity | Disclaimer |
|---------|----------|------------|------------|
| **Executive** | C-suite, external client communication | Full | Complete |
| **Standard** | Management, professional staff | Full | Complete |
| **Compact** | Site staff, mobile, internal | Reduced | Abbreviated |
| **Plain Text** | Replies, forwards, compatibility | Minimal | Required text only |

---

## 3. Typography

### Font Stack

```
Primary Design Font: Montserrat
Fallback Stack: Arial, Helvetica, sans-serif

Rationale:
- Montserrat conveys modern engineering precision
- Arial has 99%+ email client availability
- Sans-serif ensures screen readability
```

### Type Scale

| Element | Size | Weight | Case | Color | Line Height |
|---------|------|--------|------|-------|-------------|
| Company Name | 20px | Bold (700) | UPPERCASE | #0D0D0D | 1.2 |
| Full Name | 16px | Bold (700) | Title Case | #0D0D0D | 1.3 |
| Job Title | 13px | Regular (400) | UPPERCASE | #666666 | 1.4 |
| Services | 11px | Medium (500) | UPPERCASE | #888888 | 1.6 |
| Contact Info | 12px | Regular (400) | Sentence | #333333 | 1.8 |
| Disclaimer | 9px | Regular (400) | Sentence | #777777 | 1.5 |

### Letter Spacing

| Element | Tracking | Rationale |
|---------|----------|-----------|
| Company Name | 2px | Authority and presence |
| Job Title | 0.5px | Professional spacing |
| Services | 0.5px | Technical precision |

### Text Treatments

**Company Name**
```css
/* Visual reference - inline in production */
font-size: 20px;
font-weight: bold;
color: #0D0D0D;
letter-spacing: 2px;
text-transform: uppercase;
```

**Gold Divider**
- Width: 40px
- Height: 3px
- Color: #D4A017
- Spacing: 6px below company name

---

## 4. Layout & Spacing

### Grid System

```
Base Unit: 5px

Spacing Scale:
- xs: 5px
- sm: 10px
- md: 15px
- lg: 20px
- xl: 25px
- xxl: 30px
```

### Structural Measurements

| Element | Width | Height | Padding |
|---------|-------|--------|---------|
| Container | 600px max | Auto | 0 |
| Logo Panel | 160px | Auto | 25px 20px |
| Gold Divider | 3px | Auto (100%) | 0 |
| Content Area | Remaining | Auto | 25px 30px |
| Logo Image | 120px | 120px | 0 |

### Spacing Relationships

```
Logo Panel to Content: 3px (gold divider)
Company Name to Divider: 6px
Divider to Full Name: 12px
Full Name to Job Title: 2px
Job Title to Services: 15px
Services to Contact: 15px
Contact Lines: 1.8 line-height (internal spacing)
Signature to Disclaimer: 12px
```

### Responsive Behavior

| Viewport | Behavior |
|----------|----------|
| >600px | Centered, max-width constraint |
| 480-600px | Scales proportionally |
| <480px | Logo stacks above content (future enhancement) |

---

## 5. Color System

### Primary Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **QTech Black** | #0D0D0D | rgb(13,13,13) | Logo panel background, primary text |
| **QTech Gold** | #D4A017 | rgb(212,160,23) | Brand accent, dividers, links, icons |
| **White** | #FFFFFF | rgb(255,255,255) | Content background, text on dark |

### Neutral Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| **Dark Gray** | #333333 | rgb(51,51,51) | Primary contact text |
| **Medium Gray** | #666666 | rgb(102,102,102) | Secondary text, job titles |
| **Light Gray** | #888888 | rgb(136,136,136) | Services line, subtle elements |
| **Muted Gray** | #777777 | rgb(119,119,119) | Disclaimer text |
| **Border Gray** | #E0E0E0 | rgb(224,224,224) | Subtle container border |

### Color Application Matrix

| Element | Light Mode | Dark Mode Consideration |
|---------|------------|------------------------|
| Logo Background | #0D0D0D | Inverts to light (acceptable) |
| Content Background | #FFFFFF | May invert to dark (tested) |
| Primary Text | #0D0D0D | High contrast maintained |
| Links | #D4A017 | Color preserved in most clients |
| Icons | #D4A017 | Recognizable if desaturated |

### Accessibility

| Combination | Contrast Ratio | WCAG Level |
|-------------|----------------|------------|
| White on #0D0D0D | 16.8:1 | AAA |
| #0D0D0D on White | 16.8:1 | AAA |
| #D4A017 on White | 3.1:1 | AA (Large text only) |
| #D4A017 on #0D0D0D | 7.2:1 | AAA |

---

## 6. Logo Usage

### Master Logo Specifications

| Attribute | Specification |
|-----------|---------------|
| **Format** | SVG (source), PNG (deployment) |
| **Aspect Ratio** | 1:1 (square) |
| **Safe Zone** | 20px padding on all sides |
| **Minimum Size** | 80px display width |
| **Clear Space** | Equal to logo height on all sides |

### Logo Construction (Geometric Q)

```
Components:
1. Outer Circle
   - Diameter: 120px
   - Stroke: 6px #D4A017
   - Fill: None

2. Inner Mask
   - Diameter: 84px (70% of outer)
   - Fill: #0D0D0D (background color)
   - Creates ring effect

3. Cross-Bar
   - Width: 6px
   - Height: 50px
   - Rotation: 45°
   - Fill: #D4A017
   - Position: Center-right of circle

4. Tail
   - Stroke: 6px #D4A017, round caps
   - Path: From circle bottom-right, extending diagonally
   - Length: ~40px beyond circle
   - Angle: 45° downward-right

Wordmark:
- "QTECH": White, bold, uppercase, letter-spacing 4px
- "GROUP": Gold, light weight, uppercase, letter-spacing 6px
```

### Logo Variants

| Variant | Use Case | Background |
|---------|----------|------------|
| **Full Color** | Email signatures, digital | Dark #0D0D0D |
| **Reversed** | Dark backgrounds | Transparent |
| **Monochrome** | Print, fax, low-quality | White or light gray |

### Logo Don'ts

| Prohibition | Correction |
|-------------|------------|
| Stretch or distort | Maintain 1:1 ratio always |
| Change gold color | Use only #D4A017 |
| Add effects (shadow, glow) | Flat design only |
| Place on busy backgrounds | Use solid dark background |
| Reduce below 80px | Use text-only alternative |

---

## 7. Iconography

### Icon Set Specifications

| Icon | Size | Color | Format |
|------|------|-------|--------|
| Phone | 14x14px | #D4A017 | PNG with transparency |
| Email | 14x14px | #D4A017 | PNG with transparency |
| Web/Globe | 14x14px | #D4A017 | PNG with transparency |
| Location | 14x14px | #D4A017 | PNG with transparency |

### Icon Design Principles

- **Geometric**: Built on 14px grid
- **Minimal**: Maximum 3 elements per icon
- **Consistent**: 2px stroke weight, round caps
- **Monochrome**: Single color, no gradients

### Icon Construction (Inkscape)

```
Canvas: 14 x 14px
Grid: 1px subdivisions
Stroke: 2px (where applicable)
Export: 28x28px @ 144dpi (display at 14px)
```

### Phone Icon Example

```
Elements:
1. Receiver body: Curved path, 2px stroke
2. Base: Short horizontal line
Position: Centered in 14px canvas
Color: #D4A017 fill or stroke
```

### Icon Spacing

```
Icon to Text: 6px (table cell padding)
Icon Column Width: 20px fixed
Vertical Alignment: Middle
```

---

## 8. Content Guidelines

### Mandatory Elements

| Element | Required | Notes |
|---------|----------|-------|
| Company Name | Yes | "QTECH GROUP" |
| Full Name | Yes | As per HR records |
| Job Title | Yes | Official title |
| Phone | Yes | Mobile preferred for construction |
| Email | Yes | qtechgroup.co.za domain only |
| Website | Yes | https://www.qtechgroup.co.za |
| Location | Yes | "Johannesburg, South Africa" |
| Disclaimer | Yes | Variant-appropriate version |

### Optional Elements

| Element | When to Use | Format |
|---------|-------------|--------|
| Direct line | If different from mobile | "T: +27 ..." |
| Services line | External/client-facing | Pipe-separated |
| Social media | Only if professionally relevant | Icons only, max 3 |

### Prohibited Content

| Element | Reason |
|---------|--------|
| Personal mobile | Use company-issued only |
| Personal email | Brand inconsistency, security |
| "Best regards" etc. | Signature is branding, not correspondence |
| Inspirational quotes | Unprofessional, liability risk |
| Images of projects | Spam filters, loading issues |
| Animated GIFs | Unprofessional, client annoyance |

### Job Title Standards

| Level | Format | Example |
|-------|--------|---------|
| C-Suite | [Title] | Chief Executive Officer |
| Director | [Function] Director | Technical Director |
| Manager | [Function] Manager | Project Manager |
| Professional | [Role] | Senior Site Agent |
| Technical | [Discipline] [Level] | Civil Engineer |
| Support | [Function] | Office Administrator |

### Services Line Taxonomy

Use exact pipe-separated format:

```
Civil & Building Construction | Project Management | Plant Supply
```

Alternative for specialists:
```
Structural Engineering | Condition Assessments | Rehabilitation Design
```

---

## 9. Legal & Compliance

### Disclaimer Architecture

#### Tier 1: Executive/External (Full)

**Purpose**: Maximum protection for client-facing communication

**Components**:
1. Confidentiality statement
2. Contractual status clarification
3. CIDB registration scope
4. SACPCMP/ECSA professional alignment
5. Construction Regulations 2014 reference
6. POPIA compliance
7. Non-reliance language
8. Error handling instruction

**Word Count**: ~75 words
**Character Count**: ~650 characters

#### Tier 2: Compact/Internal (Abbreviated)

**Purpose**: Essential protection for mobile/internal use

**Components**:
1. Confidentiality statement
2. Non-binding clarification
3. Regulatory status reference

**Word Count**: ~25 words

### Regulatory References

| Regulation | Citation Format | Context |
|------------|-----------------|---------|
| CIDB | "CIDB registration" | Scope of authority |
| SACPCMP | "SACPCMP regulations" | Project management |
| ECSA | "ECSA regulations" | Engineering |
| Construction Regs | "Construction Regulations, 2014 (as amended)" | Safety/compliance |
| POPIA | "POPIA" | Data protection |
| NBR | "National Building Regulations" | Technical standards |

### Legal Language Specifications

| Term | Use Instead | Rationale |
|------|-------------|-----------|
| "Leading" | "Established" | Avoids comparative claims |
| "Best" | "Quality-focused" | Subjective, unprovable |
| "Guaranteed" | "Committed to" | Performance guarantee risk |
| "Within budget" | "Cost-conscious" | Implies promise |
| "Expert" | "Experienced" | Professional registration context |

### Update Triggers

Update disclaimers when:
- [ ] CIDB grading changes
- [ ] Professional registration status changes
- [ ] New legislation enacted
- [ ] Legal counsel advises revision
- [ ] Insurance policy requirements change
- [ ] Company structure changes

---

## 10. Technical Specifications

### HTML Structure

```html
<!-- Container Table -->
<table width="100%" style="max-width:600px;">
  
  <!-- Signature Block -->
  <tr>
    <td>
      <table width="100%">
        <!-- Logo | Divider | Content -->
      </table>
    </td>
  </tr>
  
  <!-- Disclaimer Block -->
  <tr>
    <td>
      <table width="100%">
        <!-- Legal text -->
      </table>
    </td>
  </tr>
  
</table>
```

### CSS Properties (Inline Only)

| Property | Values | Notes |
|----------|--------|-------|
| font-family | Arial, Helvetica, sans-serif | Web-safe only |
| font-size | 9px, 11px, 12px, 13px, 16px, 20px | From scale |
| color | Hex values from palette | No rgb() |
| background-color | Hex values | No gradients |
| padding | 0, 5px, 10px, 15px, 20px, 25px, 30px | From scale |
| width | % or px | Max 600px |
| border | 1px solid #E0E0E0 | Container only |
| text-decoration | none | Links only |
| text-transform | uppercase | Specific elements |
| letter-spacing | 0.5px, 2px | Specific elements |
| line-height | 1.2, 1.3, 1.4, 1.5, 1.6, 1.8 | From scale |
| vertical-align | top, middle | Table cells |

### Prohibited CSS

| Property | Reason |
|----------|--------|
| float | Unsupported in many clients |
| position | Unsupported |
| display: flex/grid | Poor support |
| @media queries | Stripped by most clients |
| @import | Blocked for security |
| External stylesheets | Stripped |
| `<style>` block | Stripped by many clients |
| `!important` | Can cause specificity wars |

### Image Specifications

| Attribute | Requirement |
|-----------|-------------|
| Format | PNG-24 with transparency |
| Color Profile | sRGB |
| Resolution | 144dpi (retina-ready, display at 50%) |
| Hosting | HTTPS only, company domain |
| Alt text | Descriptive, never empty |
| Width
