# Disabled Button Accessibility

## Overview

This submission improves accessibility for disabled buttons by adding `aria-disabled="true"` attribute alongside the standard HTML `disabled` attribute.

## Problem

Standard HTML `<button disabled>` provides visual indication of the disabled state, but screen readers may not properly announce it to users. Adding `aria-disabled="true"` ensures assistive technology correctly communicates the button's state.

## Solution

### Option 1: Direct HTML Attribute

```html
<button class="ease-btn ease-btn-primary" disabled aria-disabled="true">
  Disabled Button
</button>
```

### Option 2: JavaScript Enhancement

```javascript
document.querySelectorAll('.ease-btn:disabled').forEach(btn => {
  btn.setAttribute('aria-disabled', 'true');
});
```

## Benefits

1. **Screen Reader Support**: Properly announces disabled state to assistive technology
2. **Keyboard Navigation**: Clear feedback that the button cannot be activated
3. **WCAG Compliance**: Meets accessibility guidelines for interactive elements
4. **Progressive Enhancement**: Works alongside existing disabled styles

## Usage

Simply add `aria-disabled="true"` to any disabled button:

```html
<button class="ease-btn ease-btn-primary" disabled aria-disabled="true">
  Submit
</button>
```

## Files

- `demo.html` - Interactive demonstration of accessible disabled buttons
- `style.css` - Demo styling (buttons use EaseMotion CSS framework)
- `README.md` - This documentation
