# Notes from "HTML Crash Course For Absolute Beginners"

### 1. What is HTML?
*   **H**yper**T**ext **M**arkup **L**anguage.
*   It's not a programming language, but a **markup language** used to structure the content of a webpage.
*   It forms the "skeleton" or "bones" of a website.

### 2. Basic HTML Document Structure (Boilerplate)
Every HTML file should have this basic structure.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
</head>
<body>
    <!-- All visible content goes here -->
</body>
</html>
```
*   `<!DOCTYPE html>`: Declares the document type.
*   `<html>`: The root element of the page.
*   `<head>`: Contains meta-information about the page (character set, viewport settings, title, links to CSS, etc.). This content is not displayed on the page itself.
*   `<body>`: Contains all the visible content of the page (headings, paragraphs, images, etc.).

### 3. Common Elements (Tags)
*   **Headings**: `<h1>` through `<h6>`. Used to define a hierarchy of titles and subtitles. `<h1>` is the most important.
*   **Paragraphs**: `<p>`. Used for blocks of text.
*   **Links**: `<a href="https://example.com">Click me</a>`. The `href` attribute specifies the destination URL.
*   **Images**: `<img src="image.jpg" alt="Description of image">`.
    *   `src`: The path to the image file.
    *   `alt`: **Alternative text**. This is crucial for accessibility (for screen readers) and will be displayed if the image fails to load.
*   **Line Break**: `<br>`. Creates a single line break. Use sparingly.
*   **Horizontal Rule**: `<hr>`. Creates a thematic break or horizontal line.

### 4. Lists
*   **Unordered List** (`<ul>`): A bulleted list. Use when the order of items doesn't matter.
*   **Ordered List** (`<ol>`): A numbered list. Use when the order is important.
*   **List Item** (`<li>`): Represents an item within a `<ul>` or `<ol>`.

### 5. Tables
Used for displaying **tabular data**, not for page layout.
```html
<table>
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Data 1</td>
            <td>Data 2</td>
        </tr>
    </tbody>
</table>
```
*   `<table>`: The main container.
*   `<thead>`: Groups the header content.
*   `<tbody>`: Groups the body content.
*   `<tr>`: Defines a table row.
*   `<th>`: Defines a header cell (bold and centered by default).
*   `<td>`: Defines a data cell.

### 6. Forms
Used to collect user input.
*   `<form action="/process.php" method="POST">`: The container for form elements.
    *   `action`: The URL where the form data will be sent.
    *   `method`: The HTTP method to use (`GET` or `POST`).
*   **Labeling Controls**: `<label for="username">Username</label>`
    *   The `for` attribute on the `<label>` must match the `id` attribute on the `<input>` to link them. This is vital for accessibility and provides a better user experience (clicking the label focuses the input).
*   **Input Types**: `<input type="..." id="..." name="...">`
    *   `text`, `email`, `password`, `number`, `date`, `checkbox`, `radio`, etc.
*   **Dropdown/Select Box**: `<select name="gender" id="gender"> ... </select>` with `<option value="...">` elements inside.
*   **Submit Button**: The button that sends the form data.
    *   `<button type="submit">Submit</button>` (Recommended)
    *   `<input type="submit" value="Submit">`

### 7. Block vs. Inline Elements
*   **Block-level elements**: Start on a new line and take up the full width available (e.g., `<h1>`, `<p>`, `<div>`, `<ul>`, `<table>`, `<form>`).
*   **Inline elements**: Do not start on a new line and only take up as much width as necessary (e.g., `<a>`, `<img>`, `<strong>`, `<em>`, `<span>`).

### 8. Semantic HTML
Introduced in HTML5 to give more meaning to the structure of a page. This is better for SEO (Search Engine Optimization) and accessibility.
*   `<header>`: For introductory content or navigation links.
*   `<main>`: Specifies the main, unique content of the document.
*   `<footer>`: For the footer of a document or section.
*   `<nav>`: For a set of navigation links.
*   `<section>`: Defines a thematic grouping of content.
*   `<article>`: For self-contained content (e.g., a blog post, a news story).