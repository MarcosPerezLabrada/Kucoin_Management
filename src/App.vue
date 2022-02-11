<template>
<div>
<Navbar @click="getUser()"/>
<Chart @click="getUser()"/>
</div>
</template>

<script>
import Navbar from './components/Navbar'

import Chart from './components/Chart'

export default {
  name: 'App',
  components: {
    Navbar,
    Chart
  },
  methods: {
    async getUser() {
      const res = await fetch('https://api.kucoin.com/api/v1/symbols', {headers:{'Access-Control-Allow-Origin': '*'},mode:'no-cors' })
       // const {results} = await res.json()
      console.log(await res)
    }
    
  },
  
}
</script>

<style>
#app {
  font-family: 'Ubuntu', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
</style>
