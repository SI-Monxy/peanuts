<template>
  <div id="app">
    <input @click="helloWorld" type="button" value="HelloWorld">
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    helloWorld() {
      this.$axios.get('http://localhost:8080/hello')
        .then((response) => {
          alert(response.data);
        })
        .catch((e) => {
          alert(e);
        });
    }
  }
}
</script>
