Here are some core web development snippets for ICT: HTML, CSS, and JavaScript.

1. HTML: page structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Website</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>My Website</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>About</h2>
      <p>Welcome to my page.</p>
    </section>

    <form id="contactForm">
      <input type="text" id="name" placeholder="Your name" required>
      <input type="email" id="email" placeholder="Your email" required>
      <button type="submit">Send</button>
    </form>
  </main>

  <footer>&copy; 2026 My Website</footer>
  <script src="script.js"></script>
</body>
</html>
```

2. CSS: layout and responsiveness
```css
* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background: #f4f4f4;
}

header {
  background: #222;
  color: #fff;
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav a { color: #fff; margin-left: 1rem; text-decoration: none; }
nav a:hover { color: #ffcc00; }

.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  padding: 1rem;
}

@media (max-width: 600px) {
  header { flex-direction: column; }
}
```

## 3. JavaScript: DOM, validation, and fetching data
```javascript
// Form handling
document.getElementById("contactForm").addEventListener("submit", (e) => {
  e.preventDefault();
  const name = document.getElementById("name").value.trim();
  if (name.length < 2) {
    alert("Please enter a valid name");
    return;
  }
  alert(`Thank you, ${name}!`);
});

// Fetch data from an API
async function getData() {
  try {
    const res = await fetch("https://jsonplaceholder.typicode.com/posts?_limit=5");
    if (!res.ok) throw new Error("Request failed");
    const data = await res.json();
    console.log(data);
  } catch (err) {
    console.error(err.message);
  }
}
getData();
```

Good practices
- Use semantic tags (`header`, `main`, `section`, `footer`).
- Keep HTML, CSS, and JS in separate files.
- Make the site responsive with `meta viewport` and media queries.
- Validate user input and handle API errors with `try/catch`.
- Keep API keys in a `.env` file and out of GitHub.

Tell me what you need it for (a coursework task, a React page, a login form, a PHP/MySQL backend) and I can give you specific code.# simple


Here is more detail on each part of that code, so you can understand it and explain it in an exam.

## 1. HTML: more information

**What it is:** HyperText Markup Language, the structure (skeleton) of a web page.

**Key parts of the code explained**

| Code | Purpose |
|---|---|
| `<!DOCTYPE html>` | Tells the browser this is an HTML5 document |
| `<html lang="en">` | Root element; `lang` sets the page language |
| `<head>` | Holds information about the page (not displayed) |
| `<meta charset="UTF-8">` | Supports all characters and symbols |
| `<meta name="viewport">` | Makes the page fit phone screens |
| `<title>` | Text shown on the browser tab |
| `<link rel="stylesheet">` | Connects the CSS file |
| `<body>` | Everything visible on the page |
| `<script src>` | Connects the JavaScript file |

**Semantic elements:** `header`, `nav`, `main`, `section`, `footer` describe the *meaning* of content, which helps accessibility and SEO.

**Common form input types:** `text`, `email`, `password`, `number`, `date`, `checkbox`, `radio`, `file`.

**Other useful tags:** `<img src="" alt="">`, `<a href="">`, `<ul>/<ol>/<li>`, `<table>`, `<div>`, `<span>`, `<button>`.

## 2. CSS: more information

**What it is:** Cascading Style Sheets, used to style and layout HTML (colours, fonts, spacing, position).

**Ways to add CSS**
1. **Inline:** `<p style="color:red">`
2. **Internal:** inside `<style>` in the `<head>`
3. **External:** a separate `.css` file (best practice)

**Selectors:** `p` (element), `.card` (class), `#about` (id), `nav a` (descendant), `a:hover` (pseudo-class).

**The box model:** every element is a box made of **content → padding → border → margin**. `box-sizing: border-box` makes width include padding and border.

**Layout systems used in the code**
- **Flexbox** (`display: flex`): arranges items in one direction (row or column). Used for the header.
- **Grid** (`display: grid`): arranges items in rows and columns. Used for the `.cards`.
- **Media queries** (`@media`): change styles on smaller screens, which makes the site **responsive**.

## 3. JavaScript: more information

**What it is:** A programming language that makes web pages interactive.

**Key concepts in the code**

| Concept | Example | Meaning |
|---|---|---|
| **DOM** | `document.getElementById()` | Lets JS access and change HTML elements |
| **Event listener** | `addEventListener("submit", ...)` | Runs code when something happens (click, submit) |
| **`preventDefault()`** | `e.preventDefault()` | Stops the form from reloading the page |
| **Template literal** | `` `Thank you, ${name}!` `` | Inserts variables into strings |
| **`async/await`** | `async function getData()` | Waits for data without freezing the page |
| **`fetch()`** | `fetch(url)` | Requests data from an API |
| **`try/catch`** | `try { } catch (err) { }` | Handles errors safely |
| **JSON** | `res.json()` | Converts the response into a JavaScript object |

**Variables:** `let` (can change), `const` (cannot change), `var` (old style).

**Data types:** string, number, boolean, array, object, null, undefined.

## How the three work together

| Technology | Role | Human body analogy |
|---|---|---|
| **HTML** | Structure | Skeleton |
| **CSS** | Style | Skin and clothes |
| **JavaScript** | Behaviour | Muscles and brain |

## Possible exam questions
1. Define HTML, CSS and JavaScript.
2. State three advantages of using external CSS.
3. What is the purpose of the `<meta name="viewport">` tag?
4. Differentiate between Flexbox and Grid.
5. Explain the role of `fetch()` and `async/await` in web development.
6. What is the DOM?

## Related topics I can cover next
- Responsive design in detail
- JavaScript functions, loops, and arrays
- Client-side vs server-side programming
- Form validation
- React basics (useful for your Reelhouse project)

I can also give you model answers to any of the questions above.
