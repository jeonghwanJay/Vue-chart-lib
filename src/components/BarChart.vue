<template>
  <div>
    <h1>BarChart</h1>
    <canvas ref="barChart" width="400" height="400"></canvas>
  </div>
</template>

<script>
export default {
    props: ['propsdata'],
    mounted() {
    const ctx = this.$refs.barChart
    // eslint-disable-next-line
  const barChart = new this.$_Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: this.propsdata
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});
  }
}
</script>

<style>

</style>