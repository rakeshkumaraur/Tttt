index.html<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TREND SPHARE</title>
  <link rel="stylesheet" href="css/styles.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
  <header class="header">
    <div class="logo">TREND <span>SPHARE</span></div>
    <nav class="navbar">
      <a href="#home">Home</a>
      <a href="#news">News</a>
      <a href="#blogs">Blogs</a>
      <a href="#contact">Contact</a>
      <button id="theme-toggle" class="theme-toggle">🌙</button>
    </nav>
  </header>

  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Stay Updated with the Latest Trends</h1>
      <p>Explore news and blogs that redefine the way you perceive the world.</p>
      <input type="text" id="search-bar" placeholder="Search news or blogs..." />
      <a href="#news" class="btn">Explore Now</a>
    </div>
  </section>

  <section id="news" class="news">
    <h2>Trending News</h2>
    <div class="news-grid" id="news-section">
      <!-- News will load dynamically -->
    </div>
  </section>

  <section id="blogs" class="blogs">
    <h2>Our Blogs</h2>
    <div class="blogs-grid" id="blogs-section">
      <!-- Blogs will load dynamically -->
    </div>
  </section>

  <footer class="footer">
    <p>&copy; 2024 TREND SPHARE. All rights reserved.</p>
    <div class="social-links">
      <a href="#"><i class="fab fa-facebook"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
    </div>
    <a href="https://github.com/your-repository" class="btn contribute-btn">Improve this page</a>
  </footer>

  <script src="js/script.js"></script>
</body>
</html>
styles.css/* Theme Toggle */
.theme-toggle {
  background: transparent;
  border: none;
  font-size: 20px;
  color: white;
  cursor: pointer;
  outline: none;
}

body.dark-mode {
  background: #121212;
  color: white;
}

.dark-mode .header {
  background: #333;
}

.dark-mode .btn {
  background: #bb86fc;
}

#search-bar {
  margin: 15px 0;
  padding: 10px;
  width: 80%;
  border: 1px solid #ccc;
  border-radius: 5px;
}
script.jsdocument.addEventListener('DOMContentLoaded', () => {
  // Theme Toggle
  const themeToggle = document.getElementById('theme-toggle');
  themeToggle.addEventListener('click', () => {
    document.body.classList.toggle('dark-mode');
  });

  // Load News Dynamically
  const newsSection = document.getElementById('news-section');
  const blogsSection = document.getElementById('blogs-section');
  
  const newsData = [
    { title: "Global Market Insights", description: "Latest market trends and updates.", image: "images/news1.jpg" },
    { title: "Tech Revolution", description: "Discover the latest innovations in technology.", image: "images/news2.jpg" },
    { title: "Climate Change", description: "Explore the latest on climate change and solutions.", image: "images/news3.jpg" }
  ];
  
  const blogsData = [
    { title: "How to Stay Productive", description: "Tips to make the most out of your day.", image: "images/blog1.jpg" },
    { title: "Travel on a Budget", description: "Explore the world without breaking the bank.", image: "images/blog2.jpg" },
    { title: "Healthy Living", description: "Simple steps to a healthier lifestyle.", image: "images/blog3.jpg" }
  ];

  newsData.forEach(item => {
    newsSection.innerHTML += `
      <div class="news-card">
        <img src="${item.image}" alt="News">
        <h3>${item.title}</h3>
        <p>${item.description}</p>
        <a href="#">Read More</a>
      </div>
    `;
  });

  blogsData.forEach(item => {
    blogsSection.innerHTML += `
      <article class="blog-card">
        <img src="${item.image}" alt="Blog">
        <h3>${item.title}</h3>
        <p>${item.description}</p>
        <a href="#">Read More</a>
      </article>
    `;
  });
});










