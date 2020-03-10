<template>
  <div id="app">
    <ul>
      <a @mouseover="hoverOver('Products')" @mouseleave="hoverOver('')"><li>Products</li></a>
      <a><li>Developers</li></a>
      <a><li>Company</li></a>
    </ul>
    <Products v-if="hoveredTab === 'Products'"/>
  </div>
</template>

<script>

import Products from './components/Products'

export default {
  name: 'App',
  data() {
    return {
      tabs: ['Products', 'Developers', 'Company'],
      hoveredTab: ''
    }
  },
  components: {
    Products
  },
  methods: {
    hoverOver(tab) {
      this.hoveredTab = tab;
    }
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

li {
  display: inline-block;
  padding: 10px;
}

a {
  cursor: pointer;
}
</style>
