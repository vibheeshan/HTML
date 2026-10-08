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

---

## 10. Document Structure

| Element | Purpose |
|---------|---------|
| `<!DOCTYPE html>` | Tells the browser this is an HTML5 document |
| `<html>` | Root element; wraps everything |
| `<head>` | Page information (not shown on the page): title, meta, links to CSS |
| `<title>` | Text shown on the browser tab |
| `<meta>` | Metadata such as character set, viewport, description |
| `<link>` | Links an external resource, usually a CSS file |
| `<script>` | Adds JavaScript |
| `<body>` | Everything visible on the page |

```html
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Short page description for search engines">
  <link rel="stylesheet" href="style.css">
  <script src="app.js" defer></script>
</head>
```

---

## 11. Headings and Text Formatting

### Headings (`<h1>` to `<h6>`)

`<h1>` is the most important and largest; `<h6>` is the smallest. Use only **one `<h1>`** per page.

```html
<h1>Main Title</h1>
<h2>Sub Title</h2>
```

### Text formatting

| Tag | Result | Meaning |
|-----|--------|---------|
| `<strong>` | **Bold** | Important text |
| `<b>` | **Bold** | Bold only for style |
| `<em>` | *Italic* | Emphasised text |
| `<i>` | *Italic* | Italic only for style |
| `<mark>` | Highlighted | Marked/highlighted text |
| `<small>` | Smaller text | Side notes, fine print |
| `<del>` | ~~Strikethrough~~ | Deleted text |
| `<ins>` | Underlined | Inserted text |
| `<sub>` | H<sub>2</sub>O | Subscript |
| `<sup>` | x<sup>2</sup> | Superscript |
| `<br>` | Line break | Moves to the next line (empty element) |
| `<pre>` | Preformatted | Keeps spaces and line breaks |
| `<code>` | `code` | Computer code |
| `<blockquote>` | Quote block | Long quotation |

---

## 12. Attributes

Attributes give extra information about an element. They are written inside the **opening tag** as `name="value"`.

| Attribute | Use |
|-----------|-----|
| `id` | Unique identifier for one element |
| `class` | Group name that many elements can share (used by CSS/JS) |
| `style` | Inline CSS |
| `title` | Tooltip text on hover |
| `href` | Link destination (`<a>`) |
| `src` | Source file (`<img>`, `<audio>`, `<video>`, `<script>`) |
| `alt` | Alternative text for images |
| `lang` | Language of the content |
| `hidden` | Hides the element |

```html
<p id="intro" class="highlight" title="Welcome">Hello</p>
```

---

## 13. Images

`<img>` is an empty element. Always include `alt` text for accessibility and in case the image fails to load.

```html
<img src="photo.jpg" alt="A sunset over the sea" width="400" height="300">
```

### Clickable image

```html
<a href="https://example.com">
  <img src="logo.png" alt="Company logo">
</a>
```

### `<figure>` and `<figcaption>` (HTML5)

```html
<figure>
  <img src="chart.png" alt="Sales chart">
  <figcaption>Sales for 2026</figcaption>
</figure>
```

---

## 14. Links in Detail

| Type | Example |
|------|---------|
| External link | `<a href="https://example.com">Site</a>` |
| Internal page | `<a href="about.html">About</a>` |
| Same-page jump | `<a href="#contact">Go to Contact</a>` with `<section id="contact">` |
| Email | `<a href="mailto:name@example.com">Email me</a>` |
| Phone | `<a href="tel:+911234567890">Call us</a>` |
| Download | `<a href="file.pdf" download>Download PDF</a>` |

---

## 15. Tables

```html
<table border="1">
  <caption>Student Marks</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Marks</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Arun</td>
      <td>85</td>
    </tr>
    <tr>
      <td>Priya</td>
      <td>92</td>
    </tr>
  </tbody>
</table>
```

| Tag | Meaning |
|-----|---------|
| `<table>` | The table |
| `<tr>` | Table row |
| `<th>` | Header cell (bold, centred) |
| `<td>` | Data cell |
| `<thead>`, `<tbody>`, `<tfoot>` | Header, body, footer groups |
| `colspan` / `rowspan` | Make a cell span multiple columns / rows |

---

## 16. More on Lists

### Description list `<dl>`

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

### Ordered list types

```html
<ol type="A" start="3">
  <li>Item C</li>
  <li>Item D</li>
</ol>
```

`type` can be `1`, `A`, `a`, `I`, or `i`.

### Nested list

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apple</li>
      <li>Mango</li>
    </ul>
  </li>
</ul>
```

---

## 17. Forms and Input Types

Forms collect data from users.

```html
<form action="/submit" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Enter your name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="pass">Password:</label>
  <input type="password" id="pass" name="pass">

  <label for="msg">Message:</label>
  <textarea id="msg" name="msg" rows="4" cols="30"></textarea>

  <label for="city">City:</label>
  <select id="city" name="city">
    <option value="tiruppur">Tiruppur</option>
    <option value="chennai">Chennai</option>
  </select>

  <button type="submit">Submit</button>
