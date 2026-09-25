# my-wibesite-
This is my wibesite and everyone visit on it.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mehmood Store - E-Commerce</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:Arial,sans-serif;
}

html{
  scroll-behavior:smooth;
}

body{
  background:#f5f7fb;
  color:#222;
  transition:.3s;
}

/* HEADER */
header{
  position:sticky;
  top:0;
  z-index:1000;
  background:linear-gradient(135deg,#6c5ce7,#00cec9);
  color:white;
  padding:15px 5%;
  box-shadow:0 5px 20px #0003;
}

.nav{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
}

.logo{
  font-size:26px;
  font-weight:bold;
  white-space:nowrap;
}

.search{
  flex:1;
  max-width:500px;
  display:flex;
}

.search input{
  width:100%;
  padding:12px 15px;
  border:0;
  outline:0;
  border-radius:25px 0 0 25px;
  font-size:15px;
}

.search button{
  border:0;
  padding:0 18px;
  background:#222;
  color:white;
  border-radius:0 25px 25px 0;
  cursor:pointer;
}

.nav-buttons{
  display:flex;
  gap:8px;
}

.nav-buttons button{
  border:0;
  background:#ffffff25;
  color:white;
  padding:10px 13px;
  border-radius:10px;
  cursor:pointer;
  font-size:16px;
}

.nav-buttons button:hover{
  background:#ffffff45;
  transform:scale(1.05);
}

/* HERO */
.hero{
  min-height:420px;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:50px 20px;
  background:
    radial-gradient(circle at top left,#a29bfe,transparent 35%),
    linear-gradient(135deg,#0f2027,#203a43,#2c5364);
  color:white;
  overflow:hidden;
}

.hero-content{
  animation:up 1s ease;
}

.hero h1{
  font-size:52px;
  margin-bottom:15px;
}

.hero p{
  font-size:19px;
  margin-bottom:25px;
}

.shop-btn{
  padding:14px 30px;
  border:0;
  border-radius:30px;
  background:#00cec9;
  color:white;
  font-size:17px;
  cursor:pointer;
  box-shadow:0 8px 25px #00cec955;
}

.shop-btn:hover{
  transform:translateY(-4px) scale(1.04);
}

/* CATEGORIES */
.section{
  padding:45px 5%;
}

.section-title{
  text-align:center;
  font-size:32px;
  margin-bottom:30px;
}

.categories{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(130px,1fr));
  gap:18px;
}

.category{
  background:white;
  padding:25px 10px;
  text-align:center;
  border-radius:18px;
  box-shadow:0 5px 20px #00000010;
  cursor:pointer;
  transition:.3s;
}

.category:hover{
  transform:translateY(-8px);
  box-shadow:0 12px 30px #0002;
}

.category span{
  display:block;
  font-size:40px;
  margin-bottom:10px;
}

/* PRODUCTS */
.products{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:25px;
}

.product{
  background:white;
  border-radius:20px;
  overflow:hidden;
  box-shadow:0 7px 25px #00000012;
  transition:.35s;
  animation:fade .6s ease;
}

.product:hover{
  transform:translateY(-8px);
  box-shadow:0 15px 35px #00000025;
}

.product-img{
  height:210px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:linear-gradient(135deg,#dfe6e9,#ffffff);
  font-size:90px;
}

.product-info{
  padding:18px;
}

.product-info h3{
  margin-bottom:8px;
}

.price{
  color:#6c5ce7;
  font-size:21px;
  font-weight:bold;
  margin:10px 0;
}

.old-price{
  color:#999;
  text-decoration:line-through;
  font-size:14px;
  margin-left:5px;
}

.rating{
  color:#f1c40f;
  margin-bottom:12px;
}

.add-btn{
  width:100%;
  padding:12px;
  border:0;
  border-radius:10px;
  background:#6c5ce7;
  color:white;
  cursor:pointer;
  font-size:15px;
}

.add-btn:hover{
  background:#4834d4;
}

/* CART */
.cart{
  position:fixed;
  right:-400px;
  top:0;
  width:360px;
  max-width:95%;
  height:100%;
  background:white;
  z-index:2000;
  box-shadow:-10px 0 30px #0003;
  transition:.4s;
  padding:25px;
  overflow:auto;
}

.cart.open{
  right:0;
}

.cart-header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  margin-bottom:20px;
}

.close{
  border:0;
  background:#ff7675;
  color:white;
  width:35px;
  height:35px;
  border-radius:50%;
  cursor:pointer;
}

.cart-item{
  display:flex;
  justify-content:space-between;
  gap:10px;
  padding:15px 0;
  border-bottom:1px solid #ddd;
}

.qty button{
  width:25px;
  height:25px;
  border:0;
  background:#6c5ce7;
  color:white;
  border-radius:5px;
}

.total{
  font-size:22px;
  font-weight:bold;
  margin:25px 0;
}

.checkout{
  width:100%;
  padding:14px;
  background:#00b894;
  color:white;
  border:0;
  border-radius:10px;
  font-size:17px;
  cursor:pointer;
}

/* FOOTER */
footer{
  background:#111827;
  color:white;
  text-align:center;
  padding:40px 20px;
  margin-top:30px;
}

footer h2{
  margin-bottom:10px;
}

.social{
  margin-top:20px;
  font-size:25px;
  word-spacing:15px;
}

/* DARK MODE */
body.dark{
  background:#121212;
  color:white;
}

body.dark .category,
body.dark .product,
body.dark .cart{
  background:#1f1f1f;
  color:white;
}

body.dark .product-img{
  background:#292929;
}

body.dark .search input{
  background:#222;
  color:white;
}

/* ANIMATIONS */
@keyframes up{
  from{
    opacity:0;
    transform:translateY(50px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}

@keyframes fade{
  from{
    opacity:0;
    transform:scale(.95);
  }
  to{
    opacity:1;
    transform:scale(1);
  }
}

/* MOBILE */
@media(max-width:700px){
  .nav{
    flex-wrap:wrap;
  }

  .logo{
    font-size:21px;
  }

  .search{
    order:3;
    flex-basis:100%;
  }

  .hero h1{
    font-size:38px;
  }

  .hero{
    min-height:350px;
  }

  .section{
    padding:35px 4%;
  }
}
</style>
</head>

<body>

<header>
  <div class="nav">

    <div class="logo">🛍️ Mehmood Store</div>

    <div class="search">
      <input
        type="text"
        id="searchInput"
        placeholder="Search products..."
        onkeyup="searchProducts()">
      <button onclick="searchProducts()">🔍</button>
    </div>

    <div class="nav-buttons">
      <button onclick="toggleDark()">🌙</button>
      <button onclick="openCart()">🛒 <span id="cartCount">0</span></button>
    </div>

  </div>
</header>


<section class="hero">

  <div class="hero-content">

    <h1>Welcome to Mehmood Store</h1>

    <p>Discover amazing products at amazing prices.</p>

    <button class="shop-btn"
      onclick="document.getElementById('products').scrollIntoView()">
      Shop Now 🛍️
    </button>

  </div>

</section>


<section class="section">

  <h2 class="section-title">Categories</h2>

  <div class="categories">

    <div class="category" onclick="filterCategory('all')">
      <span>🛍️</span>
      All
    </div>

    <div class="category" onclick="filterCategory('mobile')">
      <span>📱</span>
      Mobiles
    </div>

    <div class="category" onclick="filterCategory('laptop')">
      <span>💻</span>
      Laptops
    </div>

    <div class="category" onclick="filterCategory('fashion')">
      <span>👕</span>
      Fashion
    </div>

    <div class="category" onclick="filterCategory('watch')">
      <span>⌚</span>
      Watches
    </div>

    <div class="category" onclick="filterCategory('shoes')">
      <span>👟</span>
      Shoes
    </div>

  </div>

</section>


<section class="section" id="products">

  <h2 class="section-title">🔥 Featured Products</h2>

  <div class="products" id="productContainer"></div>

</section>


<!-- CART -->

<div class="cart" id="cart">

  <div class="cart-header">

    <h2>🛒 Your Cart</h2>

    <button class="close" onclick="closeCart()">×</button>

  </div>

  <div id="cartItems"></div>

  <div class="total">
    Total: Rs. <span id="total">0</span>
  </div>

  <button class="checkout" onclick="checkout()">
    Proceed to Checkout
  </button>

</div>


<footer>

  <h2>🛍️ Mehmood Store</h2>

  <p>Online Shopping Made Easy</p>

  <div class="social">
    📘 📸 ▶️ 💬
  </div>

  <p style="margin-top:20px">
    © 2026 Mehmood Store. All Rights Reserved.
  </p>

</footer>


<script>

const products = [

  {
    id:1,
    name:"Premium Smartphone",
    price:45000,
    category:"mobile",
    icon:"📱",
    rating:"⭐⭐⭐⭐⭐"
  },

  {
    id:2,
    name:"Powerful Laptop",
    price:95000,
    category:"laptop",
    icon:"💻",
    rating:"⭐⭐⭐⭐⭐"
  },

  {
    id:3,
    name:"Smart Watch",
    price:8500,
    category:"watch",
    icon:"⌚",
    rating:"⭐⭐⭐⭐"
  },

  {
    id:4,
    name:"Stylish T-Shirt",
    price:2500,
    category:"fashion",
    icon:"👕",
    rating:"⭐⭐⭐⭐⭐"
  },

  {
    id:5,
    name:"Running Shoes",
    price:5500,
    category:"shoes",
    icon:"👟",
    rating:"⭐⭐⭐⭐"
  },

  {
    id:6,
    name:"Wireless Headphones",
    price:6500,
    category:"mobile",
    icon:"🎧",
    rating:"⭐⭐⭐⭐⭐"
  },

  {
    id:7,
    name:"Gaming Laptop",
    price:145000,
    category:"laptop",
    icon:"🖥️",
    rating:"⭐⭐⭐⭐⭐"
  },

  {
    id:8,
    name:"Classic Watch",
    price:12000,
    category:"watch",
    icon:"⌚",
    rating:"⭐⭐⭐⭐"
  }

];

let cart = [];


/* SHOW PRODUCTS */

function showProducts(list = products){

  const container =
    document.getElementById("productContainer");

  container.innerHTML = "";

  if(list.length === 0){

    container.innerHTML =
      "<h3 style='grid-column:1/-1;text-align:center'>No products found 😔</h3>";

    return;
  }

  list.forEach(product => {

    container.innerHTML += `

      <div class="product">

        <div class="product-img">
          ${product.icon}
        </div>

        <div class="product-info">

          <h3>${product.name}</h3>

          <div class="rating">
            ${product.rating}
          </div>

          <div class="price">
            Rs. ${product.price.toLocaleString()}
            <span class="old-price">
              Rs. ${(product.price + 2000).toLocaleString()}
            </span>
          </div>

          <button
            class="add-btn"
            onclick="addToCart(${product.id})">
            🛒 Add to Cart
          </button>

        </div>

      </div>

    `;

  });

}


/* ADD TO CART */

function addToCart(id){

  const product =
    products.find(p => p.id === id);

  const existing =
    cart.find(p => p.id === id);

  if(existing){

    existing.qty++;

  }else{

    cart.push({
      ...product,
      qty:1
    });

  }

  updateCart();

  alert("✅ Product added to cart!");

}


/* UPDATE CART */

function updateCart(){

  const items =
    document.getElementById("cartItems");

  items.innerHTML = "";

  let total = 0;
  let count = 0;

  cart.forEach(item => {

    total += item.price * item.qty;
    count += item.qty;

    items.innerHTML += `

      <div class="cart-item">

        <div>

          <strong>
            ${item.icon} ${item.name}
          </strong>

          <br>

          Rs. ${item.price.toLocaleString()}

        </div>

        <div class="qty">

          <button onclick="changeQty(${item.id},-1)">
            -
          </button>

          ${item.qty}

          <button onclick="changeQty(${item.id},1)">
            +
          </button>

        </div>

      </div>

    `;

  });

  document.getElementById("total")
    .innerText = total.toLocaleString();

  document.getElementById("cartCount")
    .innerText = count;

}


/* CHANGE QUANTITY */

function changeQty(id, amount){

  const item =
    cart.find(p => p.id === id);

  if(!item) return;

  item.qty += amount;

  if(item.qty <= 0){

    cart =
      cart.filter(p => p.id !== id);

  }

  updateCart();

}


/* OPEN CART */

function openCart(){

  document
    .getElementById("cart")
    .classList.add("open");

}


/* CLOSE CART */

function closeCart(){

  document
    .getElementById("cart")
    .classList.remove("open");

}


/* SEARCH */

function searchProducts(){

  const value =
    document
      .getElementById("searchInput")
      .value
      .toLowerCase();

  const result =
    products.filter(p =>
      p.name.toLowerCase().includes(value)
    );

  showProducts(result);

}


/* CATEGORY FILTER */

function filterCategory(category){

  if(category === "all"){

    showProducts(products);

    return;

  }

  const result =
    products.filter(p =>
      p.category === category
    );

  showProducts(result);

}


/* DARK MODE */

function toggleDark(){

  document.body.classList.toggle("dark");

}


/* CHECKOUT */

function checkout(){

  if(cart.length === 0){

    alert("🛒 Your cart is empty!");

    return;

  }

  alert(
    "🎉 Checkout system ready!\n\n" +
    "Your total is Rs. " +
    document.getElementById("total").innerText
  );

}


/* INITIAL LOAD */

showProducts();

updateCart();

</script>

</body>
</html>
