# Junction Workflow - Figma Design Specification

Use this document alongside the HTML prototype to recreate the decision tree in Figma.

---

## Canvas Setup

- **Frame Size**: 1920 x 4000 px (adjust height as needed)
- **Background**: Dark gradient `#1A1A2E` to `#16213E` (135°)
- **Padding**: 40px all sides

---

## Color Palette

### Primary Colors (copy these hex values directly)

| Purpose | Color Name | Hex Code | RGB |
|---------|------------|----------|-----|
| Entry/Exit Node Start | Purple | `#7C3AED` | 124, 58, 237 |
| Entry/Exit Node End | Blue | `#2563EB` | 37, 99, 235 |
| Decision Node Start | Amber | `#F59E0B` | 245, 158, 11 |
| Decision Node End | Orange | `#D97706` | 217, 119, 6 |
| Action Node Start | Emerald | `#10B981` | 16, 185, 129 |
| Action Node End | Green | `#059669` | 5, 150, 105 |
| Reference Node Start | Blue | `#3B82F6` | 59, 130, 246 |
| Reference Node End | Dark Blue | `#1D4ED8` | 29, 78, 216 |
| Warning Node Start | Red | `#EF4444` | 239, 68, 68 |
| Warning Node End | Dark Red | `#DC2626` | 220, 38, 38 |

### Border Colors

| Node Type | Border Color | Hex Code |
|-----------|--------------|----------|
| Entry | Light Purple | `#818CF8` |
| Decision | Yellow | `#FBBF24` |
| Action | Light Green | `#34D399` |
| Reference | Light Blue | `#60A5FA` |
| Warning | Light Red | `#F87171` |

### Text Colors

| Purpose | Hex Code |
|---------|----------|
| Primary Text (on dark) | `#FFFFFF` |
| Secondary Text | `#94A3B8` |
| Decision Node Text | `#1A1A2E` |
| Muted Text | `#64748B` |

### Confidence Badge Colors

| Confidence | Background | Text Color |
|------------|------------|------------|
| 0 - Default | `#6B7280` | White |
| 2 - Construction | `#F59E0B` | Black |
| 3 - Bad DP | `#8B5CF6` | White |
| 4 - Electric | `#06B6D4` | White |
| 5 - Map Edge | `#EC4899` | White |
| 6 - School Zone | `#84CC16` | Black |
| 7 - Time-based | `#F97316` | White |
| 8 - Weather-based | `#14B8A6` | White |

### Country Card Border Colors

| Propagation Type | Border Color |
|------------------|--------------|
| Both YES | `#10B981` (Green) |
| Straight YES / Turn NO | `#F59E0B` (Amber) |
| Both NO | `#EF4444` (Red) |

---

## Component Specifications

### Node Shapes

#### Entry Node
- **Shape**: Rectangle with rounded corners
- **Size**: 400 x 80 px
- **Corner Radius**: 12 px
- **Fill**: Linear gradient 135° (`#7C3AED` → `#2563EB`)
- **Stroke**: 2 px solid `#818CF8`
- **Text**: 20px, Bold, White, Center aligned
- **Shadow**: 0 10px 40px rgba(0,0,0,0.2)

#### Decision Node
- **Shape**: Rectangle with rounded corners (or diamond for classic flowchart)
- **Size**: 400 x 100 px
- **Corner Radius**: 12 px
- **Fill**: Linear gradient 135° (`#F59E0B` → `#D97706`)
- **Stroke**: 2 px solid `#FBBF24`
- **Text**: 16px, Regular, `#1A1A2E`, Center aligned
- **Question Mark Badge**: 28 x 28 px circle, White background, positioned top-right (-10, -10)

#### Action Node
- **Shape**: Rectangle with rounded corners
- **Size**: 350 x 80 px
- **Corner Radius**: 12 px
- **Fill**: Linear gradient 135° (`#10B981` → `#059669`)
- **Stroke**: 2 px solid `#34D399`
- **Text**: 16px, Regular, White, Center aligned

