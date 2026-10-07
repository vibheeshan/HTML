# HTML5 – Study Notes

## 1. What is HTML?

**HTML** stands for **HyperText Markup Language**.

- It is the basic building block of every web page and web application.
- It describes the **structure** of a page (headings, paragraphs, links, images, lists, etc.).
- **HTML5** is the current standard and supports modern web development.

---

## 2. What HTML5 Supports

- New **elements** and new **attributes**
- Full **CSS3** support
- Built-in **audio** and **video** support (`<audio>`, `<video>`)
- **2D and 3D graphics** (`<canvas>`, SVG, WebGL)
- **Local data storage** (`localStorage`, `sessionStorage`, IndexedDB)
- Offline support (originally *Application Cache*, now replaced by **Service Workers**)

> **Note:** Web SQL (local SQL databases) and Application Cache were part of early HTML5 but are now **deprecated**. Use **IndexedDB** and **Service Workers** instead.

---

## 3. Tags vs Elements

| Term | Meaning | Example |
|------|---------|---------|
| **Tag** | The markup written in angle brackets (opening or closing) | `<div>` and `</div>` |
| **Element** | Opening tag + content + closing tag | `<div>Hello</div>` |

```html
<p>This whole line is a paragraph element</p>
```

---

## 4. Why Use HTML5? (Semantic Elements)

HTML5 introduced **semantic elements**: elements whose names clearly describe their purpose. They make code easier to read, improve **SEO**, and help **accessibility** (screen readers).

### Semantic elements

| Element | Purpose |
|---------|---------|
| `<header>` | Top section of a page/section (logo, title, intro) |
| `<footer>` | Bottom section (copyright, contact, links) |
| `<nav>` | Navigation menu links |
| `<section>` | A group of related content (a topic/chapter) |
| `<article>` | Independent, self-contained content (blog post, news story) |
| `<aside>` | Side content, such as a left/right sidebar or related links |
| `<main>` | The main content of the page |

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
  </nav>
</header>

<main>
  <article>
    <h2>Article Title</h2>
    <p>Main content goes here.</p>
  </article>
  <aside>Sidebar content</aside>
</main>

<footer>&copy; 2026 My Website</footer>
```

### Non-semantic elements

These say nothing about their content. They are used only for grouping and styling.

- `<div>` – block-level container
- `<span>` – inline container

---

## 5. Comments

Comments are ignored by the browser and are used to explain code.

```html
<!-- This is a comment -->
```

---

## 6. Basic Elements

### Paragraph `<p>`

```html
<p>Write your content here.</p>
```

### Horizontal line `<hr>`

Creates a horizontal line across the full width of the page. It is an empty element (no closing tag).

```html
<hr>
```

### Lists

**Ordered list `<ol>`** – items are shown as numbers (1, 2, 3...).

```html
<ol>
  <li>First</li>
  <li>Second</li>
</ol>
```

**Unordered list `<ul>`** – items are shown as bullet points.

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>
```

### Non-breaking space `&nbsp;`

- An HTML **entity** that adds a space which will not break onto a new line.
- Browsers collapse multiple normal spaces into one, so `&nbsp;` is used to add extra spaces.

```html
<p>Hello&nbsp;&nbsp;&nbsp;World</p>
```

---

## 7. Inline Elements

Inline elements do not start on a new line; they take only as much width as their content.

### `<span>`

Groups and styles a small portion of text.

```html
<p>My favourite colour is <span style="color:blue;">blue</span>.</p>
```

### `<a>` (Anchor tag)

Creates a **hyperlink** to another page, file, or location. (Images are added with `<img>`, not `<a>`; `<a>` can *wrap* an image to make it clickable.)

```html
<a href="https://example.com">Visit Example</a>
```

**`target` attribute**

| Code | Behaviour |
|------|-----------|
| `<a href="url">` | Opens in the **same tab** (default) |
| `<a href="url" target="_blank">` | Opens in a **new tab** |

```html
<a href="https://example.com" target="_blank" rel="noopener">Open in new tab</a>
```

> Tip: add `rel="noopener"` when using `target="_blank"` for security.

---

## 8. Block vs Inline (Quick Summary)

| Block elements | Inline elements |
|----------------|-----------------|
| Start on a new line | Stay in the same line |
| Take full width | Take only needed width |
| `<div>`, `<p>`, `<ul>`, `<ol>`, `<section>` | `<span>`, `<a>`, `<img>` |

---

## 9. Starter Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First Page</title>
</head>
<body>
  <h1>Hello, HTML5!</h1>
  <p>This is my first web page.</p>
</body>
</html>
```