</form>
```

### New HTML5 input types

`email`, `url`, `tel`, `number`, `range`, `date`, `time`, `datetime-local`, `month`, `week`, `color`, `search`

### Other common input types

`text`, `password`, `checkbox`, `radio`, `file`, `hidden`, `submit`, `reset`

### Useful form attributes

| Attribute | Use |
|-----------|-----|
| `required` | Field must be filled |
| `placeholder` | Hint text inside the field |
| `autofocus` | Cursor starts in this field |
| `disabled` | Field cannot be used |
| `readonly` | Value can be seen but not changed |
| `min`, `max`, `step` | Limits for numbers/dates |
| `pattern` | Regular expression for validation |
| `maxlength` | Maximum number of characters |

### Checkbox and radio

```html
<input type="checkbox" id="html" name="skills" value="html">
<label for="html">HTML</label>

<input type="radio" id="male" name="gender" value="male">
<label for="male">Male</label>
<input type="radio" id="female" name="gender" value="female">
<label for="female">Female</label>
```

> Radio buttons in the same group must share the same `name`.

---

## 18. Audio and Video (HTML5)

```html
<audio controls>
  <source src="song.mp3" type="audio/mpeg">
  Your browser does not support audio.
</audio>

<video controls width="400" poster="thumb.jpg">
  <source src="movie.mp4" type="video/mp4">
  Your browser does not support video.
</video>
```

| Attribute | Use |
|-----------|-----|
| `controls` | Show play/pause/volume controls |
| `autoplay` | Start automatically (often blocked unless muted) |
| `loop` | Repeat |
| `muted` | Start with sound off |
| `poster` | Preview image for a video |

---

## 19. Graphics: Canvas and SVG

| Feature | `<canvas>` | `<svg>` |
|---------|------------|---------|
| Type | Pixel based, drawn with JavaScript | Vector based, written in XML/HTML |
| Scaling | Can lose quality | Stays sharp at any size |
| Best for | Games, animations, image processing | Icons, logos, charts |

```html
<canvas id="myCanvas" width="200" height="100"></canvas>
<script>
  const ctx = document.getElementById("myCanvas").getContext("2d");
  ctx.fillStyle = "tomato";
  ctx.fillRect(10, 10, 150, 60);
</script>
```

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="teal" />
</svg>
```

3D graphics use **WebGL** (through `<canvas>`).

---

## 20. Web Storage (HTML5)

| Storage | Lifetime | Size (approx.) |
|---------|----------|----------------|
| `localStorage` | Stays until deleted | 5 to 10 MB |
| `sessionStorage` | Cleared when the tab is closed | 5 to 10 MB |
| Cookies | Set by expiry date; sent with every request | About 4 KB |
| IndexedDB | Stays until deleted | Large, for structured data |

```js
localStorage.setItem("username", "Arun");
console.log(localStorage.getItem("username"));
localStorage.removeItem("username");
```

---

## 21. Other Useful HTML5 Features

- **`<iframe>`**: embeds another page or a video inside your page.
  ```html
  <iframe src="https://example.com" width="400" height="300" title="Example"></iframe>
  ```
- **`<progress>` and `<meter>`**: show progress or a measured value.
- **`<details>` and `<summary>`**: collapsible content without JavaScript.
  ```html
  <details>
    <summary>Click to expand</summary>
    <p>Hidden content shown on click.</p>
  </details>
  ```
- **`<datalist>`**: gives autocomplete suggestions for an input.
- **`<time>`**: marks a date or time.
- **Geolocation API**: reads the user's location (with permission).
- **Drag and Drop API**: `draggable="true"`.
- **Web Workers**: run JavaScript in the background.

---

## 22. Common HTML Entities

| Entity | Result | Meaning |
|--------|--------|---------|
| `&nbsp;` | (space) | Non-breaking space |
| `&lt;` | `<` | Less than |
| `&gt;` | `>` | Greater than |
| `&amp;` | `&` | Ampersand |
| `&quot;` | `"` | Double quote |
| `&copy;` | © | Copyright |
| `&reg;` | ® | Registered |
| `&hearts;` | ♥ | Heart |

---

## 23. Best Practices

1. Always start with `<!DOCTYPE html>`.
2. Use **semantic elements** instead of many `<div>`s.
3. Always close your tags and keep them in lowercase.
4. Always add `alt` text to images.
5. Use only one `<h1>` per page, and do not skip heading levels.
6. Use `<label>` with every form input.
7. Indent your code so it is easy to read.
8. Keep CSS and JavaScript in separate files.
9. Add the `lang` attribute to `<html>` and the viewport `<meta>` tag.
10. Validate your code at [validator.w3.org](https://validator.w3.org).

---

## 24. Quick Revision Cheat Sheet

| Category | Tags |
|----------|------|
| Structure | `html`, `head`, `body`, `title`, `meta`, `link`, `script` |
| Semantic | `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`, `figure` |
| Text | `h1`-`h6`, `p`, `br`, `hr`, `strong`, `em`, `mark`, `code`, `pre` |
| Lists | `ul`, `ol`, `li`, `dl`, `dt`, `dd` |
| Links and media | `a`, `img`, `audio`, `video`, `source`, `iframe`, `canvas`, `svg` |
| Table | `table`, `tr`, `th`, `td`, `thead`, `tbody`, `tfoot`, `caption` |
| Form | `form`, `input`, `label`, `textarea`, `select`, `option`, `button`, `datalist` |
| Non-semantic | `div`, `span` |
