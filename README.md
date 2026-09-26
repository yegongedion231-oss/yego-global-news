# yego-global-news<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Yego Global News | The World. Your News.</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: #f4f5f7;
    color: #111;
    line-height: 1.6;
}

header {
    background: #111;
    color: white;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.topbar {
    max-width: 1200px;
    margin: auto;
    padding: 18px 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 27px;
    font-weight: 800;
}

.logo span {
    color: #e31b23;
}

.tagline {
    font-size: 12px;
    color: #ccc;
}

.menu-btn {
    display: none;
    font-size: 25px;
    cursor: pointer;
}

nav {
    background: #e31b23;
}

nav ul {
    max-width: 1200px;
    margin: auto;
    display: flex;
    list-style: none;
    overflow-x: auto;
}

nav li a {
    display: block;
    padding: 13px 16px;
    color: white;
    text-decoration: none;
    font-weight: bold;
    white-space: nowrap;
}

nav li a:hover {
    background: #b80008;
}

.breaking {
    background: #fff;
    border-bottom: 1px solid #ddd;
    display: flex;
    align-items: center;
    overflow: hidden;
}

.breaking strong {
    background: #e31b23;
    color: white;
    padding: 10px 18px;
    white-space: nowrap;
}

.ticker {
    padding-left: 20px;
    white-space: nowrap;
    animation: ticker 18s linear infinite;
}

@keyframes ticker {
    from { transform: translateX(100%); }
    to { transform: translateX(-100%); }
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 25px 20px;
}

.hero {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 20px;
    margin-bottom: 30px;
}

.hero-main {
    min-height: 360px;
    background:
        linear-gradient(rgba(0,0,0,.25), rgba(0,0,0,.8)),
        url("https://images.unsplash.com/photo-1521295121783-8a321d551ad2?auto=format&fit=crop&w=1200&q=80")
        center/cover;
    color: white;
    padding: 30px;
    display: flex;
    align-items: end;
    border-radius: 10px;
}

.hero-main h1 {
    font-size: 38px;
    line-height: 1.15;
}

.category {
    display: inline-block;
    background: #e31b23;
    color: white;
    padding: 5px 10px;
    font-size: 12px;
    font-weight: bold;
    margin-bottom: 10px;
    border-radius: 3px;
}

.side-stories {
    display: grid;
    gap: 20px;
}

.side-card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    border-left: 5px solid #e31b23;
}

.side-card h3 {
    margin-top: 8px;
}

.section-title {
    border-left: 6px solid #e31b23;
    padding-left: 12px;
    margin: 30px 0 18px;
    font-size: 25px;
}

.news-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.card {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0,0,0,.08);
    transition: .2s;
}

.card:hover {
    transform: translateY(-4px);
}

.card img {
    width: 100%;
    height: 190px;
    object-fit: cover;
}

.card-content {
    padding: 17px;
}

.card h3 {
    font-size: 19px;
    margin: 8px 0;
}

.card p {
    color: #666;
    font-size: 14px;
}

.read-more {
    display: inline-block;
    margin-top: 12px;
    color: #e31b23;
    font-weight: bold;
    text-decoration: none;
}

.video-section {
    background: #111;
    color: white;
    padding: 30px;
    border-radius: 10px;
    margin-top: 35px;
}

.video-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.video {
    background: #222;
    padding: 25px;
    border-radius: 8px;
}

.video-icon {
    font-size: 40px;
    margin-bottom: 10px;
}

.newsletter {
    background: #e31b23;
    color: white;
    padding: 35px;
    text-align: center;
    margin-top: 35px;
    border-radius: 10px;
}

.newsletter input {
    padding: 13px;
    width: 60%;
    max-width: 450px;
    border: none;
    margin-top: 15px;
}

.newsletter button {
    padding: 13px 20px;
    border: none;
    cursor: pointer;
    font-weight: bold;
}

.search-box {
    display: flex;
    margin: 20px 0;
}

.search-box input {
    flex: 1;
    padding: 14px;
    border: 1px solid #ccc;
}

.search-box button {
    background: #111;
    color: white;
    border: none;
    padding: 0 20px;
}

footer {
    background: #111;
    color: white;
    margin-top: 40px;
    padding: 40px 20px;
}

.footer-inner {
    max-width: 1200px;
    margin: auto;
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    gap: 30px;
}

footer a {
    color: #ddd;
    text-decoration: none;
    display: block;
    margin: 5px 0;
}

