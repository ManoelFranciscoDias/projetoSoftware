<script setup>
import {ref} from 'vue';

const isMenuActive = ref(false);

function toggleMenu() {
  isMenuActive.value = !isMenuActive.value
}

</script>

<template>

  <header>
    <nav class="navbar">
      <router-link to="/"><h1 class="logo">LOGO.</h1></router-link>
    

    <ul :class="['nav-menu', { active: isMenuActive }]">
      <li class="nav-item">
          <router-link to="/categorias" class="nav-link">CATEGORIAS</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/eventos" class="nav-link">EVENTOS</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/sobre" class="nav-link">SOBRE</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/contato" class="nav-link">CONTATO</router-link>
        </li>
    </ul>

    <div class="hamburguer" @click="toggleMenu">
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>

      <button class="btn">LOGIN</button>
    
    </div>
  </nav>


  </header>


</template>

<style scoped>

header {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.nav-item {
  list-style: none;
}

.navbar {
  background-color: black;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
}

.logo {
  color: #fff;
  font-size: 1.8rem;
  font-weight: bold;
  text-decoration: none;
  list-style: none;
}




</style>
