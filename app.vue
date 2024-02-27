<template>
  <main>
    <div class="">
      <img src="/logo.svg" alt="logo" class="logo" />
    </div>
    <div class="container">
      <div className="inner-container">
        <h2 class="header">
          You’ve just ignited a new
          <span class="library">Nuxt 3</span> static site!
        </h2>
        <span class="pathname">
          {{ currentPath }}
        </span>
      </div>
      <p class="footer">Made in Nigeria with 💖</p>
    </div>
  </main>
</template>

<script setup>
import { ref, onMounted } from "vue";
// import logo from "./assets/logo.png";

const currentPath = ref("");

onMounted(() => {
  currentPath.value = window.location.href;
});
</script>

<style scoped>
main {
  height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 7px;
  align-items: center;
  justify-content: center;
}
.logo {
  width: 200px;
  height: 200px;
}
.container {
  display: flex;
  flex-direction: column;
  text-align: center;
  gap: 17px;
}
.inner-container {
  display: flex;
  flex-direction: column;
  line-height: 1;
}
.header {
  font-size: 36px;
  font-weight: 400;
  color: #344054;
}
.pathname {
  color: #004eeb;
  font-size: 20px;
}
.footer {
  font-size: 20px;
  font-weight: 500;
  color: #344054;
}
.library {
  color: #00dc82;
  font-weight: 600;
}
</style>
