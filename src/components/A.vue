<template>
  <div class="state" @click="setActive(true)" :class="{ active: isActive }">
    true
  </div>
  <div class="state" @click="setActive(false)" :class="{ active: !isActive }">
    false
  </div>
</template>

<script>
export default {
  name: 'A',
  props: ['modelValue'],
  computed: {
    isActive() {
      return this.modelValue;
    },
  },
  methods: {
    setActive(v) {
      this.$emit('update:modelValue', v);
    },
  },
};
</script>

<style>
div.state {
  border: 1px solid #ccc;
  margin: 10px;
  padding: 10px;
}
div.active {
  border: 1px solid green;
}
</style>
