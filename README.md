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
index.html<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Trend Sphare - Latest Blogs and News">
  <meta name="keywords" content="News, Blogs, Technology, Lifestyle, Trending">
  <title>TREND SPHARE</title>
  <link rel="stylesheet" href="css/styles.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
  <!-- Navbar -->
  <header id="navbar" class="navbar">
    <div class="logo">TREND <span>SPHARE</span></div>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li class="dropdown">
          <a href="#">Categories</a>
          <ul class="dropdown-menu">
            <li><a href="#technology">Technology</a></li>
            <li><a href="#lifestyle">Lifestyle</a></li>
            <li><a href="#sports">Sports</a></li>
          </ul>
        </li>
        <li><a href="#blogs">Blogs</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <button id="theme-toggle" class="theme-toggle">🌙</button>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <video autoplay muted loop id="hero-video">
      <source src="videos/hero-background.mp4" type="video/mp4">
    </video>
    <div class="hero-content">
      <h1>Stay Updated with the Latest Trends</h1>
      <p>Explore trending news and blogs worldwide.</p>
      <a href="#blogs" class="btn">Read More</a>
    </div>
  </section>

  <!-- Blog Section -->
  <section id="blogs" class="blogs">
    <h2>Our Blogs</h2>
    <div class="blog-grid" id="blog-section">
      <!-- Blogs will load dynamically -->
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="quick-links">
      <a href="#home">Home</a>
      <a href="#blogs">Blogs</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="social-icons">
      <a href="#"><i class="fab fa-facebook"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
    </div>
    <button id="back-to-top">Back to Top</button>
  </footer>
  <script src="js/script.js"></script>
</body>
</html>
styles.css/* General Styling */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
.navbar {
  position: sticky;
  top: 0;
  background: #333;
  color: white;
  padding: 10px 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 1000;
}
.navbar a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
}
.navbar .dropdown-menu {
  display: none;
  position: absolute;
  background: white;
  color: black;
  list-style: none;
  margin-top: 10px;
  padding: 10px;
  border-radius: 5px;
}
.navbar .dropdown:hover .dropdown-menu {
  display: block;
}
.hero {
  position: relative;
  height: 100vh;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
#hero-video {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -1;
}
.blog-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  padding: 20px;
}
footer {
  background: #222;
  color: white;
  padding: 20px;
  text-align: center;
}
footer .quick-links a, footer .social-icons a {
  color: white;
  text-decoration: none;
  margin: 0 10px;
}
script.jsdocument.addEventListener('DOMContentLoaded', () => {
  // Dark Mode Toggle
  const themeToggle = document.getElementById('theme-toggle');
  themeToggle.addEventListener('click', () => {
    document.body.classList.toggle('dark-mode');
  });

  // Dynamic Blog Loading
  const blogSection = document.getElementById('blog-section');
  const blogs = [
    { title: "Tech Trends 2024", category: "Technology", author: "John Doe", date: "Dec 25, 2024" },
    { title: "Healthy Living Tips", category: "Lifestyle", author: "Jane Smith", date: "Dec 24, 2024" },
  ];
  blogs.forEach(blog => {
    blogSection.innerHTML += `
      <div class="blog-card">
        <h3>${blog.title}</h3>
        <p>Category: ${blog.category}</p>
        <p>Author: ${blog.author}</p>
        <p>Date: ${blog.date}</p>
      </div>
    `;
  });

  // Back to Top
  const backToTop = document.getElementById('back-to-top');
  backToTop.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
});
<<script async src="https://www.googletagmanager.com/gtag/js?id=UA-XXXXXXXXX-X"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'UA-XXXXXXXXX-X');
</script>>





























