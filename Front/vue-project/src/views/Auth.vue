<script setup>
import router from '@/router';
import { onMounted } from 'vue';

onMounted(() => {
    const loginButton = document.getElementById("loginButton");
    if (loginButton) {
        loginButton.addEventListener('click', () => {
            router.push({ name: 'admin' });
        });
    }

});
</script>
<template>
    <div class="Auth">
        <form action="" method="post">
            <div class="form">Вход</div>
            <div class="form">
                Имя: <input type="text">
            </div>
            <div class="form">
                Пароль: <input type="password">
            </div>
            <div class="form">
                <button id="loginButton" type="button">Войти</button>
            </div>
        </form>
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
  