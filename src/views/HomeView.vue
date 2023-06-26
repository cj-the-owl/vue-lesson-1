<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>

  <div>
    <p>
      <span :title="message"> Hover and see the dynamic title </span>
    </p>
    <p :class="{red: isRed}" @click="toggleRed()">
      This should be red......But click me to toggle
    </p>
    <p :style="{color}" @click="toggleColor()">
      This will change color when clicking
    </p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  data() {
    return {
      message: 'Hello There',
      isRed: true,
      color: 'green',
    }
  },
  methods: {
    toggleRed() {
      this.isRed = !this.isRed
    },
    toggleColor() {
      this.color = this.color === 'green'?'blue':'green'
     },
  },
  
  
}
</script>

<style>
  .red{
    color: red;
  }
</style>
