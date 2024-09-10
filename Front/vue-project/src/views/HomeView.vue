<script setup>
import router from '@/router';
import { onMounted } from 'vue';

onMounted(() => {
    const loginButton = document.getElementById("loginButton");
    if (loginButton) {
        loginButton.addEventListener('click', () => {
            router.push({ name: 'auth' });
        });
    }

});
</script>
<template>
  Главная страница
  <div class="form">
    <button id="loginButton" type="button">Авторизация</button>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .Auth {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
.form {
  background-color: aqua;
  margin-top: 10px;
  font-size: 25px;
  margin-left: 50vw;
}
</style>
