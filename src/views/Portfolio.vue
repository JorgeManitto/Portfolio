<template>
 <div class="">
      <div id="fh5co-main">
			<div class="fh5co-narrow-content">

				<h2 class="fh5co-heading" data-animate-effect="fadeInLeft">Mi portafolio</h2>
				<div class="row row-bottom-padded-md">
				<div class="col-md-3 col-sm-6 col-padding text-center animate-box" >
					<a href="#" class="work image-popup">
						<div class="desc img1" @click="isModalOpen = true" >
						<h3 >Proyectos FrontMentor.io</h3>
						<span>VER</span>
					</div>
				</a>
			</div>
			<div class="col-md-3 col-sm-6 col-padding text-center animate-box" >
				<a href="#" class="work image-popup" >
					<div class="desc img2" @click="isModalOpen2 = true">
						<h3>SPA PORTFOLIO</h3>
						<span>VER</span>
					</div>
				</a>
			</div>

            <div class="col-md-3 col-sm-6 col-padding text-center animate-box" >
				<a href="#" class="work image-popup" >
					<div class="desc img3" @click="isModalOpen3 = true">
						<h3>LARAVEL/MYSQL</h3>
						<span>VER</span>
					</div>
				</a>
			</div>

            <div class="col-md-3 col-sm-6 col-padding text-center animate-box" >
				<a href="#" class="work image-popup" >
					<div class="desc img4" @click="isModalOpen4 = true">
						<h3>PHP/MYSQL</h3>
						<span>VER</span>
					</div>
				</a>
			</div>

            <div class="col-md-3 col-sm-6 col-padding text-center animate-box" @click.prevent="currentpage($event)">
				<a href="#" class="work image-popup" >
					<div class="desc img5"  @click="isModalOpen5 = true">
						<h3>PHP/MYSQL/AJAX</h3>
						<span>Illustration</span>
					</div>
				</a>
			</div>

          <modal v-if="isModalOpen" @close='isModalOpen= false'>
              <template v-slot:title>
                  Proyecto front
              </template>
              <frame><img src="../assets/images/modal_img01.jpg" alt="" srcset=""> </frame>
              <template v-slot:content>
                 <a href="https://www.frontendmentor.io/profile/JorgeManitto/solutions" target="blank"><button href="#" class="ghost-button">Prueba la pagina</button></a>
                 <a href="#"> <button class="ghost-button">GitHub repositorio</button> </a>
              </template>
          </modal>
         <modal v-if="isModalOpen2" @close='isModalOpen2= false'>
              <template v-slot:title>
                  SPA Portfolio
              </template>
              <frame><img src="../assets/images/img2.png" alt="" srcset=""> </frame>
              <template v-slot:content>
                 <a href="https://github.com/JorgeManitto/Portfolio" target="_blank"> <button class="ghost-button">GitHub repositorio</button> </a> 
              </template>
          </modal>
           <modal v-if="isModalOpen3" @close='isModalOpen3= false'>
              <template v-slot:title>
                  Roles y Permisos en Laravel
              </template>
              <frame><img src="../assets/images/img3.png"></frame>
              <template v-slot:content>
                 <a href="#"> <button class="ghost-button">GitHub repositorio</button> </a> 
              </template>
          </modal>
           <modal v-if="isModalOpen4" @close='isModalOpen4= false'>
              <template v-slot:title>
                  PHP Y MYSQL
              </template>
              <frame><img src="../assets/images/img4.jpg" class="img_modal"></frame>
              <template v-slot:content>
                 <a href="#"> <button class="ghost-button">GitHub repositorio</button> </a> 
              </template>
          </modal>
           <modal v-if="isModalOpen5" @close='isModalOpen5= false'>
              <template v-slot:title>
                 Tareas AJAX
              </template>
              <frame><img src="../assets/images/img5.jpg" class="img_modal"></frame>
              <template v-slot:content>
                 <a href="#"> <button class="ghost-button">GitHub repositorio</button> </a> 
              </template>
          </modal>

				</div>
			</div>
            <router-link to="/Contact"><button class="ghost-button">Contact</button></router-link>
            </div>  
    </div>
</template>

