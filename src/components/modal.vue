<template>
       <div class="modalss" @click="close()">
       </div>
              <div class="modalsss" style="overflow: hidden;" >
                <span class="close" @click="close()">&times;</span>
                <h2> <slot name="title"></slot> </h2>       
                    <slot name="img"></slot>
                    <p><slot name="about"></slot></p>
                    <slot name="content"></slot> 
              </div>     
</template>
<script>
export default {
    setup(_,{emit}) {
        function close() {
            emit("close");
        }
        return {close}
    }
}
</script>
<style>
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
  position: absolute;
  height: 90vh;
  background: #fff;
  margin-top: 0%;
  margin-left: 10%;
  z-index: 999;
 
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
@media screen and (max-width: 800px) {
  .modalss{
    width: 100%;
    position:fixed;
    margin-top: 2em;
  }
  .modalsss{
    position:fixed;
    width: 100%;
    height: auto;
    margin-left:0;
  }

}
</style>