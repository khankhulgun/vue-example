<template>
  <div id="app">
    tanii ovog: {{ovog}} <br>
    tanii  ner : {{ ner }} <br>
    <input type="text" v-model="ner">
    <input type="number" v-model="tursunOn">


    <button @click="changeMyName">Neriig Altai bolgo</button>


    <h2>
      {{ nerBolonNas }}
    </h2>

  </div>
</template>

<script>


export default {
  name: 'App',
  props:["ovog"],
  data() {
    return {
      ner: "",
      tursunOn: null,
      nerBolonNas: ""
    }
  },
  methods: {
    changeMyName(value) {
      this.ner = value
    },
    changeMyNerBolonNas() {
      if (this.ner !== null && this.ner != "" && this.tursunOn !== null && this.tursunOn >= 1) {
        this.nerBolonNas = `tanii ovog: ${this.ovog}, tanii ner: ${this.ner}, nas: ${this.nas}`
      } else {
        this.nerBolonNas = ""
      }
    },
  },

  computed: {
    nas() {
      return 2022 - this.tursunOn;
    }
  },
  watch: {
    ner() {
      this.changeMyNerBolonNas();
    },
    nas() {
      this.changeMyNerBolonNas();
    }
  },
  components: {}
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
</style>