.copyright {
    text-align: center;
    margin-top: 30px;
    padding-top: 20px;
    border-top: 1px solid #333;
    color: #aaa;
}

/* Mobile */
@media(max-width: 768px) {

    .tagline {
        display: none;
    }

    .menu-btn {
        display: block;
    }

    nav ul {
        display: none;
        flex-direction: column;
    }

    nav ul.show {
        display: flex;
    }

    .hero {
        grid-template-columns: 1fr;
    }

    .hero-main {
        min-height: 300px;
    }

    .hero-main h1 {
        font-size: 28px;
    }

    .news-grid,
    .video-grid,
    .footer-inner {
        grid-template-columns: 1fr;
    }

    .newsletter input {
        width: 100%;
    }

    .newsletter button {
        margin-top: 10px;
    }
}
</style>
</head>

<body>

<header>

    <div class="topbar">
        <div>
            <div class="logo">YEGO <span>GLOBAL NEWS</span></div>
            <div class="tagline">The World. Your News.</div>
        </div>

        <div class="menu-btn" onclick="toggleMenu()">☰</div>
    </div>

    <nav>
        <ul id="menu">
            <li><a href="#home">Home</a></li>
            <li><a href="#world">World</a></li>
            <li><a href="#africa">Africa</a></li>
            <li><a href="#kenya">Kenya</a></li>
            <li><a href="#usa">USA</a></li>
            <li><a href="#china">China</a></li>
            <li><a href="#business">Business</a></li>
            <li><a href="#technology">Technology</a></li>
            <li><a href="#defense">Defense</a></li>
            <li><a href="#videos">Videos</a></li>
        </ul>
    </nav>

</header>

<div class="breaking">
    <strong>BREAKING</strong>
    <div class="ticker">
        Latest international developments and major stories from around the world
    </div>
</div>

