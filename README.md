# Ex.07 Restuarant Website
## Date:19.11.2025

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
```
loginform.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Login Form</title>
    <style>
      body {
        font-family: "Poppins", Arial, sans-serif;
        margin: 0;
        background: linear-gradient(135deg, gold, black);
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
      }

      .login-box {
        background: white;
        padding: 40px 35px;
        border-radius: 16px;
        width: 90%;
        max-width: 350px;
        text-align: center;
        box-shadow: 0 8px 25px rgba(0, 0, 0, 0.25);
        animation: fadeIn 0.7s ease-in-out;
      }

      h2 {
        margin-bottom: 20px;
        color: #333;
      }

      hr {
        border: none;
        height: 2px;
        background: linear-gradient(to right, gold, black);
        margin: 15px;
      }

      .input-box {
        margin-bottom: 20px;
        text-align: left;
      }

      .input-box label {
        font-size: 14px;
        color: #555;
        display: block;
        margin-bottom: 6px;
      }

      .input-box input {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 8px;
        outline: none;
        transition: 0.3s;
        box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.1);
      }

      .input-box input:focus {
        border-color: gold;
        box-shadow: 0 0 8px rgba(255, 215, 0, 0.5);
      }

      .submit-btn {
        background: linear-gradient(to right, #007bff, #0056b3);
        color: white;
        border: none;
        padding: 12px 20px;
        border-radius: 8px;
        width: 100%;
        cursor: pointer;
        font-weight: bold;
        transition: 0.3s;
      }

      .submit-btn:hover {
        background: linear-gradient(to right, #0056b3, #003f7f);
        transform: scale(1.03);
      }

      .register {
        margin-top: 15px;
        color: #555;
        font-size: 14px;
      }

      .register a {
        color: #007bff;
        text-decoration: none;
        font-weight: 600;
      }

      .register a:hover {
        text-decoration: underline;
      }

      @keyframes fadeIn {
        from {
          opacity: 0;
          transform: translateY(20px);
        }
        to {
          opacity: 1;
          transform: translateY(0);
        }
      }
    </style>

    <script>
      function validation() {
        const username = document.getElementById("t1").value.trim();
        const pwd = document.getElementById("t2").value.trim();

        if (username === "" || pwd === "") {
          alert("Please fill in all fields.");
          return;
        }

        if (username === "24009351" && pwd === "1004") {
          alert("✅ Login successful!");
          window.location.href = "mainmenu.html";
        } else {
          alert("❌ Incorrect username or password.");
        }
      }
    </script>
  </head>

  <body>
    <div class="login-box">
      <h2>Login</h2>
      <hr />

      <div class="input-box">
        <label for="t1">Username</label>
        <input type="text" id="t1" placeholder="Enter your username" />
      </div>

      <div class="input-box">
        <label for="t2">Password</label>
        <input type="password" id="t2" placeholder="Enter your password" />
      </div>

      <input
        type="button"
        value="Login"
        class="submit-btn"
        onclick="validation()"
      >

      <hr />

      <div class="register">
        New to BITEBOX? <a href="register.html">Create an account</a>
      </div>
    </div>
  </body>
</html>

```

```
mainmenu.html


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BITEBOX</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: #fff8f0;
      color: #333;
    }
    .header {
      text-align: center;
      background: linear-gradient(to right, gold, black);
      padding: 40px 0;
      box-shadow: 0 4px 20px rgba(0,0,0,0.2);
    }

    h2 {
      font-size: 64px;
      color: goldenrod;
      text-shadow: 2px 2px 15px rgba(0,0,0,0.5);
      margin: 0;
      letter-spacing: 4px;
    }

    nav {
      margin-top: 20px;
    }

    nav ul {
      list-style: none;
      padding: 0;
      display: flex;
      justify-content: center;
      gap: 50px;
      margin: 0;
    }

    nav ul li {
      display: inline;
    }

    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 600;
      font-size: 18px;
      transition: 0.3s ease;
    }

    nav ul li a:hover {
      color: gold;
      text-shadow: 0 0 10px gold;
    }
    .content {
      max-width: 1100px;
      margin: 60px auto;
      text-align: center;
    }

    .card-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 40px;
      margin-bottom: 50px;
    }

    .card {
      background: white;
      border-radius: 12px;
      padding: 30px;
      width: 280px;
      text-align: center;
      box-shadow: 0 6px 20px rgba(0,0,0,0.15);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 12px 25px rgba(0,0,0,0.25);
    }

    .card h3 {
      margin-top: 0;
      color: #d2691e;
    }

    .card p {
      color: #555;
      font-size: 15px;
    }

    .card a {
      text-decoration: none;
      color: inherit;
    }
    .offer {
      background: linear-gradient(90deg, gold, orange);
      padding: 20px;
      border-radius: 10px;
      margin: 30px auto;
      max-width: 700px;
      text-align: center;
      color: #000;
      font-weight: bold;
      box-shadow: 0 4px 15px rgba(0,0,0,0.15);
      animation: pulse 2s infinite alternate;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 40px;
    }

    .gallery img {
      border-radius: 10px;
      box-shadow: 0 12px 25px rgba(0,0,0,0.25);
      transition: transform 0.3s ease;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    footer {
      bottom: 0;
      z-index: 1000;
      width: 100%;
      position: fixed;
      margin-top: 60px;
      background: #222;
      color: #ccc;
      text-align: center;
      padding: 20px 0;
      font-size: 14px;
    }

  </style>
</head>

<body>

  <div class="header">
    <h2>BITEBOX</h2>
    <nav>
      <ul>
        <li><a href="food.html">Menu</a></li>
        <li><a href="about.html">Administration</a></li>
        <li><a href="review.html">Reviews</a></li>
      </ul>
    </nav>
  </div>

  <div class="content">
    <div class="card-container">
      <div class="card">
        <a href="food.html">
          <h3>Menu</h3>
          <p>Explore our delicious menu filled with local and global flavors.</p>
        </a>
      </div>

      <div class="card">
        <a href="tablebooking.html">
          <h3>Book a Table</h3>
          <p>Reserve your seat in advance for a smooth dining experience.</p>
        </a>
      </div>

      <div class="card">
        <h3>Opening Hours</h3>
        <p><b>Weekdays:</b> 9 AM – 10 PM</p>
        <p><b>Weekends:</b> Open 24 Hours</p>
      </div>
    </div>

    <div class="offer">
      🎉 30% OFF this weekend for pre-booked customers! 🎉
    </div>
    <div class="gallery">
      <img src="https://images.squarespace-cdn.com/content/v1/5c42b91c697a9873ebf844b8/1619135748199-I56FXBEVWXC1QXGK17BZ/Apr+11+2021DSC07442.jpg?format=2500w" width="100%" alt="Restaurant Interior">
      <img src="https://images.squarespace-cdn.com/content/v1/5c42b91c697a9873ebf844b8/1566963493871-ETXLCH49FLZUB3A0Y1QT/yangskitchen_01.png?format=1000w" width="500px" alt="Dish 1">
      <img src="https://images.squarespace-cdn.com/content/v1/5c42b91c697a9873ebf844b8/1566964014153-2JAH31CL236V51TSY4SW/yangskitchen_02.png?format=1000w" width="500px" alt="Dish 2">
    </div>
  </div>

  <footer>
    DESIGNED AND DEVELOPED BY BHUVANESHWARAN TU
  </footer>

</body>
</html>


```


