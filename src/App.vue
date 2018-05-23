<template>
  <div id="app" class="container mx-auto">
    <div class="w-full my-8">
      <button @click="selectedComponent = 'Blue'" class="py-2 px-4 rounded border border-blue bg-blue hover:bg-blue-dark mr-4 text-white">Синий шаблон</button>
      <button @click="selectedComponent = 'Green'" class="py-2 px-4 rounded border border-green bg-green hover:bg-green-dark mr-4 text-white">Зеленый шаблон</button>
      <button @click="selectedComponent = 'Red'" class="py-2 px-4 rounded border border-red bg-red hover:bg-red-dark mr-4 text-white">Красный шаблон</button>
      <hr class="border border-grey">
      <component :is="selectedComponent">
        <p>Это какой-то контент</p>
      </component>

      <!-- <Blue>
          <p>Это синий контент</p>
      </Blue>
      <Green>
        <p>Это зеленый контент</p>
      </Green>
      <Red>
        <p>Это красный контент</p>
      </Red> -->

    </div>

  </div>
</template>

<script>
import Blue from './components/Blue.vue'
import Green from './components/Green.vue'
import Red from './components/Red.vue'
export default {
  name: 'app',
  data() {
    return {
      selectedComponent: 'Blue'
    }
  },
  components: {
    Blue,
    Green,
    Red
  }
}
</script>

<style>

</style>
