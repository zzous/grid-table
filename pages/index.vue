<template>
  <section class="container">
    <!-- <div>
      <app-logo/>
      <h1 class="title">
        starter-template
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
    </div> -->

    <h1>data grid table</h1>

    <div class="desc">
      data-grid-table 관련 plugin 들이 너무 다양하고 많아서 대표적인 유료 2/ 무료 2 가지만 뽑아봤습니다. <br>
      Handsontable / AG Grid 는 유료 data-table-plugin 으로 많은 UI 기능과 design 을 제공하는 반면 대략 $1,000 ~ 1,500 정도의 요금이 부과 됩니다. ( 요금부과 기준은 업체별로 상이하나 거의 비슷한 수준에 요금을 요구 하는 것 같습니다. ) <br>
      <br>
      무료 plugin 으로 대표되는 vue-good-table / vue3-easy-data-table 은 기본적인 기능은 제공되고 desigin custom 까지는 어렵지 않아보이고 document 제공까지도 되고 있으나 유료 plugin 들에 비해 기능적으로 부족한 부분들이 있어 추가개발이 필요해 보입니다.
      <ul>
        <li>cell editor : cell click 시 수정기능 ( input / select )</li>
        <li>filter : Multiple filter</li>
        <li>selection : row selection</li>
      </ul>
      <br> 등등... 추가 개발이 필요할 것으로 보여집니다.
    </div>



    <div class="section">
      <h2>Handsontable</h2>
      <div class="img"><img src="~/assets/images/handsontable.png" alt=""></div>
      <ul>
        <li>link : <a href="https://handsontable.com/demo" target="_blank">https://handsontable.com/demo</a>
        </li>
        <li>license : <a href="https://handsontable.com/pricing" target="_blank">https://handsontable.com/pricing</a>
          <p>standard : $899 ( per each developer / 1 application )</p>
        </li>
        <li>document : <a href="https://handsontable.com/docs/" target="_blank">https://handsontable.com/docs/</a></li>
      </ul>
    </div>
    <div class="section">
      <h2>AG Grid</h2>
      <div class="img"><img src="~/assets/images/github-grid-demo.jpg" alt=""></div>
      <ul>
        <li>link : <a href="https://github.com/ag-grid/ag-grid" target="_blank">https://github.com/ag-grid/ag-grid</a></li>
        <li>license : <a href="https://www.ag-grid.com/license-pricing" target="_blank">https://www.ag-grid.com/license-pricing</a>
            <p>Single Application : $750</p>
            <p>Multiple Application : $1,200</p>
            <p>Development License : $750</p>
        </li>
        <li>document : <a href="https://www.ag-grid.com/vue-data-grid/getting-started/?utm_source=ag-grid-readme&utm_medium=repository&utm_campaign=github" target="_blank">https://www.ag-grid.com/vue-data-grid/getting-started/?utm_source=ag-grid-readme&utm_medium=repository&utm_campaign=github</a></li>
      </ul>

    </div>
    <div class="section">
      <h2>vue-good-table</h2>
      <div class="img"><img src="~/assets/images/vue-good-table.png" alt=""></div>
      <ul>
        <li>link : <a href="https://xaksis.github.io/vue-good-table/" target="_blank">https://xaksis.github.io/vue-good-table/</a></li>
        <li>license : MIT</li>
        <li>document : <a href="https://xaksis.github.io/vue-good-table/guide" target="_blank">https://xaksis.github.io/vue-good-table/guide</a></li>
      </ul>
    </div>
    <div class="section">
      <h2>vue3-easy-data-table</h2>
      <div class="img"><img src="~/assets/images/vue3-easy-data-table.png" alt=""></div>
      <ul>
        <li>link : <a href="https://hc200ok.github.io/vue3-easy-data-table-doc/" target="_blank">https://hc200ok.github.io/vue3-easy-data-table-doc/</a></li>
        <li>document : <a href="https://hc200ok.github.io/vue3-easy-data-table-doc/introduction.html" target="_blank">https://hc200ok.github.io/vue3-easy-data-table-doc/introduction.html</a></li>
      </ul>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start()
      setTimeout(() => this.$nuxt.$loading.finish(), 500)
    })
  }
}
</script>

<style>
ul { margin: 0; padding: 0; }
.container { min-height: 100vh; padding: 30px 50px; font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */ }
.container h1 { text-align: center; }
.container .desc { margin-top: 30px; font-size: 18px; }
.container .desc ul { margin-top: 20px; font-size: 15px; }
.section { margin-top: 50px; }
.section ul { margin-top: 20px; }
.section .img { margin-top: 20px; }
.section img { max-width: 100%; }
.subtitle { font-weight: 300; font-size: 42px; color: #526488; word-spacing: 5px; padding-bottom: 15px; }
.links { padding-top: 15px; }
ul li { position: relative; padding-left: 10px; list-style: none; }
ul li:before { content: ''; display: block; position: absolute; top: 10px; left: 0; width: 4px; height: 4px; border-radius: 2px; background: #000; }
</style>

