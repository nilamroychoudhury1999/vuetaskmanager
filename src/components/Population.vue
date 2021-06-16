<template>
  <div>
    <canvas id="population-chart"></canvas>
  </div>
</template>
<script>
import Chart from 'chart.js'
import populationData from '../population.js'

export default {
  name: 'Population',
  data() {
    return {
      populationData: populationData
    }
  },
  mounted() {
    const ctx = document.getElementById('population-chart');
    new Chart(ctx, this.populationData);
  }
}
</script>