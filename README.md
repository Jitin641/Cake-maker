
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cake Market - Cake and Bakery Website</title>
    <style>
        /* Updated Styles */
        body {
            font-family: sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background-color: #2874f0;
            color: white;
            padding: 10px 20px;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        .logo {
            font-size: 1.5em;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }

        .search-bar {
            flex-grow: 1;
            margin: 0 20px;
        }

        .search-bar input {
            width: 100%;
            padding: 8px 12px;
            border: none;
            font-size: 1em;
        }

        .nav-menu {
            display: flex;
            gap: 15px;
        }

        .nav-item {
            color: white;
            text-decoration: none;
            font-size: 0.9em;
        }

        .nav-item:hover {
            text-decoration: underline;
        }

        main {
            padding: 10px;
            margin: 0;
            width: 100%;
        }

        .featured-cakes {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: space-around;
        }

        .item {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 300px;
            background-color: #fff;
            padding: 15px;
            margin: 0;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
        }

        .item-image {
            width: 100%;
            height: auto;
        }

        .item-title {
            font-size: 1em;
            margin: 5px 0;
            text-align: center;
        }

        .btn {
            background-color: #e74c3c;
            color: white;
            padding: 6px 10px;
            border: none;
            cursor: pointer;
            font-size: 0.9em;
            border-radius: 3px;
        }

        .btn:hover {
            background-color: #c0392b;
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <a href="#" class="logo">Cake Market</a>
        <div class="search-bar">
            <input type="text" placeholder="Search for a cake or bakery item">
        </div>
        <nav class="nav-menu">
            <a href="#" class="nav-item">Suggest a Cake</a>
            <a href="cart.html" class="nav-item">Cart</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main>
        <section class="featured-cakes">
            <!-- Cake 1 -->
            <div class="item" id="cake1">
                <img src=Cake 1.png alt="Belgium Chocolate Truffle Cake" class="item-image">
                <h3 class="item-title">Belgium Chocolate Truffle Cake</h3>
                <p class="item-details">Flavour: Chocolate</p>
                <p class="item-details">Price: ₹399</p>
                <button class="btn" onclick="addToCart('Belgium Chocolate Truffle Cake', 399)">Order Now</button>
            </div>

            <!-- Cake 2 -->
            <div class="item" id="cake2">
                <img src="Cake2.png" alt="Marvel Midnight Cake" class="item-image">
                <h3 class="item-title">Marvel Midnight Cake</h3>
                <p class="item-details">Flavour: Chocolate</p>
                <p class="item-details">Price: ₹499</p>
                <button class="btn" onclick="addToCart('Marvel Midnight Cake', 499)">Order Now</button>
            </div>

            <!-- Cake 3 -->
            <div class="item" id="cake3">
                <img src="Cake3.png" alt="Black Forest Cake" class="item-image">
                <h3 class="item-title">Black Forest Cake</h3>
                <p class="item-details">Flavour: Chocolate</p>
                <p class="item-details">Price: ₹349</p>
                <button class="btn" onclick="addToCart('Black Forest Cake', 349)">Order Now</button>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2022 True Knowledge - All rights reserved.</p>
    </footer>

    <script>
        function addToCart(itemName, price) {
            let cart = JSON.parse(localStorage.getItem('cart')) || [];
            cart.push({ itemName, price });
            localStorage.setItem('cart', JSON.stringify(cart));
            alert(`${itemName} added to cart!`);
        }
    </script>
</body>
</html>
