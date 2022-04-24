<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
</script>

<template>
  <div>
    <div>
      <div class="box">1</div>
      <div class="box" style="left:70px">2</div>
      <div class="box" style="left:140px">3</div>
      <div class="box" style="top:70px">4</div>
      <div class="box" style="top:70px; left:70px">5</div>
      <div class="box" style="top:70px; left:140px">6</div>
      <div class="box" style="top:140px">7</div>
      <div class="box" style="top: 140px; left:70px">8</div>
    </div>
    <div style="left:300px">
      <h2>Motion testing</h2>
      <br>
      <label class="switch">
        <input type="checkbox">
        <span class="slider"></span>
      </label>
    </div>
  </div>
</template>


<style>
@import '@/assets/base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;

  font-weight: normal;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }
}

.box {
  height: 70px;
  width: 70px;
  background-color: #555;
  text-align: center;
  font-size: 40px;
  color: white;
  position: absolute;
  border-style: solid;
  border-color: white;
}

.switch input { 
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: black;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #2196F3;
}

input:focus + .slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

</style>
