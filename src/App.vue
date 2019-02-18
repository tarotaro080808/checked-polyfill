<template>
  <div id="app">
    <label for="item1" v-for="item in items" v-bind:key="item.id">
      <input
        type="radio"
        :id="item.id"
        v-model="dataModel"
        :value="item.value"
        :checked="item.checked"
      >
      {{ item.value }}
    </label>
    <div>{{ dataModel }}</div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      items: [
        { id: "item1", value: 1000, checked: false },
        { id: "item2", value: 2000, checked: true }
      ],
      dataModel: 2000
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
