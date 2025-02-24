<template>
  <div id="app" class="container-fluid">
      <div class="row text-center justify content-center align-items-center vh-100">
          <div class="col-sm-7">
              <h1 class="off-white title-size">Add-Calc</h1>
          </div>
          <div class="col-sm-4">
              <p>Add-Calc is a simple Vue.js app that lets users input two numbers and get the result of the sum of the two numbers. </p>
          </div>
      </div>
      <div id="main" class="row text-center justify-content-center align-items-center vh-100">
          <div class="col">
            <p>First Number: {{ num1 }}</p>
            <button @click="num1--">-</button><input v-model="num1" placeholder="First Number"/><button @click="num1++">+</button>
          </div>
          <div class="col">
            <p>Second Number: {{ num2 }}</p>
            <button @click="num2--">-</button><input v-model="num2" placeholder="Second Number"/><button @click="num2++">+</button>
          </div>
          <div class="col">
            <h2 class="off-white">The sum of {{ num1 }} and {{ num2 }} is <b>{{ Number(num1)+Number(num2) }}</b></h2>
          </div>
      </div>
  </div>
</template>

<script>
  import { ref } from 'vue';
  export default {
      setup() {
          const num1 = ref(0);
          const num2 = ref(0);
          const sum = num1+num2
          
          return { num1, num2, sum }
      },
  }
</script>