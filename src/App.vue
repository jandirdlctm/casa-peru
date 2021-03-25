<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <header>
      <a href="/" class="logo"><img src="./assets/images/logo/logo.png"></a>
      
      
      <div id="menu-bar" class="fas fa-bars"></div>
      <nav class="navbar">
        <ul>
          <li><a><router-link to="/">Home</router-link></a></li>
          <li><a><router-link to="/menu">Menu</router-link></a></li>
          <li><a><router-link to="/reviews">Reviews</router-link></a></li>
          <li><a><router-link to="/contact">Contact</router-link></a></li>
        </ul>
      </nav>  
    </header>
    <router-view></router-view>
    <!-- FOOTER -->
    <div class="footer">
      <div class="box-container">
        <div class="box">
        <h3>Contact Info</h3>
        <p><i class="fas fa-map-marker-alt"></i>   1830 W 3500 S West Valley City, UT</p>
        <p><i class="fas fa-phone-volume"></i>   (801) 972-5807</p>
      </div>

      <div class="box">
        <h3>Quick Links</h3>
        <a href="/">Home</a>
        <a href="/menu">Menu</a>
        <a href="/reviews">Reviews</a>
        <a href="/contact">Contact</a>
      </div>
      
      <div class="box">
        <h3>Social Media</h3>
        <a href="https://www.facebook.com/pg/casaperurestaurant14/about/?ref=page_internal" target="_blank">Facebook</a>
      </div>

      <!-- <h1 class="credit">Developed by <a href="#">Jandir Porta </a> all rights reserved.</h1> -->
      </div>
    </div>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  Components: {
    Home
  },
  data: function(){
    return{
      
    }
  },
  methods:{
  }

}
</script>

<style>
#app {
}

header{
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
  width: 100%;
  background: red;
  padding: 1.5rem 10%;
  box-shadow: 0 .3rem 2rem rgba(0,0,0,.1);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

header .logo img{
  height: 8rem;
}

header .navbar ul{
  display: flex;
  align-items: center;
  justify-content: center;
  list-style: none;
}

header .navbar ul li{
  margin-left: 3rem;
}

header .navbar ul li a{
  font-size: 1.7rem;
  color: white;
}

header .navbar ul li a.active,
header .navbar ul li a:hover{
  color: black;
}

header #menu-bar{
  font-size: 3rem;
  color: white;
  cursor: pointer;
  display: none;
}

@media (max-width: 768px){
  header #menu-bar{
    display: block;
  }
  header .navbar{
    position: fixed;
    top: 8rem;
    left: 0;
    width: 100%;
    background: red;
    border-top: .2rem solid rgba(0,0,0,.1);
    transform: scaleY(0);
    transform-origin: top;
    opacity: 0;
  }
  header .navbar ul{
    flex-flow: column;
    width: 100%;
  }
  header .navbar ul li{
    margin: 1.5rem;
    width: 100%;
  }
  header .navbar ul li a{
    display: block;
    color: white;
    padding-left: 2rem;
    /* border-left: .2rem solid blac; */
    font-size: 2rem;
  }
  header .navbar ul li a:hover{
    color: black;
    border-color: black;
  }
  
}

/* footer */
.footer{
  background: #282727;
  padding: 1rem 7%;
}

.footer .box-container{
  display: flex;
  flex-wrap: wrap;
}

.footer .box-container .box{
  flex: 1 1 25rem;
  margin: 2rem;
}

.footer .box-container .box h3{
  font-size: 2.5rem;
  color: white;
  padding: 1rem 0;
  font-weight: normal;
}
.footer .box-container .box p{
  font-size: 1.7rem;
  color: #eee;
  padding: 1rem 0;
}

.footer .box-container .box a{
  font-size: 1.7rem;
  color: #eee;
  padding: 1rem 0;
  display: block;
}

.footer .box-container .box a:hover{
  color: red;
}

.footer .box-container .box p i{
  padding-right: .5rem;
  color: red;
}

.footer .credit{
  font-size: 2rem;
  text-align: center;
  border-top: .2rem solid rgba(255,255,255,.7);
  padding: 2rem 1rem;
  font-weight: normal;
  letter-spacing: 1rem;
  color: white;
}

.footer .credit a{
  color: red;

}



</style>
