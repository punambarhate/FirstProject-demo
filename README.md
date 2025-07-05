# FirstProject-demo
this is my first repository
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flipkart Clone - Online Shopping Site</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f1f3f6;
        }
        
        /* Header Styles */
        .header {
            background-color: #2874f0;
            color: white;
            padding: 12px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 24px;
        }
        
        .logo .plus {
            font-size: 12px;
            font-style: italic;
            margin-top: -10px;
            color: #ffe500;
        }
        
        .search-bar {
            display: flex;
            width: 50%;
        }
        
        .search-bar input {
            width: 100%;
            padding: 10px 15px;
            border: none;
            outline: none;
            font-size: 14px;
        }
        
        .search-bar button {
            background-color: white;
            border: none;
            padding: 0 15px;
            color: #2874f0;
            cursor: pointer;
        }
        
        .login-btn {
            background-color: white;
            color: #2874f0;
            padding: 8px 20px;
            border: none;
            border-radius: 2px;
            font-weight: 600;
            cursor: pointer;
        }
        
        .nav-links {
            display: flex;
            align-items: center;
            gap: 25px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 16px;
            font-weight: 500;
        }
        
        /* Categories Section */
        .categories {
            background-color: white;
            padding: 15px 0;
            box-shadow: 0 1px 1px 0 rgba(0,0,0,0.16);
        }
        
        .categories-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
        }
        
        .category-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
        }
        
        .category-item img {
            width: 64px;
            height: 64px;
            object-fit: contain;
        }
        
        .category-item span {
            font-size: 14px;
            margin-top: 5px;
            text-align: center;
        }
        
        /* Banner Section */
        .banner {
            max-width: 1200px;
            margin: 15px auto;
        }
        
        .banner img {
            width: 100%;
            height: auto;
            border-radius: 3px;
        }
        
        /* Products Section */
        .products-section {
            max-width: 1200px;
            margin: 15px auto;
            background-color: white;
            padding: 15px;
        }
        
        .section-title {
            font-size: 24px;
            font-weight: 500;
            margin-bottom: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .view-all {
            color: #2874f0;
            font-size: 14px;
            font-weight: 500;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
        }
        
        .product-card {
            padding: 15px;
            border: 1px solid #f0f0f0;
            cursor: pointer;
            transition: box-shadow 0.3s;
        }
        
        .product-card:hover {
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        
        .product-image {
            text-align: center;
            height: 180px;
            margin-bottom: 15px;
        }
        
        .product-image img {
            max-width: 100%;
            max-height: 100%;
            object-fit: contain;
        }
        
        .product-title {
            font-size: 14px;
            color: #212121;
            margin-bottom: 8px;
            height: 36px;
            overflow: hidden;
            text-overflow: ellipsis;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
        }
        
        .product-price {
            font-size: 16px;
            font-weight: 600;
            color: #212121;
        }
        
        .product-discount {
            color: #388e3c;
            font-size: 14px;
            margin-left: 8px;
        }
        
        .product-old-price {
            color: #878787;
            text-decoration: line-through;
            font-size: 12px;
            margin-left: 8px;
        }
        
        /* Footer */
        footer {
            background-color: #172337;
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }
        
        .footer-column h3 {
            font-size: 14px;
            color: #878787;
            margin-bottom: 20px;
            text-transform: uppercase;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: white;
            text-decoration: none;
            font-size: 12px;
        }
        
        .copyright {
            border-top: 1px solid #454d5e;
            padding-top: 20px;
            text-align: center;
            font-size: 12px;
            color: #878787;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                padding: 0 15px;
            }
            
            .search-bar {
                width: 100%;
                margin: 10px 0;
            }
            
            .nav-links {
                width: 100%;
                justify-content: space-between;
                margin-top: 10px;
            }
            
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .footer-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-container">
            <div class="logo">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0b9d4020-c089-4447-8f8e-6b39733e5f68.png" alt="Flipkart logo in white text on blue background">
                <span class="plus">Plus</span>
            </div>
            
            <div class="search-bar">
                <input type="text" placeholder="Search for products, brands and more">
                <button><i class="fas fa-search"></i></button>
            </div>
            
            <div class="nav-links">
                <a href="#" class="login-btn">Login</a>
                <a href="#">Become a Seller</a>
                <a href="#">More <i class="fas fa-chevron-down"></i></a>
                <a href="#"><i class="fas fa-shopping-cart"></i> Cart</a>
            </div>
        </div>
    </header>
    
    <!-- Categories -->
    <section class="categories">
        <div class="categories-container">
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3ef974b7-f12e-4201-a676-a09ac616fe16.png" alt="Grocery category icon with grocery basket illustration">
                <span>Grocery</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ca5a7d93-eb3d-4835-8c2b-e4e31f7ffb42.png" alt="Mobile phone category icon with smartphone illustration">
                <span>Mobiles</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/56063a16-1fd2-4c48-99d1-c58a6c7d4203.png" alt="Fashion category icon with clothing hanger illustration">
                <span>Fashion</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/71b5ab7e-9ebe-4b05-826a-5a4b916add35.png" alt="Electronics category icon with laptop illustration">
                <span>Electronics</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f5221532-f56a-4d6e-8f19-4360f0455fb6.png" alt="Home category icon with house illustration">
                <span>Home</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ac5ca805-d634-41c1-b560-4784f9f9fe04.png" alt="Appliances category icon with washing machine illustration">
                <span>Appliances</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/34233053-d806-44b7-9379-f2ab9a651445.png" alt="Travel category icon with airplane illustration">
                <span>Travel</span>
            </div>
            <div class="category-item">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/1a6a51ac-a798-426a-89a7-415822f628f6.png" alt="Beauty category icon with cosmetic products illustration">
                <span>Beauty</span>
            </div>
        </div>
    </section>
    
    <div class="banner">
        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7a8a4f83-94f9-4872-868e-542ef7228c74.png" alt="Flipkart Big Billion Days sale banner with deals and discounts text in blue and white">
    </div>
    
    <section class="products-section">
        <h2 class="section-title">Deals of the Day <a href="#" class="view-all">VIEW ALL</a></h2>
        
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0abbd5ed-159b-433f-a1a9-27d34dfd6864.png" alt="Latest model smartphone with full screen display in black color">
                </div>
                <h3 class="product-title">Brand Smartphone X with 128GB Storage and 36MP Camera</h3>
                <div class="product-price">₹24,999 <span class="product-discount">20% off</span> <span class="product-old-price">₹31,990</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f4cdad72-78ff-4a23-b90b-91750dcca9d1.png" alt="Premium wireless headphones in white with noise cancellation feature">
                </div>
                <h3 class="product-title">Premium Wireless Headphones with 40hr Battery Life</h3>
                <div class="product-price">₹3,999 <span class="product-discount">45% off</span> <span class="product-old-price">₹7,290</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3cc6b291-351e-4197-b30f-6bb60cf5ff85.png" alt="Fitness smartwatch with heart rate monitor and OLED display">
                </div>
                <h3 class="product-title">Fitness Smart Watch with Heart Rate & Blood Oxygen Monitor</h3>
                <div class="product-price">₹1,799 <span class="product-discount">60% off</span> <span class="product-old-price">₹4,500</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/4cee6ea4-a8f7-4f1c-9362-68a0d95a2bfe.png" alt="Kitchen blender with multiple speed settings and stainless steel blades">
                </div>
                <h3 class="product-title">500W Mixer Grinder with 3 Jars & Stainless Steel Blades</h3>
                <div class="product-price">₹2,299 <span class="product-discount">35% off</span> <span class="product-old-price">₹3,540</span></div>
            </div>
        </div>
    </section>
    
    <section class="products-section">
        <h2 class="section-title">Trending Offers <a href="#" class="view-all">VIEW ALL</a></h2>
        
        <div class="products-grid">
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/9fd701db-c49e-47ba-a3e0-8d0434652b7d.png" alt="55 inch 4K Ultra HD Smart LED Television with HDR">
                </div>
                <h3 class="product-title">55 inch 4K Ultra HD Smart LED Television with HDR</h3>
                <div class="product-price">₹42,990 <span class="product-discount">25% off</span> <span class="product-old-price">₹56,990</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3419fad3-171b-48c1-b3c6-046ff8ede093.png" alt="Powerful air cooler for rooms up to 250 sq ft with remote control">
                </div>
                <h3 class="product-title">Powerful Air Cooler for Rooms up to 250 sq ft with Remote</h3>
                <div class="product-price">₹12,499 <span class="product-discount">30% off</span> <span class="product-old-price">₹17,790</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/c55785a7-1eaa-4304-8b41-cea71c3e0e38.png" alt="Waterproof laptop backpack with USB charging port and anti-theft design">
                </div>
                <h3 class="product-title">Waterproof Laptop Backpack with USB Charging Port (15.6")</h3>
                <div class="product-price">₹899 <span class="product-discount">55% off</span> <span class="product-old-price">₹1,990</span></div>
            </div>
            
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/95307e32-a119-4fb1-a74a-9d60b1097c01.png" alt="Water resistant fitness tracker with color display and activity tracking">
                </div>
                <h3 class="product-title">Water Resistant Fitness Band with Color Display</h3>
                <div class="product-price">₹1,299 <span class="product-discount">50% off</span> <span class="product-old-price">₹2,599</span></div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <h3>about</h3>
                <ul>
                    <li><a href="#">Contact Us</a></li>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Careers</a></li>
                    <li><a href="#">Stories</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>help</h3>
                <ul>
                    <li><a href="#">Payments</a></li>
                    <li><a href="#">Shipping</a></li>
                    <li><a href="#">Cancellation & Returns</a></li>
                    <li><a href="#">FAQ</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>consumer policy</h3>
                <ul>
                    <li><a href="#">Return Policy</a></li>
                    <li><a href="#">Terms of Use</a></li>
                    <li><a href="#">Security</a></li>
                    <li><a href="#">Privacy</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>mail us</h3>
                <ul>
                    <li>Flipkart Clone,</li>
                    <li>abc xyz &</li>
                    <li>...........,</li>
                    <li>jalgoan 443556</li>
                </ul>
            </div>
        </div>
        
        <div class="copyright">
            © 2025 Flipkart Clone. All Rights Reserved
        </div>
    </footer>
    
    <script>
        // Simple JavaScript for some interactivity
        document.addEventListener('DOMContentLoaded', function() {
            // Add active class to clicked category
            const categories = document.querySelectorAll('.category-item');
            categories.forEach(category => {
                category.addEventListener('click', function() {
                    categories.forEach(c => c.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Login button hover effect
            const loginBtn = document.querySelector('.login-btn');
            if(loginBtn) {
                loginBtn.addEventListener('mouseenter', function() {
                    this.style.backgroundColor = '#f0f0f0';
                });
                loginBtn.addEventListener('mouseleave', function() {
                    this.style.backgroundColor = 'white';
                });
            }
        });
    </script>
</body>
</html>

