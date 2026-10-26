## Assignment 6.4 — Positioning Practice

### 1. `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Positioning</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
    </nav>

    <section id="home">
        <h1>Welcome</h1>
        <p>This page demonstrates CSS positioning.</p>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <div class="card">
            <span class="badge">NEW</span>
            <h3>Our Club</h3>
            <p>Learn and grow with us.</p>
        </div>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <p>We provide learning resources and workshops.</p>
    </section>

    <a class="contact" href="mailto:club@example.com">Contact Us</a>

</body>
</html>
```

### 2. `style.css`

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #f0f4f8;
}

nav {
    position: sticky;
    top: 0;
    z-index: 100;
    background: navy;
    padding: 18px;
}

nav a {
    color: white;
    text-decoration: none;
    margin-right: 20px;
}

section {
    min-height: 500px;
    padding: 30px;
}

.card {
    position: relative;
    max-width: 300px;
    padding: 25px;
    background: white;
    border: 2px solid navy;
    border-radius: 10px;
}

.badge {
    position: absolute;
    top: -10px;
    right: -10px;
    background: orange;
    padding: 8px;
    z-index: 2;
}

.contact {
    position: fixed;
    bottom: 20px;
    right: 20px;
    z-index: 200;
    background: green;
    color: white;
    padding: 15px;
    border-radius: 25px;
    text-decoration: none;
}
```

**Explanation:**
- `sticky`: Keeps navigation at the top while scrolling.
- `fixed`: Keeps the contact button in the viewport.
- `relative`: Sets the positioning context for the card.
- `absolute`: Positions the badge inside the card.
- `z-index`: Controls overlapping element order.

**Submission:** Open with Live Server, scroll through the sections, and take a screenshot showing the navbar, badge, and floating contact button.