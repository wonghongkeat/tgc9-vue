<template>
  <div id="app">
    <Box message="Danger danger will robinson" bgcolor="red"></Box>
    <Box message="hello javascript" v-bind:bgcolor="preferedColor"></Box>
    <h1>{{ text }}</h1>
    <button v-on:click="buttonPressed">Click</button>
    <input type="text" v-model="preferedColor" />
    <Light/>
  </div>
</template>

<script>
import Box from "./components/MessageBox";
import Light from "./components/Light";

export default {
  name: "App",
  components: {
    Box, Light
  },
  data: function () {
    return {
      text: "",
      preferedColor: "blue",
    };
  },
  methods: {
    buttonPressed: function () {
      this.text = "you clicked me!";
    },
  },
};
</script>

<style>
</style>
