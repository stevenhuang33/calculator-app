# Calculator Web App Specification

## 1. Project Overview
- **Project name**: Interactive Calculator
- **Type**: Single-page web application (HTML/CSS/JS)
- **Core functionality**: A modern, responsive calculator with basic arithmetic operations supporting both mouse and keyboard input
- **Target users**: Anyone needing quick calculations

## 2. UI/UX Specification

### Layout Structure
- Centered calculator card (max-width: 360px)
- Vertical stack: Display → Buttons grid
- Responsive: scales down on mobile, centered on all screen sizes

### Visual Design

**Color Palette**
- Background: `#1a1a2e` (deep navy)
- Calculator body: `#16213e` (dark blue)
- Display background: `#0f0f23` (near black)
- Display text: `#eaeaea` (off-white)
- Primary accent: `#e94560` (coral red) - for equals button
- Secondary accent: `#533483` (purple) - for operators
- Button background: `#1f4068` (muted blue)
- Button text: `#eaeaea`
- Button hover: `#2a5a8a`
- Clear button: `#e94560` (coral red)

**Typography**
- Font family: `'JetBrains Mono', 'Fira Code', monospace` (from Google Fonts)
- Display font size: 2.5rem
- Button font size: 1.5rem
- Font weight: 600

**Spacing**
- Calculator padding: 24px
- Button gap: 12px
- Border radius (calculator): 16px
- Border radius (buttons): 8px
- Display padding: 20px

**Visual Effects**
- Box shadow on calculator: `0 25px 50px -12px rgba(0, 0, 0, 0.5)`
- Subtle glow on display: `inset 0 2px 4px rgba(0,0,0,0.3)`
- Button hover: brightness increase + slight scale (1.02)
- Button active: scale down (0.98)
- Smooth transitions: 150ms ease

### Components

**Display**
- Shows current input and result
- Two-line display: top shows full expression, bottom shows current number/result
- Max 12 digits displayed, overflow handled with ellipsis

**Button Grid**
- 4 columns × 5 rows layout
- Row 1: C (clear), ÷, ×, ⌫ (backspace)
- Row 2: 7, 8, 9, -
- Row 3: 4, 5, 6, +
- Row 4: 1, 2, 3, = (spans 2 rows vertically)
- Row 5: 0 (spans 2 columns), . (decimal)

**Button States**
- Default: solid background
- Hover: lighter background + slight scale
- Active/pressed: darker + scale down
- Special: equals button has distinct coral color

## 3. Functionality Specification

### Core Features
1. **Number input**: 0-9, decimal point
2. **Basic operations**: +, -, ×, ÷
3. **Clear**: Reset all (C key or Escape)
4. **Backspace**: Delete last character (⌫ key or Backspace)
5. **Equals**: Calculate result (Enter or =)
6. **Keyboard support**: Full keyboard input

### User Interactions
- Click buttons or use keyboard
- Chain operations: 5 + 3 * 2 = evaluates left-to-right (no precedence)
- Decimal: only one decimal per number
- Prevent multiple operators in a row
- Display shows running expression

### Edge Cases
- Division by zero: display "Error"
- Overflow: limit to reasonable digits
- Multiple equals: repeat last operation
- Empty calculation: show 0

## 4. Acceptance Criteria
- [ ] Calculator displays centered on page with dark theme
- [ ] All number buttons (0-9) work via click and keyboard
- [ ] All operators work correctly
- [ ] Clear (C/Escape) resets calculator
- [ ] Backspace removes last character
- [ ] Enter calculates result
- [ ] Responsive on mobile devices
- [ ] Smooth hover/active animations
- [ ] Display shows current input and result clearly
- [ ] No console errors
