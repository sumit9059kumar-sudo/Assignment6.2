File 1: index.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 6.2 - Backgrounds, Borders & Display</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <header class="page-header">
    <h1>Card Designs & Display Properties Showcase</h1>
    <p>Exploring backgrounds, borders, rounded corners, and display behaviors.</p>
  </header>

  <main class="container">

    <!-- 1. Three Card Designs Section -->
    <section class="card-section">
      <h2>Pricing Tiers (Cards)</h2>
      <div class="card-grid">
        
        <!-- Basic Card -->
        <div class="card card-basic">
          <h3>Basic Plan</h3>
          <p>Essential features for personal use with a clean, simple solid border and neutral background.</p>
          <button class="card-btn">Choose Basic</button>
        </div>

        <!-- Standard Card -->
        <div class="card card-standard">
          <h3>Standard Plan</h3>
          <p>Great for growing projects with a highlighted green accent border and soft tint.</p>
          <button class="card-btn">Choose Standard</button>
        </div>

        <!-- Premium Card -->
        <div class="card card-premium">
          <h3>Premium Plan</h3>
          <p>Advanced tools and top-tier features for professionals with an amber double border.</p>
          <button class="card-btn">Choose Premium</button>
        </div>

      </div>
    </section>

    <!-- 2. Display Properties Demonstration Section -->
    <section class="display-section">
      <h2>Display Property Demonstrations</h2>
      
      <!-- Block Demo -->
      <div class="display-demo-box">
        <h3>Display: Block</h3>
        <p>Block elements take up the full available horizontal width and automatically start on a new line.</p>
        <div class="box-demo block-element">I am a block element 1</div>
        <div class="box-demo block-element">I am a block element 2</div>
      </div>

      <!-- Inline Demo -->
      <div class="display-demo-box">
        <h3>Display: Inline</h3>
        <p>Inline elements only take up as much width as necessary and do not start on a new line. <em>Note: width and height properties are ignored by inline elements.</em></p>
        <p>This is standard paragraph text containing an <span class="inline-element">inline span element</span> embedded right inside it.</p>
      </div>

      <!-- Inline-Block Demo -->
      <div class="display-demo-box">
        <h3>Display: Inline-Block</h3>
        <p>Inline-block elements flow side-by-side like inline elements, but they successfully respect custom width, height, padding, and margins!</p>
        <div class="inline-block-element">Box 1</div>
        <div class="inline-block-element">Box 2</div>
        <div class="inline-block-element">Box 3</div>
      </div>
    </section>

  </main>

  <footer>
    <p>&copy; 2026 Web Development Assignment</p>
  </footer>

</body>
</html>
File 2: styles.css
CSS
/* Global Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: system-ui, -apple-system, sans-serif;
  background-color: #f1f5f9;
  color: #1e293b;
  line-height: 1.6;
  padding: 20px;
}

.page-header {
  text-align: center;
  margin-bottom: 30px;
}

.page-header h1 {
  color: #0f172a;
  margin-bottom: 5px;
}

.container {
  max-width: 960px;
  margin: 0 auto;
}

section {
  margin-bottom: 40px;
}

section h2 {
  font-size: 1.5rem;
  margin-bottom: 20px;
  border-bottom: 2px solid #cbd5e1;
  padding-bottom: 8px;
  color: #1e3a8a;
}

/* ==========================================================================
   CARD STYLES (Distinct Backgrounds, Borders, Radius, Width/Height)
   ========================================================================== */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
}

.card {
  width: 100%;
  max-width: 320px;
  height: 240px;
  padding: 24px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

/* 1. Basic Card */
.card-basic {
  background-color: #ffffff;
  border: 1px solid #cbd5e1;
}

/* 2. Standard Card */
.card-standard {
  background-color: #f0fdf4;
  border: 2px solid #22c55e;
}

/* 3. Premium Card */
.card-premium {
  background-color: #fef3c7;
  border: 4px double #d97706;
}

.card h3 {
  font-size: 1.25rem;
  color: #0f172a;
}

.card p {
  font-size: 0.95rem;
  color: #475569;
}

.card-btn {
  padding: 8px 16px;
  background-color: #2563eb;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 600;
  transition: opacity 0.2s;
}

.card-btn:hover {
  opacity: 0.9;
}

/* ==========================================================================
   DISPLAY PROPERTY DEMONSTRATIONS
   ========================================================================== */
.display-demo-box {
  background-color: #ffffff;
  padding: 20px;
  border-radius: 8px;
  border: 1px solid #cbd5e1;
  margin-bottom: 20px;
}

.display-demo-box h3 {
  margin-bottom: 6px;
  font-size: 1.1rem;
}

.display-demo-box p {
  margin-bottom: 12px;
  color: #475569;
  font-size: 0.95rem;
}

/* 1. Block Element Demo */
.block-element {
  display: block;
  background-color: #e0f2fe;
  border: 1px solid #0284c7;
  padding: 10px;
  margin-bottom: 8px;
  width: 100%; /* Takes full width */
}

/* 2. Inline Element Demo */
.inline-element {
  display: inline;
  background-color: #fee2e2;
  border: 1px solid #dc2626;
  padding: 2px 6px;
  /* Width and height are ignored on inline elements */
  width: 300px;
  height: 100px;
}

/* 3. Inline-Block Element Demo */
.inline-block-element {
  display: inline-block;
  background-color: #f3e8ff;
  border: 1px solid #9333ea;
  width: 120px;
  height: 60px;
  padding: 10px;
  margin-right: 10px;
  text-align: center;
  line-height: 38px;
  font-weight: 600;
}

footer {
  text-align: center;
  margin-top: 40px;
  color: #64748b;
  font-size: 0.9rem;
}