```
food.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>BITEBOX Menu</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background-color: #f8f8f8;
      color: #333;
    }

    header {
      text-align: center;
      background: linear-gradient(to right, gold, black);
      color: goldenrod;
      padding: 25px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    h1 {
      margin: 0;
      font-size: 48px;
      letter-spacing: 2px;
    }

    .menu-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
      padding: 50px 20px;
    }

    .menu-card {
      background: white;
      border-radius: 12px;
      width: 280px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      overflow: hidden;
    }

    .menu-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.25);
    }

    .menu-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .menu-card h2 {
      margin: 15px 0 5px;
      color: #d2691e;
      text-align: center;
    }

    .menu-card ul {
      list-style: none;
      padding: 0;
      margin: 0 0 15px 0;
      text-align: center;
    }

    .menu-card ul li {
      padding: 5px 0;
      font-size: 16px;
      color: #555;
    }

    footer {
      bottom: 0;
      z-index: 1000;
      width: 100%;
      position: fixed;
      text-align: center;
      padding: 15px;
      background-color: black;
      color: white;
    }

    a {
      display: inline-block;
      margin: 20px;
      text-decoration: none;
      color: black;
      background: gold;
      padding: 10px 20px;
      border-radius: 8px;
      transition: 0.3s;
    }

    a:hover {
      background-color: chocolate;
      color: goldenrod;
    }
  </style>
</head>
<body>

<header>
  <h1>Our Menu</h1>
</header>

<div class="menu-container">

  <div class="menu-card">
    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxMTEhUTExMWFhUWFxUXFxUWFxUVFRYVFxUXFxUVFRcYHSggGBolHRUVITEiJSkrLi4uFx8zODMtNygtLisBCgoKDg0OGxAQGy0lICUtLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIALcBEwMBEQACEQEDEQH/xAAbAAACAwEBAQAAAAAAAAAAAAAEBQECAwYAB//EADoQAAEDAgQDBgUDAwQCAwAAAAEAAhEDIQQFEjFBUWEGEyJxgZEyocHR8EJSsSPh8RQVM4IWcgdTYv/EABoBAAIDAQEAAAAAAAAAAAAAAAADAQIEBQb/xAAyEQACAgEEAQIDBwUBAQEBAAAAAQIRAwQSITFBE1EiYXEygZGhsdHwBRRCweHxUkMj/9oADAMBAAIRAxEAPwBC2gsNFzUUEUBo2gigNBQUUBcUEUBcUEUBcUEUBcUVNASKSigLdyigJ7lRRJ7ukUBPdooCO6RQHu7UUBHdooCO7UUSR3aKA93aAKmmigI0KKAjQigILEUBUsQBUsUElCxAFTTQBQsUgVLEAZuYgDMsUAUNNBBR1NAGbqQQSU7oclJB0TcOtFFLNG0UUFmjaCKCy4oIoC4oooCwoooCwpIoC3dIAkUlAE90gDxpqKJPd2igIFJRQEd2igI0KAI0Iokg01FAYYmqGCSqTmoq2Q3RXD1g8Ai3RRHIpdERmmalivRcjQgCpYgCpYoAqWIAqWoAqWqAKliAKFqCShagChYgDNzEAZuYoAqWoAoWKSChYgDrG0VsoUXFFRQFhRRQFhSUAW0IAnQgknQoAnQgCdCAPd2oAgsQSe0IA9pQBQsUAVLVFElS1QABneP7inqiSdgkylJT+Rpx44Tj8xJlubDEOioNI5cEPa5JSMupwSh8XgbU8QxsgD4eHGFO2KtrwZcbakgvD1Q8SFMJqStG+eNwdM0IVihQhAEFqgCC1DJRQtQBUsUAULUAULUAVLUAZuagChCgChagkyc1AFC1AFNKkg7jultElhSUASKaAJ7tAE92gknu1AHu7QBZuHJ2G5hVbSAJq4NgiXBsWdJ49FkeqhbQyMQfE6GkRUab38lz5aualy+DoYlikuqYNisYybD1WrHrIrjwXyaLerj2ZjEs5wtK1GN+TFLSZY+DaBEjZM3x9xXpzXaM3Ec0zaxdm+CoCpIHuk5rgrJXJrjOzlN7muc5wDdwDAJ6rl5dRLd3waIcI5ztljqYaKTRInSfLkrwWbHbvtC46iClSXQhqYmnTGhrNI5nf0SE5zVtnS9eGSahKNL5i2iS+rqBPJbMcXVGLW7IZKgujtMvcynSeTeLAdVpqOCDb6MvqzzTSL0K4fsox5Iz5Q2UXHs0LUwqVLbgDnfoOajzRSc9pNbpFuPTql5Z7ltoRDPKLvyY02T1Uw6tmiFtWzxarFypagCjmoAzLUAZliigM3NQBUtQSUc1BBm5iAKFqAO8FNbRJYU0AT3aALd2gD3dooDwpoA9oRQBgpmnRL4BJPhB6cSsGrzem041Y3HDdwzjcVluIxFd3jimOMbneQOC50I+p82bPhhEDzSmaB4vcLOn5FZnjbk4y4FyzqLVALMcXODA0y4E22ECSfJSsHF2b8OvUko1yXrVXC26rFJnShki0bYPNi2xuORW7HqHBU4pmbJpVJ7k2dfllam9gL2hvqvRafVQnjUpJI87qMGydRdhDMfTadNMey4v9R18Jz2wV/MbhwtK2XzHGaaTnON+CyYMKlJSk7rkjUz2QpdnyTOMYXv1HaVq3b22YsUdo0pYUVWNPTcrmvI8cmjvQalFXyRWyplBuo1L8gFqxahSdeTLqdNOnOgrBYgVC1pMjc+ajV5HKl4EaaFJsLFIjYpWGbxyuJqlFSVDTC4MvZqa+43C9LhWPNj3I5890HRDvijuXTEkzaAsGXLhjJpp2hSw5MjK1qhews0hoPLeFy9Vq1OkuEdXS6F4vjmuhDmmeHDthrZcLNB+qZpZ5Mnw+CMkVbZy9btVinukuDbzAEei6SglGkxcYq7Z3WV4nvmgtFy2SPqlQmqr2IzRlubZsQmCSjggkzcEAUcEAUKgDMoskoUEGZUgfQtC2iCwYgCdCAPaUAZ1arRuR5blWUGwtA9eu8gloDWi5e8wAOaesFK5FN18IL7NUGVAave97eAR8A3BjncG6xajLBNKL4HQg19pDrGPBaWyOg6rmajPCTStWPiqOcxOBe97dD9JabDm7YzzCxyyfFUO/wBfcb6TklNvgQZh2bxDqjgS0AkanOIFibmN0uKdtz4KywR3LY7L46hRw9MspXe4QXn4tP0nklznfwx+86uHFHDUpLlnO4mtAkkD84qccLdBkak24gVPFMqeFjm982d/hqcQGngV0MumWLjte6Miz5K+Q3yvB4xzdVWnoBNgSAYiZjksmeGOKW2RVSt9DvL8DpBL3gOJEQZhv6khRjJdg1K+hnmvduY0Ay2Nvumy1EYKoO0/AmWlU5VkOX/2vBwRUfBvAJ9oRjzOUbXDJlpY4XTZODy/wODDcg6G7kxyVF8fL7NUpRhJbehbSYX6mVAZFiLyPNM27XcRuozb414CsFgW0ha4VsslKVv2/MwY4tKgmZ2v5LPAaOcjw5A13F408xCf608cfhvkh4tz+LgP7h9QE8uB49FnueRNyd/7NkZYdPVct+fYwqYBx0+EN/dffyUSg5IVl1CfmwL/AMbpvcKlQOc4GWgHSAZsTzWjBkyYEnDsxzlu4E+MydgxrqjmNMgQ0kfFxMeXNa8mvllTU1z8uBumUYcvoIwmI0GpADY3iDJHCyxwcoqrOjmxwyxUzCjjg4cvNdTHO4nGyRqXHRsXpl2LKlyLIKFBJVyCDNyCShCCChUgfSA1bhBYNU0QK8zzunSOgTUqcKbLn15eqYsfv+BFmOGw+JrkGqe5p/sZd5HV3BaI4nXsUch/gMmY2CG2PE3PnPJIyZp4e6f08fqXjFSOB/8Ak/M3d63DsP8ATAa4gbucSQJ6WBA6rl59RkyP4nxXR1NFgilu8h3YZj6TKlVwP/G0NaSRT0teZ/7S8lc/LJ+k3X7UaJ44SnGN+f1OirZk1xGqx3Ivx5WXPnsc7v8AUtHTSSuNM0figG6hA3HmOs9QruMYxUvr9DRiwt/DPkRY/MXuMnST6k+pSZZpv7TsfPRYkrXALWzVxJNQNdIiSBtw2VvVnLvk5jhXCYixTGmdtJV4N8e4OTAMo7P03VQ4mwOoNHEi4C1y1Utu3zQ3HFS768nQ5jmT4kOI0mARuPILFiTck2P188enwqOPuX6AeCz6A5rokmCYEkH+Fp9JKNo5UNQ5TSyPgS5h2xxNMPpMDdJMNcW6neQ6rVp9HjlFW/qaM/2rot2jpVmYfD1ntAMaaskSHTYiDxB24Qr48eJycYfcZM0Zf5FcpzZ7CxzXWkX/AJCTkxJO0uUKjJr4fB05r03d4QYqVI2uSOPkFXDheWL55GZc/ptLwD12ObTAF5vZZVLjYzTd8oGyqq0VA5xIgkz0Fir24NNA5XwjpX1nxrp6mg7fQxxCnUydWjZp5QmtmTkIy/F4hx0ls6TJNmehJt9VWEnk4a689f8ABeow4orcpf7/AEFeb1ajqhqUKs6b1NDvADyvuLbqyUIXf4pe5zssMqa28fX9jXL8176RU1N0+YEi8A8ZAS5xSVydrwMxy3cVT/nROfhjyAIJImRvEbKdm6SUXyWhLb2cc/Bua4gEgHrwWuUZR4kjSsu5GrGCL81WMqkmJkrVF6mGqsOqm7UP2n6LsrFHbwYL55NKWPGzvC7kUicHEunZv3yXZNE94psKI1qbIKlyAKlykg+l1nBjC95DWt3J4Dmuh9TOLKmIqYgaaJLKZ3q/qcOTBw81rx4uP9/sLbCsuyqnREMbfi43cTzJO6fGKjwirdjfA4bW6OAufJLzZfTg5ExVuh1WcIaG7EbjlFgsW/cr9xyjRxeL7I0ziX1nHVqksBvpJM+wkx5rmZdK5TbcuH18jfHUtY1BL6jfLstDKenYceW+61Y8Sx49rM8sjlKwPNsra8gNF28drHhI3j6rFqdHjnK0Pw6icF2CZhQ1w3TGm02AgLLrJQyNR4VfL9h+HPOFu3yLmYCSNMFw1G9mmASWx5Ln+g3TS47t9DZ6i+wPNsHLC9giB4mncTt0I6qiilyuv5/LFqXNMQdw4gki3AjaeSbaRL7BtekDYcYBEq9bmNxzceitZ5c6eOx/PRMUK4OZlk8uSkDU6cVXRwHzgSfmnPiNMZjgllr2GL8jqUR3jmtDyf6byA7QSPiA4nkU2qpWa53LlhuJq9/ooVBIgCXXlwFiesj5rE4ZFPddV19DRlnieKl2Z5hk00zSGht5a4AAAm0yOimGSUZpyZzpRjJCXCtdTqww6mi2qbiNxK148nvwzJmg5dHUU8PLWljjeTfZoVsujjk+KLoXh1jhxJWgvCGmKTzWohrWw/vX3bUa10ANaDvqJ8NpsbrJKPCUf+19Pma8ald+X+X8QxyvOqFfxML3Bt/hLWiLXMQfdVlilD4pp+//AKMlFx4K4nNG6iehgAwJ5yfNY3llba6/IuocUA4Ki+kDTp02+NwMFwN7byeNk3dO9vnj9S85b/ik+hnXweHcAXH4BfQXNGo76RJ3M3hOlPG27+n3/n+gqKndR8iDEY2kwO6TvJMk7mBARGbktv4DZ4Jx5aEDsVrJPsnTtkJUjPVIKqlyWYVgq5IhdPS5XW2jJmirsvisO14hw9eK3VZnE2IZWo3b42cuISZ4Uy6kE4LHtqDwm/EcQs0oOJewrWq2Se1qUyD2pTZB1mQ4LEVycRi3GHiG0BZjWG41Didl3YYd3xZPuXsZJSS4idZRw402sANuinNn9LlrgolZRtQTCtizRyK0Di0HYKsW6gP1D5DdI1sW8fH8RfF9oIpYgNZ5WvvK50Mix4+fHBpcLYN33euDW/4ULIsrqJO3auS2Y1tPhH9lOont4DGrEuIxRiJsLRzXJzfF5HxSFteoDZskk+4NlhzQUlUB0b8h2GwT6RmAXkkNG+0EzwuDv91WG/EuO/2r7uf52VlJT+gezDtpEuAkkgkuIsydmg9IP+AmxqCbj/F8r+73/QW25cMWHDsl5DWk1CNTdwTvpHIHc8DCpGb8U79vL/bz7Ms78iDP6dGqJcRrpWhpA1cGsMWAHS62aTHPLLc+vL/YVlz+jHjt9Ck4EhgeREue0wDDTNo3tc/hWjXYHBKX3f7M2m1Lx5FLsDZ2fxFOXvDWNuS57w0Ok20zcn0Smt0b6+vDOlpskY5ZPIrv25HtXOWV6Qa1zXPa0FzQfkCbE22nj5pU8ck45JNceDpOUZKUEn9QA45uhrhEnxNuDsSLjhccVfI0+Gc2SatGFLOR3ZaSJkAAmInczwhOxtLE4yXPgxZMl8oRZfVe3GBv9PVLrVSBTNjIJPMbeivGCeO0Znu3H0PF5Q7/AEpbRdpc806kAioWgyCGPtqEQd+CVjyq3CUvb+fM0YsUOG0fOs+yDFUT/VfqaJM6y5oPWfhMX9U+OXFF7VV/JG6MlLlHWdljiW0zTq0206TGtDXN06XTMuIafFdviPAuBIusmsgn8Sl/P2KNxbtdmuc0xTIcy7DLgCbjT8W24uPdYIxTfAyDbVMvlOaNc6m0eBoOoBojURxJ+pTJb01fS/nJEo0m+wmljqb3OGgwwHUC7cl8Cwm1x5XKrGFLd395PxR5T5F1UU7uZAMkFjoJbc7RZzeXEK8vdMZOc3xLkQ5o46w4m0QIAAAHAR5/NaMfMRSM6J1HSP8ACdjxOckiJS2q2OGMAFl14xS4Rhbb7Kuaqzq+wRVwTVxwVEuZZSZ7yl4XjgNiocbJTPZdmHeS1w01BuPqFknjrlDEw6UosRqQQfW2NXqDnmVd9WYY1pabGSQVkzRySkkopr5sZDZXL5CaVING0LQkkqQs0ZWDXAk2297LJrM+LHCsjq+h+DDOb+FXRXM6RI8IuFxNTFyXwo2Y37hGV0xTaSSC47kWhvIJ+lgsa5fIvK9zF2aVTfok6qT/AALYkKTcgTx47Lmyfg09DKlg2gNcQfCfjaIHl4viM8QojFzd01Ff5ftff3feVVydLz4K4jOmdAeB3i/57BZsueFfB2al/T8tWa0/EPFLpgtjTvNun4VGNy6nb/D+fiZJra6XBxnbrOa9Jv8AScCx0jvRBc2f0xPgJg34wY2K36fTblvk7XS+/nn2GY4pvlcnz/A16gq9410kbl0w4/t/i637o4qopqMKyRp9+DsOzGYnEPFIEt+Iwb+NrSYcJ2OmPyVTNmkk4vm+jmR0zffgyp499XWNBcQdJBkknePTboFzpqXDb7OvDGoRpGNajTFQ6WNp1BwAIY8cIB2KmWSUo89DsWSUV3+5liaNPS5zg5sAmxETEz5qISlaS5KZMnDvkRd41zdN49JnmtlNOzjSk5S3D/IsppO0vxQD4A7smRLRI0VBxjwkHqlT1Cjahx+n3expjiclbPomHxrHABpgCG+GwDQNgsqqXLdc+P37/AZVcAecVy/+nRYXWPi6xDiSbTBi/NLlcnUevf5+S8VXLMsrxAFGabYgeJt3HU2S5xk3BEG2wlXk5r7P/OAa55FeLLavd93TAIlsENA8RmWmOPoqXbpfgNXF2wVmFA8IkA+GG03GDyMetoUpuRNlKoGGeaj2lzTpu2GlpBjxTEtIABBumwqS2rv/AKWVzVIMOEc/Q5jQNTA5xFm7yA7rtI5qri7r6Exg3YqzfCmCDpPHw8DfaeKnHkSl2Oejy1aE2Xy2xsQuvjgmrTOdm3KVSQ6pukLajMyYQopOwspovKNnxbgviiwamIqJ+0GVmO+p2e25jiFE42rRaL8MrluMFVmofELOHXn5LHkh/khnXDCYSaJOyzHtS9sBlMi9y4TbyC6WXW5rqMf9nNTDcJ2tY4DVTcDxI29jdO/vlGNzi/u5/wCkjjD5jTqDwuB6cR5haseaGRXB2STWcADN1h1uDHlS3q6Nmnzyx/ZDKOKFRsCzov8AdYJ3TSLp82VqiGbwRN+EfhVHcY8vlFlyxRi6r+jrcDdc/NPK688D4xh9DTLcJruQQAfmow4pZfHATdOhri2mDE/D4eI2W7JGotL24KQfK+pyWZYYuMj8K85Ot7o9NgyJQ+JlcHVrU43A5fmylTcKYvPDDl5VNi/tNSovo6S4tizQJufiOocRMxZb8Gbaqj+34nL/ALfJCfPIjweQU9GvvIYPDyL3/qAB5EwSmTzS7a/n7Cpyd1R03ZnIG0qrHl4JJa+A08G7F3ExI4bKN73K/C/1YiTtOkeOHZSIdFy8uMg+IfpgcrlKxZlBQbXHt/PBoTVNfL8xZjKranxNA/a4WIvseYRaXXRTa0ch2gxRb4QIJsevErdpcal8Rn1Emo0JKeIIOy2OCaMK4HGS5pDtJmDOkbgH6LHqcFxtGjBkp7TtTiS2lTAMSCT1MrE8W6ovo0p8tjHK63dBxe4kvbtvAIsehunRxRScF/4Uk7N8BRIGq40kOEGHGOvLn5rbj0q237fiUlPkHxmCbTqOAdTotdJ1MaSRO8kHVHltyWfUaWUJKLfAyE9y9zLNKrXElrn04MFx/X4QQ8Bp4iVhnxK0Oxr35FxqPf3DaUOE6XVIvrBJJdwiDPomRUe6pm/BCNvd+BrnmekVDRY74QNR4kmxHyUyhKSt9G3FGKXXP6ADTq3uev2VcSSfJi1mTMn3X0AMZQ0ukcV1tPK1XscjJ3YVhXrbFiGexuObTEu9gplJRVlQPAZyKj9On1CUs6vngBseEK+WTULgTFc8mwbIutMSpxGMpHC4m3wOvHNp3HokTjtfyY1Pch683/NuCxzi4yaJTs+smgw2IC9EqfKOfRm7K6IE6J6BIzKfUIr6hGMfIJjsCAWupMDbXsJHO/Fcx6LLLI5S/FcfoaYyilSKVdVgSnZIPHCrJi7Z51WNljsYMsBjg9pa/wBevI+d1b07Xuid1GeNwwBlux2WLPhp2h0JjDKmEMjnx8jsFo08ajSIk12EObO/p08oWlK1yinRzvaTCaaZeyTFy0XdbcgDfnAXG12iVqUDqaTV+MhxuJr1RHhcQbjdsA9Csa076lwdOE8X2lQbmuS3aSZYHMcW7kw0FzT0Mp+x4Y+olw7RheqWRU3T/wC8Fsuy7vmaWNFMMIgAAt0uJJ3Fj91XDgyZ58c+79v57GPNOON8uxng8I7Dz4tTiIaTIaJEXaN91plpZYnw0J9RT8CvOnNLoYZtHH2Sc6hvqHQ7G3VsVsBFjt+bJSXJZ89CftBhnOp7yGuDuoEEW91q001CQjJDcjnKeCcT4T8pW95UuzM9P8x5l2DLWAOIkuAnTpieHyWLJlUpcDoQ2obYDEzpY8eGC2Ru3a49v5VNtss+B7gLQNNgdzeRwhb8Pi0JkMTVgHl5fNOlOkVSBw/Ub8J35cVnb39l1wJ+0j9dGA4tqMnQWtDtQggNeI4AmDyWWkpcq/2NOK74FfZBtTDsrGs4FzJfAMxLbA/nFGplCUk4KvH3m3TRlT3PtnOYcVH1HPJJJJI9TJ8lpltUVFDvijJzk+PB1j2hukA3tPXZc1wkm3JV7CNTlU4pJ2zHG3jzWmMpp3Hs57quSKJHBdTFdLd2ZpFqmCpkguEzzV8jjFXIqrZPdBvw02qk99tKKolV7k03wb79Fhg9uS8i59uBj5XAY2qu1GXBnEHa2mHMa/8AafkbH6KuXmJaD5D8LUa5jSNiBCjh8leUfWmsMTw5/m66M82OEtsnTM6TfRLTKPVhV2vxCmVcFZkAGLbYlYtXG4j8b5Fr3rk3yaArLHDUJFltw21wLmNM1afCWCfTksctLnnl+LryWjkSXAXQfDGwIgbfz+dUzLD0ZqKXFcDMb3o2ZiR8h7DdWjl4CURbm9UEADhJPlyWbPkjNJLxy/oMxpp8it+C7yY3Fwen22S4W20XcqM3Zc6Trc3SALEwUvJpFbybq8/9F7/CRtQxFOjT0suXEknbkIHsmf3kcUaxq2+yPScnyKMdjC6T7Dosk8sp27+4dGCQm1SbpOOPIyTMC+6GSi72BzT6hSkVYlq93IHHe1iOcrQr235KVya1abSBfifUdUqN3ySTh6sAx+4fKVLvcVHmDxdt+S2xyUhTjbDXVQRYqJTslRBa1aBeYMzul+pXZbaJ8ViYI/JCW6tMbE2rPpllQskd4WzPRuyjKlLJGMDdgltxtyBsrwrWkuA91ux42uWZs+o3qjfGjxDobLNqYve76M8HwZ1Dw6fgVYKTklErKq5K4cXXVh0Z5BWmLxJUzxr7VWyqfg8HzwIUQySbpxaBpe5m+mFZ4YO7XZG5lQI4qceNQVIG7F2e/wDC/wAld9BHs5nD5g9rQ0Gw+6TbGNcn2bF9oB3h1Q5gI0tBLXC3GRpPulwyYvVlLIk231fKMKyvpDfBZjSq31EE/pdLT7Hf0XRw4dK3cEr/ADJeSXVjN1MfpjyM/wApu+cOJK17r9g4YK5oII4qZNTiWjwJMVhy0lcjLicWaoytE4OpBTdPKmRNHSYR9gulHLD3RncWGTIjzWDXTxypxkm/r4HYLXAnxD9FTUGki8j6g+oXK3xjPdFN+6NqTlGmXw9UVBsPrvZMwTjlXQrInBlKlYs1AECYFt/y6ZKThdPukVVSF+IpGbX8+azTxNPjkupAmc06dNrCSSTc9PJV1GLFCMG3b8l8cpSbSEeNxjSfA20Df+UmbTfwLii6T8gziCZ2Q0rsizF+91RpJ8l0+DRrvmoQM5DtEGtrtIMTuBtK6Gnt42ij4aCKGJkBJlCmWYRJCoVCaNU78JEqCUhtg6xO2ysu+CC+PxMnbhtCrknuldBGNIT1mypXRKdMxIJaG8lCTux0si20M8KfDzXUg7imYpdk4wHwEC17dbLNql9mi+N9gtQ29VfFj2C5Ss3otAF1o9SEPtOhVN9GgxASf7/H5TLekyG1gT91aGtjOSil37kPE0rJctidizMqQFHaYxRPUgfOfool9ktDs57D4NzmggWP3SdrZdtWfUMT2KBvqcfVaV/TMcejmJtFaPZ17baiW9d/fdKn/TojIs6TA4moyGm4ED2W/G5JUy9Ib0Kk8ExkIjFYcOCRlxKSGRlQgqsLCuVKMscjQmmh3RrB7Wgy10QHDb/sPqs2o0vrPcnyEZbeAnCS34zJB24QOPWVljPFidO7Xf7F2m+jfEXAc3jccjwK2brSlj88omPsxJnDBQcA20hp5jURJE8Al6jAtPTh5/Ubjn6t34MWV5Gp25JtY3i3pdQsnFy9yHDwhhgDDRUePDOk8+p/OSfintipz66f7ipK3SOb7U41riQCIaPDHJZ9U4zbrpdV7DcKa7OXpuJKyJWObo0e6FZqmVIFS/ojt8k9Iiq+Bbgo2+xK7OS7TC7TxM8vzkuho7plM3gBwuKjdOnjsopDalieqyOFF7DaFUlukmyXL2J+Y1ynFhh8XKB9FfFOMX8RSab6M6tYlxcPRJfMrLeKM9U/nFXRUsYQ5JE0FYAgAzzW7TyWwTkTsMdTDhLiB+37qmapdyr2Ijx0KcQ1wMt8QE/kLIszhJpP/prw48clUzSliGloLoE8vZOWojJtZF+BXJpWpVj5L1MOLQf4S8zxUlBfUTFSXZnTonUQZ8+aplwTSuvwBTQZSw43+q6mmji7jw6M82/IQ3DLeoC7OYz+m6vWFFmzLuPAE8/T+UrIre1DIOlYxoU2U2hgE6RE8+ar6kY8Fab5PqoK6xko8WAqKAjuAoomzahS9Bz4JObNDEvi/DyyyTfRLKzXCxlXTT6J6Ma+FDhdLyYlLsvGVArGlm/DY/dc/JhlB2hqkmEsxBIgmCdisUsGLLx0y9tDCm0uYGhwkSTwHWFeWGeKGyPMf09yFNXbFuPw4fZ1wD8vsk5IerTbbQ6MtvRH+lBBHtvccvkFd4VKyqm0C45rxSFIHw7ykZY5I41iXQyLi5bjjcVhDJ5rHGNMfuKMYADa/wAlojSi/cW+WAYisEpuxkYgrsSZsEV5L7QfFY3S0ucbcfsOavDG5OkDqPLOXzHGGq6dgBAHLmunixenGjLOe52DhqZZQ3ZWLeKW4qRZSGGFzIbE3SJ4GuUW3Ia4fFgLM4FrC245oH0Cqk0HBVmJBP56oUJeA4KtzEOs0T5bKfTm+A3JDfLMET43ey2YMG3licmS+EMsRQ1CFGpw719CkJUAVcrcJIJHK/1WKeCSV1x+P6D1kRk/AQ0kAOdIgESB8vkrY9NkkNjqadN8HsTRNN+k6oMQ4/qMJDxzitzRuxSx5sdMMZaOK7Wjk3jXFHI1ONQm0mGUnt8l0YuJkaYJn+Ztw9Iu3cbMbzP2CtOahGwjFydHPZIwtomq676pJk8p/wArG5bYbn2xr5lSL6lz223bL0fRMgzxldsfDUbZ7DuDzHML00JqaMMo0OQVYgu0qAPY2nqjUSB+2QB6rlyhGWRvHTfnkanS5K03RYN9k5vU1UVFfj/wj4fIVSJ06iIAIlouSOZKyZ5ZsLUpfFJ8Lwl9P5ZeO18AmKxLR4jZpmLbxuo02olGUoZZX1Xf3os42rRgNLtgtU8MMnNEKTQQHkcPZL9HJDrkm0yDVmxt1G6NsZKmq+hKdAdYObxkcCPKw6LBmxSg/cfGSZoytpadVuhRjk4p3+ZElb4EjizUSWyLpMYxvlcDG3XYrxgbpPPgOSVKC215GRfIkrsHGPdK9JjfUQvxWYsaHNADiduPy4psMRWWQ5zGh9Te0bN4f5W2CUFxz8zPKTk+QejhL+KR5QfJWlk44NEce6PA0ZkbpjW09C5sidpErM9SvYVsoCxuDcHQLxbldNx5U1ZEosEOEdy/hO9SJWmEUaBFp9ilykmW6DG0iYBcfdKbSCxlh8jed2k+oP1Snl8IjcPMsyYtNyJ5TeFfbHzJr5roW5P2H9CjFtjyhaoYptXGaf3C3JeUGtcI2W1Q45F2YvpT0WbJpZf/AJOi6n7nmULXutOHDsiot2UlK2TWwrXiHCY25g9EvJo1J7k6ZaOVxNadADl7J2144/DG/wAiJS3O2wLOMYzD0zUe0kDkJknYHl6qq1WO6kqft+xCg30cFQpPxlU1qtqY9o4Mb90rnI90uhragqXY3rVZsBDRZoH8LLny73S6CKoygpBY+h9pMl7h78TRpB5MX4iOIjYrs54ZJLdidSMsJLqXQoyztsx7u7eO6dsC8WnlvZJwerJ1knz+RecUuYo62hVOjwuBJ/V9ltzYPVVNiFKjNmGvLiXHr9lOPBCHRLk2EgpxU3o1YWfUY3ONRS+8mLpi/M8OXu6cOQvsufj0kre5D96XRtgsLpF10oQ2qhblYU5qvRFmL6ahxTJ3GbqSVLBGRKmxRnOVVKjNLakdCAfSQkS0UJDFmaOOx+UZi34XBw6GDASpaH+WXWYQY2jmIN6Z8wGn6pT0deGX9Uvk/ZmriGPfXfUadWkNsCbAlxnhcexSMu3HJKuWPxQeSLdl/wDx6pSlzhYuc0Hj4SQCR1iUxQg+BMlJcnv9B0+SZtSKWYUsomq0Q4AzJiwtKTlxya+FGjFl2+QlmBqOc5rqboaSGuLZkA2uFilpskeYo2RyYX2yf9kqF4IZ5ybT5JsNLmca6Mc8kE+HZo7sq5xBs3ed3T72+S1Y9HNLliXmQbQ7JsbdxJHt/CXnePTr4nywjJz6GNHK6TT4WT+c1owfFBNxpi5PnsZ08KOS1rGvYXZsKHRT6aCyxw4PoqR00Iy3JEubL92nbStntCskRZ7QpoiyQxWoBDn/AGnp4cFrYfU/aNh/7H6JWXNHH9S8Mbl9BNlNeu8VX4ozSqsLdBtvsWjgAubmwPK1km6aHblFbYmD6ogMbZo2AS8ua/hQKPllCVnLnjPJSQfaaGJgQdjwK7UMldmNxEHaPsVQxQLqY0v5BNlCM1z+JEZuJxLRjcvfF30x+kyRHTkqJ5MXzQz4Z/U67Iu09HECAdL+LHWPpzWiGSM+hcoOI9BVypcFAFw5QBdpUMlFioJKFSBGlAHixBBU0wpAyfh2ngoJTAcVhNNxC4/9VTioz9jqf09ptx9wbE4cGnI4G48+KyafPHf9f/RmqxtJIU4vBtaRsSRJ6dFsx5VNuvBhcaPd0RT1QBLoHlAv7qksk3lUU6S5ClQbh8NIBXUjHgQ2avwwCTLKoupJk1fRVlMHZPSsrZL8PLSPVZs2kjkmpPwWjNpUQaQYySSRxshZI45bJfd8yatWi1MSJC0rkoy+hTQWT3amiLJ7tFARoU0AszXO6FAeN4n9ou4+ipOcYdstGLl0cni87xWLJbQaadPi7jHV3D0WaWac+IcL3GqEY/a5MaODoYYanRUqczsD0HFJcoY+e2S3KRjVxj6jpOyx5M0pl4xo0aISSxYqxBAKAPrmv+y6jMho2pG1laMnHoGrLYh4e3TUaHdf7rRDLHzwUcX4OYzXsXQqeKn4H7yLK0sMZcossjXYrbUx+EsR31Mc/ijzVbyQ75LfBL5DTLu2FB9nzSdyft7q8c0WVcGh/RrtcJa4EdDKaUCWGyqyUTKCTxKCD0qQPSgCsoA9KARjiWgtMrn/ANSxqWCV+OTfoZOOVUJMbVMaW+q8jCPrT2rpfqd7UJRhb7YqfIO67mkw+kuzh5nbDcO8OEOiy3SyQxrc1bM1N8B+Hfqs334eStj1OV8uHH5lXCPuagcDY8lqxZseX7LKSi12W7pOoqeFNFAWDfbiOCRmwRyKmWjJoGdhy13g+HiDwPRVw48kOJO0TKSZtoWmihji8RTY2XvDQOZAWfLhg/ibr7y8XJ8JHMY7tXSB00tdQjjs2fqsM5Qj9mUpfeaVhl/lSFdfEY/Efq7qnz+H57p8ZZ5L4uCjWOL45Bf9uw1HxVXd67qfDP1VHsjy+WG6T6A8b2hLvDSEN6WHoEnJnb6JUAGiC4y4knqsrdlxjRZHsqEmo+fBAHi3mrEEAFBB9ZB/Oq6plLA8hJ6qCS8/nAIZBBN+nmrRnKL4BpMq9543WiOo/wDort9hdjMqw9WdVMTzCv8A/wA5kXJCap2TLDqw9dzOk2VfRa+yy/qX2hhl2IxdNumq0PjZ449COBSMr1EOYpNDYLFLh8Bjc9aCA9pbNpiwVI63xOLRZ6b/AOWmEHOaNvGLgLStTifkU8M14CaWLY7ZwPqmqcX0xbi14Ng4c1YgiUAQgCpbNkvLBTi4vyOxT2ytAuPwLdPhEFYFoMcY1BUa5aucncmJf9reTdWjpWIllTC8PlULTHAkJcxnQw4Cbt4opZhmVL+pIbIhcnHgzY5/DVDnKLXJNPUd4C0yWoq5ypfIp8PhAeLzWmxwGtvW6MWr3Pnot6bKuzyl+nU//wBQT81q9WL65K7H5Aq+c13f8WHPm8gfwoeST6iTsj5YBiG4x48VVlMf/lJms8v8kkNhLDHxYmflVAEmtWdVPKbJThjTuTsv60uoqjOtn2HoCKbGj0kqPXjHiKFtOXbEGP7T1Km1vP7JEssmWUUhUS55lxJSXIvQXh6Pz4pbZIxo0fZVYBgsOYQB7zCCCHnnspAgA81PJB9XL/l+XXVZlLF/5zUASXeyGBIfaygDNzeZUUSUcJ6oAGcDuD6XVlkkumDSI79zeKctQ12V2mbsd+4A+it68H2G1oye6g7emFDjhl2kWU5ryY/6ahwkeRSnpcL6GLPkKupMiBWeOsoWniupP8QeZvtIzaHDbFP9YKck1/kUck/AZRZWItiJ82hMSl7lbj7FnMxg+GrTPm3+6hrJ4aJTh7A1WvmA/wDrKo/WXsWvH8wStjsx4NpyoTz3ykEvTriwV+JzU/qpN9Fe8vyKfCZBuZE+LEtHlCXJZX/kkWTgvBqcPXPx4w+hSdmXzkL7o+IkNpU23fXqOPmUOMK+KTYbn4Rk/G4ZlwwE83GSqL0ofZiTc32wGv2tY2zSB5BQ9Q10R6fuLq/bM8NR+Sr/AHEidiFeK7TVn7W+aXLLJ9llFCutjKj93FLstRk2mobJo3pYdVcgDaNDmqNkh9Cly2VQDGU4hAFrckcEEDZSgKzB6FSBm4jqoA+sarXXX7RkK1HAC26h0iUXY9CILarSgCpdvdQSUbYKEBm47/X7KCQesxQ0AI43tv15KPJJhUpzJ5fRTVgBkTMTuoTsAPEkt477KG2iUBmrUE3/AIUJskhmaVm7FXWWaI2olvaetyCn+5mGxGFbtVV4j5qr1MidiB6naapy+ao9RInYgZ3aWpy+ar68idqB6naCqeSq8rJ2gtTOqx/UB6KvqMnagarj6p3eVG5hQPUcTuSVFk0V0oJIDUWRRIYiyTVlBVbAKp4fkqtkhlKiFABdOhHkoAIY2PJQB47oA8XKSCAOCmgKT/KAPKaA/9k=" alt="Chaat">
    <h2>Chaats</h2>
    <ul>
      <li>Pani Puri</li>
      <li>Bhel Puri</li>
      <li>Dahi Puri</li>
      <li>Samosa Chaat</li>
    </ul>
  </div>

  <div class="menu-card">
    <img src="data:image/jpeg;base64,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" alt="Desserts">
    <h2>Desserts</h2>
    <ul>
      <li>Gulab Jamun</li>
      <li>Rasmalai</li>
      <li>Ice Cream</li>
      <li>Chocolate Brownie</li>
    </ul>
  </div>

  <div class="menu-card">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwA5E9LED70gvToBV0lsV2ngZRHLX9nNDU2Q&s" alt="Starters">
    <h2>Starters</h2>
    <ul>
      <li>Paneer Tikka</li>
      <li>Chicken Pakora</li>
      <li>Veg Spring Roll</li>
      <li>Masala Fries</li>
    </ul>
  </div>

  <div class="menu-card">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTguE93hDnpX6RG1NSS-nyQJfEPE-RdB6IUcQ&s" alt="Main Course">
    <h2>Main Course</h2>
    <ul>
      <li>Butter Chicken</li>
      <li>Paneer Butter Masala</li>
      <li>Veg Biryani</li>
      <li>Roti / Naan</li>
    </ul>
  </div>

  <div class="menu-card">
    <img src="data:image/jpeg;base64,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" alt="Drinks">
    <h2>Drinks</h2>
    <ul>
      <li>Cold Coffee</li>
      <li>Lassi</li>
      <li>Lemon Mojito</li>
      <li>Masala Chai</li>
    </ul>
  </div>

</div><hr>

<a href="mainmenu.html">Back to Home</a>
<hr>
<br>
<br>
<footer>
  © 2025 BITEBOX Restaurant. All Rights Reserved.
</footer>

</body>
</html>


```

