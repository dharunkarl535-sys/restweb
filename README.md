# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ANNAPOORANI RESTAURANT</title>
    <style>
        body {
            background-color: #FFF8F0;
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: #4B1D0F;
        }
        header {
            background-color: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 30px 10px 20px 10px;
        }
        nav {
            background-color: #F39237;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: #4B1D0F;
            text-align: center;
            padding: 16px 36px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            background-color: #FFD166;
            color: #B23A48;
        }
        .banner {
            width: 100%;
            height: 360px;
            background-image: url(https://t4.ftcdn.net/jpg/04/17/20/73/360_F_417207342_G7LYJqMP12em9M6szV1rEaUEGuVwBEYH.jpg);
            background-size: cover;
            background-position: center;
        }
        .container {
            max-width: 1000px;
            margin: 40px auto;
            padding: 24px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 24px rgba(180,58,72,0.07);
        }
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 22px;
        }
        .menu-item {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            padding: 20px 12px;
            text-align: center;
        }
        .menu-item img {
            width: 90px;
            height: 70px;
            object-fit: cover;
            border-radius: 8px;
        }
        .admin-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
            margin-top: 18px;
        }
        .admin-card {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            text-align: center;
            padding: 24px 12px;
        }
        .admin-card img {
            width: 78px;
            height: 78px;
            border-radius: 50%;
            object-fit: cover;
        }
        footer {
            background: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 18px 0 8px 0;
            position: relative;
        }
        .active {
            background-color: #FFD166;
            color: #B23A48 !important;
        }
        @media (max-width: 800px) {
            .menu-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .admin-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        @media (max-width: 500px) {
            .menu-grid, .admin-grid {
                grid-template-columns: 1fr;
            }
            nav a {
                float: none;
                display: block;
            }
        }
    </style>
    <script>
        function showPage(pageId) {
            document.querySelectorAll('.container').forEach(c=>c.style.display='none');
            document.getElementById(pageId).style.display = 'block';
            document.querySelectorAll('nav a').forEach(a=>a.classList.remove('active'));
            document.getElementById('nav-' + pageId).classList.add('active');
        }
        window.onload = function() {
            showPage('home');
        }
    </script>
</head>
<body>
    <header>
        <div class="banner"></div>
        <h1>ANNAPOORANI RESTAURENT</h1>
        <p>Nourish Your Body, Feed Your Soul!</p>
    </header>
    <nav>
        <a id="nav-home" href="#" onclick="showPage('home');return false;">Home</a>
        <a id="nav-menu" href="#" onclick="showPage('menu');return false;">Menu</a>
        <a id="nav-admin" href="#" onclick="showPage('admin');return false;">Administration</a>
        <a id="nav-contact" href="#" onclick="showPage('contact');return false;">Contact Us</a>
    </nav>
    <div id="home" class="container">
        <h2>Welcome. Discover the art of vegetarian cuisine!</h2>
        <p>Welcome to our pure vegetarian hotel, where every dish is a celebration of fresh, flavorful ingredients. We invite you to experience a culinary journey that delights the senses with our traditional recipes and innovative creations, all crafted with passion and care. Whether you're a lifelong vegetarian or simply curious, we promise a wholesome and satisfying dining experience that will leave you feeling nourished and refreshed. </p>
    </div>
    <div id="menu" class="container" style="display:none;">
        <h2>Our Menu</h2>
        <div class="menu-grid">
            <div class="menu-item"><img src="c:\Users\acer\Downloads\MASAL.jpg"><br>MASAL DOSA<br>₹120</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\gheedosa.webp"><br>GHEE ROST<br>₹140</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\PODI.jpg"><br>PODI DOSA<br>₹130</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\CholaPoori.webp"><br>CHOLA PURI<br>₹150</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\easy-vegetable-biryani.jpg"><br>VEG BIRIYANI<br>₹145</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\chilli-parotta-feat.jpg"><br>CHILLI PAROTTA<br>₹100</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\paneer-butter-masala-recipe-step-by-step-instructions.jpg"><br>PANNER BUTTER MASALA<br>₹90</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\best_quick_easy_veg_mushroom_biryani.jpg"><br>MUSHROOM BIRIYANI<br>₹150</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\Vegetable-Burger.webp"><br>VEG Burger<br>₹170</div>
            <div class="menu-item"><img src="c:\Users\acer\Downloads\Homemade-French-Fries_8.jpg"><br>FRENCH Fries<br>₹110</div>
            
        </div>
    </div>
    <div id="admin" class="container" style="display:none;">
        <h2>Administration</h2>
        <div class="admin-grid">
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\vijay.jpg">
                <b>Vijay</b><br>
                Manager
            </div>
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\1 chechef.jpg">
                <b>Sanjeev Kapoor</b><br>
                Head Chef
            </div>
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\ld cook.jpg">
                <b>K.Damodharan</b><br>
                Lead Cook
            </div>
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\mg.webp">
                <b>Anjali</b><br>
                Marketing Head
            </div>
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\li.jpg">
                <b>Lingesh</b><br>
                Finance Manager
            </div>
            <div class="admin-card">
                <img src="c:\Users\acer\Downloads\fm.jpg">
                <b>Kruthika</b><br>
                Customer Relations
            </div>
        </div>
    </div>
    <div id="contact" class="container" style="display:none;">
        <h2>Contact Us</h2>
        <p><b>Address:</b> 53 BANGALA STREET, PANRUTI, CUDDALORE, 607 207</p>
        <p><b>Phone:</b> +91-9876543210</p>
        <p><b>Email:</b> info@Annapoorani.com</p>
        <p>We welcome all your feedback and enquiries!</p>
    </div>
    <footer>
        &copy; 2025 Annapoorani RESTAURENT.
    </footer>
</body>
</html>


## OUTPUT:

<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/1958c081-60e3-4556-8fb1-1608f3aff6e6" />
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/878277a5-2c80-4b47-a415-326b5d764814" />

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