#### Reference Node
- **Shape**: Rectangle with rounded corners
- **Size**: 350 x 80 px
- **Corner Radius**: 12 px
- **Fill**: Linear gradient 135° (`#3B82F6` → `#1D4ED8`)
- **Stroke**: 2 px solid `#60A5FA`
- **Text**: 16px, Regular, White, Center aligned

#### Warning Node
- **Shape**: Rectangle with rounded corners
- **Size**: 350 x 80 px
- **Corner Radius**: 12 px
- **Fill**: Linear gradient 135° (`#EF4444` → `#DC2626`)
- **Stroke**: 2 px solid `#F87171`
- **Text**: 16px, Regular, White, Center aligned

### Connectors

#### Vertical Connector
- **Shape**: Rectangle
- **Size**: 3 x 40 px
- **Fill**: Linear gradient vertical (`#60A5FA` → `#818CF8`)

#### Horizontal Connector (for branches)
- **Shape**: Line or thin rectangle
- **Size**: Variable width x 3 px
- **Fill**: Linear gradient horizontal (`#60A5FA` → `#818CF8` → `#60A5FA`)

### Branch Labels

#### YES Label
- **Shape**: Pill/Stadium shape
- **Size**: 80 x 36 px
- **Corner Radius**: 18 px (full round)
- **Fill**: `#10B981`
- **Text**: 14px, Bold, White, "YES"

#### NO Label
- **Shape**: Pill/Stadium shape
- **Size**: 80 x 36 px
- **Corner Radius**: 18 px (full round)
- **Fill**: `#EF4444`
- **Text**: 14px, Bold, White, "NO"

### Country Cards

- **Shape**: Rectangle with rounded corners
- **Size**: 300 x Auto (fit content)
- **Corner Radius**: 12 px
- **Fill**: `rgba(255,255,255,0.05)` or `#FFFFFF` at 5% opacity
- **Left Border**: 4 px solid (color based on propagation type)
- **Padding**: 20 px

### Confidence Badges

- **Shape**: Pill/Stadium
- **Size**: Auto x 28 px
- **Corner Radius**: 14 px (full round)
- **Padding**: 4 px horizontal, 12 px vertical
- **Text**: 12px, Bold

### Tables

- **Header Row Background**: `rgba(124, 58, 237, 0.3)` or `#7C3AED` at 30% opacity
- **Row Background**: `rgba(255,255,255,0.02)`
- **Hover Row**: `rgba(255,255,255,0.05)`
- **Border**: 1 px solid `rgba(255,255,255,0.1)`
- **Header Text**: 14px, Bold
- **Cell Text**: 14px, Regular
- **Cell Padding**: 12-15 px

---

## Typography

### Font Family
- **Primary**: Segoe UI, or Inter (available in Figma)
- **Fallback**: -apple-system, system-ui, sans-serif

### Font Sizes

| Element | Size | Weight |
|---------|------|--------|
| Main Title | 40px | Bold |
| Section Title | 24px | Semi-bold |
| Subsection Title | 18px | Semi-bold |
| Node Title | 16-20px | Bold |
| Node Body | 14-16px | Regular |
| Small Text | 12-14px | Regular |
| Badge Text | 12px | Bold |
| Caption | 11px | Regular |

---

## Layout Structure

