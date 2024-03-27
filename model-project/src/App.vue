<template>
  <h1>{{ title }}</h1>
  <p>welcome...</p>
  <div v-if="showModal">
    <MyModal :header="header" :text="text" theme="sale" @close="toggleModal"/>
  </div>

  <button @click="toggleModal">open modal</button>
</template>

<script>
import MyModal from './components/MyModal.vue'
export default {
  name: 'App',
  components:{MyModal},
  data () {
    return {
      title: 'my first vue app',
      header: 'Signup for the giveaway!',
      text:'grab your ninja swag for half price',
      showModal:false,
    }
  },
  methods:{
    toggleModal(){
        this.showModal = !this.showModal
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

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