```
about.html



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>About Us - BITEBOX</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #f5f5f5;
        }
        h1 {
            font-family: 'Times New Roman', Times, serif;
        }
        header {
            background: linear-gradient(to right, gold, black);
            color: goldenrod;
            top: 0%;
            position: fixed;
            width: 100%;
            text-align: center;
            padding: 10px 0;
        }
        .chef-section {
            text-align: center;
            padding: 80px 20px 60px;
        }
        .chef-section h2 {
            margin-bottom: 30px;
        }
        .chefs {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
        }
        .chef-card {
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            width: 250px;
            transition: transform 0.3s;
        }
        .chef-card:hover {
            transform: scale(1.05);
        }
        .chef-card img {
            width: 100%;
            border-radius: 10px;
        }
        .chef-card h3 {
            margin: 10px 0 5px;
        }
        .chef-card p {
            margin: 0;
            color: gray;
        }
        a.back {
            display: inline-block;
            margin: 20px;
            text-decoration: none;
            color: black;
            background: gold;
            padding: 10px 20px;
            border-radius: 8px;
            transition: 0.3s;
        }
        a.back:hover {
            background: goldenrod;
            color: white;
        }
        footer {
            text-align: center;
            bottom: 0%;
            position: fixed;
            width: 100%;
            background-color: black;
            color: white;
            padding: 10px 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Meet Our Master Chefs</h1>
</header>

<div class="chef-section">
    <h2>Our Culinary Artists</h2>
    <div class="chefs">
        <div class="chef-card">
            <a href="chef1.html"><img src="https://lh3.googleusercontent.com/a/ACg8ocIp7Feb0yNJl1_j8OjNTU981J8qT7XHdMf_CRwr3jtMSvcEFbE=s360-c-no" alt="Chef 1" width="500px"></a>
            <h3>BTU</h3>
            <p>CEO - BITEBOX</p>
        </div>  

        <div class="chef-card">
            <a href="chef2.html"><img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxAQEBUQEBIVEBAQEA8QFxUQFQ8PFRAQFRUWFhUVFRYYHSggGBonHRUVITEhJSkrLi4uGB8zODMsNygtLisBCgoKDg0OGhAQGi0lHx0tLSstLy0tLSsrLS0tLS0tLS0rLS0tLS0tLS0tLS0tLS0tLS0tLS0tLSstLS0tLS0tLf/AABEIAP0AxwMBIgACEQEDEQH/xAAcAAABBQEBAQAAAAAAAAAAAAACAQMEBQYABwj/xAA+EAACAQIEAwUGBQIEBgMAAAABAgADEQQFEiExQVEGEyJhcTJCgZGhsSNScsHRFPAHYpLhFTNDgqLCY9Lx/8QAGQEAAgMBAAAAAAAAAAAAAAAAAAECAwQF/8QAIxEAAgICAwACAwEBAAAAAAAAAAECEQMhBBIxE0EiUWFxQv/aAAwDAQACEQMRAD8A606LFtOMaQYsK060ABnQolowEtBMOC0YAGJCMSAAkQCI4YBgABiGERBIgMBoBEcIg2gA3EMctAIgA0YloRE60ABIjbR0xtowGmE5RFMVREAtp0K06MC/tOtCtOkBCToVp1oAJaJaFOgMAwDHGgERiERCxCqCSSAANySeUeOArXI7qpccRoe49dpMyChqq6uSKW+J2H3PymkoZhVpG6tbhe+4IHDj6zXh43ePZsqlkp0Yuphqi+0jL+pWH3Ejmen0u0nKqnxTf6GSSMLXFytN/wBarf6iTfE/TF8v8PJrRCJ6Ri+zmDfhTCnrTYj6cJSYvsgP+lVI8qgv9R/EqlxZrzZNZUZAiARLbH5HiKW5TUo96n4x8uI+IlSZRKLjpommn4DaC0cgNEMbIgmOWgsIANmNmOMI2YAAYSwTCWIYcSLOjEaCdOiiRELadFnQGDOhWiQAAwYZgmMC87PLZGb8zAfBR/uZMriM5emiko6jV/q3hM87OKPXGkZJO5MBhJGGvGV3kjDiMRPosefzGxk5aJO4N/XaRKCydTuIqAgYxXQ3IIlXjcDQri7oA/5k8Lep5H4zXI1xY7jz3kavlVJtwCh/ybD5cISSapjWjzbMsiqUgXX8SmNyQLMo/wAy9PMfSVBnqrZW6nwkN/4n+PrPOs/wzUsTVUp3f4jMF4AIxutvKxE5/IwqG0Xwm3pldAaOQGmYsGmjbR1o2YDGzCSIYaQAW06FadAC+tFtOigRCFE6KJ0AEtEMKJAASIDCOGR8bi6dFDUqnSi2vzJ34AczGlboRq2FlA6KB9JEfjHqONpV0FSi61KbcGU3H+x8oyx3ndfhjQ/SW4k2gvzkSgJY4dJAZNoptH6R5GNUjaOi14ATKYjojCOBCuW9k284AOP8rTyLP8d/UYipV5M1l/Qo0r9AJ6D2txzUMI292qWpA8CNQOo/6QZ5gZi5c/Il+JfY3EMMiNtMJcA0AxyA0BjZhpAMcSACkToVp0AL4ToonWgROnTp0AOiGLOgAMyf+IFU93Tpj3nZj56RYfUzWzIdpaffYumg4Itvid7faXYF+aIy8E7LZOaJDNiXw71AG00rE6eRcNsfQiaHMe0VXBVlpYlFxFN1DpVo/hsy87odtQ5i4+spsxxiUG3XU7gNcm2x4AW6DaBVVMThqZLeJC+xJJAYk23+E0LLO7+jRPBBRpem7yfPsHiLd3VCt+Wp4Gv8ePwmlw6EeY6jefPb3NwNgptNL2axmYU7dxWdUHJz3i/JuA9Jd8qXpk+K/D2xFuIZSZPK+0+JA/GopU6tSJpk/wDabj6y9w/aTCts7NQbpWUqP9XD6yUc0H4xPDNfRcUQCN4476eAjeGqo4ujK4PNGDfaOVL8OcnZXRiP8QsXqalS6K1Qj1Nh9mmPln2hxXe4mo3IMUH6V8I+1/jKycvNLtNs0wVIExthHTGzKiY2YJjhgGADRjiCCRDSIAokKdAC+nRZ0ZEQiJCnWgAkSdDx2EqdwHpmz3vYWuU8vPnLMeNzdITaQ1UawJ6C8yuXp3ldnPHUfnJzV2bYux63JMey5As0Qgsd7JKNsZz7LO8pFgLlF8DEi6G99PmLfeMkDQrhdPgXYcrDhL111IV6iV1SltbpIJNGqUk0Z3LssZ2u3A7n58Js8uwwVbKNhIFBNPAS5yyso2PORyNsjCKS0FTcA2O3rJf9Stt0ZgOJUAxntDgGNLvaBBZdyp4MPXlK3IMzrVSaZoODwvdSg2/N0kKJWWtLG4QtYFNV7W2DX6CN4/MVQNSWrUZ2HsmpUYIp5kE7SDj+z7YekKtNRUrNUC7WQKpuSb28pEDAgWQUzzA3JPUnnBuiE3SAIgxwwDKikAwCI4YJgA2RAYR4iNuIAMmOIIJEcQQGLadCM6Ai8MUxbRDGRBizo7h6DVDZRf7D1jim3SBuhulT1MF6n6c5cFSOI8PAW5CWeUZQqLdtyefX/aSsRgrAm2w5eU6eDD8cd+szzn2Zh89yAvepR2c7kcA/8GZnC4go+hwVYGxB2IPnPTjRtw4fYyj7S5Elcax4ai8GH2PUQy4r2i3FmrTKzDOCPW0brUd7yHg2em3d1BpccOjjqp5y3YBhM38Zqf7ICrDSmbgjbf5x7RHaI5SLGmXWWKStjwI3iJiFQlKS7KdyBcA+cHADkTYfeZw5nVwVdwyE03qMQ4OxVzcC3xtK6stTX2anN3b+mY+nyJAP3mUlzi8x1UTT5kjgb2F7/CVFpXL0oytXoAiCRHbQSJErGbQTHSIBEBgxthHIDQAatHUEAxxIgOIixTOgBdwTFJ/vpLjLMIQNeyta4LDUfgtxYeZ38pow4ZZHrwqlNRAy7I3qbvdR05kdT+UTT4XK6SLZR/H+8j4RiCFuSTbUdraulugk8bGx2P8AfCdLHijj8M0pOXo8lAAW87wUbexhJfjBqLfccZYIiYvA+8vy/iQTTuLHnLujUvseMDEYQNuNj9/WAGHzrKweIuL3vwKnqDylFSxHdsKb89lbgD5HoZ6LXwvusJk8/wCz5IOkalPEHf5SjJjvZfjyVor6rWPCNPitPAG8h5caqakq+OmpshPtgcwT7w8+M02XZE2ITvKZC8dmuL/ITP8AG26Rp7pbZQLXZmHd4gBjtoIU3J6c7/GXmF7P4vEBqdUCygMO8pvS8YPDe9/WXWTdjUpVVr1SGZG1BV9nVyJJ4zWXlkOPa/Irnya1E8ox2CqUW0VFKt9COoPORZ6rmuW08TT0VB5qw4oeonnOcZVUwz6XGx9lhwceXn5TLn47x7XhCGRS0/SBEMKCTM5aAYDCGTAJgMbMEwmMAtAADHUjJaEHiYxwxY1rnRBRpMJSDHU3sKQAPzN1mywlJRuBcBLm+924zJKQXCr7KCbDBG1K43JE7ySiqXhz272yryzH8ARxY725mX9WkKqW4MNweh/iZ1h4TyOrV9Ze5TX1pbnAAMBiySUfZ1NjeTrbyBmeGLDvU/5icQPfUfvJWCrirTDDmIwFq0/eHER2jUuIl97QCLG4gA8yA7ESDiKO4Qe9c3/Ko4n13k9TeV1KvqxLqfdVAPQbn7xiIuaZFRqgWGkqLC3SP9n8J3VPTyuZY1N9v7tCVbcIuu7H21QQnKYgM4SREK8ZxuDp10NOqupT8weoPIxwmIxkWr0NHmnaDJnwjfmpMfC/7N0MpWeerY/CpXVqD+y62v8AlYcCPOePZ3TqYWs1GoLMp2PJl5MPKcrk4fjdrxmzDPtp+khqkbaqJTvjzGGxp6zLsvoumriMviBKV8UesaNcx9WBctih1gHGjrKY1DBJMfQC2bHidKexnR9EB6zhVsCes1OXVfwx6TNHZQJoMqPgF+YncZzR+pSU/GBgz3b+RjxpRt6J5RAWpexvyMh4JO6qvT91j3i+QPEfO8XDuWSx4iJUqjwHncr8CL/tGBOqrcQUe43nUKlxG6q2NxAB5NtpV5t+FWp1/dPgb+/T7SyV7idXorVQo3Bhb0PIxoQ5TG1+u8UyJldUlND+3SOhvhwPxEmRiEnat7RDB7sXvEM6s1heAxOodI642I8jGXayjrAEMo13v5yn7ddnBjaGpR+PSBZD+Yc1PrLiiu95MUjnITipKmSTp2j5yq0tJIIsQSCDxBHKMmek/wCJHZkb4ugN+NRV5j848+s81M5GTG4SpnQxzUlYhgGKxgGRRMW8QmIYBaSoQV50bLidHQrPYKxl5lTeASgqcZa5VUNrdJ2Gc0vVh0xGKZNo/TeIBQtmuIOIpWF/MN+37x07xG3UjnbaAEehW0mWD7i8pqx5yZgsWCNJjAkiFTaxgA3i3gBCxLmlilb3Ky6T+oG37rLW8rc9p3oFhxQq48rGTsNWDorfmUGMKK3tJ2go4CkKtfVpZwngGo3MiVMemZYRxgMSq1GGzKTqQ9GXisu8Xh0qKUqKrqeIYBgfgZhc1/w5plzXy+q2DrjhpLaSfhuPtFZJURsN2txuXuKGaUyUvZa9MXuP/b7zY4bM6FZBUp1VemeBU3+fQzz7Hdpsdgl/p86wgxWHbw98oU387+yT/pMqVwiFziMkxGocWw7nTUXqNLe0PI/OVufUs6dj2EV1tcbiRrmpuSVp/VvSYLJu3lNx3GKU4asCAb3CHrx3U+vzm8TMaIAOktsLezpt5bw+SP7IrFL6Qpw4YEabIQRY73B43niPanLzhMU9Eiy31L5oeH8fCe9YTGGqCVAUA25HfylL2t7N0cfTtUW1RQdFRbXU+fUeUrzY1kimiUJPHKmeCtVgGoZKxWCNOo1JvbRihA6g22mw7LdkEJD4pbk2Ip9B1e3Pbh85gSRsTbMGSYOkz2XN+xODxCjQow7r71FVUN+peB9djMD2s7NtgWTx95TqA2a2khhxUi56gx+CcTM92Z0eMSFio9XZ4/l+IcVABuCRGGIsPSWmS4e51dJ1WYDQIdohrgRio55TkwzNChBnFmKuL3iHCERqrQIjAPGW9ocG+/OREqWMfJvTI6EH9v3kRVvGMsqGMjj1byuSiZMThEBIwzGpTemeJUgevKDkGIvRsdirEW6eX3i4WoFuzEKOp2lVUzZKRfu7EM5YE8r+XrISmorZKMHLw0VR5VYzOadFSBZm68h/MzWY9o2ItqvfpsPpM/XxT1ee0olyP0aYcZ/9FnnnaF6wKbOCCPEAw+R2mcyXIsHSqCoyXfVcWLAKfLpJSkIbnhwMdFNWYWbYzPLI2aoY4r01dfK8FUK1KtNKzAAAuNZHlcyWDhwulaagDgFCgfKDgsCvdC5NiOI5SN/wuh71WofQgfYSu2OlZZYPF2000uq8NPAcd/8A9k/F41KS6mIu1wi82b+JmsZhaGjwd4HSzB0LNUFuY339JSZhm5L0Q7JU094O8UEMRYbOh3Q9RNWKbUGZc0E5ou8zxAq2Z0Qspup0JcHqDa8i5PjgxIG5HEc9tv79ZHqV9aeE3PHbpK/KKJTHk38D0if+7Uu8qk7LscUbPEV9JUE+0T8dpGzrA0cTT7mqNnB0nmjgbMvnvG8WuvFUgD4Up1CbbgklQPsZIxR1V1APhpqzHzJ2H2MrJtHj2fZNVwdY0qm9xqVhwdOo6enKdPV84wGGxFInEqGQMNJvpKbi5Dcr8J0VFdFWu+kTV5Rh/wAMED2vtMjRq7bc9pocpzg9zoIsFuNQ5r5zqnOZcnSvmf3gf1DB9rtt7C/cnlKuhiifxTwB8I6+cnjFEjcBSdyF4D16mMRJWtVJtpUfG9pKNW2xFx/lF7fCUWQZgKlWoC3hJ8NzyHG0uqlf8o/k+Z6CFgRsVhRYsm4I4dDI9PCMNyQPrGaNeo9ckn8NPCByvxJkmrWhYBaEG7MbAEn0HGUOZZ+o2orbzO5MsMwf8Gof/jaYWpczJyMrjpGvj4lLbLOpmrPuTv5/tINWqzc4FKkZICWmJzbNyil4Nf0u1zG2GnhsJPpDrtEOW1GFwjleoViPnaRtvwf+lRUF/OHTp8LyaMMAfTrDFMdLyLbJosRWrLTB8QUDbzlUMXXLWAAuedz+8k/8TVgF1nRuCUswFuXzlhl9FAVu6sjWJLAEkHa4vt5kWmjFx+6uTpGXLyemkrZIwjKtjxa1ib/O0zvbclTSq011HUQxUXOm3MjeXuFoqdyqvZzZVXD2K8SwAAOxBA46um+w5xldKpR1Du1LB90UJuBewbVe9jfhOhKEFGk9HPWaTlbRjaeaqviV1HUEqPW4kqnmxFalVRdQ3DAEG4J4iZzF4FalQU6VqtZy1kRVYWUXNidybA+W80XZrs8BRBr1O5ZtYNMqF0FWIBt1PPlwmDM4xh2izdim1OpKjaCoDVdg6ltFM+E6hvc2EyGaZ5XSpUKK5BOx0OQOXTy+sdwqrgsWtSjWa5ujKoUrUG1rg3ueHyE2tHtJX3sVew3uB4QfSQhKMlbHPI46R5Dm3aGtiKYoknQpubXuxHXynT0btBhjjtAqa1Wnc6aRSmrMbjU3huTvOg1vRnlknekUOS4jVSBPFQQfhw+lpb4M94Uw68xrf9PG0x+U4oprXkUJHqP7+kuezmbCg7VqgLArp243M24MnaCK8kakzUYitqbSuwHhEiZ5jxRp90vtMLGBQx40mqRpG5F+MzVXEmvWLH2QZbKRBI03Zynd18heafMK2hdI9puMy3ZbM6KuwdgpttfgfKSszzuml6pOsKRwhF6E1slZdVtUqgm9mHwOkSc7XmRwGcI1So6nZ6lx6WE0tGrcXjTsGjs0e2Gq/o/9hMYlW81HaSrpwlT0Qf8AkJ59/wASA9eg3vMfJVtG3jOos0KGTMuwTV6gRbDV7zXA24+scyTJKjAVMQNK8RT94/rPL0lxmdV9dE0qdhSv7IsFW42kcfG+5kp8mtRLzK+ztCjZiO9qdXtYHyXgPrLmUtTPAPZpsfXwiRnzyqeC6fQH7ma04RVIxy7SdsvMXRRvaRWtvdgD95k+2GXGvhGpUdCVCyEbimLBhe5A4WvJZx9VuRPrGqtFn4kj4SqeRNUSimjIZT2RNIWrYoaTuUopffydv/rL1cuwyoUXvDfmzX3624D5SVVy6r7pX43Eh1cvxHMX9GErtJUT9dlFXrtQaz+Jb2BO9vj0j1LNgOIPwF/lYydUyuq40svhPKwM7CdnFXj9Znm4/RJA0cQr2dV3PvW3tzG+4kzDd4xuQB4uVwT6mT6GBVZIVAOEqtgRlpt5/EmPopHM/Mwi0AvFYBWnRsvFisZ5DQex9bj5i0sALKic3e/wEzz44cBcn95cZ1h6tFkqFiwCqP0tbcTZxVJJ2iOarRa5xjdhSU8hK6rixSWw4mVdbMQLsW1NykCk71qgA4sbC5sJocrKki5pU3q7g2k3F4VlpWL3lnkvZCqQC9amg/ynUZp6HZHDf9R2q+Raw+Qi7xoKPN8FV0nSu5vwG89E7NPWZRqpsB1II+8u8HllCiLUqSJ6AX+cl6j0kFk6jasrc8yk4in3WrQuoEm1yQOUrsB2NwtJg51VHUgjWbAEeQmhYmDYyuWVt2TimlQcJSekaDWnd7I9w6kgXigSP3hi6jDsFD8QsIwWglouwDrVYy1SAzRtnkJSGhwtB1xkvBLSlsdD5qQDUjV50jYwi8TVEnWgAt506dADx3LKK99T2H/MQ/I3mvrVQ2oVRqQ3BH7zJ4Laon6hNSTf0InT4j/Flef1GOxWWIzE0yVW5sG329YwcudQTdbAX2Jv9ppa1BQTINalqDb28JlslRCJS08Q44Ow9GYSRRzLEA+GrU+DNJ+AyhGtckzSYDJaQ5TDaNNmfwuaZifZqv8AGxl/gcfmXOsfiBL7DZbTHKWNLBqIEHIrsJjsbzcH4S1oY6sfaAP0jyUAI5YCFiOWsTxEMNGiYmqKwJAaLqjAadqgA9qgM0G8EwYHM0AmKYMqkMSJFiStjFnRJ0AFnXgzoALeLBiwA//Z" alt="Chef 2" width="500px"></a>
            <h3>Chef Kenji</h3>
            <p>Sushi Master - Japanese Cuisine</p>
        </div>

        <div class="chef-card">
            <a href="chef3.html"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSIceIOtfEcRlEkAGH0m1e-puf7AsanlksujA&s" alt="Chef 3"></a>
            <h3>Chef Isabella</h3>
            <p>Pasta Expert - Italian Cuisine</p>
        </div>

        <div class="chef-card">
            <a href="chef4.html"><img src="data:image/jpeg;base64,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" alt="Chef 4"></a>
            <h3>Chef Marcus</h3>
            <p>Grill Master - American BBQ</p>
        </div>

        <div class="chef-card">
            <a href="chef5.html"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSOJAP6RuVZGtN4kmyaA0nTOhDT9hql5J6UQA&s" alt="Chef 5"></a>
            <h3>Chef Ayesha</h3>
            <p>Spice Specialist - Indian Cuisine</p>
        </div>

        <div class="chef-card">
            <a href="chef6.html"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRQiimIHmSzC3lYGavMfJBPh0WSHkL66OqOVg&s" alt="Chef 6"></a>
            <h3>Chef Louis</h3>
            <p>Pastry Chef - French Desserts</p>
        </div>
    </div>
</div>
<hr>
<a href="mainmenu.html" class="back">Back to Home</a>
<hr>
<br>
<hr>
<footer>
    <p>© 2025 BITEBOX Restaurant. All Rights Reserved.</p>
</footer>

</body>
</html>


```

