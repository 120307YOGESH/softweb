# Ex.07 Restuarant Website
## Date: 2.11.2025

## AIM:
To develop a static Resturant website to display the menu and services provided by the resturant.

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

# index.html :

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Restaurant Login</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h2>🍽️ Restaurant Login</h2>
    <form onsubmit="return loginUser()">
      <input type="text" id="username" placeholder="Enter Username" required>
      <input type="password" id="password" placeholder="Enter Password" required>
      <button type="submit">Login</button>
    </form>
  </div>

  <script>
    function loginUser() {
      const user = document.getElementById('username').value;
      const pass = document.getElementById('password').value;

      if (user === "admin" && pass === "1234") {
        window.location.href = "home.html";
      } else {
        alert("Invalid login credentials!");
      }
      return false;
    }
  </script>
</body>
</html>
```

#Home.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Restaurant Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <h1>🍴 My Restaurant</h1>
    <ul>
      <li><a href="home.html">Home</a></li>
      <li><a href="dishes.html">Dishes</a></li>
      <li><a href="order.html">Order</a></li>
      <li><a href="index.html">Logout</a></li>
    </ul>
  </nav>

  <section class="content">
    <h2>Welcome to My Restaurant!</h2>
    <p>Delicious food made with love ❤️</p>
  </section>
</body>
</html>

```
# Orders.html :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Order Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <h1>🍴 My Restaurant</h1>
    <ul>
      <li><a href="home.html">Home</a></li>
      <li><a href="dishes.html">Dishes</a></li>
      <li><a href="order.html" class="active">Order</a></li>
      <li><a href="index.html">Logout</a></li>
    </ul>
  </nav>

  <section class="order">
    <h2>Place Your Order</h2>
    <form onsubmit="return placeOrder()">
      <label>Select Dish:</label>
      <select id="dish" required>
        <option value="">-- Select --</option>
        <option>Burger</option>
        <option>Pizza</option>
        <option>Salad</option>
        <option>Pasta</option>
      </select>

      <label>Quantity:</label>
      <input type="number" id="qty" min="1" required>

      <button type="submit">Order Now</button>
    </form>

    <p id="msg"></p>
  </section>

  <script>
    function placeOrder() {
      const dish = document.getElementById('dish').value;
      const qty = document.getElementById('qty').value;
      if (dish && qty > 0) {
        document.getElementById('msg').innerText = `✅ Order placed for ${qty} ${dish}(s)!`;
      } else {
        document.getElementById('msg').innerText = `⚠️ Please fill all fields.`;
      }
      return false;
    }
  </script>
</body>
</html>
```
# Style.css :

```
body {
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
  margin: 0;
  padding: 0;
}

.container {
  width: 350px;
  margin: 100px auto;
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  text-align: center;
}

input, select {
  width: 90%;
  padding: 10px;
  margin: 10px 0;
  border: 1px solid #ccc;
  border-radius: 8px;
}

button {
  background-color: #ff7043;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background-color: #e64a19;
}

nav {
  display: flex;
  justify-content: space-between;
  background-color: #ff7043;
  padding: 15px;
  color: white;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

nav ul li a.active {
  text-decoration: underline;
}

.content, .dishes, .order {
  text-align: center;
  margin-top: 50px;
}

.dish-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  margin-top: 20px;
}

.dish-card {
  background: white;
  padding: 20px;
  width: 150px;
  border-radius: 12px;
  box-shadow: 0 0 5px rgba(0,0,0,0.1);
}
```

## OUTPUT:

![alt text](<Screenshot 2025-11-02 164858.png>)

![alt text](<Screenshot 2025-11-02 164912.png>)

![alt text](<Screenshot 2025-11-02 164922.png>)

![alt text](<Screenshot 2025-11-02 164934.png>)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
