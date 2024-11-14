
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navbar</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar">
        <div class="navbar-left">
            <div class="dropdown">
                <button class="dropbtn">Menu 1</button>
                <div class="dropdown-content">
                    <a href="#">Option 1</a>
                    <a href="#">Option 2</a>
                    <a href="#">Option 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Menu 2</button>
                <div class="dropdown-content">
                    <a href="#">Option 1</a>
                    <a href="#">Option 2</a>
                    <a href="#">Option 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Menu 3</button>
                <div class="dropdown-content">
                    <a href="#">Option 1</a>
                    <a href="#">Option 2</a>
                    <a href="#">Option 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Menu 4</button>
                <div class="dropdown-content">
                    <a href="#">Option 1</a>
                    <a href="#">Option 2</a>
                    <a href="#">Option 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Menu 5</button>
                <div class="dropdown-content">
                    <a href="#">Option 1</a>
                    <a href="#">Option 2</a>
                    <a href="#">Option 3</a>
                </div>
            </div>
        </div>
        <div class="navbar-right">
            <div class="dropdown">
                <button class="dropbtn">Profile</button>
                <div class="dropdown-content">
                    <a href="#">Account</a>
                    <a href="#">Settings</a>
                    <a href="#">Logout</a>
                </div>
            </div>
        </div>
        <button class="mobile-menu-btn" onclick="toggleMobileMenu()">Menu</button>
    </nav>

    <script src="script.js"></script>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    padding: 10px;
}

.navbar-left,
.navbar-right {
    display: flex;
}

.dropdown {
    position: relative;
}

.dropbtn {
    background-color: #333;
    color: white;
    padding: 10px 15px;
    border: none;
    cursor: pointer;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #444;
    min-width: 160px;
    box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
    z-index: 1;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.dropdown-content a {
    color: white;
    padding: 10px 15px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {
    background-color: #555;
}

.dropdown:hover .dropdown-content {
    display: block;
    opacity: 1;
}

.mobile-menu-btn {
    display: none;
    background-color: #333;
    color: white;
    padding: 10px 15px;
    border: none;
    cursor: pointer;
}

@media (max-width: 768px) {
    .navbar-left {
        display: none;
        flex-direction: column;
    }
    .navbar-right {
        display: none;
    }
    .mobile-menu-btn {
        display: block;
    }
    .navbar-left.show {
        display: flex;
    }
}