```
review.html


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BITEBOX | Reviews</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background-color: #fafafa;
      margin: 0;
      padding: 0;
    }
    h1 {
      background: linear-gradient(to right, gold, black);
      color: goldenrod;
      position: fixed;
      top: 0;
      width: 100%;
      text-align: center;
      font-size: 40px;
      z-index: 1000;
    }
    .container {
      margin-top: 120px;
      padding: 20px;
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
    }

    a {
      display: inline-block;
            margin: 20px;
            text-decoration: none;
            color: black;
            background: gold;
            padding: 10px 20px;
            border-radius: 8px;
            transition: 0.3s;
    }

    a:hover {
      color: goldenrod;
      background-color: chocolate;
    }

    h3 {
      color: #fff;
      background-color: black;
      display: inline-block;
      padding: 6px 12px;
      border-radius: 8px;
      transition: transform 0.3s;
    }

    h3:hover {
      transform: scale(1.05);
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
    }

    .review {
      margin-top: 20px;
    }

    .r {
      background: white;
      border: 1px solid #ddd;
      border-radius: 12px;
      padding: 20px;
      margin-bottom: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .r:hover {
      transform: scale(1.02);
      box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
    }

    .r p {
      font-size: 16px;
      color: #333;
      margin: 8px 0;
    }

    .r h4 {
      margin-top: 5px;
      color: #555;
      font-style: italic;
    }
    fieldset {
      border-radius: 10px;
      border: 2px solid goldenrod;
      padding: 20px;
      margin-top: 40px;
      background: white;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    legend {
      color: goldenrod;
      font-size: 20px;
      font-weight: bold;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
      max-width: 400px;
    }

    label {
      font-weight: 600;
      color: #333;
    }

    input[type="text"] {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 15px;
      width: 100%;
    }

    input[type="submit"] {
      background: linear-gradient(to right, gold, black);
      color: white;
      border: none;
      padding: 10px;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    input[type="submit"]:hover {
      background: goldenrod;
    }
    textarea{
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 8px;;
      width: 100%;
    }
    footer {
      bottom: 0;
      z-index: 1000;
      position: fixed;
      width: 100%;
      text-align: center;
      padding: 15px;
      background-color: black;
      color: white;
      margin-top: 50px;
    }
  </style>
</head>

<body>
  <h1>BITEBOX Reviews</h1>

  <div class="container">
    <a href="mainmenu.html">Back to Home</a>
    <hr>

    <fieldset>
      <legend>Write a Review</legend>
      <form>
        <label>Name</label>
        <input type="text" placeholder="Your name" required>

        <label>Review</label>
        <textarea>Write your review here</textarea>

        <label>Rating</label>
        <input type="text" placeholder="⭐ (1-5)" required>

        <input type="submit" value="Submit Review">
      </form>
    </fieldset>
  </div>

  <footer>
    © 2025 BITEBOX Restaurant. All Rights Reserved.
  </footer>
</body>
</html>


```

