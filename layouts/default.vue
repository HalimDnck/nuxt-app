<template>
   
   <div class="body">

      <header>
         <input type="search" id="search" name="search" placeholder="Search Location">
         <button><img src="~/assets/search-interface-symbol.png" alt="search icon" class="search-icon"></button>
      </header>

      <main>
         <div class="card-container">
            <div class="card">
               <div class="top-card">
                  <p id="time">9:28 PM</p>
               </div>

               <div class="mid-card">
                  <div class="mid-left-card">
                     <p id="deg">26°C</p>
                     <img src="" alt="">
                  </div>
                  <div class="mid-right-card">
                     <ul>
                        <li>Humidity <p id="hum">76%</p></li>
                        <li>Wind <p id="wind">10km/h</p></li>
                        <li>Night <p id="night">6°C</p></li>
                     </ul>
                  </div>
               </div>

               <div class="bottom-card">
                  <p id="loc">Gaziantep/Turkey</p>
               </div>
            </div>
         </div>
      </main>

      <div>
         <slot />
      </div>

   </div>
</template>

<script>
   export default {
   };
</script>

<style lang="scss">
   @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&display=swap');
   *{
      padding: 0;
      margin: 0;
      font-family: 'Roboto', sans-serif;
   }
   .body{
      padding: 0;
      margin: 0;
      width: 100vw;
      height: 100vh;
      background-image: url("assets/background-img.jpg");
   }

   header{
      width: 100%;
      height: 10vh;
      display: flex;
      align-items: center;
      justify-content: center;
      input{
            width: 300px;
            height: 30px;
            font-size: 18px;
            border-left: none;
            border-right: none;
            border-top: none;
            border-bottom: 2px solid black;
            background: none;
            transition: all 1s;
            &:focus{
               font-size: 19px;
               height: 32px;
               width: 350px;
               outline: none;
            }
            &:-webkit-autofill,
            &:-webkit-autofill:hover,
            &:-webkit-autofill:focus,
            &:-webkit-autofill:active {
               transition: background-color 5000s ease-in-out 0s;
               margin-right: 50px;
               font-size: 19px;
               height: 32px;
               width: 350px;
               outline: none;
            }
      }
      button{
         border: none;
         background: none;
         margin-left: -30px;
         cursor: pointer;
         transition: all 1s;
         img{
            width: 15px;
            
         }
      }
   }

   main{
      width: 100%;
      height: 70vh;
      display: flex;
      align-items: center;
      justify-content: center;

      .card-container{
         width: 100%;
         height: 100%;
         display: flex;
         align-items: center;
         justify-content: center;
         color: white;
         .card{
            background: rgba(0, 0, 0, 0.6);
            width: 750px;
            height: 400px;
            border-radius: 30px;
            display: flex;
            flex-direction: column;
            .top-card{
               width: 100%;
               height: 15%;
               display: flex;
               justify-content: flex-end;
               align-items: center;
               p{
                  font-size: 24px;
                  color: white;
                  padding: 20px;
               }
            }
            .mid-card{
               width: 100%;
               height: 70%;
               display: flex;
               .mid-left-card{
                  width: 50%;
                  height: 100%;
                  font-size: 96px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
               }
               .mid-right-card{
                  width: 50%;
                  height: 100%;
                  font-size: 32px;
                  display: flex;
                  align-items: center;
                  justify-content: center;
                  ul{
                     list-style: none;
                     display: flex;
                     flex-direction: column;
                     gap: 50px;
                     justify-content: center;
                     align-items: flex-start;
                     li{
                        display: flex;
                        gap: 50px;
                     }
                  }
               }
            }
            .bottom-card{
               width: 100%;
               height: 15%;
               display: flex;
               justify-content: flex-start;
               align-items: center;
               p{
                  font-size: 24px;
                  color: white;
                  padding: 20px;
               }
            }
         }
      }
   }

</style>