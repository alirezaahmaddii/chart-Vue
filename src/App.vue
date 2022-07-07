<template>
  <div>
    <ag-charts-vue
    :options="options"
    >



    </ag-charts-vue>
  </div>
</template>


<script>
import  {AgChartsVue} from 'ag-charts-vue3'

export default {
  components:{
    'ag-charts-vue':AgChartsVue
  },
  data:() =>({
        options:null
  }),
  created() {
    this.options={
      data: [
        { os: 'Android', share: 56.9, satisfaction: 10 },
        { os: 'iOS', share: 22.5, satisfaction: 12 },
        { os: 'BlackBerry', share: 6.8, satisfaction: 9 },
        { os: 'Symbian', share: 8.5, satisfaction: 8 },
        { os: 'Bada', share: 2.6, satisfaction: 7 },
        { os: 'Windows', share: 1.9, satisfaction: 6 },
      ],
      series: [
        {
          type: 'pie',
          labelKey: 'os',
          angleKey: 'share',
          radiusKey: 'satisfaction',
        },
      ],
    }
  },
  mounted() {},
  methods: {},
}
</script>


<style lang="scss">


</style>