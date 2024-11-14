<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navbar with Hover Dropdowns</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar">
        <!-- Sol taraftaki sütun -->
        <div class="navbar-left">
            <div class="dropdown">
                <button class="dropbtn">Sol Sütun</button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
        </div>
        <!-- Sağ taraftaki sütunlar -->
        <div class="navbar-right">
            <!-- Dropdown sütunları -->
            <div class="dropdown">
                <button class="dropbtn">Sağ Sütun 1</button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Sağ Sütun 2</button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Sağ Sütun 3</button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
            <div class="dropdown">
                <button class="dropbtn">Sağ Sütun 4</button>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </div>
            <div class="static-link">
                <a href="#">Sağ Sütun 5</a>
            </div>
        </div>
        <!-- Mobil menü butonu -->
        <button class="menu-toggle" onclick="toggleMenu()">Menu</button>
    </nav>
    <div class="mobile-menu" id="mobileMenu">
        <a href="#">Sol Sütun Link 1</a>
        <a href="#">Sol Sütun Link 2</a>
        <a href="#">Sol Sütun Link 3</a>
        <a href="#">Sağ Sütun 1 Link 1</a>
        <a href="#">Sağ Sütun 1 Link 2</a>
        <a href="#">Sağ Sütun 1 Link 3</a>
        <a href="#">Sağ Sütun 2 Link 1</a>
        <a href="#">Sağ Sütun 2 Link 2</a>
        <a href="#">Sağ Sütun 2 Link 3</a>
        <a href="#">Sağ Sütun 3 Link 1</a>
        <a href="#">Sağ Sütun 3 Link 2</a>
        <a href="#">Sağ Sütun 3 Link 3</a>
        <a href="#">Sağ Sütun 4 Link 1</a>
        <a href="#">Sağ Sütun 4 Link 2</a>
        <a href="#">Sağ Sütun 4 Link 3</a>
        <a href="#">Sağ Sütun 5</a>
    </div>
</body>
</html>

/* Navbar Temel Stili */
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
    color: white;
}

.navbar-left, .navbar-right {
    display: flex;
    align-items: center;
}

.dropdown {
    position: relative;
}

.dropbtn {
    background-color: #333;
    color: white;
    padding: 10px;
    font-size: 16px;
    border: none;
    cursor: pointer;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #444;
    min-width: 160px;
    box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
    z-index: 1;
    animation: dropdownFade 0.3s ease-in-out;
}

.dropdown-content a {
    color: white;
    padding: 8px 12px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {
    background-color: #555;
}

/* Hover olduğunda dropdown göster */
.dropdown:hover .dropdown-content {
    display: block;
}

.static-link a {
    color: white;
    padding: 10px;
    text-decoration: none;
}

.static-link a:hover {
    background-color: #444;
}

.menu-toggle {
    display: none;
    font-size: 24px;
    color: white;
    background-color: transparent;
    border: none;
    cursor: pointer;
}

/* Mobil Menu Stili */
.mobile-menu {
    display: none;
    flex-direction: column;
    background-color: #333;
    padding: 10px;
}

.mobile-menu a {
    color: white;
    padding: 8px 12px;
    text-decoration: none;
}

.mobile-menu a:hover {
    background-color: #555;
}

/* Medya Sorguları */
@media (max-width: 768px) {
    .navbar-right {
        display: none;
    }
    .menu-toggle {
        display: block;
    }
    .mobile-menu {
        display: none;
    }
}

@keyframes dropdownFade {
    from { opacity: 0; transform: translateY(-10px); }
    to { opacity: 1; transform: translateY(0); }
}


