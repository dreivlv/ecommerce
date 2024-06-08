# ecommerce

<!DOCTYPE html>
<html>
<head>
    <title>E-COMMERCE</title>
    <style>
        body {
            position: relative;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            color: white;
            background: url(hotdogbg.jpg) no-repeat center center fixed;
            background-size: cover;
        }

        .topnav {
            overflow: hidden;
            background-color: rgba(73, 222, 70, 0.7); 
            text-align: left; 
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 20px 0; 
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-links {
            display: flex;
        }

        .button {
            background-color: transparent;
            border: none;
            color: white;
            padding: 24px 30px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 30px; 
            margin: 0;
            cursor: pointer;
            position: relative;
        }

        .button:hover {
            background-color: #ddd;
            color: #050505;
        }

        .search-container {
            display: flex;
            align-items: center;
            margin-right: 20px; 
        }

        .search-input {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 20px;
            font-size: 16px;
            margin-right: 10px;
        }

        .search-button {
            padding: 10px 20px;
            background-color: #4CAF50;
            border: none;
            color: white;
            font-size: 16px;
            border-radius: 20px;
            cursor: pointer;
        }

        .search-button:hover {
            background-color: #45a049;
        }

        .content {
            position: relative;
            z-index: 1;
            padding: 20px;
        }

        .main-images {
            position: absolute;
        }

        .logo {
            top: 160px;
            right: 190px;
            width: 900px;
            height: 500px;
            border-radius: 100%;
        }

        .logo-name {
            top: 490px;
            right: 210px;
            width: 850px;
            height: 250px;
            border-radius: 100%;
        }

        .order-button {
            background-color: rgba(73, 222, 70, 0.8); 
            border: none;
            color: white;
            padding: 15px 62px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 30px;
            font-family: inherit;
            position: absolute;
            top: 670px;
            left: 470px;
            cursor: pointer;
            border-radius: 20px;
            font-weight: bold;
        }

        .order-button:hover {
            background-color: white;
            color: #45a049;
        }

        .sign-in-button {
            background-color: rgba(73, 222, 70, 0.8); 
            border: none;
            color: white;
            padding: 15px 30px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 30px;
            font-family: inherit;
            cursor: pointer;
            border-radius: 20px;
            font-weight: bold;
        }

        .sign-in-button:hover {
            background-color: white;
            color: #45a049;
        }

        section {
            padding: 100px 20px;
            min-height: 100vh;
            box-sizing: border-box;
            background-color: rgba(0, 0, 0, 0.5); 
        }

        #home {
            padding-top: 150px;
        }

        .divider {
            height: 20px;
            background-color: rgb(10, 6, 6); 
            margin: 0; 
            width: 100%; 
            margin: 0 auto; 
        }

        #menu {
            background-color: rgba(0, 0, 0, 0.5); 
        }

        .sub-menu {
            display: none;
            position: absolute;
            background-color: rgba(65, 168, 64, 0.7); 
            min-width: 160px;
            z-index: 1001; 
            top: 0;
            right: 100%;
        }

        .sub-menu a {
            color: rgb(255, 255, 255);
            padding: 12px 16px;
            font-family: Arial, Helvetica, sans-serif;
            font-size: 20px ;
            text-decoration: none;
            display: block;
        }

        .sub-menu a:hover {
            background-color: #ddd;
            color: #050505;
        }

        .button.menu-button:hover .sub-menu {
            display: block;
        }

        .section-container {
            position: relative; 
            z-index: 1;
        }

        .menu-orders {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 50px;
            margin-top: 10px;
        }

        .menu-item {
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 10px;
            overflow: hidden;
            width: 300px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .menu-item button {
            background-color: #5ad160; 
            border: none;
            color: rgb(0, 0, 0);
            padding: 10px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 0 0 10px 10px;
            width: 100%;
            font-weight: bold;
        }

        .menu-item button:hover {
            background-color: white;
            color: #45a049;
        }

        #about {
            background-color: rgba(0, 0, 0, 0.5); 
        }

        #contact {
            background-color: rgba(0, 0, 0, 0.5); 
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .contact-form input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 18px;
        }

        .contact-form button {
            padding: 10px 20px;
            background-color: #4CAF50;
            border: none;
            color: white;
            font-size: 28px;
            border-radius: 5px;
            cursor: pointer;
        }

        .contact-form button:hover {
            background-color: #45a049;
        }

        #log-in {
            background-color: rgba(0, 0, 0, 0.5); 
            
        }

        .log-in-form {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .log-in-form input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 18px;
        }

        .log-in-button {
            padding: 20px 30px;
            background-color: #4CAF50;
            border: none;
            color: white;
            font-size: 30px;
            font-weight: bold;
            border-radius: 5px;
            cursor: pointer;
        }

        .log-in-button:hover {
            background-color: #45a049;
        }

    </style>
