# Ex02 Commercial Website
## Date:11/8/2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
## STEP 1
Create an HTML file (index.html)

## STEP 2
Create a CSS file (style.css)

## STEP 3
Include a navigation bar with links to different sections.

## STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

## STEP 5
Include social media links at the footer with copyright information.

## STEP 6
Define global styles for fonts, colors, and layout.

## STEP 7
Style the header, navigation bar, and sections.

## STEP 8
Use Flexbox for layout design.

## STEP 9
Add hover effects and transitions for interactivity.

## STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

## STEP 12
Open the HTML file in a browser to check layout and functionality.

## STEP 13
Fix styling issues and refine content placement.

## STEP 14
Deploy the website.

## STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM:
## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Golden Elegance Jewelry</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Open+Sans&display=swap" rel="stylesheet">

<style>
/* === GLOBAL STYLES === */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background-color: #121212;
  color: white;
  font-family: 'Open Sans', sans-serif;
  line-height: 1.6;
}
h1, h2, h3 {
  font-family: 'Playfair Display', serif;
  color: white;
}

/* === NAVIGATION === */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em 2em;
  background-color: goldenrod;
}
.logo {
  font-size: 1.5em;
  font-weight: bold;
}
.nav-links {
  display: flex;
  gap: 1.5em;
  list-style: none;
}
.nav-links a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s;
}
.nav-links a:hover {
  color: #121212;
}

/* === HERO === */
.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
.hero img {
  max-width: 100%;
  border-radius: 8px;
}
.hero-text {
  animation: fadeIn 2s ease-in;
}
.hero h1 {
  font-size: 3em;
}
.btn {
  background: goldenrod;
  color: #121212;
  padding: 0.7em 1.5em;
  border-radius: 5px;
  text-decoration: none;
  transition: all 0.3s;
  display: inline-block;
  margin-top: 1em;
}
.btn:hover {
  background: linear-gradient(45deg, goldenrod, silver);
}

/* === PRODUCTS === */
.products {
  padding: 3em 2em;
  text-align: center;
}
.product-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 2em;
  justify-content: center;
}
.product-card {
  background-color: #1a1a1a;
  border-radius: 10px;
  padding: 1em;
  width: 250px;
  transition: transform 0.3s;
  border: 2px solid transparent;
  border-image: linear-gradient(45deg, goldenrod, silver) 1;
}
.product-card img {
  width: 100%;
  border-radius: 10px;
}
.product-card:hover {
  transform: scale(1.05);
}

/* === ABOUT === */
.about {
  padding: 3em 2em;
  text-align: center;
}

/* === TESTIMONIALS === */
.testimonials {
  padding: 3em 2em;
  background-color: #1a1a1a;
  text-align: center;
}
.testimonial-container {
  display: flex;
  flex-wrap: wrap;
  gap: 2em;
  justify-content: center;
}
.testimonial {
  background-color: #121212;
  padding: 1.5em;
  border-radius: 10px;
  width: 300px;
}

/* === CONTACT === */
.contact {
  padding: 3em 2em;
  text-align: center;
}
form {
  display: flex;
  flex-direction: column;
  gap: 1em;
  max-width: 400px;
  margin: auto;
}
input, textarea {
  padding: 0.8em;
  border-radius: 5px;
  border: none;
}

/* === ACCOUNT === */
.account {
  padding: 3em 2em;
  text-align: center;
}

/* === FOOTER === */
footer {
    background-color: #222;
    text-align: center;
    padding: 1em;
    color: white;
}

.social-icons {
    display: flex;
    justify-content: center;
    gap: 1em;
    margin-bottom: 1em;
}

.social-icons img {
    width: 24px;
    height: 24px;
    transition: transform 0.3s ease, filter 0.3s ease;
}

.social-icons img:hover {
    transform: scale(1.2);
    filter: brightness(1.2);
}

/* === ANIMATIONS === */
@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}

/* === RESPONSIVE === */
@media (max-width: 768px) {
  .nav-links {
    flex-direction: column;
    align-items: center;
  }
  .product-grid, .testimonial-container {
    flex-direction: column;
  }
}
</style>
</head>
<body>

