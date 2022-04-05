<template>
  <div id="app">
    <Hun ref="Zundui" ovog="Mendug"></Hun>
    <Hun ref="Oyuka" :ovog="`Bayarsaikhan`"></Hun>

    <button @click="changeZ">Change Zundui</button>
    <button @click="changeO">Change Oyuka</button>
  </div>
</template>

<script>

import Hun from "./components/hun"

export default {
  name: 'App',
  data() {
    return {

    }
  },
  methods: {
    changeZ(){
      this.$refs.Zundui.changeMyName("Mr Z")
    },
    changeO(){
      this.$refs.Oyuka.changeMyName("Miss O")
    },
  },

  computed: {

  },
  watch: {

  },
  components: {
    Hun
  }
}
</script>

