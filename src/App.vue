<template>
  <div id="app">
    state {{ state }}
    <A v-model="state" />
  </div>
</template>

<script>
import A from './components/A.vue';

export default {
  name: 'App',
  components: {
    A,
  },
  data() {
    return {
      state: false,
    };
  },
};
</script>