<!-- HEADER -->
<header>
  <nav class="navbar">
    <div class="logo">Elite</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#about">About Us</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#account">Account</a></li>
    </ul>
  </nav>
</header>

<!-- HERO -->
<section id="home" class="hero">
  <div class="hero-text">
    <img src="./imagess/bg.png" alt="jewel shop">
    <h1>Luxury Handmade Jewelry</h1>
    <p>Timeless elegance crafted just for you.</p>
    <a href="#products" class="btn">Shop Now</a>
  </div>
</section>

<!-- PRODUCTS -->
<section id="products" class="products">
  <h2>Our Collection</h2>
  <div class="product-grid">
    <div class="product-card">
      <img src="./imagess/product1.png" alt="Gold Necklace">
      <h3>Gold Leaf Necklace</h3>
      <p>$120</p>
    </div>
    <div class="product-card">
      <img src="./imagess/product2.png" alt="Silver Earrings">
      <h3>Silver Pearl Earrings</h3>
      <p>$90</p>
    </div>
    <div class="product-card">
      <img src="./imagess/product3.png" alt="Bracelet">
      <h3>Charm Bracelet</h3>
      <p>$75</p>
    </div>
    <div class="product-card">
      <img src="./imagess/product4.png" alt="Gold Ring">
      <h3>Vintage Silver Ring</h3>
      <p>$150</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about" class="about">
  <h2>About Us</h2>
  <p>
    At Elite, we believe jewelry is more than just an accessory – it’s a reflection of your story.  
    Every piece is meticulously handcrafted with premium gold and silver, ensuring quality, beauty, and uniqueness.
  </p>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials" class="testimonials">
  <h2>What Our Customers Say</h2>
  <div class="testimonial-container">
    <div class="testimonial">
      <p>"Absolutely stunning craftsmanship! I feel like royalty when I wear it."</p>
      <h4>- Sarah W.</h4>
    </div>
    <div class="testimonial">
      <p>"Unique designs with exceptional attention to detail."</p>
      <h4>- Emily R.</h4>
    </div>
    <div class="testimonial">
      <p>"I’m in love with my bracelet! Worth every penny."</p>
      <h4>- Anna L.</h4>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" class="contact">
  <h2>Contact Us</h2>
  <form>
    <input type="text" placeholder="Your Name" required>
    <input type="email" placeholder="Your Email" required>
    <textarea placeholder="Your Message" rows="5" required></textarea>
    <button type="submit" class="btn">Send Message</button>
  </form>
</section>

<!-- ACCOUNT -->
<section id="account" class="account">
  <h2>User Account</h2>
  <p>Login or sign up to save your favorites and track orders.</p>
  <a href="#" class="btn">Login</a>
  <a href="#" class="btn">Sign Up</a>
</section>

<!-- FOOTER -->
<footer>
    <div class="social-icons">
        <a href="https://facebook.com" target="_blank" aria-label="Facebook">
            <img src="./imagess/facebook.png" alt="Facebook">
        </a>
        <a href="https://instagram.com" target="_blank" aria-label="Instagram">
            <img src="./imagess/instagram.png" alt="Instagram">
        </a>
        <a href="https://twitter.com" target="_blank" aria-label="Twitter">
            <img src="./imagess/twitter.png" alt="Twitter">
        </a>
    </div>
    <p>&copy; 2025 Elite Jewelry | All Rights Reserved</p>
</footer>


</body>
</html>


```

## OUTPUT:
<img width="1919" height="1013" alt="Screenshot 2025-08-11 183246" src="https://github.com/user-attachments/assets/d36ebbb0-d6e7-4438-b34d-4a9a593cff05" />
<img width="1919" height="1012" alt="Screenshot 2025-08-11 183259" src="https://github.com/user-attachments/assets/e7c3b149-3e42-46dd-a783-0d3b55c4ff00" />
<img width="1914" height="922" alt="Screenshot 2025-08-11 183315" src="https://github.com/user-attachments/assets/7409297a-13f7-4043-88f7-ddbb80612e18" />
<img width="1919" height="1015" alt="Screenshot 2025-08-11 183324" src="https://github.com/user-attachments/assets/7dff369e-5e03-48cf-aa7b-34c274b7a36f" />



## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
