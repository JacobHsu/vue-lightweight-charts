<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
import { createChart } from 'lightweight-charts';
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  created() {
    const chart = createChart(document.body, { width: 400, height: 300 });
    const candlestickSeries = chart.addCandlestickSeries();

    // 设置数据
    candlestickSeries.setData([
      {
        time: '2018-12-19',
        open: 141.77,
        high: 170.39,
        low: 120.25,
        close: 145.72,
      },
      {
        time: '2018-12-20',
        open: 145.72,
        high: 147.99,
        low: 100.11,
        close: 108.19,
      },
      {
        time: '2018-12-21',
        open: 108.19,
        high: 118.43,
        low: 74.22,
        close: 75.16,
      },
      {
        time: '2018-12-22',
        open: 75.16,
        high: 82.84,
        low: 36.16,
        close: 45.72,
      },
      { time: '2018-12-23', open: 45.12, high: 53.9, low: 45.12, close: 48.09 },
      {
        time: '2018-12-24',
        open: 60.71,
        high: 60.71,
        low: 53.39,
        close: 59.29,
      },
      { time: '2018-12-25', open: 68.26, high: 68.26, low: 59.04, close: 60.5 },
      {
        time: '2018-12-26',
        open: 67.71,
        high: 105.85,
        low: 66.67,
        close: 91.04,
      },
      { time: '2018-12-27', open: 91.04, high: 121.4, low: 82.7, close: 111.4 },
      {
        time: '2018-12-28',
        open: 111.51,
        high: 142.83,
        low: 103.34,
        close: 131.25,
      },
      {
        time: '2018-12-29',
        open: 131.33,
        high: 151.17,
        low: 77.68,
        close: 96.43,
      },
      {
        time: '2018-12-30',
        open: 106.33,
        high: 110.2,
        low: 90.39,
        close: 98.1,
      },
      {
        time: '2018-12-31',
        open: 109.87,
        high: 114.69,
        low: 85.66,
        close: 111.26,
      },
    ]);
    // const areaSeries = chart.addAreaSeries();
    // areaSeries.setData([
    //     { time: '2019-04-11', value: 80.01 },
    //     { time: '2019-04-12', value: 96.63 },
    //     { time: '2019-04-13', value: 76.64 },
    //     { time: '2019-04-14', value: 81.89 },
    //     { time: '2019-04-15', value: 74.43 },
    //     { time: '2019-04-16', value: 80.01 },
    //     { time: '2019-04-17', value: 96.63 },
    //     { time: '2019-04-18', value: 76.64 },
    //     { time: '2019-04-19', value: 81.89 },
    //     { time: '2019-04-20', value: 74.43 },
    // ]);
    chart.timeScale().fitContent();
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
