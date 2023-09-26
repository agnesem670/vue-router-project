<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ personalInfo.name }} - {{ personalInfo.age }}</p>
    <button @click="updateInfo">Update info One</button>
    <h2>Reactive</h2>
    <p>{{ personalTwo.name }} - {{ personalTwo.age }}</p>
    <button @click="updateInfoTwo">Update info Two</button>
  </div>
</template>

<script>
import { ref, reactive } from 'vue';

export default {
  name: 'HomeView',
  setup() {

    const personalInfo = ref({ name: 'aga', age: 39 })
    const personalTwo = reactive({name: 'ela', age: 35})

    const updateInfo = () => {
      personalInfo.value.age = 40
    }

     const updateInfoTwo = () => {
      personalTwo.age = 55
    }

    return { personalInfo, updateInfo, personalTwo, updateInfoTwo }
  }

}
</script>
