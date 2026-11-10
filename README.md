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
