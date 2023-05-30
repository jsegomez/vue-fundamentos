<template>
    <Counter title="Entraron" v-bind:start="15"></Counter>
    
</template>

<script>

import Counter from './components/Counter.vue';

export default {
  name: 'App',
  components: {
    Counter
  }
}
</script>