<main class="container" id="home">

    <div class="search-box">
        <input type="text" id="searchInput"
               placeholder="Search Yego Global News..."
               onkeyup="searchNews()">
        <button>Search</button>
    </div>

    <section class="hero">

        <div class="hero-main">
            <div>
                <span class="category">WORLD</span>
                <h1>Major Global Developments Shape Today's News</h1>
                <p>Stay informed with the latest international stories.</p>
            </div>
        </div>

        <div class="side-stories">

            <article class="side-card">
                <span class="category">AFRICA</span>
                <h3>Important developments across Africa</h3>
                <p>Read the latest regional updates.</p>
            </article>

            <article class="side-card">
                <span class="category">BUSINESS</span>
                <h3>Global economy and markets</h3>
                <p>Follow major business developments.</p>
            </article>

            <article class="side-card">
                <span class="category">TECH</span>
                <h3>New technology changing the world</h3>
                <p>Latest technology and AI stories.</p>
            </article>

        </div>

    </section>

    <section id="world">

        <h2 class="section-title">🌍 World News</h2>

        <div class="news-grid">

            <article class="card">
                <img src="https://images.unsplash.com/photo-1521295121783-8a321d551ad2?auto=format&fit=crop&w=800&q=80">
                <div class="card-content">
                    <span class="category">WORLD</span>
                    <h3>Global leaders discuss major international issues</h3>
                    <p>Follow the latest developments from around the world.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <img src="https://images.unsplash.com/photo-1529107386315-e1a2ed48a620?auto=format&fit=crop&w=800&q=80">
                <div class="card-content">
                    <span class="category">POLITICS</span>
                    <h3>International politics and diplomacy</h3>
                    <p>Important political developments and statements.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <img src="https://images.unsplash.com/photo-1556761175-b413da4baf72?auto=format&fit=crop&w=800&q=80">
                <div class="card-content">
                    <span class="category">ECONOMY</span>
                    <h3>Global business and economic updates</h3>
                    <p>Markets, trade and economic developments.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

        </div>

    </section>

    <section id="africa">

        <h2 class="section-title">🌍 Africa</h2>

        <div class="news-grid">

            <article class="card">
                <div class="card-content">
                    <span class="category">AFRICA</span>
                    <h3>Latest developments across Africa</h3>
                    <p>News covering politics, economy, development and regional affairs.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card" id="kenya">
                <div class="card-content">
                    <span class="category">KENYA</span>
                    <h3>Kenya's latest national developments</h3>
                    <p>Stay updated on major events across Kenya.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">REGIONAL</span>
                    <h3>East Africa news</h3>
                    <p>Important developments from the region.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

        </div>

    </section>

    <section id="business">

        <h2 class="section-title">💰 Business & Economy</h2>

        <div class="news-grid">

            <article class="card">
                <div class="card-content">
                    <span class="category">BUSINESS</span>
                    <h3>Global markets and business</h3>
                    <p>Follow major developments affecting businesses and markets.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">TRADE</span>
                    <h3>International trade developments</h3>
                    <p>Major developments in global trade and commerce.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">AFRICA</span>
                    <h3>African economies</h3>
                    <p>Economic developments across the continent.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

        </div>

    </section>

    <section id="technology">

        <h2 class="section-title">🤖 Technology & AI</h2>

        <div class="news-grid">

            <article class="card">
                <div class="card-content">
                    <span class="category">AI</span>
                    <h3>Artificial Intelligence</h3>
                    <p>Discover the latest developments in AI and technology.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">TECH</span>
                    <h3>New technology</h3>
                    <p>Technology innovations changing everyday life.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">SPACE</span>
                    <h3>Space and science</h3>
                    <p>Explore important developments in science and space.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

        </div>

    </section>

    <section id="defense">

        <h2 class="section-title">🪖 Defense & Security</h2>

        <div class="news-grid">

            <article class="card">
                <div class="card-content">
                    <span class="category">SECURITY</span>
                    <h3>International security developments</h3>
                    <p>Follow documented developments in global security and diplomacy.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">DEFENSE</span>
                    <h3>Defense technology</h3>
                    <p>News about defense systems and international security affairs.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

            <article class="card">
                <div class="card-content">
                    <span class="category">DIPLOMACY</span>
                    <h3>International diplomacy</h3>
                    <p>Major diplomatic developments around the world.</p>
                    <a class="read-more" href="#">Read More →</a>
                </div>
            </article>

        </div>

    </section>

    <section id="videos" class="video-section">

        <h2>🎥 Yego Global News Videos</h2>

        <div class="video-grid">

            <div class="video">
                <div class="video-icon">▶️</div>
                <h3>Today's Top 10 Global Stories</h3>
                <p>Watch our latest news update.</p>
            </div>

            <div class="video">
                <div class="video-icon">▶️</div>
                <h3>Global News in 60 Seconds</h3>
                <p>Quick updates on major stories.</p>
            </div>

            <div class="video">
                <div class="video-icon">▶️</div>
                <h3>Africa News Update</h3>
                <p>Latest stories from Africa.</p>
            </div>

        </div>

    </section>

    <section class="newsletter">

        <h2>📩 Get Yego Global News Updates</h2>

        <p>Subscribe to receive important news directly in your inbox.</p>

        <form onsubmit="subscribe(event)">
            <input type="email" id="email"
                   placeholder="Enter your email address"
                   required>
            <button type="submit">SUBSCRIBE</button>
        </form>

    </section>

</main>

<footer>

    <div class="footer-inner">

        <div>
            <h2>YEGO GLOBAL NEWS</h2>
            <p>The World. Your News.</p>
            <p>Independent digital news covering Kenya, Africa and the world.</p>
        </div>

        <div>
            <h3>Sections</h3>
            <a href="#world">World</a>
            <a href="#africa">Africa</a>
            <a href="#kenya">Kenya</a>
            <a href="#business">Business</a>
            <a href="#technology">Technology</a>
        </div>

        <div>
            <h3>Contact</h3>
            <p>📱 0722310256</p>
            <p>📧 Contact Yego Global News</p>
            <p>▶️ YouTube</p>
            <p>🎵 TikTok</p>
        </div>

    </div>

    <div class="copyright">
        © 2026 Yego Global News. All rights reserved.
    </div>

</footer>

<script>

function toggleMenu() {
    document.getElementById("menu").classList.toggle("show");
}

function searchNews() {

    const input = document
        .getElementById("searchInput")
        .value
        .toLowerCase();

    const cards = document.querySelectorAll(".card");

    cards.forEach(card => {

        const text = card.innerText.toLowerCase();

        if (text.includes(input)) {
            card.style.display = "";
        } else {
            card.style.display = "none";
        }

    });
}

function subscribe(event) {

    event.preventDefault();

    const email = document.getElementById("email").value;

    alert(
        "Thank you for subscribing to Yego Global News!\\n\\n" +
        "Subscription received for: " + email
    );

    document.getElementById("email").value = "";

}

</script>

</body>
</html>
