<template>
  <div class="app">
    <img class="img1" src="./assets/seedbg.png" alt="">
    <img class="img2" src="./assets/wateringbg.png" alt="">
    <img class="img3" src="./assets/seedbag.png" alt="" @click.prevent="$refs.modalName.openModal()">
    <img class="img4" src="./assets/watering.png" alt="" >
    <img class="img5" src="./assets/pot.png" alt="">
    <modal ref="modalName">
    </modal>
    
  <!-- <div>
		<div id="login"><button onclick="login();">Please Login</button></div>
		<div id="gotin" style="display:none;">
			Welcome <b><span id="user"></span></b>
			<br>
			<button id="logout" onclick="logout();">Logout</button>
		</div>
	</div> -->

  </div>
</template>

<script>
import Modal from "./components/Modal";

export default {
  name: "App",
   components: {
     Modal
    }
  
};
</script>

<style>
  @import './assets/style.css';
</style>