<script>
import modal from '../components/modal';
import {ref} from 'vue'
export default {
  components :{modal},
   setup() {
        const isModalOpen = ref (false);
        const isModalOpen2 = ref (false);
        const isModalOpen3 = ref (false);
        const isModalOpen4 = ref (false);
        const isModalOpen5 = ref (false);
        return {isModalOpen,isModalOpen2,isModalOpen3,isModalOpen4,isModalOpen5,}
    },
 
}
</script>
<style scoped>
.modals {
  display: none;
  
}
.close{
  cursor: pointer;
  margin-right: 2%;
  margin-top: 1%;
  transition-delay: .1s;
}
.close:hover{
  color: #228896;
  transform: scale(1.4);
}
.modalss{
  position: absolute;
  width: 77.2vw;
  height: 100vh;
  background-color: rgba(0,0,0,0.7);
  left: 0%;
  top: 0%;
}
.modalsss{
  width: 60vw;
  height: 80vh;
  background: #fff;
  margin-top: 10%;
  margin-left: 10%;
  z-index: 998;
}
.modalsss h2{
  margin: 0;
}
.modalsss img{
  width:100%;
  height: 500px;
  object-fit: cover;
  z-index: 999;
  margin-top: 0;
}
#fh5co-main {
  width: 80%;
  float: right;
  -webkit-transition: 0.5s;
  -o-transition: 0.5s;
  transition: 0.5s; 
}
#fh5co-main .fh5co-narrow-content {
  position: relative;
  width: 93%;
  margin: 0 auto;
  padding: 1em 0;
  clear: both;
}
.fh5co-heading{
    text-transform: uppercase;
}
.work {
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  position: relative;
  height: 270px;
  width: 100%;
  display: table;
  overflow: hidden;
  margin-top: 1em;
}
.work .desc {
  display: table-cell;
  vertical-align: middle;
  height: 270px;
  background-image:url(../assets/images/img-4.jpg);
  -webkit-transition: 0.3s;
  -o-transition: 0.3s;
  transition: 0.3s;
   background-repeat: no-repeat;

}
.work .img1{
  background-image:url(../assets/images/modal_img01.jpg);
   background-size: 33em;

}
.work .img2{
  background-image:url(../assets/images/img2.png);
  background-size: 33em;
}
.work .img3{
  background-image:url(../assets/images/img3.png);
  background-size: 33em;
}
.work .img4{
  background-image:url(../assets/images/img4.jpg);
  background-size: 33em;
}
.work .img5{
  background-image:url(../assets/images/img5.jpg);
  background-size: 33em;
 
}
.work .desc h3 {
  font-size: 16px;
  -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
  transition: transform 0.3s, opacity 0.3s;
  -webkit-transform: translate3d(0, -15px, 0);
  transform: translate3d(0, -15px, 0);
  color: #000;
  font-weight: 600;
}
.work .desc span {
  display: block;
  color: #000;
  font-size: 12px;
  -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
  transition: transform 0.3s, opacity 0.3s;
  -webkit-transform: translate3d(0, 15px, 0);
  transform: translate3d(0, 15px, 0);
}
.work:hover .desc {
  opacity: 1;
}
.work:hover .desc h3 {
  -webkit-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
}
.work:hover .desc span {
  -webkit-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
}
.ghost-button {
  cursor: pointer;
  color:  #228896;
  background:  #fff;
  border: 1px solid  #228896;
  font-size: 17px;
  padding: 7px 12px;
  font-weight: normal;
  margin: 6px 0;
  margin-right: 12px;
  display: inline-block;
  text-decoration: none;
  font-family: 'Open Sans', sans-serif;
  min-width: 120px;
  transition: all .2s ease-in-out;
}
.ghost-button:hover, .ghost-button:active {
  color:#fff;
  background: #228896;
  transform: scale(1.1);
}
@media screen and (max-width: 1200px) {
  #fh5co-main {
    width: 70%;
  }
}
@media screen and (max-width: 799px) {
  #fh5co-main {
    width: 100%;
  }
 
}
@media screen and (max-width: 768px) {
  #fh5co-main .fh5co-narrow-content {
    width: 100%;
    padding: 4em 1em;
  }
}
@media screen and (max-width: 768px) {
  .work {
    height: 400px;
  }
}
@media screen and (max-width: 480px) {
  .work {
    height: 270px;
  }
}
@media screen and (max-width: 800px) {
  .work .desc{
opacity: 1;
  }
  .work .desc h3 {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    color: #000;
    
  }
  .work .desc span {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    color: #000;
  }
  .modalss{
    width: 100%;
    position:fixed;
    margin-top: 2em;
  }
  .modalsss{
    width: 100%;
    height: 100%;
    margin-left:0;
  }
 
}
</style> 
          