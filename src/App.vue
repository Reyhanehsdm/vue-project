
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increase() {
  count.value++
}

function decrease() {
  count.value--
}

function reset() {
  count.value = 0
}
</script>

<template>
  <div class="page">
    <div class="counter-card">

      <span class="subtitle">MY FIRST VUE APP</span>

      <h1>شمارنده</h1>

      <p class="stdName">==ریحانه صادقی مجرد==</p>

      <div class="number">
        {{ count }}
      </div>

      <div class="buttons">
        <button class="btn minus" @click="decrease">−</button>

        <button class="btn plus" @click="increase">+</button>
      </div>

      <button class="reset" @click="reset">
        Reset Counter
      </button>

    </div>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

.page {
  min-height: 100vh;
  background: #eef7f2;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.counter-card {
  width: 350px;
  background: white;
  padding: 40px 30px;
  border-radius: 24px;
  text-align: center;
  box-shadow: 0 15px 40px rgba(40, 100, 70, 0.10);
}

.subtitle {
  color: #65a888;
  font-size: 11px;
  font-weight: bold;
  letter-spacing: 3px;
}

h1 {
  color: #244c3b;
  font-size: 32px;
  margin-top: 15px;
}

.stdName {
  color: #91a69a;
  margin-top: 8px;
  font-size: 14px;
}

.number {
  font-size: 75px;
  font-weight: bold;
  color: #3c936d;
  margin: 35px 0;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.btn {
  width: 65px;
  height: 65px;
  border: none;
  border-radius: 18px;
  font-size: 32px;
  cursor: pointer;
  transition: 0.2s;
}

.plus {
  background: #65b68c;
  color: white;
}

.minus {
  background: #edf5ef;
  color: #438566;
}

.btn:hover {
  transform: translateY(-4px);
  filter: brightness(0.96);
}

.reset {
  margin-top: 25px;
  background: transparent;
  border: none;
  color: #8b9d92;
  cursor: pointer;
  font-size: 14px;
}

.reset:hover {
  color: #438566;
}


</style>
