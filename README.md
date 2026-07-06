# responsive-landing-page-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Navigation Menu</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

html{
    scroll-behavior:smooth;
}

/* Navigation Bar */
#navbar{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    padding:20px 40px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    background:transparent;
    transition:0.4s;
    z-index:1000;
}

/* Navbar style when scrolled */
#navbar.scrolled{
    background:#222;
    box-shadow:0 2px 10px rgba(0,0,0,0.3);
}

.logo{
    color:white;
    font-size:28px;
    font-weight:bold;
}

.menu{
    list-style:none;
    display:flex;
}

.menu li{
    margin-left:20px;
}

.menu li a{
    text-decoration:none;
    color:white;
    padding:10px 15px;
    transition:0.3s;
    border-radius:5px;
}

/* Hover Effect */
.menu li a:hover{
    background:white;
    color:#222;
}

/* Page Sections */
section{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:40px;
    color:white;
}

#home{
    background:#3498db;
}

#about{
    background:#2ecc71;
}

#services{
    background:#9b59b6;
}

#contact{
    background:#e74c3c;
}

/* Responsive Design */
@media(max-width:768px){

    #navbar{
        flex-direction:column;
        padding:15px;
    }

    .menu{
        flex-direction:column;
        text-align:center;
        margin-top:10px;
    }

    .menu li{
        margin:8px 0;
    }
}
</style>

</head>
<body>

<nav id="navbar">
    <div class="logo">My Website</div>

    <ul class="menu">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<section id="home">
    <h1>Home</h1>
</section>

<section id="about">
    <h1>About</h1>
</section>

<section id="services">
    <h1>Services</h1>
</section>

<section id="contact">
    <h1>Contact</h1>
</section>

<script>
// Change navbar color when scrolling
window.addEventListener("scroll", function() {

    let navbar = document.getElementById("navbar");

    if(window.scrollY > 50){
        navbar.classList.add("scrolled");
    }
    else{
        navbar.classList.remove("scrolled");
    }

});
</script>

</body>
</html>
