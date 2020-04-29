<template>
  <div id="app">
    <a href="/" @click="handleClick">blah</a>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    handleClick() {
      console.log('blah')
    }
  }
}
</script>
