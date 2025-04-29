
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Responsive Grid Layout</title>
  <style>
    /* Reset default styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f9f9f9;
    }

    /* NAVIGATION BAR */
    header {
      background: #121212;
      color: #fff;
      padding: 1rem;
      display: grid;
      grid-template-columns: 1fr auto;
      align-items: center;
    }

    header h1 {
      font-size: 1.5rem;
    }

    nav ul {
      display: grid;
      grid-auto-flow: column;
      gap: 1.5rem;
      list-style: none;
    }

    nav ul li a {
      color: #00ffff;
      text-decoration: none;
      font-weight: 500;
    }

    /* MAIN LAYOUT */
    .grid-container {
      display: grid;
      gap: 1rem;
      padding: 1rem;
    }

    .section {
      background: #ffffff;
      padding: 1.5rem;
      border: 1px solid #ccc;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    /* MEDIA QUERIES */

    /* Mobile */
    @media (max-width: 599px) {
      .grid-container {
        grid-template-columns: 1fr;
      }
    }

    /* Tablet */
    @media (min-width: 600px) and (max-width: 899px) {
      .grid-container {
        grid-template-columns: 1fr 1fr;
      }
    }

    /* Desktop */
    @media (min-width: 900px) {
      .grid-container {
        grid-template-columns: repeat(3, 1fr);
      }
    }
  </style>
</head>
<body>

  <!-- Header / Nav -->
  <header>
    <h1>GridSite</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Portfolio</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Grid Content -->
  <main class="grid-container">
    <div class="section">Section 1</div>
    <div class="section">Section 2</div>
    <div class="section">Section 3</div>
    <div class="section">Section 4</div>
    <div class="section">Section 5</div>
    <div class="section">Section 6</div>
  </main>

</body>
</html>
``
