k<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Discover the best bikes at our showroom. Explore sports bikes, cruisers, electric bikes, and more with easy booking and test rides.">
    <meta name="keywords" content="bike showroom, motorcycles, sports bikes, electric bikes, test ride booking">
    <title>Bike Showroom - Your Dream Ride Awaits</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Roboto', sans-serif; background-color: #121212; color: #fff; }
        .hero { background: linear-gradient(135deg, #000, #333); height: 100vh; display: flex; align-items: center; justify-content: center; text-align: center; position: relative; overflow: hidden; }
        .hero::before { content: ''; background: url('https://source.unsplash.com/1600x900/?motorcycle') no-repeat center/cover; position: absolute; top: 0; left: 0; width: 100%; height: 100%; opacity: 0.5; z-index: -1; }
        .hero h1 { font-size: 3rem; animation: fadeIn 2s; }
        .hero p { font-size: 1.2rem; margin-bottom: 2rem; }
        .btn-custom { background: #ff0000; border: none; padding: 10px 20px; color: #fff; transition: 0.3s; }
        .btn-custom:hover { background: #cc0000; transform: scale(1.05); }
        .section { padding: 60px 0; }
        .bike-card { background: #1e1e1e; border-radius: 10px; padding: 20px; margin: 10px; transition: 0.3s; box-shadow: 0 4px 8px rgba(0,0,0,0.3); }
        .bike-card:hover { transform: translateY(-5px); }
        .compare-btn { background: #ff0000; color: #fff; border: none; padding: 5px 10px; margin-top: 10px; }
        .promo-card { background: #ff0000; color: #fff; padding: 20px; border-radius: 10px; text-align: center; }
        .testimonial { background: #1e1e1e; padding: 20px; border-radius: 10px; margin: 10px; }
        .map { height: 400px; background: #333; display: flex; align-items: center; justify-content: center; color: #fff; }
        .form-control { background: #1e1e1e; color: #fff; border: 1px solid #555; }
        .form-control:focus { background: #1e1e1e; color: #fff; border-color: #ff0000; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @media (max-width: 768px) { .hero h1 { font-size: 2rem; } }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">Bike Showroom</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#catalogue">Catalogue</a></li>
                    <li class="nav-item"><a class="nav-link" href="#booking">Booking</a></li>
                    <li class="nav-item"><a class="nav-link" href="#locator">Locator</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                    <li class="nav-item"><a class="nav-link" href="#offers">Offers</a></li>
                    <li class="nav-item"><a class="nav-link" href="#store">Store</a></li>
                    <li class="nav-item"><a class="nav-link" href="#testimonials">Reviews</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <section id="home" class="hero">
        <div class="container">
            <h1>Welcome to Bike Showroom</h1>
            <p>Discover your perfect ride with our premium collection of bikes.</p>
            <a href="#catalogue" class="btn btn-custom">Explore Bikes</a>
        </div>
    </section>

    <section id="catalogue" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Bike Catalogue</h2>
            <div class="mb-3">
                <select class="form-select" id="categoryFilter">
                    <option>All</option>
                    <option>Sports Bikes</option>
                    <option>Cruisers</option>
                    <option>Electric Bikes</option>
                </select>
            </div>
            <div class="row" id="bikeGrid">
                <div class="col-md-4 bike-card" data-category="Sports Bikes">
                    <img src="https://source.unsplash.com/400x300/?sports-bike" alt="Sports Bike" class="img-fluid mb-3">
                    <h5>Sports Bike Model X</h5>
                    <p>Engine: 1000cc, Top Speed: 200km/h, Price: $15,000</p>
                    <button class="compare-btn" onclick="addToCompare('Sports Bike Model X')">Add to Compare</button>
                    <a href="#product" class="btn btn-custom mt-2">View Details</a>
                </div>
                <div class="col-md-4 bike-card" data-category="Cruisers">
                    <img src="https://source.unsplash.com/400x300/?cruiser-bike" alt="Cruiser Bike" class="img-fluid mb-3">
                    <h5>Cruiser Model Y</h5>
                    <p>Engine: 1200cc, Top Speed: 180km/h, Price: $12,000</p>
                    <button class="compare-btn" onclick="addToCompare('Cruiser Model Y')">Add to Compare</button>
                    <a href="#product" class="btn btn-custom mt-2">View Details</a>
                </div>
                <div class="col-md-4 bike-card" data-category="Electric Bikes">
                    <img src="https://source.unsplash.com/400x300/?electric-bike" alt="Electric Bike" class="img-fluid mb-3">
                    <h5>Electric Model Z</h5>
                    <p>Battery: 100km range, Top Speed: 120km/h, Price: $10,000</p>
                    <button class="compare-btn" onclick="addToCompare('Electric Model Z')">Add to Compare</button>
                    <a href="#product" class="btn btn-custom mt-2">View Details</a>
                </div>
            </div>
            <div id="compareSection" class="mt-4" style="display:none;">
                <h4>Compare Bikes</h4>
                <ul id="compareList"></ul>
            </div>
        </div>
    </section>

    <section id="product" class="section" style="display:none;">
        <div class="container">
            <h2>Bike Details</h2>
            <img src="https://source.unsplash.com/600x400/?motorcycle" alt="Bike" class="img-fluid mb-3">
            <p>Features: High-performance engine, advanced suspension, LED lights.</p>
            <div class="reviews">
                <h5>Reviews</h5>
                <p>★★★★★ Excellent ride! - John Doe</p>
            </div>
        </div>
    </section>

    <section id="booking" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Book a Test Ride or Service</h2>
            <form id="bookingForm">
                <div class="row">
                    <div class="col-md-6 mb-3"><input type="text" class="form-control" placeholder="Name" required></div>
                    <div class="col-md-6 mb-3"><input type="email" class="form-control" placeholder="Email" required></div>
                    <div class="col-md-6 mb-3"><input type="tel" class="form-control" placeholder="Phone" required></div>
                    <div class="col-md-6 mb-3"><select class="form-select" required><option>Select Bike</option><option>Sports Bike</option></select></div>
                    <div class="col-md-6 mb-3"><input type="datetime-local" class="form-control" required></div>
                    <div class="col-md-6 mb-3"><button type="submit" class="btn btn-custom w-100">Book Now</button></div>
                </div>
            </form>
        </div>
    </section>

    <section id="locator" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Find a Dealer</h2>
            <input type="text" class="form-control mb-3" placeholder="Enter city or zip">
            <div class="map">Interactive Map Placeholder (Integrate Google Maps API here)</div>
            <p>Nearest Location: 123 Bike St, City, State - Open 9AM-9PM</p>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Contact Us</h2>
            <form id="contactForm">
                <div class="row">
                    <div class="col-md-6 mb-3"><input type="text" class="form-control" placeholder="Name" required></div>
                    <div class="col-md-6 mb-3"><input type="email" class="form-control" placeholder="Email" required></div>
                    <div class="col-md-12 mb-3"><textarea class="form-control" rows="4" placeholder="Message" required></textarea></div>
                    <div class="col-md-12"><button type="submit" class="btn btn-custom">Send Message</button></div>
                </div>
            </form>
            <p class="mt-3">Phone: (123) 456-7890 | Email: info@bikeshowroom.com</p>
        </div>
    </section>

    <section id="offers" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Offers & Promotions</h2>
            <div class="row">
                <div class="col-md-4 promo-card">
                    <h5>20% Off Electric Bikes</h5>
                    <p>Limited time offer!</p>
                </div>
                <div class="col-md-4 promo-card">
                    <h5>Free Helmet with Purchase</h5>
                    <p>On select models.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="store" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Online Store</h2>
            <div class="row">
                <div class="col-md-4 bike-card">
                    <img src="https://source.unsplash.com/400x300/?helmet" alt="Helmet" class="img-fluid mb-3">
                    <h5>Safety Helmet</h5>
                    <p>$50</p>
                    <button class="btn btn-custom">Add to Cart</button>
                </div>
                <div class="col-md-4 bike-card">
                    <img src="https://source.unsplash.com/400x300/?bike-gear" alt="Gear" class="img-fluid mb-3">
                    <h5>Bike Gear Set</h5>
                    <p>$100</p>
                    <button class="btn btn-custom">Add to Cart</button>
                </div>
            </div>
        </div>
    </section>

    <section id="testimonials" class="section">
        <div class="container">
            <h2 class="text-center mb-4">Customer Testimonials</h2>
            <div class="row">
                <div class="col-md-4 testimonial">
                    <p>"Best bikes and service ever!" - Jane Smith</p>
                </div>
                <div class="col-md-4 testimonial">
                    <p>"Loved the test ride experience." - Mike Johnson</p>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-dark text-center py-3">
        <p>&copy; 2023 Bike Showroom. All rights reserved.</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Filter bikes
        document.getElementById('categoryFilter').addEventListener('change', function() {
            const category = this.value;
            const cards = document.querySelectorAll('.bike-card');
            cards.forEach(card => {
                if (category === 'All' || card.dataset.category === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });

        // Compare feature
        let compareList = [];
        function addToCompare(bike) {
            if (compareList.length < 3 && !compareList.includes(bike)) {
                compareList.push(bike);
                updateCompare();
            }
        }
        function updateCompare() {
            const list = document.getElementById('compareList');
            list.innerHTML = compareList.map(bike => `<li>${bike}</li>`).join('');
            document.getElementById('compareSection').style.display = compareList.length ? 'block' : 'none';
        }

        // Form submissions (placeholder - integrate with backend)
        document.getElementById('bookingForm').addEventListener('submit', e => {
            e.preventDefault();
            alert('Booking submitted! (Integrate with server)');
        });
        document.getElementById('contactForm').addEventListener('submit', e => {
            e.preventDefault();
            alert('Message sent! (Integrate with server)');
        });
    </script>
</body>
</html>
