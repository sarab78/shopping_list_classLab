<template>
  <div>
  <h1>My Shopping List</h1>
  <ul>
<shopping-item v-for="(item, index) in items"  :key="index" :item="item"></shopping-item>
</ul>
</div>
</template>

<script>

import ShoppingItem from './components/ShoppingItem'

export default {
  name: 'app',
  components: {
    'shopping-item': ShoppingItem
  },
data(){
  return {
    items: [
      {name: 'Milk', purchased: false},
      {name: 'Cheese', purchased: true},
      {name: 'Beans', purchased: false}
    ]
  }
}

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
