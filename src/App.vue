<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref } from 'vue'
import { Magnifier } from 'vue3-zoomer'

const imageSrc = ref('src/assets/Ermestagliato.png')
</script>

<template>
  <header>
    <div class="containerImg">
      <Magnifier :src="imageSrc" alt="Ermes image" :zoom-scale="2" :size="300" />
    </div>

    <div class="wrapper">
      <HelloWorld title="The best dog in the world" msg="Ermes" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.containerImg {
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  padding: 1rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
