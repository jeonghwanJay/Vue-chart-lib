<template>
  <div>
    <h1>LineChart</h1>
    <div>
        <canvas ref="LineChart"></canvas>
    </div>
  </div>
</template>

<script>
export default {
    mounted() {
        const labels = [
    'January',
    'February',
    'March',
    'April',
    'May',
    'June',
  ];

  const data = {
    labels: labels,
    datasets: [{
      label: 'My First dataset',
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [0, 10, 5, 2, 20, 30, 45],
    }]
  };
    // eslint-disable-next-line
  const config = {
    type: 'line',
    data: data,
    options: {}
  };
  // eslint-disable-next-line
   const lineChart = new this.$_Chart(
    this.$refs.LineChart,
    config
  );
    }
}
</script>

<style>

</style>