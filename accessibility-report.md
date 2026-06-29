# Accessibility Audit Report — index.html

## Issues Found & How They Were Fixed

### 1. Images — Missing `alt` Text

**Issue:** Images without `alt` text are invisible to screen readers, making them inaccessible to visually impaired users.

**Fix:** Added descriptive `alt` text to all images.

```html
<!-- Before -->
<img src="https://placehold.co/400x300">

<!-- After -->
<img src="https://placehold.co/400x300" alt="Profile picture of Trevor Wachira">
```

---

### 2. Heading Hierarchy — Skipping Levels

**Issue:** Jumping from `<h1>` directly to `<h3>` confuses screen readers and breaks the document outline.

**Fix:** Ensured headings follow a logical order: `<h1>` → `<h2>` → `<h3>`.

```html
<!-- Before -->
<h1>Trevor Wachira</h1>
<h3>My Hobbies</h3>

<!-- After -->
<h1>Trevor Wachira</h1>
<h2>My Hobbies</h2>
```

---

### 3. Links — Non-Descriptive Link Text

**Issue:** Links that just say "click here" or show a raw URL don't tell screen reader users where the link goes.

**Fix:** Replaced vague link text with descriptive text.

```html
<!-- Before -->
<a href="https://www.freecodecamp.org/">Click here</a>

<!-- After -->
<a href="https://www.freecodecamp.org/">Visit freeCodeCamp — my favourite learning platform</a>
```

---

### 4. Language — Missing `lang` Attribute

**Issue:** Without a `lang` attribute on the `<html>` tag, screen readers can't determine which language to use when reading the page aloud.

**Fix:** Added `lang="en"` to the `<html>` tag.

```html
<!-- Before -->
<html>

<!-- After -->
<html lang="en">
```

---

### 5. Form Labels — Inputs Without Associated Labels

**Issue:** Inputs without `<label>` elements are not accessible — screen readers won't announce what the input is for.

**Fix:** Added a `<label>` with a matching `for` attribute to every input.

```html
<!-- Before -->
<input type="email" placeholder="Your email">

<!-- After -->
<label for="email">Email Address</label>
<input type="email" id="email" placeholder="e.g. trevor@email.com" required>
```

---

## Final Lighthouse Accessibility Score

**Score: 90/100**

---

## Tools Used

- Chrome DevTools Lighthouse
- [WAVE Web Accessibility Tool](https://wave.webaim.org/)
