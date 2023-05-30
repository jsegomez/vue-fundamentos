<template>
  <div class="text-center">
    <h2>{{ customTitle }}</h2>
    <p>{{ counter }}</p>
    <button class="btn btn-primary" v-on:click="() => changeValue(1)">+1</button>
    <button class="btn btn-primary mx-3" @click="() => changeValue(0)">reset</button>
    <button class="btn btn-primary" @click="() => changeValue(-1)">-1</button>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    start: Number
  },
  data() {
    return {
      counter: this.start,
    };
  },
  methods: {
    changeValue(valueFn) {
      if (valueFn == 0) {
        this.counter = 0;
        return;
      }
      return this.counter = this.counter + valueFn;
    },
  },
  computed() {
    return {
      customTitle(){        
        return this.start || 'Counter'
      }
    };
  },
};
</script>

<style>
</style>




