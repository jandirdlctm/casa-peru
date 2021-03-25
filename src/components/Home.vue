<template>
  <section class="home" id="home">
    <div class="content">
      <h3>CASA PERU IS WAITING FOR YOU TO EXPERIENCE THE BEST OF PERUVIAN CUISINE</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit, placeat voluptas architecto iure quasi earum rem! Recusandae velit quam, nam beatae sapiente nostrum soluta maiores temporibus, rem placeat nobis! Nobis!</p>
      <a href="https://www.clover.com/online-ordering/casa-peru-west-valley-city" target="_blank"><button class="btn">ORDER NOW</button></a>
    </div>

    <div class="image">
      <!-- <img src="../assets/images/menu/chicken/mostrito/mostrito-cortado.png" alt=""> -->
      <img src="images/menu/meats/parrillada-de-la-casa/IMG_6611.JPG" alt="">
    </div>
    
  </section>
</template>

<script>
export default {
  name: 'Home',
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  section{
    min-height: 100vh;
    padding: 1rem 10%;
    padding-top: 8.5rem;
    background: lightgray;
  }
  .home{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    position: relative;
    z-index: 0;
    overflow: hidden;
  }
  .home .image{
    flex: 1 1 39rem;
  }
  .home .image img{
    width: 120%;
  }
  .home .content{
    flex: 1 1 39rem;
  }
  .home .content h3{
    color: #333;
    font-size: 4rem;
  }
  .home .content p{
    color: #666;
    font-size: 1rem;
    padding: 1rem 0;
  }
  .btn{
    font-size: 1.7rem;
    padding: .7rem 4rem;
    border-radius: 5rem;
    margin-top: 1rem;
    background: red;
    /* color: #333; */
    cursor: pointer;
    border: .2rem solid white;
    color: white;
  }
  .btn:hover{
    background: black;
    color: white;
  }
  .home::before,
  .home::after{
    content: '';
    position: absolute;
    top: 5rem;
    right: -6rem;
    background: black;
    border-radius: 3rem;
    transform: rotate(-45deg);
    height: 40rem;
    width: 70rem;
    z-index: -2;
    animation: animate 1s linear 1;
  }

  @media (max-width: 1581px){
    section{
      background: red;
    }
    .home .content h3{
      margin-top: 5rem;
      color: white;
      font-size: 4rem;
  }
    .home .content p{
      color: #FFFFFF;
      font-size: 1rem;
      padding: 1rem 0;
  }
  .btn{
    font-size: 1.7rem;
    padding: .7rem 4rem;
    border-radius: 5rem;
    margin-top: 1rem;
    background: none;
    /* color: #333; */
    cursor: pointer;
    border: .2rem solid white;
    color: white;
  }
  .btn:hover{
    background: white;
    color: red;
  }
  .home .image img{
    width: 100%;
  }
  }

  @media (max-width: 754px){
  .home::before,
  .home::after{
    display: none;  
  }
  .home .content{
    text-align: center;
  }
   .btn{
    font-size: 1.7rem;
    padding: .7rem 4rem;
    border-radius: 5rem;
    margin-top: 1rem;
    background: black;
    /* color: #333; */
    cursor: pointer;
    border: .2rem solid white;
    /* color: ; */
  }
  .btn:hover{
    background: white;
    color: red;
  }
  
  }
 
</style>