```
┌─────────────────────────────────────────────────────────────┐
│                        HEADER                                │
│   Title: Junction Workflow Decision Tree                     │
│   Subtitle: Legal Speed Annotation Guide for Map Marker      │
│   Version: 1.0 | Last Updated: February 2026                 │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │            SECTION: Main Decision Flow                │   │
│  │                                                       │   │
│  │    [Entry Node: START - Approaching a Junction]       │   │
│  │                         │                             │   │
│  │    [Decision: Explicit speed sign?]                   │   │
│  │              /          \                             │   │
│  │           YES           NO                            │   │
│  │            │             │                            │   │
│  │     [Action]      [Decision]                          │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Speed Propagation by Country         │   │
│  │                                                       │   │
│  │   ┌─────────┐  ┌─────────┐  ┌─────────┐              │   │
│  │   │Both YES │  │Str Y/T N│  │Both NO  │              │   │
│  │   │ Card    │  │ Card    │  │ Card    │              │   │
│  │   └─────────┘  └─────────┘  └─────────┘              │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Direction of Travel                  │   │
│  │                                                       │   │
│  │              [Decision: Straight or Turn?]            │   │
│  │                    /          \                       │   │
│  │              STRAIGHT        TURN                     │   │
│  │                 │              │                      │   │
│  │            [Branch]       [Branch]                    │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Road Type Determination              │   │
│  │                                                       │   │
│  │     [Urban]     [Rural]     [Highway]                 │   │
│  │        │           │            │                     │   │
│  │    [Action]    [Action]    [Action]                   │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Exception Checks                     │   │
│  │                                                       │   │
│  │   ┌────────┐  ┌────────┐  ┌────────┐  ┌────────┐     │   │
│  │   │ Zones  │  │ Danger │  │  City  │  │Special │     │   │
│  │   │  Card  │  │  Card  │  │  Card  │  │  Card  │     │   │
│  │   └────────┘  └────────┘  └────────┘  └────────┘     │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Roundabout Rules (dashed border)     │   │
│  │                                                       │   │
│  │   ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌────────┐  │   │
│  │   │ Entry   │  │ Changes │  │  Exit   │  │Complex │  │   │
│  │   │  Rule   │  │  Inside │  │  Prop   │  │  RAs   │  │   │
│  │   └─────────┘  └─────────┘  └─────────┘  └────────┘  │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │         SECTION: Reference Tables                     │   │
│  │                                                       │   │
│  │   ┌───────────────────────────────────────────────┐  │   │
│  │   │         Speed Propagation Chart                │  │   │
│  │   │  Country | Straight | Turn | Exceptions        │  │   │
│  │   └───────────────────────────────────────────────┘  │   │
│  │                                                       │   │
│  │   ┌───────────────────────────────────────────────┐  │   │
│  │   │         Confidence Values Table                │  │   │
│  │   │  Value | Meaning | When to Use                 │  │   │
│  │   └───────────────────────────────────────────────┘  │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐   │
│  │                       LEGEND                          │   │
│  │   [■ Entry] [■ Decision] [■ Action] [■ Ref] [■ Warn] │   │
│  └──────────────────────────────────────────────────────┘   │
│                                                              │
│                        FOOTER                                │
└─────────────────────────────────────────────────────────────┘
```

---

## Spacing Guidelines

| Element | Spacing |
|---------|---------|
| Section margin | 40px top/bottom |
| Section padding | 30px |
| Node vertical gap | 20px |
| Branch horizontal gap | 60px |
| Card grid gap | 20px |
| Table cell padding | 12-15px |

---

## Figma Components to Create

1. **Node Components** (with variants for each type)
   - Entry Node
   - Decision Node
   - Action Node
   - Reference Node
   - Warning Node

2. **Connector Components**
   - Vertical connector
   - Horizontal connector
   - Branch connector (Y-shape)

3. **Label Components**
   - YES label
   - NO label
   - STRAIGHT label
   - TURN label

4. **Badge Components**
   - Confidence badges (0-8)

5. **Card Components**
   - Country card (3 variants by color)
   - Exception card
   - Roundabout rule card

6. **Table Components**
   - Table header
   - Table row
   - Table cell

---

## Figma Prototype Interactions (Optional)

If creating an interactive prototype:

1. **Node hover**: Scale to 103%, add shadow
2. **Node click**: Highlight with white outline
3. **Tooltips**: Show on hover over decision nodes
4. **Section navigation**: Link legend items to sections

---

## Export Settings

For sharing the design:

- **PNG**: 2x scale for high resolution
- **PDF**: For printing reference sheets
- **SVG**: For web use or further editing

---

## Files Included

1. `junction-workflow-decision-tree.html` - Interactive HTML prototype
2. `figma-specification.md` - This specification document

Open the HTML file in a browser to see the visual reference while building in Figma.
