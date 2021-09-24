<!DOCTYPE HTML>
<html lang="en" dir="ltr"> 
<head>
  <meta charset ="utf-8">
  <title>Side Menu Bar CSS </title>
  <link rel="stylesheet" href="Gstyle2.css">
  <script src="https://kit.fontawesome.com/a076d05399.js"></script>
  </head>
  <body>
      <input type="checkbox" id="check">
      <label for="check">
          <i class="fas fa-bars" id="btn"></i>
          <i class="fas fa-times" id="cancel"></i>
      </label>
    <div class="sidebar">
        <header>My App</header>
        <ul>
            <li><a href="#"><i class="fas fa-qrcode"></i> Dashboard</a></li>
            <li><a href="#"><i class="fas fa-link"></i> Shortcuts</a></li>
            <li><a href="#"><i class="fas fa-stream"></i> Overview</a></li>
            <li><a href="#"><i class="fas fa-calendar-week"></i> Events</a></li>
            <li><a href="#"><i class="fas fa-question-circle"></i> About</a></li>
            <li><a href="#"><i class="fas fa-sliders-h"></i> Services</a></li>
            <li><a href="#"><i class="fas fa-envelope"></i> Contact</a></li>
        
        </ul>
    </div>
    <section></section>
  </body>
</html>
@import url(https://fonts.googleapis.com/css);
body{
    font-family :'Roboto' , sans-serif;
}
*{
    margin: 0;
    padding: 0;
    list-style: none;
    text-decoration: none;
}
.sidebar{
    position: fixed;
    left: -250px;
    width: 250px;
    height: 100%;
    background: #042331;
}

.sidebar header{
    font-size: 22px;
    color: white;
    text-align : center;
    line-height: 70px;
    background: #063146;
    user-select: none;
}

.sidebar ul a{
    display: block;
    height: 100%;
    width: 100%;
    line-height: 3;
    font-size: 20px;
    color: white;
    padding-left: 40px;
    box-sizing: border-box;
    border-top: 1px solid rgba(255,255,255,.1);
    border-bottom: 1px solid black;
    transition: all .5s ease;
}

ul li:hover a{
    padding-left: 50px;
}
.sidebar ul a i{
    margin-right: 16px;
}
#check{
    display: none;
}
label #btn , label #cancel{
    position: absolute;
    cursor: pointer;
    background: #042331;
    border-radius: 3px;
}
label #btn{
    left: 40px;
    top: 25px;
    font-size: 35px;
    color: white;
    padding: 6px 12px;
    transition: all .5s;
}

label #cancel{
    z-index: 1111;
    left: -195px;
    top: 17px;
    font-size: 30px;
    color: #0a5275;
    padding: 4px 9px;
    transition: all .5s;
}

#check:checked ~ .sidebar{
    left:0;
}
#check:checked ~ label #btn{
    left:250px;
    opacity: 0;
    pointer-events: none;
}
#check:checked ~ label #cancel{
    left:195px;
   
}
#check:checked ~ section{
    margin-left: 250px;
}
section{
    background:url(MS.jpg) no-repeat;
    background-position: center;
    background-size: cover;
    height: 100vh;
    transition: all .5s;
}