</head>
<body>

    <div class="topnav">
        <div class="nav-links">
            <a class="button" href="#home">HOME</a>
            <div class="button menu-button">MENU ▼
                <div class="sub-menu">
                    <a href="#menu1">Menu 1</a>
                    <a href="#menu2">Menu 2</a>
                </div>
            </div>
            <a class="button" href="#about">ABOUT</a>
            <a class="button" href="#contact">CONTACT</a>
            <a class="button" href="#log-in">SIGN-IN</a>
        </div>

        <div class="search-container">
            <input type="text" class="search-input" placeholder="Search...">
            <button class="search-button">Search</button>
        </div>
    </div>

    <section id="home">
        <div class="main-images logo">
            <img src="logobg.png" alt="Logo" style="width: 900px; height: 500px; border-radius: 100%;">
        </div>

        <div class="main-images logo-name">
            <img src="foodfiestalogoname2.png" alt="Logo Name" style="width: 850px; height: 250px; border-radius: 100%;">
        </div>

        <img src="socmed.png" alt="SocMed" style="position: absolute; top: 800px; left: 0px; width: 250px;">

        <a href="#menu1" class="order-button" style="position: absolute; top: 670px; left: 470px; font-weight: bold;">ORDER NOW!</a>
   
        <a href ="#log-in" class="sign-in-button" style="position: absolute; top: 800px; right: 20px; font-weight: bold;">Sign-In</a>
    </section>

    <div class="divider"></div>

    <section id="menu1" class="section-container">
        <h1 style = "font-size: 50px; font-family: Verdana, Geneva, Tahoma, sans-serif; 
        position: absolute; top: 1030px; left: 540px; color: #ffffff;">Menu 1</h1>
        <div class="menu-orders">
            <div class="menu-item">

                <img src="stickdog.jpg" alt="STICKDOG">
                <button>STICKDOG <br> Starts at ₱ 10.00 || ⭐⭐⭐⭐☆</button>
            </div>

            <div class="menu-item">
                <img src="burgerclassic.jpg" alt="BURGER CLASSIC">
                <button>BURGER CLASSIC<br> Starts at ₱ 25.00 || ⭐⭐⭐⭐☆</button>
            </div>

            <div class="menu-item">
                <img src="hamcheesepizza.jpg" alt="HAM&CHEESE PIZZA">
                <button>HAM & CHEESE PIZZA<br> Starts at ₱ 75.00 || ⭐⭐⭐⭐☆</button>
            </div>

            <div class="menu-item">
                <img src="wichdog.jpg" alt="WICHDOG">
                <button>WICHDOG <br> Starts at ₱ 16.00 || <br> ⭐⭐⭐⭐☆</button>
            </div>
            
            <div class="menu-item">
                <img src="Cheeseburger.jpg" alt="CHEESE BURGER">
                <button>CHEESE BURGER<br> Starts at ₱ 35.00 || <br> ⭐⭐⭐⭐☆</button>
            </div>

            <div class="menu-item">
                <img src="hawaiianpizza.jpg" alt="HAWAIIAN PIZZA">
                <button>HAWAIIAN PIZZA<br> Starts at ₱ 89.00 || ⭐⭐⭐⭐⭐</button>
            </div>

            <div class="menu-item">
                <img src="wichdogsupreme.jpg" alt="WICHDOG SUPREME">
                <button>WICHDOG SUPREME<br> Starts at ₱ 30.00 || ⭐⭐⭐⭐⭐</button>
            </div> 

            <div class="menu-item">
                <img src="deluxe burger.jpg" alt="DELUXE BURGER">
                <button>DELUXE BURGER<br> Starts at ₱ 55.00 ||  ⭐⭐⭐⭐⭐</button>
            </div>


            <div class="menu-item">
                <img src="pepperoni.jpg" alt="PEPPERONI">
                <button>PEPPERONI PIZZA<br> Starts at ₱ 99.00 || ⭐⭐⭐⭐⭐</button>
            </div>

        </div>
    </section>

    <div class="divider"></div>

    <section id="menu2" class="section-container">
        <h1 style = "font-size: 50px; font-family: Verdana, Geneva, Tahoma, sans-serif; 
        position: absolute; top: 700px; left: 540px; color: #ffffff;">Menu 2</h1>
        <div class="menu-orders">

            <div class="menu-item">
                <img src="coke.jpg" alt="Coke">
                <button>COKE <br> Starts at ₱ 15.00 || S | M | L || ⭐⭐⭐⭐☆ </button>
            </div>

            <div class="menu-item">
                <img src="iced tea.jpg" alt="Iced Tea">
                <button>ICED TEA LEMON <br> Starts at ₱ 15.00 || S | M | L || ⭐⭐⭐⭐☆ </button>
            </div>
           
            <div class="menu-item">
                <img src="sprite.png" alt="sprite">
                <button>SPRITE <br> Starts at ₱ 15.00 || S | M | L || ⭐⭐⭐⭐⭐</button>
            </div>

            <div class="menu-item">
                <img src="chocobutternut.jpg" alt="chocobutternut">
                <button>CHOCO BUTTERNUT DONUT <br> Starts at ₱ 25.00 || ⭐⭐⭐⭐⭐</button>
            </div>

            <div class="menu-item">
                <img src="heartglazed.jpg" alt="heart glazed donut">
                <button>HEART GLAZED DONUT <br> Starts at ₱ 25.00 || <br> ⭐⭐⭐☆☆</button>
            </div>

            <div class="menu-item">
                <img src="bavarian cream donut.jpg" alt="bavarian cream donut">
                <button>BAVARIAN CREAM DONUT <br> Starts at ₱ 25.00 || <br> ⭐⭐⭐☆☆ </button>
            </div>
        </div>
    </section>

    <div class="divider"></div>

    <section id="about">
        <h1 style="font-size: 50px; font-family: Verdana, Geneva, Tahoma, sans-serif; text-align: center; color:#ffffff;">ABOUT</h1>
        <p style="font-size: 25px; font-family: Verdana, Geneva, Tahoma, sans-serif; font-weight: bold; color: rgb(255, 255, 255); text-align: center;">
            Welcome to FoodFiesta, your ultimate culinary destination founded in 2024 in the heart of 
            Mamatid, Cabuyao, Laguna. Spearheaded by our visionary founding chef, Andrei Perfecto, 
            FoodFiesta is committed to delivering an unparalleled dining experience that combines
            affordable prices with top-notch quality. <br> <br>

            At FoodFiesta, we believe that everyone deserves a taste of excellence without breaking the
             bank. Our menu is a celebration of diverse flavors, meticulously crafted with fresh, high-
             quality ingredients to tantalize your taste buds. Whether you're craving classic comfort 
             foods or adventurous new dishes, we have something to delight every palate. <br><br>

            Join us at FoodFiesta, where exceptional dining meets unbeatable value. Experience the 
            perfect blend of flavor, quality, and affordability that makes us the go-to spot for food lovers 
            in Laguna. Your fiesta of flavors awaits!
        </p>
    </section>

    <div class="divider"></div>

    <section id="contact">
        <h1 style="font-size: 50px; font-family: Verdana, Geneva, Tahoma, sans-serif; text-align: center; color:#ffffff;">Contact Us!</h1>
        <p style="font-size: 35px; font-family: 'Times New Roman', Times, serif; color: rgb(255, 255, 255); text-align: center;">
            You can find us with these number: 0995-525-4372 <br>
            And these address! <br>
            Ph 6 Blk 22 Mabuhay City Mamatid Cabuyao, Laguna
            <br>
            <h3 style="font-size: 50px; font-family:Verdana, Geneva, Tahoma, sans-serif; text-align: center; color: #ffffff">BOOK A RESERVATION NOW!</h3>
        </p>

        <div class="contact-form">
            <input type="text" id="name" name="name" placeholder="Your Name">
            <input type="email" id="email" name="email" placeholder="Your Email">
            <textarea id="message" name="message" placeholder="Your Message" rows="4"></textarea>
            <button type="submit">Submit</button>
        </div>

    </section>

    <div class="divider"></div>

    <section id="log-in">
        <h1 style="font-size: 50px; font-family: Verdana, Geneva, Tahoma, sans-serif; text-align: center; color:#ffffff;">Log-In</h1>

       <div class="log-in-form">
            <input type="email" id="email" name="email" placeholder="Your Email">
            <input type="password" id="password" name="password" placeholder="Your Password">
            <a href="#home" class="log-in-button">LOG-IN</a>
        </div>

    </section>
</body>
</html>


