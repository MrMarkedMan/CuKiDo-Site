# CuKiDo-Site
/*===== FILE: style.css =====*/
  
/* style.css */

/* Reset & Base */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: Arial, sans-serif;
  background: #f7f7f7;
  color: #333;
}
a {
  text-decoration: none;
  color: inherit;
}
img {
  max-width: 100%;
  display: block;
}
.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

/* Header */
header {
  background: #131921;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}
header h1 {
  font-size: 2em;
}
header p {
  font-size: 1.2em;
}

/* Navigation */
nav {
  background: #232f3e;
}
nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
}
nav ul li {
  margin: 0 10px;
}
nav ul li a {
  color: #fff;
  padding: 10px 15px;
  font-weight: bold;
}
nav ul li a:hover {
  background: #37475a;
}

/* Slider (Moving Banners) */
.slider {
  position: relative;
  overflow: hidden;
  width: 100%;
  height: 400px;
  margin: 20px 0;
}
.slide {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0;
  transition: opacity 1s ease-in-out;
}
.slide.active {
  opacity: 1;
}
.slider img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Sections & Headings */
section {
  padding: 40px 0;
}
section h2 {
  text-align: center;
  color: #131921;
  margin-bottom: 20px;
  font-size: 2em;
}

/* Store Page - Product Grid */
.product-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}
.product {
  background: #fff;
  border: 1px solid #ddd;
  width: 280px;
  padding: 15px;
  text-align: center;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.product img {
  width: 100%;
  height: 200px;
  object-fit: contain;
  margin-bottom: 15px;
}
.product h3 {
  font-size: 1.3em;
  margin-bottom: 10px;
}
.product p {
  font-size: 1.1em;
  margin-bottom: 10px;
}
.product button {
  background: #febd69;
  border: none;
  padding: 10px 20px;
  color: #111;
  font-weight: bold;
  border-radius: 4px;
  cursor: pointer;
}
.product button:hover {
  background: #f3a847;
}

/* Contact Form */
form {
  max-width: 600px;
  margin: 0 auto;
}
form label {
  display: block;
  margin-top: 15px;
  font-weight: bold;
}
form input, form textarea {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
form button {
  margin-top: 20px;
  background: #febd69;
  border: none;
  padding: 12px 20px;
  font-size: 1em;
  font-weight: bold;
  cursor: pointer;
  border-radius: 4px;
}
form button:hover {
  background: #f3a847;
}

/* Footer */
footer {
  background: #232f3e;
  color: #fff;
  text-align: center;
  padding: 20px 0;
  margin-top: 30px;
}

/* Responsive */
@media (max-width: 768px) {
  .product-grid {
    flex-direction: column;
    align-items: center;
  }
  nav ul {
    flex-direction: column;
  }
}

/*===== END FILE: style.css =====*/


/*===== FILE: index.html =====*/
  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>CuKiDo - Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Header -->
  <header class="container">
    <h1>CuKiDo</h1>
    <p>The Premium Cookie Dough Destination</p>
  </header>
  
  <!-- Navigation -->
  <nav class="container">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="store.html">Store</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>
  
  <!-- Slider Section -->
  <section id="landing" class="container">
    <div class="slider">
      <div class="slide active">
        <img src="https://via.placeholder.com/1200x400?text=Welcome+to+CuKiDo" alt="Banner 1">
      </div>
      <div class="slide">
        <img src="https://via.placeholder.com/1200x400?text=Delicious+Cookie+Dough" alt="Banner 2">
      </div>
      <div class="slide">
        <img src="https://via.placeholder.com/1200x400?text=Fresh+Ingredients,+Bold+Flavors" alt="Banner 3">
      </div>
    </div>
  </section>
  
  <!-- Footer -->
  <footer class="container">
    <p>&copy; 2025 CuKiDo. All rights reserved.</p>
  </footer>
  
  <!-- Slider Script -->
  <script>
    const slides = document.querySelectorAll('.slide');
    let currentSlide = 0;
    function nextSlide() {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }
    setInterval(nextSlide, 3000);
  </script>
</body>
</html>
  
/*===== END FILE: index.html =====*/


/*===== FILE: store.html =====*/
  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>CuKiDo - Store</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Header -->
  <header class="container">
    <h1>CuKiDo Store</h1>
    <p>Buy Your Favorite Cookie Dough Now!</p>
  </header>
  
  <!-- Navigation -->
  <nav class="container">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="store.html">Store</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>
  
  <!-- Product Grid -->
  <section id="store" class="container">
    <h2>Our Products</h2>
    <div class="product-grid">
      <div class="product">
        <img src="https://via.placeholder.com/280?text=Product+1" alt="Product 1">
        <h3>Classic Chocolate Chip</h3>
        <p>$5.99</p>
        <button>Add to Cart</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/280?text=Product+2" alt="Product 2">
        <h3>Oatmeal Raisin</h3>
        <p>$6.49</p>
        <button>Add to Cart</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/280?text=Product+3" alt="Product 3">
        <h3>Peanut Butter Crunch</h3>
        <p>$6.99</p>
        <button>Add to Cart</button>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/280?text=Product+4" alt="Product 4">
        <h3>Sesame Caramel Delight</h3>
        <p>$7.49</p>
        <button>Add to Cart</button>
      </div>
    </div>
  </section>
  
  <!-- Footer -->
  <footer class="container">
    <p>&copy; 2025 CuKiDo. All rights reserved.</p>
  </footer>
</body>
</html>
  
/*===== END FILE: store.html =====*/


/*===== FILE: about.html =====*/
  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>CuKiDo - About</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Header -->
  <header class="container">
    <h1>About CuKiDo</h1>
  </header>
  
  <!-- Navigation -->
  <nav class="container">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="store.html">Store</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>
  
  <!-- About Content -->
  <section id="about" class="container">
    <h2>Our Story</h2>
    <p>CuKiDo was born out of a passion for exceptional cookie dough. We source only premium, natural ingredients to craft dough that promises indulgent flavor and an unforgettable texture.</p>
    <p>Inspired by the heritage of homemade baking and the innovation of modern cuisine, our mission is to redefine dessert indulgence—one scoop at a time.</p>
  </section>
  
  <!-- Footer -->
  <footer class="container">
    <p>&copy; 2025 CuKiDo. All rights reserved.</p>
  </footer>
</body>
</html>
  
/*===== END FILE: about.html =====*/


/*===== FILE: contact.html =====*/
  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>CuKiDo - Contact</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- Header -->
  <header class="container">
    <h1>Contact CuKiDo</h1>
  </header>
  
  <!-- Navigation -->
  <nav class="container">
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="store.html">Store</a></li>
      <li><a href="about.html">About</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>
  
  <!-- Contact Form -->
  <section id="contact" class="container">
    <h2>Get in Touch</h2>
    <form action="mailto:your-email@example.com" method="post" enctype="text/plain">
      <label for="name">Your Name:</label>
      <input type="text" id="name" name="name" placeholder="Your name" required>
      
      <label for="email">Your Email:</label>
      <input type="email" id="email" name="email" placeholder="you@example.com" required>
      
      <label for="message">Message:</label>
      <textarea id="message" name="message" rows="5" placeholder="Your message here..." required></textarea>
      
      <button type="submit">Send Message</button>
    </form>
    <p>Alternatively, you can reach us at <strong>support@cukido.com</strong>.</p>
  </section>
  
  <!-- Footer -->
  <footer class="container">
    <p>&copy; 2025 CuKiDo. All rights reserved.</p>
  </footer>
</body>
</html>
  
/*===== END FILE: contact.html =====*/
