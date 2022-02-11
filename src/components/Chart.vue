<template>
  <div id="chartDiv" style="width:50%; height:300px; margin:0 auto;"></div>
</template>

<script>

export default {
  name: 'Chart',
    created(){
          JSC.Chart('chartDiv', {
   type: 'horizontal column',
   series: [
      {
         points: [
            {x: 'Apples', y: 50},
            {x: 'Oranges', y: 42}
         ]
      }
   ]
});
      },
  
}
</script>


<style scoped>

</style>