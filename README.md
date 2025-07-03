<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Toko Online Rifki</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: sans-serif;
      background: #f4f4f4;
    }
    header {
      background: #3498db;
      color: white;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.5rem;
      padding: 2rem;
    }
    .product {
      background: white;
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      text-align: center;
    }
    .product img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 5px;
    }
    .product h3 {
      margin: 0.5rem 0;
    }
    .product button {
      background: #2ecc71;
      color: white;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 5px;
      cursor: pointer;
    }
    #cart {
      position: fixed;
      top: 1rem;
      right: 1rem;
      background: white;
      padding: 1rem;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      border-radius: 10px;
      max-width: 300px;
      display: none;
    }
    #cart h2 {
      margin-top: 0;
    }
    #cart ul {
      padding-left: 1rem;
    }
    .cart-btn {
      background: #e67e22;
      color: white;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <h1>Toko Rifki</h1>
  <button class="cart-btn" onclick="toggleCart()">Cart 🛒 (<span id="cart-count">0</span>)</button>
</header>

<div class="products">
  <div class="product">
    <img src="https://via.placeholder.com/200x150" alt="Parfum A">
    <h3>Parfum A</h3>
    <p>Rp50.000</p>
    <button onclick="addToCart('Parfum A')">Add to Cart</button>
  </div>
  <div class="product">
    <img src="https://via.placeholder.com/200x150" alt="Parfum B">
    <h3>Parfum B</h3>
    <p>Rp60.000</p>
    <button onclick="addToCart('Parfum B')">Add to Cart</button>
  </div>
  <div class="product">
    <img src="https://via.placeholder.com/200x150" alt="Parfum C">
    <h3>Parfum C</h3>
    <p>Rp70.000</p>
    <button onclick="addToCart('Parfum C')">Add to Cart</button>
  </div>
</div>

<div id="cart">
  <h2>Cart</h2>
  <ul id="cart-items"></ul>
</div>

<script src="https://rifkira.psl17.my.id/js/app.js"></script>

</body>
</html>
