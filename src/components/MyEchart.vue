<template>
  <v-chart class="chart" :option="option" autoresize />
</template>

<script setup>
import { use } from 'echarts/core';
import { SVGRenderer } from 'echarts/renderers';
import { PieChart, LineChart, BarChart } from 'echarts/charts';
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent,
  GridComponent,
  ToolboxComponent,
  VisualMapComponent
} from 'echarts/components';
import VChart, { THEME_KEY } from 'vue-echarts';
import { provide, defineProps } from 'vue';

defineProps({
  option: {
    type: Object,
    isRequired: true
  },
});

use([
  SVGRenderer,
  PieChart,
  LineChart,
  BarChart,
  TitleComponent,
  TooltipComponent,
  LegendComponent,
  GridComponent,
  ToolboxComponent,
  VisualMapComponent
]);

provide(THEME_KEY, 'dark');

</script>

<style scoped>
.chart {
  width: 600px;
  height: 400px;
}
</style>
