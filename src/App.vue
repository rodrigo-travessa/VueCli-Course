<template>
  <h1>Ny First Vue SPA with a {{ title }}</h1>
  <br>
  <input type="text" ref="name">
  <br>
  <button @click="handleClick"> Click Me</button>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      title: 'Data() title'
    }
  },
  methods:{
    handleClick(){
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()

    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