```
tablebooking.html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book a Table</title>

    <style>
      body {
        background: linear-gradient(135deg, #f5deb3, #deb887);
        font-family: 'Poppins', Arial, sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
      }

      .book {
        background: #fff;
        padding: 40px 35px;
        border-radius: 16px;
        width: 350px;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        text-align: left;
        animation: fadeIn 0.6s ease-in-out;
      }

      @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
      }

      .book h2 {
        text-align: center;
        color: #5a3d2b;
        margin-bottom: 25px;
      }

      .input-box {
        margin-bottom: 18px;
      }

      .input-box label {
        display: block;
        font-weight: 600;
        color: #333;
        margin-bottom: 6px;
      }

      .input-box input,
      .input-box textarea {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 8px;
        font-size: 15px;
        transition: border-color 0.3s ease;
      }

      .input-box input:focus,
      .input-box textarea:focus {
        outline: none;
        border-color: #d2691e;
      }

      textarea {
        resize: both;
        min-height: 80px;
      }
      .book button {
        width: 100%;
        background-color: #d2691e;
        color: white;
        border: none;
        padding: 12px;
        border-radius: 8px;
        font-size: 16px;
        cursor: pointer;
        transition: background-color 0.3s;
      }

      .book button:hover {
        background-color: #a0522d;
      }

      @media (max-width: 480px) {
        .book {
          width: 90%;
          padding: 30px;
        }
      }
    </style>
  </head>

  <body>
    <div class="book">
      <h2>🍴 Book a Table</h2>

      <div class="input-box">
        <label>Full Name</label>
        <input type="text" placeholder="Enter your full name" required>
      </div>

      <div class="input-box">
        <label>Last Name</label>
        <input type="text" placeholder="Enter your last name" required>
      </div>

      <div class="input-box">
        <label>Date</label>
        <input type="date" required>
      </div>

      <div class="input-box">
        <label>Time</label>
        <input type="time" required>
      </div>

      <div class="input-box">
        <label>Number of Guests</label>
        <input type="number" min="1" max="20" required>
      </div>

      <div class="input-box">
        <label>Special Requests</label>
        <textarea placeholder="Any special instructions..."></textarea>
      </div>

      <button type="button" onclick="reserveTable()">Reserve Table</button>
    </div>

    <script>
      function reserveTable() {
        alert("✅ Your table has been reserved successfully!");
      }
    </script>
  </body>
</html>


```
## OUTPUT:
<img width="1007" height="610" alt="Screenshot 2025-11-19 112645" src="https://github.com/user-attachments/assets/7d4c2fdb-9c94-4e43-9175-75bdfd9fc150" />

<img width="1007" height="592" alt="Screenshot 2025-11-19 112709" src="https://github.com/user-attachments/assets/1220e1f8-8ae5-4b30-b967-6409f3aceaff" />
<img width="1000" height="571" alt="Screenshot 2025-11-19 112703" src="https://github.com/user-attachments/assets/76944ea6-fa78-4d27-8bce-af3f75feed52" />
<img width="1001" height="608" alt="Screenshot 2025-11-19 112654" src="https://github.com/user-attachments/assets/e9b9af3e-dedb-46af-878a-3138665af062" />
<img width="1009" height="617" alt="Screenshot 2025-11-19 112717" src="https://github.com/user-attachments/assets/6a853b35-d5e0-418c-98ea-0b2b4ad906fa" />

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
